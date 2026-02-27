---
title: "Booking Slice"
status: "refined"
domain: "HotelBooking"
version: 1
created: "2026-02-23"
tags:
  - "hotel-booking"
  - "companion-repo"
---

# Booking Slice

## Overview

The booking slice extracted from the full model. Shows how a guest books a room: Booking Form provides input to Room Availability Calendar, which feeds BookRoom command, producing a RoomBooked event, displayed as a Booking Confirmation.

## Slices

### Slice: BookRoom

**Wireframe:** Booking Form with guest name, room type (Deluxe King), dates, and Book Now button

```emlang
slices:
  BookRoom:
    steps:
      - t: BookingForm
      - v: RoomAvailabilityCalendar
      - c: BookRoom
      - e: RoomBooked
      - v: BookingConfirmation
      - t: BookingConfirmationScreen
```
