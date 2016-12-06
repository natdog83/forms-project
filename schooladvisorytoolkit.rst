***********
Care Kit
***********

The School Advisory Toolkit form on jdrf.org goes to the lead object in Salesforce.  When the form is submitted it creates
a lead in Salesforce and through a workflow the lead is convereted into a contact and an outreach reaquest and the
status is marked as fulfilled.  An email is sent to the chapter to the chapter once the Outreach Request is created
with details to follow up.

 * The link to the production environment is: http://typeonenation.org/resources/newly-diagnosed/t1d-toolkits/toolkit-request-form/?toolkitType=1

 * The link to the staging environment is: http://type1nation.staging.wpengine.com/request-toolkit-school/

T1D Care Kit Form Fields
########################

+---------------------------------+-------------------------------+-----------+--------------------+------------------------+
| Field                           | Type/Options                  | Required  | Validation         | Notes                  |
+=================================+===============================+===========+====================+========================+
| Title                           | Picklist                      | Yes       |                    |                        |
+---------------------------------+-------------------------------+-----------+--------------------+------------------------+
| First Name                      | Text                          | Yes       |                    |                        |
+---------------------------------+-------------------------------+-----------+--------------------+------------------------+
| Last Name                       | Text                          | Yes       |                    |                        |
+---------------------------------+-------------------------------+-----------+--------------------+------------------------+
| Email                           | email                         | Yes       |                    |                        |
+---------------------------------+-------------------------------+-----------+--------------------+------------------------+
| Phone                           | Phone                         | No        |                    |                        |
+---------------------------------+-------------------------------+-----------+--------------------+------------------------+
| Date of Diagnosis               | Date                          | No        |                    |                        |
+---------------------------------+-------------------------------+-----------+--------------------+------------------------+
| What is your connection         | Radio                         | Yes       |                    |                        |
| to type 1 diabetes?             |  * I have T1D                 |           |                    |                        |
|                                 |  * My child                   |           |                    |                        |
|                                 |  * My grandchild              |           |                    |                        |
|                                 |  * My sibling                 |           |                    |                        |
|                                 |  * My spouse/partner          |           |                    |                        |
|                                 |  * My parent                  |           |                    |                        |
|                                 |  * Another family member      |           |                    |                        |
|                                 |  * Friend or co-worker        |           |                    |                        |
|                                 |  * I prefer not to answer     |           |                    |                        |
+---------------------------------+-------------------------------+-----------+--------------------+------------------------+
| Do you want a printed copy      | Radio                         | Yes       |                    |                        |
| mailed to you?                  |  * Yes, please                |           |                    |                        |
|                                 |  * No, thank you              |           |                    |                        |
+---------------------------------+-------------------------------+-----------+--------------------+------------------------+
| Street Address                  | Text                          | No        |                    |                        |
+---------------------------------+-------------------------------+-----------+--------------------+------------------------+
| Address Line 2                  | Text                          | No        |                    |                        |
+---------------------------------+-------------------------------+-----------+--------------------+------------------------+
| City                            | Text                          | No        |                    |                        |
+---------------------------------+-------------------------------+-----------+--------------------+------------------------+
| State                           | Picklist                      | No        |                    |                        |
+---------------------------------+-------------------------------+-----------+--------------------+------------------------+
| ZIP Code                        | Text                          | No        |                    |                        |
+---------------------------------+-------------------------------+-----------+--------------------+------------------------+
| Country                         | Picklist                      | No        |                    |                        |
+---------------------------------+-------------------------------+-----------+--------------------+------------------------+
| School                          | Text                          | No        |                    |                        |
+---------------------------------+-------------------------------+-----------+--------------------+------------------------+
| Grade(s)                        | Check box                     | No        |                    |                        |
|                                 |  * Preschool / Kindergarten   |           |                    |                        |
|                                 |  * Elementary                 |           |                    |                        |
|                                 |  * Middle / Junior High       |           |                    |                        |
|                                 |  * High School                |           |                    |                        |
|                                 |  * Other                      |           |                    |                        |
+---------------------------------+-------------------------------+-----------+--------------------+------------------------+

Form Submit Confirmation Message
################################

Thanks for contacting us! We will get in touch with you shortly.

Triggers
########

Trigger run when a lead is created with School Advisory Toolkit lead source and does the following (details below):
 * Create contact from Lead data
 * Create Outreach Request record from Lead data and link contact to outreach request.
 * Delete Lead record upon conversion to Contact record

