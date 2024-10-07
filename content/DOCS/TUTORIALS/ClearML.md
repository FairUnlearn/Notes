Start here https://www.youtube.com/watch?v=s3k9ntmQmD4&list=PLMdIlCuMqSTnoC45ME5_JnsJX0zWqDdlO&index=2


Make fully reusable tasks. Put every variable and path as hyperparameter. [Watch this](https://www.youtube.com/watch?v=gCjxLXLuH3Y)


configuration objects - whole files that we will not use

task.connect_configuration(
name="My config file not parsed",
configuration="config.yaml"
)

run simply with python (if you have init clearml task in the code)

or run clearml task via CLI

Get artifacts programmatically

t = Task.get_task(task_id=1) or name="
a = t.artifacts['features]
sth = a.get_local_copy()


Models are separate entities. You can pull model by ID or tag

We use TensorboardX (so you can have it locally as well as stored remotly)

not utils from torch as they can cause problems with autocapture

pip install tensorboardX