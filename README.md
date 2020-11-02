# APICodingChallenge
APICodingChallenge project 
This is API integration Pytest framework based on python.

## Workspace preparation
### Prerequisites
- Install Pycharm IDE (community)
- Install Python 3 (if it is still needed)

### Virtual environments preparation
- Install virtual environment `pip install virtualenv` or `pip3 install virtualenv`
- Create virtual environment `virtualenv venv` or 'python3 -m venv venv'
- Activate the environment `.\venv\Scripts\activate`

More info: https://stackoverflow.com/questions/48730595/activating-python-virtual-environment-on-windows


### Install packages
`pip install -r requirements.txt`

### Configure PyCharm
Steps
- Open solution in PyCharm
- Navigate via **Project** explorer to: External Libraries > Lib > site-packages.
- Right click to folder **API_requests**
- Select **Copy Path**
- Navigate via **Main menu** to: Run > Edit Configurations...
- Paste the path into **Script path** field
- Set path to features folder into **Parameters** field 

More info with picture: https://stackoverflow.com/questions/40520301/how-to-run-a-feature-file-using-pycharm-community#50843378

### Plugins 
- Open *.py* file
    - Click to add interpreted in top yellow line and select python 3 and confirm
- project-->File-->Settings-->Projects-->Python Interpreter-->add (pytest-html)

## Folder structure
Let us split automation to few elements:

	Behave
	├───TestCase
	│───file
	└───reports

Purpose 

TestCase File contains python code with take care about API directly. For example methods which sent a request.
File-contain json file required to create and update request
report-Contain html report

# Run
Execution command `pytest filename.py`


## Report
Run following command to see HTML report: `pytest --html=report.html --self-contained-html test_api_codeing_challenge.py`
`

## Coding

### JSONPath
Json path is very similar to Xpath. The difference is there is no navigation throw XML document but Json document.
Should be used similar way like a css locators in Cucumber.js.

More info:
- https://goessner.net/articles/JsonPath/index.html
- https://jsonpath.com/

### Assertion
Nothing needs to be imported. Use just `assert` like this 

`assert int(ping) == 200`



