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

## Get familiar with pyBGPStream

The [pyBGPStream documentation](https://bgpstream.caida.org/docs/api/pybgpstream/_pybgpstream.html) and [tutorial](https://bgpstream.caida.org/docs/tutorials/pybgpstream) are useful references to get familiar with pyBGPStream. 
