#Calculator
A Python 3 calculator used from the Terminal, built step by step in SCCM4910.

## What it will do
Add, subtract, multiply and divide two numbers; display the result.

## How to run it
Run: ./run.sh
Enter the first number, operator (+ - * /), then second number.
The program prints Result: followed by the answer.
It will then ask again for the first number
Stop the program with CTRL C


## Sample test
cd ~/h-drive/calculator
./run.sh
6
*
7

Result: 42.0

Asks again for first number

## Testing the entire calculator
To activate the SCCM4910 environment and python 3: 
source /opt/python-venv/sccm-4910/bin/activate
python3 -m pytest --version

To access the correct directory:
cd ~/h-drive/calculator

Command for the test:
./ check.sh

Expected passing result: 
=== Calculator quality gate ===
=================================================== test session starts ===================================================
platform linux -- Python 3.12.3, pytest-9.1.1, pluggy-1.6.0 -- /opt/python-venv/sccm-4910/bin/python3
cachedir: .pytest_cache
rootdir: /home/tolkien/h-drive/calculator
collected 5 items                                                                                                         

test_calculator.py::test_add PASSED                                                                                 [ 20%]
test_calculator.py::test_divide PASSED                                                                              [ 40%]
test_calculator.py::test_subtract PASSED                                                                            [ 60%]
test_calculator.py::test_multiply PASSED                                                                            [ 80%]
test_calculator.py::test_divide_uneven PASSED                                                                       [100%]

==================================================== 5 passed in 0.05s ====================================================
QUALITY GATE PASSED

To confirm exit status:
echo $?

Why - because the passed test may not mean the program is running exactly as intended




