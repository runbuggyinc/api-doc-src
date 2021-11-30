## Order Statuses

There are 2 types of order statuses `VehicleTransferOrder` statuses and `Shipper` statuses.  

Almost always the VehicleTransferOrder statuses should always be used to track placed orders through the API.

VehicleTransferOrder statuess can be found using the get
/orders/{id}/full api endpoint

##VehicleTransferOrder Statuses
The `VehicleTransferOrder.status` field has the following possible values:
```
DRAFT
READY
AVAILABLE
CLAIMED
UNCLAIMED
ASSIGNED
REJECTED
ACCEPTED
DRIVER_ARRIVED
PICKED_UP
SIGNATURE_ON_PICKUP
PROVIDED_ETA_DROPOFF
UNLOADED
DELIVERED
CANCELED
COMPLETE
ERROR
PENDING
```

### Draft
The Vehicle Transfer Order has been successfully received by the system and is being processed.

### Ready
The Vehicle Transfer Order has been successfully processed and will be made available to be claimed shortly.

### Available
The Vehicle Transfer Order has been successfully entered into the system and is available to be accepted by a
 transporter.

### Claimed
The Vehicle Transfer Order has been claimed by a transportation company to be transferred.

### Unclaimed
The Vehicle Transfer Order has been unclaimed by a transportation company.

### Assigned
The Vehicle Transfer Order has been assigned to a transportation company driver.

### Rejected
The Vehicle Transfer Order has been rejected by a transportation company driver.

### Accepted
The Vehicle Transfer Order has been accepted by a transportation company driver.

### Driver Arrived
The Vehicle Transfer Order driver has arrived to the pick up location.

### Picked up
The Vehicle Transfer Order vehicle has been picked up by the driver.

### Signature on Pickup
The Vehicle Transfer Order pick up paperwork has been signed by the transportation company driver.

### Provided ETA - Drop-off
The Vehicle Transfer Order drop-off ETA has been set by the driver.

### Unloaded
The Vehicle Transfer Order has been delivered and unloaded at the destination.

### Delivered
The Vehicle Transfer Order delivery paperwork has been signed.

### Complete
The Vehicle Transfer Order delivery process has been completed.

### Error
The Vehicle Transfer Order contains errors.

### Canceled
The Vehicle Transfer Order has been canceled.

### Pending
This is a temporary status which exists only as the order is being created.

##Shipper Order Statuses

These should generally not be used as they do not provide detailed enough information about the current status of the order.

```ERROR
DRAFT_CREATED
PENDING
CREATED
CANCELED
COMPLETED
