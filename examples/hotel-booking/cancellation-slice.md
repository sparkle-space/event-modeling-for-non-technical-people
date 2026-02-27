---
title: "Cancellation Slice"
status: "refined"
domain: "HotelBooking"
version: 1
created: "2026-02-23"
tags:
  - "hotel-booking"
  - "companion-repo"
---

# Cancellation Slice

## Overview

The cancellation slice. Shows how a guest cancels a booking: Booking Details wireframe displays the Booking Details view, which feeds CancelBooking command, producing a BookingCancelled event, displayed as a Cancellation Confirmation.

## Slices

### Slice: CancelBooking

**Wireframe:** Booking Details page with reservation reference, status, room info, and Cancel Booking button

```emlang
slices:
  CancelBooking:
    steps:
      - t: BookingDetailsScreen
      - v: BookingDetails
      - c: CancelBooking
      - e: BookingCancelled
      - v: CancellationConfirmation
      - t: CancellationConfirmationScreen
```
