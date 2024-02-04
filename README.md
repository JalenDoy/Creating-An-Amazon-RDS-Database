# Creating-An-Amazon-RDS-Database

<h2>Task 1: Creating an Amazon RDS database </h2>

1. In the search bar type in "RDS" and click on RDS to open the RDS console
2. Choose "Create Database"
3. Under "Engine Options", select MySQL
4. Set the templates and availability and durability options:
    - Under the Templates section, select  Dev/Test.
    - Under the Availability and durability section, select   Single DB instance
    - Note: the default Multi-AZ deployment option automatically creates a replica of the database in a second Availability Zone for High Availability, however in this lab that is not needed.
5. Under the Settings section, configure these options:
    - DB instance identifier: inventory-db
    - Username: admin
    - Password: lab-password
    - Confirm password: lab-password
6. Under the DB instance class section, configure these options:
    - Select Burstable classes (includes t classes).
    - Select db.t3.micro
7. Under the Connectivity section, configure these options: 
    - Virtual Private Cloud (VPC): Lab VPC
    - Existing VPC security groups: 
      - Choose DB-SG. It will be highlighted.
      - Remove the default security group.
 8. Expand the Additional configuration panel, then configure these settings:
    - Initial database name: inventory
    - Note: This is the logical name of the database that will be used by the application.
    - Clear (turn off) the Enable Enhanced monitoring option





<p align="center">
<br/>
<img src="https://i.imgur.com/V97GtNn.png"/>
