# Python Notes and Examples for RPA

## **1. Python Basics**
### **Data Types**
- **Numbers**: `int`, `float`
- **Sequences**: `str`, `list`, `tuple`
- **Mappings**: `dict`
- **Booleans**: `True`, `False`
- Example:
  ```python
  num = 10         # int
  name = "Alice"   # str
  items = [1, 2, 3] # list
  is_active = True  # bool
  ```

### **Conditional Statements**
- Example:
  ```python
  age = 18
  if age >= 18:
      print("Adult")
  else:
      print("Minor")
  ```

### **Loops**
- Example:
  ```python
  for i in range(5):
      print(i)

  i = 0
  while i < 5:
      print(i)
      i += 1
  ```

### **Functions and Modules**
- Example:
  ```python
  def greet(name):
      return f"Hello, {name}!"

  print(greet("Alice"))
  ```

### **Exception Handling**
- Example:
  ```python
  try:
      result = 10 / 0
  except ZeroDivisionError:
      print("Cannot divide by zero!")
  ```

---

## **2. File Handling**
### **Reading and Writing Files**
- Example:
  ```python
  with open('data.txt', 'w') as file:
      file.write("Hello, RPA Team!")

  with open('data.txt', 'r') as file:
      content = file.read()
      print(content)
  ```

### **Directory Management**
- Example:
  ```python
  import os

  os.mkdir("new_folder")
  print(os.listdir())
  ```

---

## **3. Web Scraping and Automation**
### **Web Scraping**
- Example:
  ```python
  import requests
  from bs4 import BeautifulSoup

  response = requests.get('https://example.com')
  soup = BeautifulSoup(response.text, 'html.parser')
  print(soup.title.text)
  ```

### **Web Automation**
- Example:
  ```python
  from selenium import webdriver

  driver = webdriver.Chrome()
  driver.get("https://example.com")
  driver.quit()
  ```

---

## **4. APIs and Web Requests**
### **API Interaction**
- Example:
  ```python
  import requests

  response = requests.get('https://api.example.com/data')
  if response.status_code == 200:
      print(response.json())
  ```

---

## **5. Data Handling**
### **Using `pandas`**
- Example:
  ```python
  import pandas as pd

  data = {'Name': ['Alice', 'Bob'], 'Age': [25, 30]}
  df = pd.DataFrame(data)
  print(df)
  ```

### **Excel Manipulation**
- Example:
  ```python
  from openpyxl import Workbook

  wb = Workbook()
  ws = wb.active
  ws.append(["Name", "Age"])
  ws.append(["Alice", 25])
  wb.save("data.xlsx")
  ```

---

## **6. Working with Dates and Times**
- Example:
  ```python
  from datetime import datetime

  now = datetime.now()
  print(now.strftime("%Y-%m-%d %H:%M:%S"))
  ```

---

## **7. Scripting and Process Automation**
- Example:
  ```python
  import subprocess

  subprocess.run(["echo", "Hello, RPA Team!"])
  ```

---

## **8. Keyboard and Mouse Automation**
- Example:
  ```python
  import pyautogui

  pyautogui.moveTo(100, 100, duration=1)
  pyautogui.click()
  ```

---

## **9. Regular Expressions**
- Example:
  ```python
  import re

  text = "Contact: alice@example.com"
  match = re.search(r'[\w.]+@[\w.]+', text)
  if match:
      print(match.group())
  ```

---

## **10. Libraries for RPA**
### **`pywin32`**
- Example:
  ```python
  import win32com.client

  excel = win32com.client.Dispatch("Excel.Application")
  excel.Visible = True
  workbook = excel.Workbooks.Add()
  workbook.SaveAs("example.xlsx")
  ```

### **`PyPDF2`**
- Example:
  ```python
  from PyPDF2 import PdfReader

  reader = PdfReader("example.pdf")
  for page in reader.pages:
      print(page.extract_text())
  ```

---

## **11. Logging and Debugging**
### **Logging**
- Example:
  ```python
  import logging

  logging.basicConfig(level=logging.INFO, format='%(asctime)s - %(message)s')
  logging.info("Automation script started")
  ```

---

## **12. Introduction to RPA Libraries**
### **`pywinauto`**
- Example:
  ```python
  from pywinauto import Application

  app = Application().start("notepad.exe")
  app.Notepad.Edit.type_keys("Hello, RPA Team!", with_spaces=True)
  ```

---

These notes provide a comprehensive foundation for Python in RPA workflows. Let me know if additional details or topics are required!

