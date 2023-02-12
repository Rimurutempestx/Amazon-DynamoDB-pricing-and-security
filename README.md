# Amazon-DynamoDB-pricing-and-security

A quick breakdown of Amazon DynamoDB pricing and security concepts.

## Overview

I thought that since the DynamoDB users are only increasing as time goes by I would create this repository to help newer users breakdown pricing and security concepts into more basic and staright-forward terms. This quick breakdown will be divided into two parts, starting with cost optimization and slowly getting into security concepts. By the end of this you should be able to quickly assess your needs and limits as it pertains to your DynamoDB database.

# Amazon DynamoDB pricing

DynamoDb charges for reading, writing, and storing data in your DynamoDB tables, along with any optional features you choose to enable so your utilization is a big factor that will determine price of the services that you use. DynamoDB has two capacity modes, which come with specific billing options for processing reads and writes on your tables: on-demand capicity mode: With on-demand capacity mode, you pay per request for the data reads and writes your application performs on your tables. You do not need to specify how much read and write throughput you expect your application to perform, as DynamoDB instantly accommodates your workloads as they ramp up or down and provisioned capacity mode: With provisioned capacity mode, you specify the number of reads and writes per second that you expect your application to require. You can use auto scaling to automatically adjust your table’s capacity based on the specified utilization rate to ensure application performance while reducing costs. I will include the roundabout estimate cost for each DynamoDB service, to get a more comfortable feel of service prices.


# DynamoDB detailed feature pricing (On-demand capacity)

Even though DynamoDB is one service there are a multitude of things that can determine your price output. AWS calls it DynamoDB deatiled featured pricing where pricing split up into diffrent types of DynamoDB use cases read and write requests, Data storage, backup and restore, global tables, change data capture for Amazon Kinesis Data Streams, change data capture for AWS Glue, data export to Amazon S3, data import from Amazon S3, DynamoDB Accelerator (DAX), DynamoDB streams, and data transfers. I know it's alot but were going to seperate it and break it all down (remember that some of theses pricings can be difrrent depending on the region you live in, for this specific breakdown I'm going to be using my region which is US East (Ohio)).

### Read and write requests 

When you select on-demand capacity mode for your DynamoDB table, you pay only for the reads and writes your application performs. You can make API calls as needed without managing throughput capacity on the table. DynamoDB handles the management of hardware resources to accommodate your workload with consistent, low-latency performance. DynamoDB charges one write request unit for each write (up to 1 KB) and two write request units for transactional writes. For reads, DynamoDB charges one read request unit for each strongly consistent read (up to 4 KB), two read request units for each transactional read, and one-half read request unit for each eventually consistent read. The prices for read and write requests depend on your table class. 

DynamoDB Standard table class:

On-Demand Throughput Type	Price

Write Request Units (WRU) -	$1.25 per million write request units
Read Request Units (RRU) - $0.25 per million read request units


DynamoDB Standard-Infrequent Access (DynamoDB Standard-IA) table class:


On-Demand Throughput Type	Price

Write Request Units (WRU)	- $1.56 per million write request units
Read Request Units (RRU)	- $0.31 per million read request units

### Data storage





