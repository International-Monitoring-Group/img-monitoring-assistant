# IMG Monitoring Assistant

Ask Claude about your vehicle fleet in plain language. IMG Monitoring Assistant connects Claude to your account on a Wialon Local GPS monitoring server operated by International Monitoring Group, and teaches Claude how to answer the questions fleet owners and dispatchers actually ask: what is happening with the fleet right now, which vehicles have gone silent and why, who is due for maintenance, where each vehicle is, and what the trip, mileage and fuel reports say.

The assistant is **read-only**. It never changes settings, never sends commands to trackers, and never creates or edits notifications.

## What you can ask

- "What's the state of the fleet?" — online and moving vehicles, plus a breakdown of every unit that has lost contact: how long it has been silent, last known power, ignition, battery and GSM state, the likely cause, and what to check.
- "Why is unit 148 offline?" — a step-by-step diagnosis from the tracker's raw parameters.
- "Who is due for an oil change?" — overdue and upcoming service intervals by mileage, date and engine hours.
- "Trips for the Cobalt 148 last week" — any report template configured in your Wialon account, for any period.
- "Who is at the warehouse right now?" — vehicle locations by geofence name instead of coordinates.
- "What notifications do I have, and why didn't the fuel-drain alert fire?" — a review of configured notifications and how to set up missing ones in Wialon.

## Getting started

1. Install the plugin, then open its **Connectors** tab and connect **IMG Monitoring**.
2. Choose your Wialon server from the list and sign in on the Wialon login page.
3. Return to Claude and ask a question about your fleet.

You need an active account on one of the Wialon Local servers operated by International Monitoring Group (wialon.uz, 2.wialon.uz or 3.wialon.uz).

## Skills

| Skill | Use it for |
| --- | --- |
| `fleet-overview` | Fleet status and daily briefing |
| `offline-diagnostics` | Why a unit has lost contact, and what support should check |
| `maintenance` | Service intervals that are overdue or coming up |
| `reports` | Running Wialon report templates for a vehicle and period |
| `locations` | Where vehicles are, by geofence and by group |
| `notifications` | Reviewing configured notifications and explaining how to add new ones |

## Data and privacy

The plugin contains only instructions for Claude and a reference to one remote MCP server, `https://ai.img.uz/mcp`, operated by International Monitoring Group. It runs no local code and sends data nowhere else.

- **Sign-in** happens on your Wialon server's own login page. Your Wialon password never reaches the MCP server.
- **What the server stores**: the address of your Wialon server and the access token Wialon issues after sign-in, so that Claude can make requests on your behalf. Tokens can be revoked at any time by disconnecting the connector or in your Wialon account settings.
- **What the server reads**: unit positions, telemetry, sensors, service intervals, geofences, groups, report templates and notifications in your Wialon account, only when Claude calls a tool to answer your question. Access is requested with read-only rights.
- **What it does not do**: it does not write to Wialon, does not send commands to trackers, does not read your Claude conversation history, and does not share data with third parties.

Full privacy policy: https://ai.img.uz/privacy

## Support

International Monitoring Group — https://img.uz — support@img.uz

---

## По-русски

**IMG Monitoring Assistant** — ассистент для клиентов Wialon Local. Подключите коннектор, выберите свой сервер Wialon, войдите своим логином на странице Wialon и спрашивайте Claude о машинах обычными словами: что с парком, какие машины не на связи и почему, кому пора на ТО, где сейчас техника, что показывают отчёты по поездкам и топливу. Ассистент только читает данные и ничего не меняет в Wialon. Пароль от Wialon на наш сервер не передаётся.

## License

MIT — see [LICENSE](LICENSE).
