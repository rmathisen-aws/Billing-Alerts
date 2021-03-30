# Billing Alerts using CloudWatch and SNS

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<img src="https://user-images.githubusercontent.com/80132085/112924969-0d4a1e00-90df-11eb-85ab-989ba5b7ff81.png" width="311" height="232.5"> \
![image](https://user-images.githubusercontent.com/80132085/112925011-25ba3880-90df-11eb-8e94-96aea27d9095.png)

Account dropdown → My Billing Dashboard \
Preferences → Billing Preferences \
Check (3) boxes for..."Receive PDF Invoice by Email"..."Recieve Free Tier Usage Alerts" (fill in your email address)..."Receive Billing Alerts" \
Save Preferences

\
**Configure the Billing Alert:** \
CloudWatch → Alarms → Create Alarm \
Select Metric → Billing → Total Estimated Charge → Check USD → Select Metric (blue button) \
Conditions: Static...Greater...$XX.XX USD \
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
