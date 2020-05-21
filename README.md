## Library Management System Lito for a university

## Technologies
Spring, DI, MVC, ORM, transactions.

## Tools
IntelliJ, Maven, MySQL, Apache Tomcat

## Requirements implemented

### Functional Requirements
This app manages many aspects of a university library system, including cataloging, search, circulation, and waiting list. The interface is web based, and the server needs to be hosted on the cloud, and is accessible from anywhere with Internet connection.

#### Users and Authentication
There are two roles of users, librarian and patron.

1. A librarian manages cataloging, and can assist circulation as well.

2. A patron is a customer of the library. He can search for books, borrow and returns books.

3. For simplicity, we allow any user with any email address to be able to create his account using an email as the username, and password of his choice. The user also needs to provide a university ID of 6 digits.

4. App sends an email to the user with a verification code. The user needs to use that verification code to complete his account registration. A registered user cannot really use features in the system until his account is verified. A confirmation email must be sent to the user after completion of account verification.

5. For simplicity, we only and automatically register any user with an SJSU email account (@sjsu.edu) to be a librarian.  A librarian cannot be a patron, which means he has to use a different email to register if he needs a patron account as well.

6. No two patrons can have the same university ID, neither can two librarians.

#### Cataloging

1. A librarian is able to manage the catalog of the books.

2. A book item contains the following properties 

  * Author
  * Title
  * Call number
  * Publisher
  * Year of publication
  * Current status
  * Keywords


3. A librarian is able to search, add, update, and delete books.

  * Search capability functions as a superset of search features to be described below for patrons.  
    * Search has the apability to search for books created or updated by a particular librarian.  
  * Update and deletion works together with search, i.e., a librarian has the capability to find a book through search, then decide to update/delete it.
  * A book cannot be deleted if it’s checked out by a patron.
  * Deleting a book also removes the waiting list for it, if there is any.
  * [Bonus Feature] Integrated with external APIs to simplify the input the book info based on ISBN.

#### Waiting list
1. A patron can add himself to a waiting list if the book he is interested in is currently checked out by somebody else. There is no limit on how many people can be added to a waiting list, yet the order in the waiting is preserved. You cannot add the same person to the same list twice for the same book.
2. When a book becomes available, the first person on the waiting list is notified about its availability, and the person is removed from the waiting list. The book is reserved for this person for three days, during which only this person can check out this book. After these three days, the reservation is cancelled, and the next person in the waiting list (if there is any) is notified about the availability, and a three-day reservation is created for him as well. So on and so forth.


## Github setup
1. Use a github UI application. E.g. Source Tree
2. Clone this repository to your workstation: https://github.com/Marlen1703/BackEnd_Final
3. Follow the instructions from this document to setup the environment on your local machine.


## Contributor:
Ibraimov Marlen


## Home Page
![](images/greeting.jpg)


## List Page
![](images/list.jpg)

## Add Book
![](images/add.jpg)


## Add Author
![](images/add_author.jpg)


## Request
![](images/postman.jpg)









