Python Automation Examples from "Automate the Boring Stuff with Python"
-----------------------------------------------------------------------

### 1\. **File Renaming:**

*   Renaming a batch of files with a consistent pattern, such as adding a prefix or suffix.
    

Python

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   import os  for filename in os.listdir('.'):      if filename.endswith('.txt'):          new_name = 'new_' + filename          os.rename(filename, new_name)   `

### 2\. **Data Scraping:**

*   Extracting information from websites, such as product prices, news headlines, or weather data.
    

Python

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   import requests  from bs4 import BeautifulSoup  url = 'https://www.example.com'  response = requests.get(url)  soup = BeautifulSoup(response.text, 'html.parser')     prices = soup.find_all('span', class_='product-price')  for price in prices:      print(price.text)   `

### 3\. **Email Automation:**

*   Sending automated emails based on specific triggers, like scheduling reminders or sending reports.
    

Python

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`import smtplib  from email.mime.text import MIMEText  sender_email = 'your_email@example.com'  receiver_email = 'recipient_email@example.com'  password = 'your_password'  message = MIMEText('This is an automated email.')  message['From'] = sender_email  message['To'] = receiver_email  message['Subject'] = 'Automated Email'  with smtplib.SMTP('smtp.gmail.com', 587) as server:      server.starttls()      server.login(sender_email, password)      server.sendmail(sender_email, receiver_email, message.as_string())`      

### 4\. **Text Message Automation:**

*   Sending automated text messages, such as appointment confirmations or weather alerts.
    

Python

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   import twilio  # Replace with your Twilio account SID and auth token  account_sid = 'YOUR_ACCOUNT_SID'  auth_token = 'YOUR_AUTH_TOKEN'  client = twilio.rest.Client(account_sid, auth_token)  message = client.messages.create(      to='recipient_phone_number',      from_='your_twilio_number',      body='This is an automated text message.'  )   `

### 5\. **Excel Spreadsheet Automation:**

*   Automating tasks within Excel, such as formatting data, creating charts, or performing calculations.
    

Python

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   import openpyxl  workbook = openpyxl.load_workbook('your_workbook.xlsx')  sheet = workbook.active  # Perform operations on the spreadsheet  sheet['A1'] = 'New Value'  sheet.insert_rows(1, 2)  workbook.save('updated_workbook.xlsx')   `

### 6\. **PDF Manipulation:**

*   Extracting text from PDFs, merging multiple PDFs, or converting PDFs to other formats.
    

Python

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   import PyPDF2  pdf_reader = PyPDF2.PdfReader('input.pdf')  text = pdf_reader.pages[0].extract_text()  print(text)   `

### 7\. **Web Automation:**

*   Interacting with web pages, such as filling out forms, clicking buttons, or downloading files.
    

Python

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   from selenium import webdriver  driver = webdriver.Chrome()  driver.get('https://www.example.com')  # Find elements and interact with them  element = driver.find_element_by_id('username')  element.send_keys('your_username')  # ... other actions  driver.quit()   `

### 8\. **Image Manipulation:**

*   Resizing, cropping, or adding watermarks to images.
    

Python

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   from PIL import Image  image = Image.open('image.jpg')  resized_image = image.resize((200, 200))  resized_image.save('resized_image.jpg')   `

### 9\. **Desktop Automation:**

*   Automating repetitive tasks on your desktop, such as moving files, opening applications, or controlling the mouse and keyboard.
    

Python

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   import pyautogui  # Move the mouse to a specific location  pyautogui.moveTo(100, 100)  # Click the mouse  pyautogui.click()  # Type text  pyautogui.typewrite('Hello, world!')   `

### 10\. **Data Cleaning:**

*   Cleaning and preparing data for analysis, such as removing duplicates, handling missing values, or formatting data consistently.
    

Python

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   import pandas as pd  data = pd.read_csv('data.csv')  # Clean the data  data = data.dropna()  # Remove missing values  data = data.drop_duplicates()  # Remove duplicates  # Format the data  data['date'] = pd.to_datetime(data['date'])  # Save the cleaned data  data.to_csv('cleaned_data.csv', index=False)   `