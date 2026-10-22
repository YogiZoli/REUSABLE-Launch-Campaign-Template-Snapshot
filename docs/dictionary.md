# Custom Value Dictionary (frozen)

Merge field format: `{{custom_values.<key>}}`. Dates: `2026-11-03 12:00` in the sub-account time zone.

## Foundation keys (referenced only, created by the Brand Foundation snapshot)

| Key | Group | Placeholder | Source value | Used in |
|---|---|---|---|---|
| brand_name | Foundation | [BRAND NAME] | Brand Foundation snapshot | page headers |
| brand_sender_name | Foundation | [SENDER NAME] | Brand Foundation snapshot | every email footer |
| brand_support_email | Foundation | [SUPPORT EMAIL] | Brand Foundation snapshot | sales page FAQ, footer |
| brand_domain | Foundation | [DOMAIN] | Brand Foundation snapshot | every internal link https://{{custom_values.brand_domain}}/slug |
| brand_logo_url | Foundation | [LOGO URL] | Brand Foundation snapshot | page headers only (never emails) |
| brand_color_primary | Foundation | [PRIMARY COLOR] | Brand Foundation snapshot | page buttons |
| legal_company_name | Foundation | [COMPANY NAME] | Brand Foundation snapshot | page footers |
| legal_address | Foundation | [ADDRESS] | Brand Foundation snapshot | page footers |
| legal_governing_law | Foundation | [GOVERNING LAW] | Brand Foundation snapshot | terms page |
| legal_privacy_url | Foundation | [PRIVACY URL] | Brand Foundation snapshot | every page footer |
| legal_terms_url | Foundation | [TERMS URL] | Brand Foundation snapshot | every page footer |

## Offer keys (referenced only, from the Offer Card export "Copy for Launch Engine")

| Key | Group | Placeholder | Source value | Used in |
|---|---|---|---|---|
| offer_name | Offer | [OFFER NAME] | Offer Card export | Open Cart emails, sales page |

Exact key list is added when the Biz In A Box Offer Card export is pasted.

## Launch keys (created in the target sub-account, 22)

| Key | Group | Placeholder | Source value (Biz In A Box sample) | Used in |
|---|---|---|---|---|
| launch_id | Launch | [LAUNCH ID] | per launch | workflows save it to launch_id_joined and launch_id_bought |
| launch_survey_url | Launch | [SURVEY URL] | native GHL survey link | survey page, survey workflow |
| launch_plc_1_date | Launch | [PLC 1 DATE] | 2026-11-03 12:00 style | PLC 1 announcement Wait step |
| launch_plc_1_title | Launch | [PLC 1 TITLE] | per launch | PLC 1 page headline, announcement subject |
| launch_plc_1_subtitle | Launch | [PLC 1 SUBTITLE] | per launch | PLC 1 page |
| launch_plc_1_video_url | Launch | [PLC 1 VIDEO URL] | https://youtu.be/IHR8B8EA77w | PLC 1 page video |
| launch_plc_1_leadmagnet_name | Launch | [PLC 1 LEADMAGNET NAME] | per launch | PLC 1 page, PLC 1 delivery email |
| launch_plc_1_leadmagnet_url | Launch | [PLC 1 LEADMAGNET URL] | per launch | PLC 1 delivery email |
| launch_plc_2_date | Launch | [PLC 2 DATE] | per launch | PLC 2 announcement Wait step |
| launch_plc_2_title | Launch | [PLC 2 TITLE] | per launch | PLC 2 page, announcement subject |
| launch_plc_2_subtitle | Launch | [PLC 2 SUBTITLE] | per launch | PLC 2 page |
| launch_plc_2_video_url | Launch | [PLC 2 VIDEO URL] | https://youtu.be/WvE26cOoYaY | PLC 2 page video |
| launch_plc_2_leadmagnet_name | Launch | [PLC 2 LEADMAGNET NAME] | per launch | PLC 2 page, PLC 2 delivery email |
| launch_plc_2_leadmagnet_url | Launch | [PLC 2 LEADMAGNET URL] | per launch | PLC 2 delivery email |
| launch_plc_3_date | Launch | [PLC 3 DATE] | per launch | PLC 3 announcement Wait step |
| launch_plc_3_title | Launch | [PLC 3 TITLE] | per launch | PLC 3 page, announcement subject |
| launch_plc_3_subtitle | Launch | [PLC 3 SUBTITLE] | per launch | PLC 3 page |
| launch_plc_3_video_url | Launch | [PLC 3 VIDEO URL] | https://youtu.be/iPCIMZGI7IU | PLC 3 page video |
| launch_plc_3_leadmagnet_name | Launch | [PLC 3 LEADMAGNET NAME] | per launch | PLC 3 page, PLC 3 delivery email |
| launch_plc_3_leadmagnet_url | Launch | [PLC 3 LEADMAGNET URL] | per launch | PLC 3 delivery email |
| launch_cart_open_date | Launch | [CART OPEN DATE] | per launch | Open Cart workflow start |
| launch_cart_close_date | Launch | [CART CLOSE DATE] | per launch | Open Cart deadline emails 5 to 8 |

## Contact fields (Contact object, folder Additional Info)

| Field | Written by |
|---|---|
| launch_id_joined | Survey and PLC opt-in workflows |
| launch_id_bought | Buyer Suppression workflow |

## Tags

launch-survey-done, launch-list, launch-plc-1, launch-plc-2, launch-plc-3, launch-buyer

## Page slugs

/plc-1, /plc-2, /plc-3, /offer. Footer of every page links legal_privacy_url and legal_terms_url.
