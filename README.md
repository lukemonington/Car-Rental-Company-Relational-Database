<h1> Relational Database Development </h1>
<h2> The Scenario </h2>
The challenge is to develop a relational database using Oracle SQL Developer for a hypothetical car rental business with several addresses. The business rents multiple different types of cars, which each have their own respective rental prices. The rental pricing is also dependent upon available promotions. Additionally, the business keeps track of all of its customers and employees. It is also possible to be both an employee and a customer at the same time.
<h2> Assumptions </h2>
To better understand the constraints, I created a list of assumptions for use with table design. These assumptions were:
<ol>
  <li> A person does not have more than two ID numbers. </li>
  <li> A person can be an employee, a customer, or both.</li>
  <li> The return date is predetermined at time of rental. </li>
  <li> Store locations have at least one car.</li>
  <li> Employees are assigned to exactly one store.</li>
  <li> A car can be rented many times</li>
  <li> A rental transaction is limited to one car.  </li>
  <li> A car classification can only have one discount code at a time. </li>
</ol>
<h2> Table Creation & Logical ER Model </h2>
After diving into the details, I determined that it was necessary to create 6 tables: Car, CarClassification, Promotion, RentalTransaction, and StoreLocation. I listed the attributes that I would keep track of, and then designed a data dictionary (attached as another file in this repository). 
![Logical ER Model](https://user-images.githubusercontent.com/42416078/78065518-a588b800-7350-11ea-9a98-13b80d8543ba.png)
<h2> The Normalization Process </h2>
Normalization is a database design technique that organizes tables in a manner that reduces redundancy and removes potential anomalies. The 3 main types of anomalies are:
<ol>
  <li> Deletion Anomalies: where deleting one row inadvertently deletes something else </li>
  <li> Insert Anomalies: where a table can't add a new record until it already exists </li>
  <li> Update Anomalies: where the same data is stored multiple times, and all of them don't get updated </li>
</ol>
For this project, I normalized 
