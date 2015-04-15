# rcl_interfaces
This package contains the messages and services which ROS client libraries will use under the hood to
communicate higher level concepts such as parameters.


## Parameter Groups
Parameters are contained in groups.
The default group is '/'.
It behaves like a filepath, where you can nest sub-groups within groups.

## Standard topics for parameters

The ROS API for a node will be as follows inside the node's namespace.

### Topics:
 * `parameter_updates`: `ParameterEvent`
  * This topic provides a way to subscribe to all parameter updates occuring on the node, including addition removal and changes in value.

### Services:

 * `get_parameters`: `GetParameters`
  * The service to get the value of parameters which are set on this node.
 * `has_parameters`: `HasParameters`
  * Query this node if specific parameters are set.
 * `list_parameters`: `ListParameters`
  * List the parameters on this node matching the filters.
 * `set_parameters`: `SetParameters`
  * Set parameters on this node.
