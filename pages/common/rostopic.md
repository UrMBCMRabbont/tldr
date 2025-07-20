#ros

> ROS (Robotic Operating System), is an inter-process communication system for robots, enables robots to execute multiple independent programs with standard interface and standard types.
> For more information: https://wiki.ros.org/


- Echo incoming messages in the terminal:

`rostopic echo {{/topic_name}}`

- Show the rate of incoming messages:

`rostopic hz {{/topic_name}}`

- Inspect topic information:

`rostopic info {{topic_info}}`

- List all active topics:

`rostopic list`

- Publish data to a topic:

`rostopic pub {{/topic_name}} {{message_type}} {{args}}`

