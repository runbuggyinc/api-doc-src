# Order and Quote Creation Limitations 

####Order Creation using the API has the following limitations:
1. When creating an order with multiple vehicles, each vehicle must specify matching payer ids, fare names, and service levels
2. In a multi car order, all vehicles must use either the "vin" field or the "year", "make", "model" fields for the order to be created properly. They must be consistent
3. In the vehicle object is the field vin. Do not use the field name "VIN" as it will not register unless "vin" is lowercase. Our field names are case sensitive

####Quoting using the API has the following limitations:
1. You can create a quote for multiple vehicles to different addresses but you can't use the same json to create the order
2. An order quote's response will provide the fare for Standard, Gold, Platinum and Repo service levels
3. Quotes cannot be stored and used at a later date.

