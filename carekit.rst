***********
Care Kit
***********

The Care Kit form on jdrf.org goes to the lead object in Salesforce.  When the form is submitted it creates
a lead and through a workflow the lead is convereted into a contact and an outreach reaquest and marks the
status as fulfilled.  An email is sent to the chapter to the chapter once the Outreach Request is created
with details to follow up.

 * The link to the production environment is: http://type1nation.staging.wpengine.com/request-care-kit/

 * The link to the staging environment is: http://type1nation.staging.wpengine.com/request-care-kit/

T1D Care Kit Form Fields
########################

Form Submit Confirmation Message
################################

Thanks for contacting us! We will get in touch with you shortly.

Triggers
########

Trigger run when a lead is created with T1D Care Kit lead source and does the following (details below):
 * Lead records are AUTOMATICALLY converted to Contact records immediately
 * Delete Lead record upon conversion to Contact record
 * Update Outreach Request record from Lead record lookup to Contact record lookup upon conversion to Contact record

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
Endocrinologist
Birthdate
Diagnosis Date
Outreach Volunteer Opt Out
Preferred Gender of OV
Created By
Last Modified By

T1D Care Kit Layout in the Leads Object
#######################################################

The T1D Care Kit Layout is assigned to the T1D Care Kit lead record type and assigned to all user profiles.

(Layout will go here)

Map fields from Leads object to Outreach Request object
#######################################################

Requested By
Requested Date
Existing Walk Supporter
Request Status
Record Type
Contact
Diagnosis Date (Date of Diagnosis)
Endocrinologist
Outreach Volunteer Opt Out
Preferred Gender of OV
T1D Connection
Online T1D Connection
Map Fields from Leads Object to Contact Object
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

T1D Care Kit Layout in the Outreach Request Object
##################################################

The T1D Care Kit Layout is assigned to the T1D Care Kit Outreach Request record type and assigned to all user profiles.

(Layout will go here)

Email Content
#############

GS - needs to be added.
