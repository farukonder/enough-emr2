# Data and Streaming using Spark on EMR, ElasticSearch, Iceberg and ..

[This is part of series of](https://farukonder.github.io/thats-enough-cloud-for-today)

The other day, I was curious about whether I should start a composite project on my own to investigate alternative solutions for different kinds of platform needs in my current company. 

Given my responsibility for platform services, I want to delve into specifics such as data-at-rest services, integration, streaming, and NoSQL/NewSQL solutions.
In my company, there are separate Elasticsearch services for logging and searching purposes for every product. Especially for logging purposes, Elasticsearch services contain valuable data that can be utilized for fraud detection, campaign management, error tracking, monitoring, alerting, and more.

The nature of logging data on Elasticsearch is convenient for putting as data producer in my solution as streaming, searching, and transferring, as data on it is both huge and fast-increasing.

In the upcoming series, the p