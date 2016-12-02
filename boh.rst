***********
Bag of Hope
***********

When your child receives a diagnosis of type 1 diabetes (T1D), it can be an overwhelming time. As you navigate this challenging period of adjustment to life with T1D, you can find helpful information and support through the JDRF Bag of Hope®. The JDRF Bag of Hope is filled with useful resources for both the child who has been diagnosed with T1D and his or her caregivers. Along with educational materials, we’ve included a special friend — Rufus, the Bear with Diabetes® — to show your child he or she is not alone while learning to take shots and test blood sugar.
Resources in your JDRF Bag of Hope.

The BOH form was creatd in Gravity Forms and sends the data to the Salesforce Lead object.

Form Fields
######

+---------------------------------+-------------------------------+---------------------------+-----------+--------------------+
| Field                           | Type/Options                  | Destination               | Required  | Validation         |
+=================================+===============================+===========================+===========+====================+
| Please confirm this request is  | Checklist                     | N/A                       | Yes       |                    |
| for a newly diagnosed child...  |  * 16 years or younger        |  Javacript for form       |           |                    |
|                                 |  * Less than one year ago     |                           |           |                    |
|                                 |  * United States resident     |                           |           |                    |
+---------------------------------+-------------------------------+---------------------------+-----------+--------------------+
| Lead Source                     | Hidden Field                  | Lead Source               | Yes       |                    |
|                                 |  * BOH                        |                           |           |                    |
+---------------------------------+-------------------------------+---------------------------+-----------+--------------------+
| Title                           | Picklist                      | Salutation                | Yes       |                    |
+---------------------------------+-------------------------------+---------------------------+-----------+--------------------+
| First Name                      | Text                          | Name - First Name         | Yes       |                    |
+---------------------------------+-------------------------------+---------------------------+-----------+--------------------+
| Last Name                       | Text                          | Name - Last Name          | Yes       |                    |
+---------------------------------+-------------------------------+---------------------------+-----------+--------------------+
| Suffix                          | Picklist                      | Suffix                    | No        |                    |
+---------------------------------+-------------------------------+---------------------------+-----------+--------------------+
| Email                           | Text                          | Email                     | Yes       |                    |
+---------------------------------+-------------------------------+---------------------------+-----------+--------------------+
| Phone                           | Text                          | Other Phone               | Yes       |                    |
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
| Child Title                     | Text                          | Child Title               | Yes       |                    |
+---------------------------------+-------------------------------+---------------------------+-----------+--------------------+
| Child First Name                | Text                          | Child First Name          | Yes       |                    |
+---------------------------------+-------------------------------+---------------------------+-----------+--------------------+
| Child Last Name                 | Text                          | Child Last Name           | Yes       |                    |
+---------------------------------+-------------------------------+---------------------------+-----------+--------------------+
| Child Suffix                    | Text                          | Child Suffix              | No        |                    |
+---------------------------------+-------------------------------+---------------------------+-----------+--------------------+
| Child DOB                       | Text                          | Child Date of Birth       | Yes       |                    |
+---------------------------------+-------------------------------+---------------------------+-----------+--------------------+
| Child Date of Diagnosis         | Text                          | Child Date of Diagnosis   | Yes       |                    |
+---------------------------------+-------------------------------+---------------------------+-----------+--------------------+
| Gender                          | Text                          | Child Gender              | No        |                    |
+---------------------------------+-------------------------------+---------------------------+-----------+--------------------+
| Hospital                        | Text                          | Diagnosis Detail          | No        |                    |
+---------------------------------+-------------------------------+---------------------------+-----------+--------------------+
| Endocrinologist                 | Text                          | Diagnosis Detail          | No        |                    |
+---------------------------------+-------------------------------+---------------------------+-----------+--------------------+
| Do you want to be connected     | Picklist                      | Mentor Opt Out            | Yes       |                    |
| with a JDRF Outreach Volunteer? |  * No                         |                           |           |                    |
|                                 |  * Yes                        |                           |           |                    |
+---------------------------------+-------------------------------+---------------------------+-----------+--------------------+
| Child's Hobbies/Interests       | Text                          | Child's Hobbies           | No        |                    |
+---------------------------------+-------------------------------+---------------------------+-----------+--------------------+
| School                          | Text                          | School                    | No        |                    |
+---------------------------------+-------------------------------+---------------------------+-----------+--------------------+

Triggers
########

Trigger run when a lead is created with BOH as the lead type and does the following (details below):
 * Creates a contact for the parent contact record
 * Creates a contact for the child contact record and adds the contact to the parent household
 * Creates an Outreach request and links both the parent and child contact record to the outreach request
 * Automatically create new Additional Interest record upon Contact record creation

Parent Contact Record
*********************

+---------------------------+---------------------------+-----------------------------+
| Lead Object               | Contact Object            | Auto fill                   |
+===========================+===========================+=============================+
| Lead Source               | Lead Source               |                             |
+---------------------------+---------------------------+-----------------------------+
| Salutation                | Salutation                |                             |
+---------------------------+---------------------------+-----------------------------+
| Name - First Name         | Name - First Name         |                             |
+---------------------------+---------------------------+-----------------------------+
| Name - Last Name          | Name - Last Name          |                             |
+---------------------------+---------------------------+-----------------------------+
| Suffix                    | Suffix                    |                             |
+---------------------------+---------------------------+-----------------------------+
| Email                     | Email                     |                             |
+---------------------------+---------------------------+-----------------------------+
| Other Phone               | Other Phone               |                             |
+---------------------------+---------------------------+-----------------------------+
| Address - Street          | Address - Street          |                             |
+---------------------------+---------------------------+-----------------------------+
| Address - Street2         | Address - Street2         |                             |
+---------------------------+---------------------------+-----------------------------+
| Address - City            | Address - City            |                             |
+---------------------------+---------------------------+-----------------------------+
| Address - State/Province  | Address - State/Province  |                             |
+---------------------------+---------------------------+-----------------------------+
| Address - Zip/Postal Code | Address - Zip/Postal Code |                             |
+---------------------------+---------------------------+-----------------------------+

When the parent record is created it will automatically create a household record.

Child Contact Record
********************

The child contact record is created and linked as a member of the parent household.

+---------------------------+---------------------------+
| Lead Object               | Contact Object            |
+===========================+===========================+
| Lead Source               | Lead Source               |
+---------------------------+---------------------------+
| Child Title               | Salutation                |
+---------------------------+---------------------------+
| Child First Name          | Name - First Name         |
+---------------------------+---------------------------+
| Child Last Name           | Name - Last Name          |
+---------------------------+---------------------------+
| Child Suffix              | Suffix                    |
+---------------------------+---------------------------+
| Address - Street          | Address - Street          |
+---------------------------+---------------------------+
| Address - Street2         | Address - Street2         |
+---------------------------+---------------------------+
| Address - City            | Address - City            |
+---------------------------+---------------------------+
| Address - State/Province  | Address - State/Province  |
+---------------------------+---------------------------+
| Address - Zip/Postal Code | Address - Zip/Postal Code |
+---------------------------+---------------------------+
| Child Date of Birth       | Birthdate                 |
+---------------------------+---------------------------+
| Child Date of Diagnosis   | Diagnosis Date            |
+---------------------------+---------------------------+
| Child Gender              | Gender                    |
+---------------------------+---------------------------+
| Diagnosis Detail          | Hospital                  |
+---------------------------+---------------------------+
| Endocrinologist           | Endocrinologist           |
+---------------------------+---------------------------+
| Child's Hobbies           | Hobbies                   |
+---------------------------+---------------------------+
| School                    | School                    |
+---------------------------+---------------------------+
