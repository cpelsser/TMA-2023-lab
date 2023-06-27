## Lab Prerequisite: BGPStream and PyBGPStream

_For this lab you'll need BGPStream installed on your laptop or on a server that you can access remotely, e.g. via SSH._

The [BGPStream website](https://bgpstream.caida.org) has
[install instructions](http://bgpstream.caida.org/docs/install) for a variety of
operating systems.

## Methodology

It is expected that you clone this repository. Then, you can edit this readme to provide the answers to the different questions. This will give you notes to go back to later on.

## Get familiar with BGPreader

BGPreader is a command line tool. 

1. Scroll the [BGPreader documentation](https://bgpstream.caida.org/docs/tools/bgpreader) to find out how do download BGP data from a collector for a given time interval.

    The timestamps are in unix format. You may use a [unix timestamp converter]{https://www.unixtimestamp.com} to help you with the conversion.

2. Explore the data
    - Find out what ``R|R``,``R|E``, ``R|B``, ``U|A`` and ``U|W`` correspond to? You need to be able to explain the BGP concepts behind each combination of ``dump-type`` and ``elem-type``.
    - Each line is composed of other elements. What are they? What do they represent? 
    - What is a full-feed and how to identify one **directly** from the BGP data? Explain your methodology.
    - What can you say about IPv4 and IPv6? Look at the session identifiers and at the prefixes announced.

## Get familiar with pyBGPStream

The [pyBGPStream documentation](https://bgpstream.caida.org/docs/api/pybgpstream/_pybgpstream.html) and [tutorial](https://bgpstream.caida.org/docs/tutorials/pybgpstream) are useful references to get familiar with pyBGPStream. 

## Stub AS identification

The objective here is to identify the ASs that are at the bottom of the Internet hierarchy.

1. To get your hands on the data, you'll first take a BGP feed from a single peer and determine all the stub ASs. These are ASs that always appear as the origin AS for all prefixes.

2. Take another peer, quantify the change in the obtained result.

    What metrics do you propose to measure the change?

3. Repeat with other feeds.
    
    Present the data in a plot. Try multiple representations. Which one do you find convenes best the differences between peers?

## Type-0 hijacks

Now let's look at the new links appearing between the origin ASs and their direct upstream.

1. Monitor the appearance of such new links.

2. Do some ASs appear more frequently as a result of this study? 

## AS topology and new links

Let's generalise to the detection of other hijacks.

1. Parse all the AS-paths, represent the resulting links in a graph. You need to be able to remove an edge if no prefixes contains the edge in the AS-path.

2. Load data as it appears and generate the set of new links that appear

3. Do these new links appear to be legitimate? How to find out?