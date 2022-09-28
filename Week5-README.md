# Python & Simple Publisher and Subscriber

<br />

## Step 1: Creating a Python package

<br />

At first, we open the terminal in our Virtual Machine and navigate to the ```ros2_ws/src``` folder that we created before. Then, we run the following code to create the package:
```
ros2 pkg create --build-type ament_python py_pubsub
```

<br />

## Step 2: Writing the publisher node

<br />

After that, the python package will be installed in a folder ```ros2_ws/src/py_pubsub/py_pubsub``` where we will navigate to and download the example talker code by running the following command:
```
wget https://raw.githubusercontent.com/ros2/examples/humble/rclpy/topics/minimal_publisher/examples_rclpy_minimal_publisher/publisher_member_function.py
```
Then, if we type ```ls``` command, we can see two files ```publisher_member_function.py``` and ```__init__.py```. In order to open the file and edit using the text editor, we use the command ```open``` before the filename:
```
open publisher_member_function.py
```

### Adding dependencies
If we navigate one level back to the ```ros2_ws/src/py_pubsub```, we can see a file ```package.xml```. We open the file in a text editor using the command below:
```
open package.xml
```
Then, we must fill in the following tags using our personal data:
```
<description>Examples of minimal publisher/subscriber using rclpy</description>
<maintainer email="ozodjonkunishev@gmail.com">Ozodjon</maintainer>
<license>Apache License 2.0</license>
```
Next, we should add the following dependencies after the lines above.
```
<exec_depend>rclpy</exec_depend>
<exec_depend>std_msgs</exec_depend>
```

<br />

### Adding an entry point
Next, we open the ```setup.py``` file and math the personal information with the ```package.xml``` file:
```
maintainer='Ozodjon',
maintainer_email='ozodjonkunishev@gmail.com',
description='Examples of minimal publisher/subscriber using rclpy',
license='Apache License 2.0',
```
