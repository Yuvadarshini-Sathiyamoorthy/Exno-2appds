# Exno-2appds
## AIM:
    
To Perform Data Collection through web scraping using python.

## ALGORITHM:
Step 1: Include the Necessary python libraries.
 
Step 2: Use the requests library to send HTTP requests to a web page.
 
Step 3: Retrieve the HTML content and use BeautifulSoup to parse it.
 
Step 4: Navigate and extract the necessary data.
 
Step 5: Handle the Java script content and retrieve the data using the html tags.
 
Step 6: Check with the website permission and scrap the content.

## CODING & OUTPUT:
```
pip install beautifulsoup4 requests
import requests
from bs4 import BeautifulSoup
import pandas as pd
url = 'https://www.w3schools.com/html/html_tables.asp'
response = requests.get(url)
```
![image](https://github.com/user-attachments/assets/79ef5ad9-7665-40df-a163-dfa12e5051f0)
```
response
soup = BeautifulSoup(response.content, 'html.parser')
headings = soup.find_all('h2')
for heading in headings:
  print(heading.text)
```
![image](https://github.com/user-attachments/assets/13d869a3-b929-4830-9dfb-1a78cb6bf7c4)
```
data = []
for heading in headings:
  data.append(heading.text)
df=pd.DataFrame(data)
df.to_csv('newdata.csv', index=False)
df.head()
```
![image](https://github.com/user-attachments/assets/291a6028-eba2-48c5-823c-746b235f2e62)

## RESULT:
 Thus , data Collection through web scraping using python is successfully performed.
