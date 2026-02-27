---
title: "Automation Slice"
status: "refined"
domain: "HotelBooking"
version: 1
created: "2026-02-23"
tags:
  - "hotel-booking"
  - "companion-repo"
---

# Automation Slice

## Overview

The automation slice from the full hotel booking model. RoomBooked triggers an automation that sends a confirmation email, producing a ConfirmationEmailSent event.

## Slices

### Slice: ConfirmationEmail

**Wireframe:** Automated email sending triggered by booking event

```emlang
slices:
  ConfirmationEmail:
    steps:
      - e: RoomBooked
      - a: Automation
      - c: SendConfirmationEmail
      - e: ConfirmationEmailSent
```
