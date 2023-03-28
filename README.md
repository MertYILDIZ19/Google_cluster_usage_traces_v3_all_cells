# Google_cluster_usage_traces_v3_all_cells


The data has been constructed as follow:


| Job_ID        | Task_ID       | Arrival_Time | CPU   | Memory |
| ------------- | ------------- | -------------| ---   | -------|
| J_1  | 0             |   603000123  | 0.5   | 0.012  |
| J_2  | 0             |   605000237  | 0.16  | 0.019  |
| J_3  | 0             |   603000123  | 0.23  | 0.003  |
| J_3  | 1             |   603000123  | 0.27  | 0.0021 |
| J_4  | 0             |   605000237  | 0.56  | 0.0054 |
| J_4   | 1             |   605000237  | 15.12 | 0.0027 |
| J_4   | 2             |   605000237  | 1.689 | 0.0018 |


As it is shown in the above table, we simply have column Job_ID that is a hashed number for each unique job by google. One job might have 1 or more task, that is represented in the Task_ID column as index of the task. For example J_1 and J_2 have only 1 task which the tasks has index 0 for both, but J_3 has 2 task that the 1st task has index 0 and 2nd task has index 1. The same for J_4 that has 3 task indexed as 0,1,2. Arrival times of jobs has been recorded in microseconds. And it is assumed that all tasks that belongs to a job arrive at the same time. Last 2 columns includes the overal CPU and memory amount needed to properly finish a task. 



The data can be found and downloaded here:

https://drive.google.com/file/d/1a6Avhg1ayRsuV8S3-6lh1vOl3pgAj95r/view?usp=share_link
