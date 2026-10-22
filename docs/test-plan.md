# Test Plan (skeleton)

## Setup

- Dummy product: [OFFER NAME], 1 USD, not in the online store.
- Test contact: a Gmail plus address, for example yourname+le1@gmail.com.
- Test dates: PLC 1 at now plus 10 minutes, PLC 2 plus 20, PLC 3 plus 30, cart open plus 40, cart close plus 3 hours.
- Open decision before the run: temporary placeholders for brand_sender_name, brand_domain, offer_name, or load the Foundation snapshot.

## Per workflow

| Workflow | Do | Check |
|---|---|---|
| LE 01 Launch Survey | submit the native survey | tag launch-survey-done, launch_id_joined filled |
| LE 02a to 02c | opt in on /plc-1, /plc-2, /plc-3 | tags launch-list and launch-plc-N, delivery email arrives, link works |
| LE 03 | wait for the PLC dates | Wait step reads the custom value date, 3 announcements on time |
| LE 04 | wait for cart open | Open Cart 1 to 4 arrive, deadline emails count from close date |
| LE 05 | buy the 1 USD product | tag launch-buyer, launch_id_bought filled, no more Open Cart emails |
| Evergreen | publish LE 03E on a second test contact | sequence starts from join date |

## Every email

- Plain text, black and white, one link, sender name and Unsubscribe in the footer.
- No empty merge fields. No price, no absolute dates.

## Fallback if the Wait step cannot read a custom value date

Copy the date into a contact date field at entry, then wait on that field.
