# Google cluster usage traces v3 all cells

A large dataset of workload measurements has been released by Google for the month of May 2019. This robust collection details user requests and the corresponding utilization of cloud resources, totaling a significant 2.4TB in size. It encompasses data from eight distinct data centers, as delineated in the subsequent table. For a more granular breakdown of the trace data and its various components, please refer to the detailed documentation provided [here](https://drive.google.com/file/d/10r6cnJ5cJ89fPWCgj7j4LtLBqYN9RiI9/view).

In our pursuit to enable more efficient computational resource management, we have conducted an extensive analysis of the dataset. The result is a curated set of data, meticulously preprocessed to extract only the most pertinent information for advancing dispatching and scheduling algorithms. 

## Related Publication

This dataset has been used in the following research paper:

📄 **M. Yildiz and A. Baiocchi,**  
**"Data-driven workload generation based on Google data center measurements,"**  
*2024 IEEE 25th International Conference on High Performance Switching and Routing (HPSR)*, 2024.  
[🔗 Read the full paper](https://ieeexplore.ieee.org/document/10635925)

## Dataset Overview

| Trace    | Trace start (t=600s)       | Timezone           |
|----------|----------------------------|--------------------|
| 2019-05-a | 1 May 2019 00:00 PDT      | America/New_York   |
| 2019-05-b | 1 May 2019 00:00 PDT      | America/Chicago    |
| 2019-05-c | 1 May 2019 00:00 PDT      | America/New_York   |
| 2019-05-d | 1 May 2019 00:00 PDT      | America/New_York   |
| 2019-05-e | 1 May 2019 00:00 PDT      | Europe/Helsinki    |
| 2019-05-f | 1 May 2019 00:00 PDT      | America/Chicago    |
| 2019-05-g | 1 May 2019 00:00 PDT      | Asia/Singapore     |
| 2019-05-h | 1 May 2019 00:00 PDT      | Europe/Brussels    |

***

After preprocessing and thorough analysis the data has been constructed as follows:

***

| Job_ID        | Task_ID       | Arrival_Time | CPU   | Memory |
| ------------- | ------------- | -------------| ---   | -------|
| J_1  | 0             |   603123  | 0.5   | 0.012  |
| J_2  | 0             |   605237  | 0.16  | 0.019  |
| J_3  | 0             |   607123  | 0.23  | 0.003  |
| J_3  | 1             |   607123  | 0.27  | 0.0021 |
| J_4  | 0             |   609237  | 0.56  | 0.0054 |
| J_4   | 1             |   609237  | 15.12 | 0.0027 |
| J_4   | 2             |   609237  | 1.689 | 0.0018 |

***
### Column Descriptions:

- **Job_ID**: A unique identifier for each job, represented by a hashed number assigned by Google. Each job may encompass multiple tasks.
- **Task_ID**: The index of individual tasks within a job. For example, J_1 and J_2 are jobs each consisting of a single task (indexed as 0), while J_3 is a job comprising tasks indexed as 0 and 1, and J_4 includes tasks indexed as 0, 1, and 2.
- **Arrival_Time**: The time at which jobs are received, recorded in milliseconds. It is presumed that all tasks under a job arrive concurrently.
- **CPU_Usage**: The CPU resources each task requires for execution.
- **Memory_Usage**: The amount of memory resources required for each task.
