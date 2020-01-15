I did the following optimizations

* Moved all RUN commands to one command to reduce the number of layers (this doesn't seem to have much impact to the size)
* Run the django project under django -user
* I also tried to use python-slim but it didn't work out as there are quite many requirements in the requirements file and pip install fails if using python-slim. Probably this is due to some missing dependencies but don't have now time to investigate this further in the scope of this task.
* Ps. this is an OLD project which I now dockerized, that's why it's using python 2.7