Form Fields Mapping to Lead Object
##################################

+---------------------------------+-------------------------------+---------------------------+-----------+--------------------+
| Field                           | Type/Options                  | Destination               | Required  | Validation         |
+=================================+===============================+===========================+===========+====================+
| Please confirm this request is  | Checklist                     | N/A                       | Yes       |                    |
| for a newly diagnosed child...  |  * 16 years or older          |  Javacript for form       |           |                    |
|                                 |  * United States resident     |                           |           |                    |
+---------------------------------+-------------------------------+---------------------------+-----------+--------------------+
| Lead Source                     | Hidden Field                  | Lead Source               | Yes       |                    |
|                                 |  * T1D Care Kit               |                           |           |                    |
+---------------------------------+-------------------------------+---------------------------+-----------+--------------------+
| Is the care kit for you         | Picklist                      | Salutation                | Yes       |                    |
| or someone else?                |                               |                           |           |                    |
+---------------------------------+-------------------------------+---------------------------+-----------+--------------------+
| Title                           | Picklist                      | Title                     | Yes       |                    |
+---------------------------------+-------------------------------+---------------------------+-----------+--------------------+
| First Name                      | Text                          | Name - First Name         | Yes       |                    |
+---------------------------------+-------------------------------+---------------------------+-----------+--------------------+
| Last Name                       | Text                          | Name - Last Name          | Yes       |                    |
+---------------------------------+-------------------------------+---------------------------+-----------+--------------------+
| Email                           | Text                          | Email                     | Yes       |                    |
+---------------------------------+-------------------------------+---------------------------+-----------+--------------------+
| What is your connection         | Radio                         | Online T1D Connection     | Yes       |                    |
| to type 1 diabetes?             |                               |                           |           |                    |
+---------------------------------+-------------------------------+---------------------------+-----------+--------------------+
| Street Address                  | Text                          | Address - Street          | Yes       |                    |
+---------------------------------+-------------------------------+---------------------------+-----------+--------------------+
| Address Line 2                  | Text                          | Address - Street          | Yes       |                    |
+---------------------------------+-------------------------------+---------------------------+-----------+--------------------+
| City                            | Text                          | Address - City            | Yes       |                    |
+---------------------------------+-------------------------------+---------------------------+-----------+--------------------+
| State                           | Text                          | Address - State/Province  | Yes       |                    |
+---------------------------------+-------------------------------+---------------------------+-----------+--------------------+
| Zip Code                        | Text                          | Address - Zip/Postal Code | Yes       |                    |
+---------------------------------+-------------------------------+---------------------------+-----------+--------------------+

Lead Object
##########################################

Lead Owner
Lead Status
Lead Source
Lead Record Type
Name - Salutation
Name - First Name
Name - Last Name
Company
Online T1D Connection
Street
City
State/Province
Zip/Postal Code
Country
Other Phone
Email
JDRF Location Name
Region
Chapter
Branch
Diagnosis Date
Outreach Volunteer Opt Out
Preferred Gender of OV
School (School Advisory Toolkit and Teen Toolkit ONLY)
Which group best fits your interests (School Advisory Toolkit and Teen Toolkit ONLY)
Created By
Last Modified By

School Advisory Tookkit Layout in the Leads Object
#######################################################

The Toolkit Layout is assigned to the School Advisory Toolkit lead record type and assigned to all user profiles.

(Layout will go here)

Map fields from Leads object to Contact object
#######################################################

Lead Source
Name - Salutation
Name - First Name
Name - Last Name
Online T1D Connection (Luminate Online T1D Connection)
Has Diabetes
Diagnosis Date
Street
City
State/Province
Zip/Postal Code
Country
Other Phone
Email

Map fields from Leads object to Outreach Request object
#######################################################

Toolkit Type
Requested By
Requested Date
Existing Walk Supporter
Request Status
Record Type
Contact
School Name
Diagnosis Date (Date of Diagnosis)
Outreach Volunteer Opt Out
Preferred Gender of OV
T1D Connection
Online T1D Connection
Which group best fits your interests

School Advisory Toolkit Layout in the Outreach Request Object
##############################################################

The Toolkit Layout is assigned to the School Advisory Toolkit type and assigned to all user profiles.

(Layout will go here)

Email Content
#############

GS - needs to be added.
