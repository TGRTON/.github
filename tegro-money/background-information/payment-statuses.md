---
description: Possible payment statuses
---

# Payment statuses

## Waiting

Usually the status is immediately changed to successful or erroneous, but in case the user has not completed the payment, left the 3DS stage, form or other, the status may remain for a certain period of time.

This usually lasts for 24 hours, after which the timeout ends. At this point the payment can still take the status "Paid" if the customer completes the payment.

In some situations, the wait lasts longer, but payments that have been pending for more than 24 hours almost always go into error.

## Paid

The payment was successful.

## Error

Status is final, there may be many reasons, contact support.

## Cancelled

Most often it is assigned when the payment is not completed in the timeout we specified _(e.g., left the payment page or widget, 3DS code is incorrect or not entered, etc.)._

## Rejected

This status occurs when an erroneous response to our "Check" request is sent to your payment processor URL.
