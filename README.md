# AgroGrow
Java micro project

## Abstract

Agriculture is the main occupation in India. Two-third of population is dependent on agriculture directly or indirectly. It is not merely a source of livelihood but a way of life. It is the main source of food, fodder and fuel. It is the basic foundation of economic development. Agriculture provides highest contribution to national income.

But agriculture community is riddled with several challenges. Some of the main challenges like they are not aware about the ideal crop conditions required for the crop, updated prices of the crop in the mandis, not having a simple tool to store their expenses and at last visualize their profit/loss based on the amount earned at the end.

So, I thought of creating a java application which will take care of the pain points of farmers and provide better solution. So, that they can look every detail about the crop and farm at one place. This in turn helps farmer to increase his farming output and having better chances of profit since they are aware of the crop condition using the application. So, the name of application is AgroGrow.


<br/><br/>
## Working

Working

The application works on local storage concept so there is no need to login. The application starts by asking following options to the user:
  1.	Crop related details
  2.	Add expenses 
  3.	Price comparison chart
  4.	Data in Graph
  5.	To exit

Based on the given input corresponding class runs. We will see each operation in detail.

### 1.	Crop related details:
After entering first option user is asked the crop name of which he wants to see the details of. Based on the input the class function searches in the crop details related file to check crop exits or not. If the crop exists then the user is asked what he/she would like to see about the crop that is information, ideal conditions, soil requirements, yield or exit. And based on the option selected the corresponding detail is begin displayed. If the crop name would have not begin found we would have shown a prompt of no crop found.

### 2.	Add expenses:
If the user feels of adding any expense, he/she can press 2nd option at the starting option. Firstly, it is checked if the user has already entered farm area or not if not, user is asked to enter farm area in acre. The there are two options one to add expenses and other to exit. If the user enters first option user is asked to enter expense name and asked to enter cost per acre for the entered expense. Based on the entered value the data is stored in file for further usage.

### 3.Price comparison chart
In this option the user is asked to enter the crop name and total kg’s gown per acre. The entered values are stored inside farm class also. The entered name of crop is then been searched in price list file using buffer reader class. In this file data is stored in below format
name tomato region jalna minPrice 1200 maxPrice 1500
The line is then split into array and 1st index is compared with the entered crop name. If we are able to find the crop name in the file we will take the min price and max price of the crop and also the region. After traversing the file, we will show the user the options to sell his crop with location and price ranges. So, this helps user clear idea where to sell and at what price. 

### 4.	Data in graph
This option can be used to see the expenses and profit/loss in the applet viewer. On pressing 4th option, a check is made to see if the user has added any expenses or not. If not, user is asked to add expenses. If user has added the expenses a runtime class exec function is used to open the command prompt and run the command to run applet. In the applet screen the user is asked to enter the amount earned after selling his crops. After the form submission all the expenses from the expenses file are added. The total is then compared with total money earned at the end of cycle. 
•	If the amount is greater then it is profit. And we use the graphic functions like draw arc, fill arc to draw a pie chart to represent the details of the expenses and profit. 
•	If the amount is smaller than expenses the user is shown a loss message and a pie chart with a value of earned and no profit is shown. 
