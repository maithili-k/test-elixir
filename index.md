---
layout: workshop      # DON'T CHANGE THIS.
carpentry: "swc"    # what kind of Carpentry (must be either "lc" or "dc" or "swc").  
                      # Be sure to update the Carpentry type in _config.yml as well.  
venue: "Getting started with high-throughput data processing on the Spider platform"        # brief name of host site without address (e.g., "Euphoric State University")
address: "SURF Utrecht Kantoren Hoog Overborch Office Building (Hoog Catharijne)
3511 EP Utrecht Moreelspark 48"      # full street address of workshop (e.g., "Room A, 123 Forth Street, Blimingen, Euphoria")
country: "Netherlands"      # lowercase two-letter ISO country code such as "fr" (see https://en.wikipedia.org/wiki/ISO_3166-1#Current_codes)
language: "EN"     # lowercase two-letter ISO language code such as "fr" (see https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes)
latlng: "52.088924,5.113097"       # decimal latitude and longitude of workshop venue (e.g., "41.7901128,-87.6007318" - use https://www.latlong.net/)
humandate: "Aug 28, 2019"    # human-readable dates for the workshop (e.g., "Feb 17-18, 2020")
humantime: "13:00-17:00"    # human-readable times for the workshop (e.g., "9:00 am - 4:30 pm")
startdate: 28/08/2019      # machine-readable start date for the workshop in YYYY-MM-DD format like 2015-01-01
enddate: 28/08/2019        # machine-readable end date for the workshop in YYYY-MM-DD format like 2015-01-02
instructor: ["Maithili Kalamkar Stam (SURFsara)", "Natalie Danezi (SURFsara)"] # boxed, comma-separated list of instructors' names as strings, like ["Kay McNulty", "Betty Jennings", "Betty Snyder"]
helper: ["Mateusz Kuzak (DTL)"]     # boxed, comma-separated list of helpers' names, like ["Marlyn Wescoff", "Fran Bilas", "Ruth Lichterman"]
email: ["?"]    # boxed, comma-separated list of contact email addresses for the host, lead instructor, or whoever else is handling questions, like ["marlyn.wescoff@example.org", "fran.bilas@example.org", "ruth.lichterman@example.org"]
collaborative_notes:             # optional: URL for the workshop collaborative notes, e.g. an Etherpad or Google Docs document
eventbrite:           # optional: alphanumeric key for Eventbrite registration, e.g., "1234567890AB" (if Eventbrite is being used)
---

{% comment %}
EVENTBRITE

This block includes the Eventbrite registration widget if
'eventbrite' has been set in the header.  You can delete it if you
are not using Eventbrite, or leave it in, since it will not be
displayed if the 'eventbrite' field in the header is not set.
{% endcomment %}
{% if page.eventbrite %}
<iframe
  src="https://www.eventbrite.com/tickets-external?eid={{page.eventbrite}}&ref=etckt"
  frameborder="0"
  width="100%"
  height="280px"
  scrolling="auto">
</iframe>
{% endif %}


