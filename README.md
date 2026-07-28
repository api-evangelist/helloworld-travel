# Helloworld Travel (helloworld-travel)

Helloworld Travel Limited (ASX: HLO) is an Australian travel distribution group headquartered in Sydney, operating retail agency networks, corporate travel, wholesale packaging, air ticket consolidation and inbound tour operations across Australia, New Zealand, Fiji and Europe with more than 700 staff and over 2,700 retail members. It sits on the demand side of the travel distribution chain — an aggregator and reseller of third-party air, hotel and land content rather than an inventory owner — reaching travellers through its member agencies and reaching air supply through GDS-based consolidation and ticketing (Air Tickets, Express Tickets, SmartTickets). Its API posture is closed. There is no public developer portal, no OpenAPI, Swagger, AsyncAPI or Postman artifact, and no machine-readable contract of any kind. Every trade system is behind an agent login — ReadyRooms (B2B hotel and activity booking), AOTonline.net (inbound trade booking engine), Air Tickets and Express Tickets. A developer host is provisioned at developer.readyrooms.com.au but returns HTTP 401 with a Basic auth challenge on every path probed, so access is partner-only. There is no published exit path — the only documented way to get data back is a Privacy Act access request to the Helloworld Privacy Officer.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/helloworld-travel/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/helloworld-travel/refs/heads/main/apis.yml)

## Tags

- Travel
- Australia
- New Zealand
- Travel Agency
- Distribution
- Corporate Travel
- Wholesale
- Hotels
- Booking
- Air Consolidation
- Inbound Tourism
- Tour Operator

## Timestamps

- **Created:** 2026-07-28
- **Modified:** 2026-07-28

## APIs

None. Helloworld Travel Limited publishes no documented public API, and no machine-readable API contract of any kind was found on 2026-07-28. `apis[]` is intentionally empty rather than populated with login pages.

The group's real product surfaces are agent-login web applications, recorded in `review.yml`:

| Surface | Capability | Access |
| --- | --- | --- |
| ReadyRooms | Availability and rates, hotel and activity search, booking | Agent login (`athena.readyrooms.com.au`); signup via a Microsoft Forms application |
| AOTonline.net | Inbound trade shopping, quoting and booking — accommodation, transfers, car hire, tours, rail, attractions, fly-drives, packages | Agency Code + password; agent login requested manually, answered within 24 hours |
| Air Tickets / SmartTickets | Fulfilment and ticketing, reissues, refunds, revalidations, post-ticketing processing for 100+ airlines | Agent login |
| Express Tickets | Airfare and airline ticketing consolidation for agencies, tour operators and OTAs | Agent login |

## Switching Cost

| Dimension | Finding |
| --- | --- |
| Interface shape | `none-published` — no NDC, no OpenTravel/OTA, no HTNG, no OpenAPI, no standard referenced anywhere |
| Second source | `alternatives-with-migration` — WebBeds/Hotelbeds vs ReadyRooms, Consolidated Travel vs Air Tickets, Flight Centre Independent / Travellers Choice / TravelManagers vs the Helloworld networks; none shares an interface, so a move is a commercial project |
| Exit path | `export-on-request` — Privacy Act access request to `privacyofficer@helloworld.com.au`; no export, dump or bulk operation documented |
| Identifier portability | Proprietary AOT Agency Codes and opaque internal quote/booking IDs; IATA and TAANZ accreditation numbers and IATA airline codes are the only portable keys |
| Contractual lock-in | Terms of Use grant a "limited, personal, non-transferable, revocable licence"; clause 8 forbids exporting site material without prior written consent; AOT forbids re-uploading rates to any online booking site. Franchise and membership terms are unpublished. |
| Access gate | `partner-only` — no developer route exists; you must already be a travel trade partner |
| Distribution model | `aggregator-reseller`, consuming GDS intermediation for air rather than being GDS-distributed |
| NDC posture | Not an airline; no NDC statement, certification claim or endpoint found anywhere |

## Common Properties

- [Website](https://www.helloworldlimited.com.au/)
- [Consumer Website](https://www.helloworld.com.au/)
- [LinkedIn](https://www.linkedin.com/company/helloworld-com-au/)
- [Terms of Service](https://www.helloworldlimited.com.au/terms-of-use/)
- [Privacy Policy](https://policies.helloworldlimited.com.au/privacy-policy/)
- [Cookie Policy](https://policies.helloworldlimited.com.au/cookies-policy/)
- [Investor Relations](https://www.helloworldlimited.com.au/investors/)
- [Annual Reports](https://www.helloworldlimited.com.au/annual-reports/)
- [Contact](https://www.helloworldlimited.com.au/contact/)
- [Blog](https://www.helloworldlimited.com.au/feed/)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
