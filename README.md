# myui-using-python
1.Install pyqt5 package after installing python3 using 
      sudo apt install python3-pip
      sudo apt install python3-pyqt5
      sudo apt install pyqt5-dev-tools

      

2.python3 myui.py (in command prompt)


Pyqt5:
pyqt5 is a python GUI package 

let's continue with the myui file from the previous section.Now, let's see how to add a user-defined function to the Python script and connect it to the clicked signal of the OK button. Assume that we want to print the message ‘Valid Password’ if the password field contains the text 'Internshala' otherwise print the message, ‘Invalid Password’.

1.Open the myui.py file in IDLE.
Now, add the following function inside the class, Ui_MainWindow
def chkPassword(self):
        txt=self.lineEdit.text()
        if txt=='saleekah':
            print ('Valid password')
        else:
            print ('Invalid password')
In this function, lineEdit refers to the name of ththe Password line edit field generated in Qt Designer.
Next, add the following statement inside the method, setupUi()
 self.button1.clicked.connect(self.chkPassword)
 
 Save this script and run it. Test the working of the OK button by entering any password and by entering the password, saleekah
