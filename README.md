# Google_cluster_usage_traces_v3_all_cells


The data has been constructed as follow:


| Job_ID        | Task_ID       | Arrival_Time | CPU   | Memory |
| ------------- | ------------- | -------------| ---   | -------|
| J_1  | 0             |   603123  | 0.5   | 0.012  |
| J_2  | 0             |   605237  | 0.16  | 0.019  |
| J_3  | 0             |   607123  | 0.23  | 0.003  |
| J_3  | 1             |   607123  | 0.27  | 0.0021 |
| J_4  | 0             |   609237  | 0.56  | 0.0054 |
| J_4   | 1             |   609237  | 15.12 | 0.0027 |
| J_4   | 2             |   609237  | 1.689 | 0.0018 |


The above table presents the Job_ID column, which represents a unique hashed number assigned by Google to each job. It should be noted that a job may comprise one or more tasks, which are indexed in the Task_ID column. For instance, J_1 and J_2 consist of a single task, with index 0 in both cases. Conversely, J_3 has two tasks with indexes 0 and 1 respectively, while J_4 encompasses three tasks with indexes 0, 1, and 2. The arrival times of jobs are recorded in miliseconds, and it is assumed that all tasks pertaining to a job arrive simultaneously. The last two columns of the table indicate the total CPU and memory resources required to successfully execute a task.





In the zip file there are all the informations that we have mentioned above for 8 different cells. 
The data can be found and downloaded [here](https://drive.google.com/file/d/1WryZF0o-7LOB0gmpw0C9xPFIMa9kd2DU/view?usp=share_link)


