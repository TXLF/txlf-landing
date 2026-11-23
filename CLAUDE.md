# Texas Linux Fest landing site

Hugo site. Each past event has a page in `content/event/<year>-<venue>.md`
with Location, Dates, Keynote, Schedule, Videos and Media Links sections.

## Media Links

The "Media Links" list on each event page collects coverage of that year's
event by people outside the organizing team.

### What belongs

- Write-ups that report on the event: recaps, trip reports, LWN-style
  articles on talks, booth/sponsor reports written after the event.
- Podcast episodes that cover the event.
- Speaker slides, talk notes or repos from a talk given at that year's event.
- Pre-event posts from speakers or sponsors that describe what they brought
  (talk preview, booth announcement) are acceptable but rank below reports.

### What doesn't

- Call for papers announcements, including ones that also name the keynote
  or venue.
- Wiki planning pages (Fedora, Debian, openSUSE, LibreOffice event pages and
  similar). They track logistics, not the event itself.
- Generic event-calendar or listing pages (10times, Eventil, Linux Journal
  event listings, community calendar entries).
- Posts that only mention TXLF in passing.
- Third-party aggregations of talk summaries (for example personal GitHub
  repos summarizing other people's talks).
- The TXLF YouTube channel or playlists; those go under the Videos section.

### Verifying a link

Open every link before adding it, and confirm the page is about the year it
is filed under. Check the post's own date, not just the URL or a search
snippet: a post can be filed under the wrong year (the Opscode post on
chef.io looked like 2013 but is dated March 2011).

- Page loads and is on topic: link the original URL.
- Page is gone, or redirects somewhere unrelated, but archive.org has a
  snapshot: link the archived copy
  (`https://web.archive.org/web/<timestamp>/<original-url>`).
- Page is gone and archive.org has no record of it: treat it as never having
  existed and leave it out.
- A bot-check page (SlideShare, Cloudflare) is not a dead page; keep the
  original link if archive.org confirms it exists.
- Link to the specific post, not a blog's monthly archive or index page.

### Format

```
* [Title of the post (Outlet or Author)](https://example.org/post/)
```

Use the post's own title. Add the outlet or author in parentheses when the
title alone doesn't say where it's from, and note "slides" for slide decks.
