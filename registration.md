# Registration & Ticketing

This document describes the registration and ticketing flow for UniEvents. It covers how students sign up for events, how tickets are generated, and how the system handles capacity overflow.

## Requirements

- **Registration** — A student registers for an event by clicking "Register" on the event page. The system verifies the student is authenticated with a valid university account, checks that the event has remaining capacity, and creates a registration record linked to the student and the event.
- **Waitlist logic** — When an event is at full capacity, new registrations are placed on a waitlist in the order they arrive. If a registered student cancels, the next person on the waitlist is automatically promoted to a confirmed registration and notified by email.
- **QR code ticket generation** — Each confirmed registration triggers the generation of a unique QR code containing a signed token (event ID, registration ID, and a short-lived signature). The QR code is rendered as an image and attached to the confirmation email. At the event venue, organizers scan the QR code to validate entry.
- **Confirmation email** — Sent immediately after a successful registration. Contains the event title, date/time, venue, the QR-code ticket, and a link to cancel the registration if plans change.
- **Cancellation** — Students can cancel up to 1 hour before the event start time. Cancellation frees a capacity slot and triggers waitlist promotion.
