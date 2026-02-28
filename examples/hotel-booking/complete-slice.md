---
title: "Complete Booking Slice with Automation"
status: "refined"
domain: "HotelBooking"
version: 1
created: "2026-02-23"
tags:
  - "hotel-booking"
  - "companion-repo"
---

# Complete Booking Slice with Automation

## Overview

A single complete booking slice with all 4 swimlanes. Shows the full lifecycle: a guest fills in the Booking Form, the system checks Room Availability, executes BookRoom, records RoomBooked, shows Booking Confirmation, and an automation sends a confirmation email.

## Slices

### Slice: BookRoom

**Wireframe:** Booking Form with guest name, check-in date, room type, and Book Now button

```emlang
slices:
  BookRoom:
    steps:
      - t: BookingForm
      - v: RoomAvailabilityCalendar
      - c: BookRoom
      - e: RoomBooked
      - v: BookingConfirmation
      - t: BookingConfirmation
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
