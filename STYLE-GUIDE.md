# Data Model and Style Guide for HPC Best Practices web site

## Webinars

### Data Model

```
---
webinar-id: sequence number of webinar
date: date of presentation including time AND TIME ZONE
title: webinar title
presenter-ids: array of presenter's presenter-ids
registration-url: url for event registration site
ecp-abbreviation: abbreviation used for webinar on ECP Training site
vtc-url: url for video conference session
vtc-session: video conference session id (string)
vtc-password: video conference session password (string) [optional]
qa-public-url: url for live Q&A document to be exposed to the public
survey-public-url: url for feedback survey to be exposed to the public
archives:
  - label: text for hyperlink to archival asset
    format: notes about format/soudce of asset (rendered in parenthesis) [optional]
	url: url for hyperlink to archival asset
  -label: (repeat as needed for all archival assets)
   format: ...
   url: ...
---
content
```

### Conventions

- `title` must be quoted if it contains colons (true for any other variable too) (best practice: always quote)
- `date` must include time and time zone of presentation, e.g., 2019-01-23T13:00-0500
- By convention, time zone is U.S. Eastern Time, which is -0500 for standard time or -0400 for daylight saving time
- `presenter-ids` is always an array, even if only one item
- if a `presenter-ids` element does not match any of the actual presenter-ids, the two common failure modes are for it to be blank or for it to pick up the first presenter-id, alphabetically
- `archives` are currently presented like "*Archives:* [Video](http://example.com) (YouTube) | [Slides](http://example.com) (PDF) | [Q&A](http://example.com) (PDF)"

### Notes
- Content required to advertise an upcoming webinar:
  - `webinar-id`
  - `date`
  - `title`
  - `presenter-ids`
  - `registration-url`
- Additional content required for "connection information" message:
  - `ecp-abbreviation`
  - `vtc-url`
  - `vtc-session`
  - `vtc-password` [optional]
  - `qa-public-url`
  - `survey-public-url`
- Additional content required for archives:
  - `archives`

## Presenters

### Data Model

```
---
presenter-id: lastname-firstname-webinarid
lastname: presenter's last name
firstname:  presenter's first name
aka: Additional name variants used in past webinars.  String. e.g. "Michael A. Heroux" [optional]
pres-email:  presenter's email address [optional]
pres-url: presenter's URL (optional) [optional]
affiliations: array of presenter's institutional affiliations
past-affiliations: array of institutional affiliations used in past webinars [optional]

---
content
```

#### Notes

- `lastname` may be a compound last name, e.g. "Chue Hong" or "Bernholdt-Musfeldt"
- `firstname` may include multiple names or initials
- `affiliations`, `past-affiliations` are always arrays, even if only one item
- `affiliations`, `past-affiliations` can include markdown links
- `pres-email` is so named because `email` seems to be predefined, even though I can't find any documentation of it

### Conventions

- `presenter-id` should be `lastname`-`firstname`.  If lastname is a compound, spaces and punctuation (usually hyphens) are stripped to make presenter-id.  Same for firstname component
- file name should match presenter-id
- `affiliations` should prefer full name of organization(s), not abbreviations (e.g., "Oak Ridge National Laboratory" rather than "ORNL"
  - Maybe we should revisit this.  Some of those full names are rarely used and may not be as recognizable as the shorthand (e.g., NERSC).
- content of a presenter object should be a short biographical sketch
- content should begin with "presenter name (<presenter@example.com>) is..."
- we do not retain previously used email addresses, as they're likely to be outdated if the presenter has a new one. 
  - Exception: they provide an institutional email for one webinar and an external service email (e.g., gmail) for another. Still seems safe to assume the most recent is preferred, if not the only valid email to reach the presenter.
- `pres-url` should be the URL for the presenter's web page
  - Not clear what we should do with past urls.  We don't currently accommodate them.  Are they like emails, where we assume changes likely mean invalidation of older ones?

## General notes
- We need to run a link-checker periodically against all urls.  
  - Can we script that into the build?  Probably takes too long, and wouldn't work on GitHub.io
  - Can we script this into CI testing?
  - Can we script this as part of rest of the planned automation?

