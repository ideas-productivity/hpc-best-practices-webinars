# Items to do

- HTML title metadata derived from filename.  Probable better choices
- What's up with navigation???
- look for useful HTML5 (or other) semantic tags
- Do something more intelligent when the webinar presenter-id doesn't match a presenter.  Right now, it causes Jekyll to error out, silently.
- Decide whether we want to expose aka names, past affiliations, past bios
  - Additional bios within details tags are not being markdownified
  - Incorporation of presenter bios into webinar pages includes past bios because past bios are merely part of the presenter content.  This is probably not desirable in the long run.
- Add BSSw category/topic tags to webinar entries going forward
  - Render them in bssw-events
  - Accomulate and render them in the cc article
- Properly setup md2md.rb plugin (gemfile, bundle, etc.)
  - there is a built-in identity.rb converter.  Can we use that instead?
- Presumably GH.io will no longer work due to plugin.  Work around this.
- Can we add next/previous links in individual webinar pages? Presenter pages?
- Multi-paragraph webinar abstracts (and presenter bios?) cause problems when embedding \{\{ content \}\} within other HTML constructs.  How to do better?
  - Change the way we markup such content?
  - Change the way we process such content?
- Should we generate the whole HPC-BP page on the ideas-producticity.org site?
- Can we do a better job of presenting the ipweb content as HTML code?
- Add warnings about title length (> site.youtube-title-max) as early as possible (commit or CI testing)
  - On YouTube, we prefix with "Webinar xxx: " so deduct 13 char
  - SEO site recommend no more than 70 char YT titles, after which Google will truncate in search results
- Add schema checking for YAML front matter
  - Maybe <https://github.com/18F/jekyll_frontmatter_tests>
  - Added a lot of checking for expected variables wherever they are used, but nothing yet with actual YAML schemas
  - No checking yet for artifacts
  - Maybe add error-checking versions of collections where the only content generated is listings of missing variables
- Add JSON+LD markup for events and maybe people
- Plugins of possible interest (eventually)
  - tag cloud
  - pluralize
  - feed
  - sitemap generator
  - Youtube embeding
  - Search
  - Redirect from
  - Analytics
  - Front matter tests
- How can we do formatting that transfers better to other tools?
  - connection-emails --> email client
  - ipweb-entries --> Wordpress

# Items done

- Webinars with a future date are **ignored** by the collection unless `future: true` is set in _config.yml (or jekyll is invoked with --future)
- Add an "upcoming webinars" page which links to all of the formats for upcoming webinars (duh)
  - We want this for the most recent completed webinar too (for archiving and followup notifications)
  - This assumes we're never more than one behind.  Probably okay.
