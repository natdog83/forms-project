***********
ODST
***********

The ODST form was creatd in Gravity Forms and sends the data to the Salesforce Case Object.

Form Fields
######

+---------------------------------+-------------------------------+---------------------------+-----------+--------------------+
| Field                           | Type/Options                  | Destination               | Required  | Validation         |
+=================================+===============================+===========================+===========+====================+
|                                 | Hidden Field                  |                           | Yes       |                    |
|                                 |  * ODST                       |                           |           |                    |
+---------------------------------+-------------------------------+---------------------------+-----------+--------------------+
| Your question about type 1      | Picklist                      |                           | Yes       |                    |
| diabetes                        |                               |                           |           |                    |
+---------------------------------+-------------------------------+---------------------------+-----------+--------------------+

Triggers
########


Emails
########

Confirmation email to constituents
==================================

Dear {!Case.FirstName__c} ,

Thank you for contacting the JDRF Online Diabetes Support Team. This is an automated reply to let you know we've received your request.

We warmly welcome you to the JDRF family and look forward to offering you the support you have asked for. Within 48 hours, a member of our team will make personal contact with you by e-mail. There's no need for you to reply to this message.

In the meantime, if you have an urgent medical question, we strongly suggest you contact your doctor.

Thank you,

JDRF.org

Case Created
============
