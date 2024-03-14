# Step Functions 
- AWS Step Functions allow you to design and build the flow of
  execution of AWS serverless modules in an application.


- This lets developers focus solely on ensuring that each module
  performs its intended task, without having to worry about
  connecting each module with others.
## How AWS Step Functions Work 
- The state machine is a core component of the AWS Step Functions
  service. It defines communication between states and how data is
  passed from one state to another.


- States are elements in your state machine. A state is referred to by
  its name, which can be any string, but which must be unique within
  the scope of the entire state machine.

## Use Case 
- Automate extract, transform, and load (ETL) processes.Ensure that
  multiple long-running ETL jobs run in order and complete successfully,


- Combine multiple AWS Lambda functions into responsive serverless
  applications and microservices.


- Iterate over and process large data-sets such as security logs, transaction
  data, or image and video files. (scale parallel workloads)

## State Types
It's essential to remember that States aren't the same thing as Tasks since
Tasks are one of the State types. There are numerous State types, and all of
them have a role to play in the overall workflow:

- **Pass**: Pushes input to output.
- **Task**: Takes input and produces output.
- **Choice**: Allows the user to use Branching Logic that's based on the input.
- **Wait**: It adds delays to State Machine execution.
- **Success**: Has an expected dead-end that stops execution successfully.
- **Fail**: Has an expected dead-end that stops execution with a failure.
- **Parallel**: Allows a user to implement parallel branches in execution,
  meaning the user can start multiple states at once.
- **(Dynamic) Mapping:** Runs a set of steps for every input item.