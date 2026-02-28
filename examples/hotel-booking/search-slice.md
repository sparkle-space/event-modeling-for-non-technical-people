---
title: "Search Slice"
status: "refined"
domain: "HotelBooking"
version: 1
created: "2026-02-23"
tags:
  - "hotel-booking"
  - "companion-repo"
---

# Search Slice

## Overview

The search/read slice. This is a view-only slice: multiple past events (RoomCreated, RoomBooked, BookingCancelled) feed into a Room Availability Calendar view, which displays on a wireframe. No commands are issued -- this is a read operation.

## Slices

### Slice: Search

**Wireframe:** Room Availability Calendar showing room grid with types, dates, prices, and availability status

```emlang
slices:
  Search:
    steps:
      - e: RoomCreated
      - e: RoomBooked
      - e: BookingCancelled
      - v: RoomAvailabilityCalendar
      - t: RoomAvailability
```
