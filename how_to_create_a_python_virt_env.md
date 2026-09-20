How to create a Python virtual environment (venv) and install de dependencies only on it, without touching the OS.

1. Install venv if not available
```sudo apt install python3.14-venv```

2. Navigate to your project directory
```cd path/to/your/project```

3. Create the virtual environment
```python3 -m venv venv```

4. Activate the virtual environment
```source venv/bin/activate```

5. To deactivate the virtual environment
```deactivate```

How to install the requirements/dependencies using a single txt file

1. Create a new file
```touch requirements.txt```

2. Add the needed libraries in the file
Ex:
```nano requirements.txt```

````bash
netmiko
paramiko
````

3. Install the requirements in the environment
```pip3 install -r requirements.txt```

If you don't have pip3 installed use:
```sudo apt install python3-pip```
Then run again step 3.