# ShoppingApi
This is python Script that provides an Api for kilimall and Jumia Shopping sites.

#Getting Started
Clone the repository from GitHub<br />
`$ git clone https://github.com/Keithwachira/ShoppingApi.git`

#Prerequisites
You need python 2.6 or a later version to run this script,you also need requests,lxml and BeautifulSoup
#installing the prerequisites
`$ pip install requests`<br /><br />
`$ pip install BeautifulSoup`<br /><br />
`pip install lxml`<br /><br />
or<br />
`$ easy_install requests`<br /><br />
`$ easy_install BeautifulSoup `<br /><br />
`$ easy_install lxml`<br /><br />
#Example 
using the jumia Api
```python
import ShoppingApi
url="https://www.jumia.co.ke/smartphones/?page=2"
#downloading all smartphone from second jumia page
try:
  jumia_items=ShoppingApi.storeJumia("url")
  #loop trough the list returned and store the data
  """to print first item in the shop"""
  try:
      print jumia_items[0]
  except indexError:
      print "page has no phones"
  for items in jumia_items:
      #store items in a database for later use
except AttributeError:
     print "No such page found"
```
<br /><br />
using the Kilimall Api
```python
import ShoppingApi
url="https://www.kilimall.co.ke/smartphones/"
#downloading all smartphone from kilimall first page
try:
  kilimall_items=ShoppingApi.storeKilimall("url")
  #loop trough the list returned and store the data
  for items in jumia_items:
      #store items in a database for later use
except AttributeError:
     print "No such page found"
```

#Running the Program in terminal
1.Open the terminal and cd into the directory you extracted the project.<br />
2.On the terminal run **python ShoppingApi.py** and if all your text run you should get output as follows<br />
![Alt text](/test.png?raw=true "Optional Title")



 
 
