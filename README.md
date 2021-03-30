# Billing Alerts using CloudWatch and SNS

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<img src="https://user-images.githubusercontent.com/80132085/112924969-0d4a1e00-90df-11eb-85ab-989ba5b7ff81.png" width="321" height="229.5"> \
Account dropdown → My Billing Dashboard

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<img src="https://user-images.githubusercontent.com/80132085/112925436-dc1e1d80-90df-11eb-8134-fb78827bba5a.png" width="148.5" height="249"> \
Preferences → Billing Preferences

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<img src="https://user-images.githubusercontent.com/80132085/112925731-5058c100-90e0-11eb-8af1-1e319429b1c1.png" width="873.75" height="321"> \
Check (3) boxes for..."Receive PDF Invoice by Email"..."Recieve Free Tier Usage Alerts" (fill in your email address)..."Receive Billing Alerts" \
Save Preferences

<br/>

### Configure the Billing Alert:

![image](https://user-images.githubusercontent.com/80132085/112926232-2522a180-90e1-11eb-9d57-1b232526ed1d.png) \
CloudWatch → Alarms → Create Alarm

\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<img src="https://user-images.githubusercontent.com/80132085/112926710-d6c1d280-90e1-11eb-8884-94cdc10c6b6d.png" width="310.5" height="183">

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<img src="https://user-images.githubusercontent.com/80132085/112926781-f48f3780-90e1-11eb-8ab6-7174f23a1a56.png" width="374.25" height="198">

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<img src="https://user-images.githubusercontent.com/80132085/112926829-040e8080-90e2-11eb-9049-fe5afb94f2cc.png" width="617.25" height="144">

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<img src="https://user-images.githubusercontent.com/80132085/112926917-21dbe580-90e2-11eb-8ec3-3286c125af19.png" width="198.75" height="144">

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<img src="https://user-images.githubusercontent.com/80132085/112926939-2a342080-90e2-11eb-9250-075c335560b2.png" width="220.5" height="79.5">\
Select Metric → Billing → Total Estimated Charge → Check USD → Select Metric

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<img src="https://user-images.githubusercontent.com/80132085/112927779-88adce80-90e3-11eb-9ede-88e53688cb7a.png" width="576" height="393.75"> \
Conditions: Static...Greater...$XX.XX USD

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<img src="https://user-images.githubusercontent.com/80132085/112928168-22757b80-90e4-11eb-8bf1-9af8b556a2e7.png" width="565.5" height="317.25"> \
Previous → look at the Graph \
Notice the Red $10 USD limit line in comparison to the costs up to this point

Alarm State Trigger: In Alarm......SNS: Create New Topic...Name: BillingAlert...Email: enter your email address \
Alarm Name: BillingAlert \
Create Alarm \
Notice your alarm's "Action" status shows "Pending Confirmation" \
Read the email that was just sent to you & confirm subscription \
Refresh the alarm \
State will change from "Insufficient Data" to "OK"

\
By default, only the Account Root User can access the Billing area on the AWS Console. \
**To allow IAM Users to access the billing area:** \
Account dropdown → My Account \
IAM User and Role Access to Billing Information → Edit → Check box "Activate IAM Access" → Update

\
**For an Overview of all Costs on the Account:** \
Account dropdown → My Billing Dashboard \
Cost Management → **Cost Explorer** → Launch Cost Explorer

\
For best practices, explicitly fill out the \
**Billing, Operations & Security Alternate Contact Information:** \
Account dropdown → My Account \
Alternate Contacts → Edit → fill in all fields
