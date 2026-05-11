# Event Catalog Data Model

This document defines the data fields that each event in UniEvents must have. The catalog allows students and staff to browse and search events by category, date, and location.

## Event Fields

- **Title** — short, descriptive name of the event (e.g., "AI in Healthcare Workshop"). Required, 5–100 characters.
- **Description** — full text describing the event, agenda, speakers, and any prerequisites. Required, supports basic markdown.
- **Date/Time** — start and end timestamps in ISO 8601 format with timezone (e.g., 2026-05-20T14:00:00+02:00). Required.
- **Venue** — physical location or virtual meeting link. Includes building, room number, and address for on-campus events.
- **Capacity** — maximum number of registered attendees. Integer ≥ 1. Used to trigger waitlist logic when full.
- **Organizer** — reference to the user account (with Organizer role) responsible for the event. Displayed on the event page.
- **Category** — one of a fixed set: Academic, Social, Career, Sports, Cultural, Workshop. Used for filtering and search.

## TODO

- Decide on category enum vs free-text tags
- Add support for recurring events
