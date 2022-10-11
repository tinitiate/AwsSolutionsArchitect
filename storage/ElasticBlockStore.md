|              FEATURE              |               SSD <br/> SSD Solid State Drive                |                  HDD  <br/> Hard Disk Drive                  |
| :-------------------------------: | :----------------------------------------------------------: | :----------------------------------------------------------: |
|     Best for workloads with:      |            **small, random**<br/> I/O operations             |          **large, sequential**<br/> I/O operations           |
| Can be used as a bootable volume? |                             Yes                              |                              No                              |
|        Suitable Use Cases         | - Best for **transactional workloads**<br/>- Critical business applications that require sustained IOPS performance<br/>- Large database workloads such as MongoDB, Oracle, Microsoft SQL Server and many others... | - Best for **large streaming workloads** requiring consistent, fast throughput at a low price<br/>- Big data, Data warehouses, Log processing<br/>- Throughput-oriented storage for large volumes of data that is **infrequently** accessed |
|               Cost                |                       moderate / high                        |                             low                              |
|  Dominant Performance Attribute   |                             IOPS                             |                      Throughput (MiB/s)                      |





|                                    |                 SSD Solid State Drives (SSD)                 |                                                              |                    Hard Disk Drive (HDD)                     |                                                              |
| :--------------------------------: | :----------------------------------------------------------: | :----------------------------------------------------------: | :----------------------------------------------------------: | :----------------------------------------------------------: |
|          **Volume type**           |                     General Purpose SSD                      |                     Provisioned IOPS SSD                     |                   Throughput Optimized HDD                   |                           Cold HDD                           |
|          **Description**           | General Purpose SSD volume that balances price performance for a wide variety of transactional workloads | Highest performance SSD volume designed for **mission-critical** latency-or high-throughput workloads | Low cost HDD volume designed for frequently accessed, throughput-intensive workloads | Low cost HDD volume designed for less frequently accessed workloads |
|           **Use Cases**            | • Recommended for most workloads <br/>• Critical business applications that require sustained <br/>• System boot volumes<br/>• Virtual desktops<br/>• Low-latency interactive apps<br/>• Development and test environments | • Critical business applications that require sustained IOPS performance, or more than 16,000 IOPS or 250 MiB/s of throughput per volume<br/>• Large database workloads, such as:<br/>  • MongoDB <br/>  • Cassandra <br/>  • Microsoft SQL Server <br/>  • MySQL <br/>  • PostgreSQL <br/>  • Oracle | Streaming workloads requiring consistent, fast throughput at a<br/>low price <br/>• Big data <br/>• Data warehouses<br/>• Log processing <br/>• Cannot be a boot volume | Scenarios where the lowest storage cost is important• Throughput-oriented storage for large volumes of data that is<br/>• infrequently accessed <br/>• Scenarios where the lowest<br/>• storage cost is important <br/>• Cannot be a boot volume |
|          **Volume Size**           |                        1 GiB – 16 TiB                        |                        4 GiB – 16 TiB                        |                       500 GiB - 16 TiB                       |                       500 GiB - 16 TiB                       |
|      **Max. IOPS Per Volume**      |                          16,000***                           |                          64,000***                           |                             500                              |                             250                              |
|   **Max.Throughput Per Volume**    |                         250 MiB/s***                         |                        1000 MiB/s***                         |                         500 MiB/s***                         |                         250 MiB/s***                         |
|     **Max. IOPS Per Instance**     |                            80,000                            |                            80,000                            |                            80,000                            |                            80,000                            |
|  **Max.Throughput Per Instance**   |                         1,750 MiB/s                          |                         1,750 MiB/s                          |                         1,750 MiB/s                          |                         1,750 MiB/s                          |
| **Dominant Performance Attribute** |                             IOPS                             |                             IOPS                             |                      Throughput (MiB/s)                      |                      Throughput (MiB/s)                      |



| **Configuration** | Use                                                          | Advantages                                                   | Disadvantages                                                |
| ----------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| RAID 0            | When I/O performance is more important than fault tolerance. example , heavily used database where data replication is already set up seperately. | I/O is distributed across the volumes in a stripe. As we add volume we get the straight addition of throughput. | Performance of the stripe is limited to the worst performing volume in the set. Loss of a single volume results in complete data loss for the array. |
| RAID 1            | When  fault tolerance is more important than I/O performance. example , critical application. | Safer from the standpoint of data durability.                | Does not provide a write perfoemance improvement; requires more Amazon EC2 to Amazon EBS bandwidth than non-RAID configurations beacuse the data is written  to mutliple volumes simultaneously. |


