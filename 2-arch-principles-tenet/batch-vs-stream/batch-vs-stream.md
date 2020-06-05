---
title: Analytics Warehouse - Batch vs. Stream
layout: template
filename: batch-vs-stream.md
permalink: /arch-principles-tenet/batch-vs-stream/
--- 

# Batch vs. Stream

One of the most important core principle is the distinction between **batch processing** and **stream processing**.

- **Batch (bounded data)**:<br/>
    *Batch processing is where the processing happens of blocks of data that have already been stored over a period of time. For example, processing all the transaction that have been performed by a major financial firm in a week. This data contains millions of records for a day that can be stored as a file or record etc. This particular file will undergo processing at the end of the day for various analysis that firm wants to do.* 

    → In Batch you process one (or sometimes more than one) file with a lot of rows.

- **Stream (unbounded data)**:<br/>
    *Stream processing is a golden key if you want analytics results in real time. Stream processing allows us to process data in real time as they arrive and quickly detect conditions within small time period from the point of receiving the data. Stream processing allows you to feed data into analytics tools as soon as they get generated and get instant analytics results.* 

    → In Stream you process one message - in general one json-file per request. 
<br/>

[Source: [Big Data Battle : Batch Processing vs Stream Processing](https://medium.com/@gowthamy/big-data-battle-batch-processing-vs-stream-processing-5d94600d8103){:target="_blank"}]

In general we highly recommend to tune your system to be able to do stream, because streaming data processing is a chance for companies
these days. Some Examples:
- Businesses crave ever-more timely insights into their data, and switching to streaming is a good way to achieve lower latency
- The massive, unbounded datasets that are increasingly common in modern business are more easily tamed using a system designed for such never-ending volumes of data.
- Processing data as they arrive spreads workloads out more evenly over time, yielding more consistent and predictable consumption of resources.

[Source: [The-world-beyond-batch-streaming-101](https://www.oreilly.com/radar/the-world-beyond-batch-streaming-101/){:target="_blank"}]