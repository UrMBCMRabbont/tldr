#ros

> ROS (Robotic Operating System), is an inter-process communication system for robots, enables robots to execute multiple independent programs with standard interface and standard types.
> For more information: https://wiki.ros.org/


- Echo the incoming messages on terminal:

`rostopic echo {{/topic_name}}`

- Show rate of the incoming messages:

`rostopic hz {{/topic_name}}`

- Inspect topic information:

`rostopic info {{topic_info}}`

- List all the active topics:

`rostopic list`

- Publish data to topic:

`rostopic pub {{/topic_name}}`

