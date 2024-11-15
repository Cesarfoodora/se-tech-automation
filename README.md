Update this code:



In the order_data extract  for stream A, please include following data:

"eligibilities": message_data.get('content', {}).get('eligibilities'),

"unit": message_data.get('content', {}).get('order', {}).get('order_volume', {}).get('unit'),

"value": message_data.get('content', {}).get('orderr', {}).get('order_volume', {}).get('value')



In the FILTERING LOGIC:

The distance filter should be:  "equal or greater than 3000".



Also add to the filtering logic:

eligibilities = order_data.get('eligibilities')

unit = order_data.get('unit')

value = order_data.get('value')



where I want to filter out all orders that has string called "age_restricted" for the eligibilities field. 

and also:

if "unit" = Liters and "value" > 40

or if "unit" = CubicMeter and "value" > 0,04

or if "unit" = CubicCentimeter and "value" > 40000



then filter out these orders.    





Give me the complete updated code please
