# Data Model and Style Guide for HPC Best Practices web site

## Webinars

### Data Model

```
---
webinar-id: sequence number of webinar
date: date of presentation including time AND TIME ZONE
title: webinar title
presenter-ids: array of presenter's presenter-ids
---
content
```

### Conventions

- *title* must be quoted if it contains colons (true for any other variable too)
- *date* must include time and time zone of presentation, e.g., 2019-01-23T13:00-0500
- By convention, time zone is U.S. Eastern Time, which is -0500 for standard time or -0400 for daylight saving time
- *presenter-ids* is always an array, even if only one item
- if a *presenter-ids* element does not match any of the actual presenter-ids, the two common failure modes are for it to be blank or for it to pick up the first presenter-id, alphabetically

## Presenters

### Data Model

```
---
presenter-id: lastname-firstname-webinarid
lastname: presenter's last name
firstname:  presenter's first name
pres-email:  presenter's email address
affiliations: array of presenter's institutional affiliations
---
content
```

#### Notes

- *affiliations* is always an array, even if only one item
- *affiliations* can include markdown links
- *pres-email* is so named because *email* seems to be predefined, even though I can't find any documentation of it

### Conventions

- file name should match presenter-id
- *affiliations* should prefer full name of organization(s), not abbreviations (e.g., "Oak Ridge National Laboratory" rather than "ORNL"
- content of a presenter object should be a short biographical sketch
- content should begin with "presenter name (<presenter@example.com>) is..."
