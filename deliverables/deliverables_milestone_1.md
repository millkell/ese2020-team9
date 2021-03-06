# More than Ebay

More than Ebay (MtB) is an online market place that allows users to sell and buy products online, but extents the classic functionalities of web-based markets with a ground-braking new feature. 

<br/><br/>

## Introduction

This Document provides an overview of the project scope, objectives, use cases, functional and non-functional requirements, use case diagrams and reveals (in a later version) the seminal invention.

<br/><br/>


## Project Scope

The scope of this project is a web-based market place that allows users to sell and buy products online. After registering and setting up an account, users can upload products they want to sell on the website. Once an administrator has checked the product and given  permission to sell it, it will be displayed on the webiste and other users will be able to buy it. To buy products a registration is also required.

<br/><br/>

## Functional Requirements

* *Registration:* Users need to be able to register, with their registration data being stored and kept after closing the website.
* *Login:* After prior registration, users need to be able to login with their username and password.
* *Viewing Products:* Users need to be able to access to products up for sale. To examine the products, no login is required.
* *Selling Products:* Logged in users need be able to upload the products they want to sell.  
* *Buying Products:* Logged in users need be able to buy the available products they desire.
* *Searching Products:* The web-application shall provide a search facility that narrows the products displayed as desired. The search facility may allow full-text searching or click-based selecetion of categories.

* *Admitting Products:* The application shall allow administrative users to check and admit or decline uploaded products before they are publicly displayed.

## Non-Functional Requirements

* *Privacy:* User data must remain confidential and must confirm to
Swiss privacy laws. This includes registration data as well as the products bought. Users have the right to audit their data and to request that their data be removed from the system.
* *Usability:* Users should be able to register within one minute.
* *Usability II:* Users should be able to register, login, sell and buy products without having to read a manual.
* *Performance:* Submitting the registration form shall not exceed 10 seconds. Logging in shall not exceed 5 seconds.
* *Reliability:*The system shall be completely operational at least 95 percent of the time.
 
 <br/><br/>


## Use Case Diagram

#### A basic diagram
![](Use_Case_Diagram_I.png)

#### An extended use case diagram
![](Use_Case_Diagram_II.png)

The above diagrams were created from: https://online.visual-paradigm.com/ 

<br/><br/>


## Use Cases

In the following part, the uses cases for the two user types are listed.

#### *User*

* View products up for sale (without prior login)
* Registration
* Login
* Upload product
* Buy Product


#### *Administrator*

* Registration
* Login
* Check uploaded products (admit or decline)

<br/><br/>


## Use Case Descriptions

| View Products  |             |       
|----------|:-------------|
|  *Summary*|  Products up for sale can be looked at by any user without logging into the system  |
| *Basic Flow* |  <ol><li>The use case start when a user indicates that he wants look at the products up for sale.  </li><li>The system displays the products. </li><li> The user may read additional information about a product, e.g. the price or seller. </li><li>The user stops examing the product when desired and leaves the system, registers or logges in.	
| *Alternative Flows* | **Step 3:** If the user wants to buy a product, she will be prompted to log into the system or register.      |
| *Extension Points* |    none  |
| *Preconditions* |    none |
| *Postconditions* |     The user will have an idea about the products available and possibly log into the system or register.   |

<br/><br/>




| Register User  |             |       
|----------|:-------------|
|  *Summary*|  In order to get personalized or restricted information, place orders or do other specialized transactions a new user must register a username and password.   |
| *Basic Flow* |  <ol><li>The use case start when a user indicates that he wants to register.  </li><li>The system requests a username and password. </li><li> The user enters a username and password. </li><li>The system checks that the username does not duplicate any existing registered usernames.  </li><li>The system requests a name (\*), location, and email address(\*). Items marked by (\*) are required. </li><li>   The user enters the information. </li><li>  The system determines the user's access level and stores all user information. </li><li> The system starts a login session and displays a welcome message based on the user's preferences.  </li> </ol> 	
| *Alternative Flows* | **Step 4:** If the username duplicates an existing username the system displays a message and the use case goes back to step 2.  <br> **Step 5:**  If the user does not enter a required field, a message is displayed and the use case repeats step 4.       |
| *Extension Points* |    none  |
| *Preconditions* |    none |
| *Postconditions* |      The user can now obtain data and perform functions according to his registered access level. On the next visit, the user can login to the syste without prior registration.   |

<br/><br/>

| Login User  |             |       
|----------|:-------------|
|  *Summary*|  In order to get personalized or restricted information, place orders or do other specialized transactions a user must login so that that the system can determine his access level.  |
| *Basic Flow* |  <ol><li>The use case starts when a user indicates that he wants to login. </li><li>The system requests the username and password. </li><li> The user enters his username and password. </li><li>The system verifies the username and password against all registered users. </li><li>The system starts a login session and displays a welcome message based on the user's preferences.</li>  </ol> 	
| *Alternative Flows* | **Step 4:** if username is invalid, the use case goes back to step 2. <br> **Step 4:** if the password is invalid the system requests that the user re-enter the password. When the user enters another password the use case continues with step 4 using the original username and new password.       |
| *Extension Points* |    none  |
| *Preconditions* |    The user is logged in. |
| *Postconditions* |     The product can now be examined by an admin.  |

