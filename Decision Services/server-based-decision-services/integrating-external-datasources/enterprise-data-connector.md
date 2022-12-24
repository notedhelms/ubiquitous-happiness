# Simple Database Connectivity

Corticon [EDC ](https://documentation.progress.com/output/ua/Corticon/#page/corticon%2Fidentity-strategies.html%23)is designed to augment data when processing a discrete Decision Service request. It is used by rule authors who seek the least-technical requirements for modeling data access in their rules, to read/write to an external relational database. However, because it is built on Hibernate and is tied to Hibernate’s object relational model and transactional models, it introduces query and data processing overhead when reading data from a database with related tables. So, EDC's limitations are in its performance in large, data intensive operations where large chunks of data are loaded into Corticon for processing and updating the connected database. Corticon ships with Progress DataDirect drivers for RDBMSs, but you can also use the drivers bundled to[ create new database connections](https://documentation.progress.com/output/ua/Corticon/#page/corticon%2Fusing-datadirect-drivers.html%23).

### Summary: Enterprise Data Connector

|                             Benefits                            |                              Drawbacks                             |
| :-------------------------------------------------------------: | :----------------------------------------------------------------: |
|             Model driven approach – No SQL/JDBC code            |                          Limited to RDBMS                          |
|     Database independence – Rules don’t change if data does     |               Require good DB schema (PKs, FKs, etc)               |
| Minimize client application re-factoring when data needs change |                Require JDBC connectivity to database               |
|    Leverages industry leading Progress DataDirect technology    | Poor performance for large datasets due to ‘chatty’ DB interaction |

### Watch: Corticon Using SQL Server with EDC

{% embed url="https://www.youtube.com/watch?v=qULKijbr_Qc&list=PLYNw760GOr2BIxRuUKMkiJEJjm2wnUtU7&index=12" %}

#### To learn more, see [Getting Started with EDC](https://docs.progress.com/bundle/corticon-data-integration/page/Getting-Started-with-EDC.html) on Corticon Information Hub.
