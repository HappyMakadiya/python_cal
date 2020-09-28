# Python GUI using PyQt

## Install

    PIP install PyQt5

## Test installation of PyQt5
   To check installation and to simulate working of library try below code:  
   Test.py:  
    
######    _import module_ 
     
    import sys  
    from PyQt5.QtWidgets import QApplication  
    from PyQt5.QtWidgets import QLabel  
    from PyQt5.QtWidgets import QWidget  
    
######    _Create GUI_ 
       
    app = QApplication(sys.argv)  
    window = QWidget()  
    window.setWindowTitle('PyQt5 App')  
    window.setGeometry(100, 100, 280, 80)  
    window.move(600, 15)  
    helloMsg = QLabel('This is Test', parent=window)   
    helloMsg.move(60, 30)  
    window.show()  
    
    
######    _Retain GUI Window_ 

```
sys.exit(app.exec_())
```     

# Calculator Using PyQt5 

## View of application
  
      
##### _1. Create view.py_ 
     
##### _2. Import following modules_ 
```
from PyQt5.QtCore import Qt  
from PyQt5.QtWidgets import QMainWindow      
from PyQt5.QtWidgets import QWidget    
from PyQt5.QtWidgets import QGridLayout    
from PyQt5.QtWidgets import QLineEdit    
from PyQt5.QtWidgets import QPushButton     
from PyQt5.QtWidgets import QVBoxLayout 
```  
    
##### _3. Create GUI class and extend QMainWindow class_
```
class GUI(QMainWindow):
```
 - ###### _Add constructor and Parameter_
```
    - SuperClass Constructor
    - setWindowTitle
    - setFixedSize
    - generalLayout
    - centralWidget
    - createDisplayLED
    - createButtons
```
 - ###### _Define Methods_
    ######   (Which will create method for Display Panel, Buttons layout and method for set/get/clear display)
```
    - createDisplayLED()
    - createButtons()
    - setDisplayText()
    - getDisplayText()
    - clearDisplay()
```

## Model of application
      
##### _1. Create model.py_ 
     
##### _2. Create function for calculator's operation_ 
```
ERROR_MSG = 'ERROR'
def evaluateExpression(expression):
    try:
        result = str(eval(expression, {}, {}))
    except Exception:
        result = ERROR_MSG

    return result
```  

## Controller of application
     
##### _1. Create controller.py_ 
     
##### _2. Import following module_ 
```
from functools import partial
```  
    
##### _3. Create Controller class_
```
class Controller:
```
 - ###### _Add constructor_
```
    def __init__(self, model, view):
        self._evaluate = model
        self._view = view
        self._connectSignals()
```
 - ###### _Define Methods_
    ######   (Which will create method for CalculateResult Build expression Connect signals and slots.)
```
    - calculateResult()
    - buildExpression()
    - connectSignals()
```
