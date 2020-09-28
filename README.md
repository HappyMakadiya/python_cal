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
