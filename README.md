# Employee Dashboard Challenge

## Requirements

* One page, two sections
* Left side list all employees
* Font size relative to popularity in data
* Clicking on a person in the list shows a view of their details and highlights people they have worked with in the employee list
* Must match design as closely as possible
* Must be responsive to different desktop sizes

## Basic Design
### Components:
* EmployeePage
* EmployeeList
* EmployeeDetail


#### EmployeePage
* Contains the other components
* Loads employee data
* Passes names and popularity to EmployeeList
* Passes selected employee and employee data to EmployeeDetail

#### EmployeeList
* Takes the employee data from EmployeePage as props and lists them
* Responds to click by emitting the name of the selected employee
* Adjusts size of text based on current popularity of employee derived from props
* Highlights names in the list where they have worked with the selected employee (derived from props)

#### EmployeeDetail
* Takes the employee data for the selected employee from EmployeePage as props
* Allows user to adjust popularity using a slider control
* Emits changes to popularity to EmployeePage


### Other Files
#### EmployeeDataAPI
Handles loading the data from the API which in this case is a json file

## Installation Instructions

1. Clone this repo
2. Run `npm install`
3. Run `npm serve` to run a local instance of the project.
  