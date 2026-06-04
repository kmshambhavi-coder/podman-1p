
# Asana

Asana is a software-as-a-service designed to improve team collaboration and work management. It helps teams manage projects and tasks in one tool. Teams can create projects, assign work to teammates, specify deadlines, and communicate about tasks directly in Asana.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Token|The personal access token|True|Password|*****|
|Base URL|Base URL|True|String|https://app.asana.com/api/1.0|


#### Dependencies
| |
|-|
|charset_normalizer-3.4.2-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|urllib3-2.5.0-py3-none-any.whl|
|idna-3.10-py3-none-any.whl|
|certifi-2025.6.15-py3-none-any.whl|
|requests-2.32.4-py3-none-any.whl|


## Actions
#### Get Task
Retrieves the task details
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Task ID|The task ID can be found in the URL:https://app.asana.com/0/{your_project_ID}/{your_task_ID}|True|String|<Task-Id>|



#### Update Task
Updates a given task in Asana
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Task ID|The task ID can be found in the URL:https://app.asana.com/0/{your_project_ID}/{your_task_ID}|True|String|<Task-Id>|
|Due Date|The due date is in the format YYYY-MM-DD|False|String|2020-10-08|
|Description|The task description|False|String|Your new description for this task|
|Assignee|The user's email of the person you would like to re-assign the task to. Note: This is case sensitive|False|String|email@gmail.com|



#### Add User To Workspace
Add a user to a specific workspace
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Workspace Name|The workspace to which you want to add the user.Note: It is case sensitive!|True|String|Your Workspace Name|
|User's Email|The email address of the user you want to add|True|String|email@gmail.com|



#### Create Task
Create a task for a specific project 
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Task Subject|The new task subject|True|String|Your Task Subject|
|Assignee|The user to whom you will assign the task.Note: This is case sensitive!|False|String||
|Due Date|The due date is in the format YYYY-MM-DD|False|String||
|Description|The description of the new task|True|String|Your task description|
|Project Name|The name of the project to which you want to assign the task.Note: this is case sensitive|True|String|Your Project Name |



#### Remove User From Workspace
Removes a given user from a workspace in Asana
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Workspace Name|The workspace from which you want to remove the userNote: It is case sensitive!|True|String|Your Workspace Name|
|User's Email|The email address of the user you want to remove.|True|String|email@gmail.com|



#### List My Tasks
Lists all the tasks associated with a user in Asana
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|User's Email|The email of the user you would like to retrieve tasks for in Asana|True|String|email@gmail.com|
|Workspace Name|The workspace name.Note: This is case sensitive|True|String|Your Workspace Name|
|Completed Status|Marking the checkbox will retrieve only the tasks that were completed by the user. |False|Boolean|false|



#### List Project Tasks
Lists all the tasks associated with a specific project
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Project Name|The name of the project from which you would like to fetch all the tasks|True|String|Your Project Name|
|Completed Status|Marking the checkbox will retrieve only the tasks that were completed by the user. |False|Boolean|false|



#### Ping
Testing connectivity with Asana
Timeout - 600 Seconds










Readme text