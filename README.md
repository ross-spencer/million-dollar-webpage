# Million Dollar Web Page: Summary of Results

In response to Harvard Library Innovation Lab's work, an open dataset studying the [Million Dollar Web Page](http://www.milliondollarhomepage.com/) (2005)

- Seen on Boing Boing: http://boingboing.net/2017/07/27/link-rot-only-half-of-the-lin.html
- Available here: https://lil.law.harvard.edu/blog/2017/07/21/a-million-squandered-the-million-dollar-homepage-as-a-decaying-digital-artifact/

The Boing Boing and Harvard links do not seem to point to open data sources. Here we have an open set of links automatically
extracted by the HTTPreserve suite. 

We also have a CSV that explores the various responses from the web. Including earliest, and latest Internet Archive links.

The numbers don't seem to align with those of Harvard, but the process followed is not all that transparent. 

Process followed:

- Clean the Million Dollar Page HTML to remove anything not in the image map. 
- Extract links using Tikalinkextract

       $./tikalinkextract -noprotocol -quote -file million/ > mil.csv
    
- Run the CSV through HTTPreserve workbench:

       $./workbench --csv --list mil.csv > mil_ia.csv

The process takes approx 138 minutes. No screenshots are created but they are available if wanted.

## Links

Unique Links using [Tikalinkextract](https://github.com/httpreserve/tikalinkextract): 3046 (Harvard: 2816)

## IA Data

- Earliest time the IA first archived a page from this site: 31 October 1996
- Latest time the IA first archived a page from this site: 16 April 2015

      - http://www.tkqlhce.com/click-1772197-2831550
      - http://www.digden.net/index.php?affid=MDHP2

- Last IA archived page: 05 July 2017

## Response Codes and Counts

- 0xx: 569
- 2xx: 2258
- 4xx: 187
- 5xx: 31

## HTTPreserve

The suite of tools can be found here: https://github.com/httpreserve

Try it here: http://httpreserve.info

Most workflows will involve just two, extract links using Tikalinkextract followed by analysis using Workbench:

- https://github.com/httpreserve/tikalinkextract
- https://github.com/httpreserve/workbench

The code is licensed under GPLv3.

## Data License

<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons Licence" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/80x15.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>.
