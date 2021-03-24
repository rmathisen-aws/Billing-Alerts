# Billing-Alerts

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
\
**For an Overview of all Costs on the Account:** \
Account dropdown → My Billing Dashboard \
Cost Management → **Cost Explorer** → Launch Cost Explorer\
