# Billing-Alerts

Account dropdown → My Billing Dashboard \
Preferences → Billing Preferences \
Check (3) boxes for..."Receive PDF Invoice by Email"..."Recieve Free Tier Usage Alerts" (fill in your email address)..."Receive Billing Alerts" \
Save Preferences

**Configure the Billing Alert:** \
CloudWatch → Alarms → Create Alarm \
Select Metric → Billing → Total Estimated Charge → Check USD → Select Metric (blue button) \
Conditions: Static...Greater...$XX.XX USD \
Alarm State Trigger: In Alarm \
SNS: Create New Topic...Name: BillingAlert...Email: enter your email address \

![image](https://user-images.githubusercontent.com/80132085/112333665-2e4ee100-8c91-11eb-9afd-4e03752d9562.png)
![image](https://user-images.githubusercontent.com/80132085/112333760-40308400-8c91-11eb-8dfb-febcb12ee279.png)





**For an Overview of all Costs on the Account:** \
Account dropdown → My Billing Dashboard \
Cost Management → **Cost Explorer** → Launch Cost Explorer\
