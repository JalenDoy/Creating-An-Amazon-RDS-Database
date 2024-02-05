# Creating-An-Amazon-RDS-Database

<h2>Task 1: Creating an Amazon RDS database </h2>

1. In the search bar type in "RDS" and click on RDS to open the RDS console
2. Choose "Create Database"
3. Under "Engine Options", select MySQL
4. Set the templates and availability and durability options:
    - Under the Templates section, select  Dev/Test.
    - Under the Availability and durability section, select "Single DB instance"
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
9. Choose "Create Database"

<p align="center">
<br/>
<img src="https://i.imgur.com/2usy9oo.png"/>



<h2>Task 2: Creating an Amazon RDS database </h2>

1. In the search bar, type EC2 to open the EC2 console
2. In the left navigation pane, choose Instances. In the center pane, there should be a running instance that is named App Server.
3. Select the App Server instance.
4. In the Details tab, copy the Public IPv4 address to your clipboard.
5. Open a new web browser tab, paste the IP address into the address bar, and then press ENTER. The web application should appear. It does not display much information because the application is not yet connected to the database.
6. Choose Settings
7. Return to the AWS Management Console
8. In the search bar, type in RDS to open the RDS console
9. Choose Databases in the left navigation pane
10. Choose inventory-db
11. Scroll to the Connectivity & Security section and copy the Endpoint to your clipboard.
12. Return to the Browser tab and enter the following information:
    - Endpoint: Paste the endpoint that was copied earlier
    - Databsase: Invetory
    - Username: admin
    - lab-password: lab-password
    - Choose Save

<p align="center">
<br/>
<img src="https://i.imgur.com/RdnOCYH.png"/>
