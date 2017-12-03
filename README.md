### Jupyter notebook setup (Python kernel)

**Note: We should be using Python 3.6.1**

1. Install the latest stable release of Python 3 from [here](https://www.python.org/downloads/)
	- This installation will include other necessary tools such as `pip` (python package manager)

2. run `pip install virtualenv` from anywhere in Terminal

 - `virtualenv` allows us to make virtual environments to hold our code dependences. The primary benefits of using virtual environments are: 

 		- We won't have to push/pull large code dependencies (libraries) to the remote repo.
 	
 		- These dependencies will be scoped to our a particular project as to not interfere with other Python projects you might have on your machine. 

3. Clone the `beersheet` Git repo

4. `cd` into the top level directory of the `beersheet` repo

5. create a virtual environment for our project
	- `virtualenv -p python3 venv`, where `-p python3` specifies the Python version and `venv` is the name of the directory that will contain the virtual environment 

	- NOTE: I've already added `venv/` to the `.gitignore`, so I think it makes sense to stick with that name. 

### Using the virtual environment

1. Activating the virtual environment
	- `source venv/bin/activate`
	- your command prompt should now indicate that you're in the virtual environment:
	```
	(venv) Jareds-MacBook-Pro:beersheet jaredkatz$
	```
2. Deactivating the virtual environment
	- `deactivate`
	- your command prompt should now indicate that you've left the virtual environment:
	```
	Jareds-MacBook-Pro:beersheet jaredkatz$
	```

7. Install existing dependencies from `requirements.txt`
	- **NOTE: Be sure to activate the virtual environment before running this command!**
	- `pip install -r requirements.txt`
	- **NOTE: Some packages may fail to install. If so, try `sudo pip install -r requirements.txt`**

You should be good to go.

### Jupyter notebook usage

1. Activate the virtual environment
	- `source venv/bin/activate`

2. Start the Jupyter notebook server from Terminal
	- `jupyter notebook`
	- The Jupyter notebook UI should open in a new browser tab

### Using `pip`

- Again, be sure you're only installing packages from within the virtual environment
- To install a new package, simply use the command `pip install <package_name>`

### Best practices

 - I suggest opening two Terminal windows: one to run the notebook server, another where you've activated the virtual environment so you can conveniently install packages as needed.
- Upon installing new Python packages, be sure to update the `requirements.txt` file by running the following command:
	- `pip freeze > requirements.txt`