<br/><br/>



| Upload Products |             |       
|----------|:-------------|
|  *Summary*|  In order to sell products through the system, users will have to upload products, that can then by examined by administrators.   |
| *Basic Flow* |  <ol><li>The use case start when a user indicates that he wants to upload a product.  </li><li>The system requests a product name (\*), category, and price. Items marked by (\*) are required. </li><li>   The user enters the information. </li><li>  The system stores all user information. </li><li> The system displays a message indicating a successful upload. </li> </ol> 	
| *Alternative Flows* | **Step 5:**  If the user does not enter a required field, a message is displayed and the use case repeats step 4.       |
| *Extension Points* |    none  |
| *Preconditions* |    none |
| *Postconditions* |      The user can now obtain data and perform functions according to his registered access level. On the next visit, the user can login to the syste without prior registration.   |

<br/><br/>

| Check Product  |             |       
|----------|:-------------|
|  *Summary*| All product need to be checked by administrators before they are displays publicly in the system and put up for sale.   |
| *Basic Flow* |  <ol><li>The use case start when a admin indicates that he wants to examine a uploaded product.  </li><li>The system displays the product information. </li><li> The admin decides whether the product will be admitted or declined.</li><li>The admin admits the product.  </li><li> The system displays a message that the product has been admitted and will be displayd on the website.  </li> </ol> 	
| *Alternative Flows* | **Step 4:** If the admin declines the product it will be deleted from the database.   |
| *Extension Points* |    none  |
| *Preconditions* |    The product has  been uploaded. |
| *Postconditions* |  The product will be visible for everyone on the system.  |

<br/><br/>



| Buy Product  |             |       
|----------|:-------------|
|  *Summary*|  If a user finds an suitable product she may buy it.  |
| *Basic Flow* |  <ol><li>The use case start when a user indicates that she wants to buy a product.  </li><li> The product information are displayed. </li><li> The user confirms that she wants to buy the product. </li><li> The system checks if the user has enough money available.  </li><li> The system displays a message indicating that the purchase was successful. </li><li> The system removes the product from the visible part of the system. </li><li>   The product information and who bought it is stored in the database.  </li> </ol> 	
| *Alternative Flows* | **Step 4:** If not enough money is deposited at the user the purchase is terminated and the user informed with a message.  |
| *Extension Points* |    none  |
| *Preconditions* |    The users is logged in. The product has been checked by an admin and is displayed. |
| *Postconditions* |  The product will no longer be displayed on the system.  |

<br/><br/>

## User Stories

### Who?
*Alex* is a person that wants to sell and buy products on our platform. 

### Story 1
Alex wants to browse the products on our website without having to log in, so that she can have an overview of the available products before she registers. (functional)



### Story 2
Alex wants to register and login to our system, so that she will be allowed to buy and sell products easily from home. (functional)

### Story 3
Alex does not have a lot of spare time and wants to be able to perform all essential actions to buy or sell a product on our website, without having to read a manual. This ensures that she feels confident about the system and not overwhelmed by the functionalities. This also encourages her to spend more time on our system.(non-functional)

### Story 4 
Alex wants that all her data remains confidential and can be deleted upon request, so that she is willing to share the necessary data for the transaction and the online market place to work and trusts in our services. (non-functional)

### Story 5
Alex wants to be able to search for different keywords or product categories, so that she can find the desired products faster. (functional)

<br/><br/>



## CRC Cards 

As a first suggestion the application could consist of the following classes. A *Product* that belongs to a *Category*. The *User* may have sold or bought *Products* and knows its registration information. The class-responsibility-collaboration cards below identify possible responisabilites and collabarating classes of each class. Additonial responsabilties or classes may be added. Possibly the users can be split into normal users, registerd users and admins. 


| Product  |               |       
|----------|-------------:|
|  *Responsibility*|  *Collaborator* |
|  |
| knows name |  |
| knows price |       |
| knows seller | Seller (User) |
| knows if sold or lent | Buyer (User)   |
| knows product category |    Category  |


<br/><br/>

| Category  |             |       
|----------|-------------:|
|  *Responsibility*|  *Collaborator* |
|  |
| knows category name |       |
| knows product of that category |    Product  |


<br/><br/>

| User  |               |       
|----------|-------------:|
|  *Responsibility*|  *Collaborator* |
|  |
| knows registration info|       |
| uploads products |    Product |
| knows uploaded products |    Product |
| sells products |    Product  |
| knows sold products |    Product |
| buys products |    Product  |
| knows bought products |    Product |
| knows lent products |    Product |
| knows if it is an admin| |
| knows amount of money available |     |





