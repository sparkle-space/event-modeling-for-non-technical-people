---
title: "Full Hotel Booking Model"
status: "refined"
domain: "HotelBooking"
version: 1
created: "2026-02-23"
tags:
  - "hotel-booking"
  - "companion-repo"
---

# Full Hotel Booking Model

## Overview

The complete hotel booking event model with 4 swimlanes spanning the entire system. Shows search, booking, confirmation email automation, and cancellation slices working together. This is the most comprehensive diagram in the Event Modeling book.

## Slices

### Slice: Search

**Wireframe:** Room Search page with check-in/check-out date pickers and guest count

```emlang
slices:
  Search:
    steps:
      - e: RoomCreated
      - e: RoomBooked
      - e: BookingCancelled
      - v: RoomAvailabilityCalendar
      - t: RoomSearch
```

### Slice: Booking

**Wireframe:** Booking Form with guest name, room selection, and Book Now button

```emlang
slices:
  Booking:
    steps:
      - t: BookingForm
      - v: RoomAvailabilityCalendar
      - c: BookRoom
      - e: RoomBooked
      - v: BookingConfirmation
```

### Slice: ConfirmationEmail

**Wireframe:** Automated email sending triggered by booking

```emlang
slices:
  ConfirmationEmail:
    steps:
      - e: RoomBooked
      - a: Automation
      - c: SendConfirmationEmail
      - e: ConfirmationEmailSent
```

### Slice: Cancellation

**Wireframe:** Booking Details page with cancellation button

```emlang
slices:
  Cancellation:
    steps:
      - t: BookingDetails
      - v: BookingDetails
      - c: CancelBooking
      - e: BookingCancelled
      - v: CancellationConfirmation
```
