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

<h2 id="general">General Information</h2>

Vastly increasing data volumes and data complexity imply that researchers require novel solutions to large scale cluster computing. This workshop aims to provide an introduction and
hands-on experience with our new solution to this problem: "Spider - a new and versatile platform for high-throughput data processing".
The objective of the workshop is to distinguish the different functionalities of the Spider platform, to provide information on applying for access, and to give participants hands-on experience with basic job processing, software distribution and portability, using internal and external storage systems, and how to collaborate on data analysis within a project. Participants will acquire first hand experience with the flexibility, interactivity and interoperability offered by the Spider platform.

{% comment %}
AUDIENCE
{% endcomment %}

<p id="who">
  <strong>Who:</strong>
  Anyone who wants to start processing large data volumes (tens to hundreds of terabytes or even more)
</p>

{% if page.carpentry == "dc" %}
{% include dc/who.html %}
{% elsif page.carpentry == "lc" %}
{% include lc/who.html %}
{% endif %}

{% comment %}
LOCATION
{% endcomment %}

{% if page.latlng %}
<p id="where">
  <strong>Where:</strong>
  {{page.address}}.
  Get directions with
  <a href="//www.openstreetmap.org/?mlat={{page.latlng | replace:',','&mlon='}}&zoom=16">OpenStreetMap</a>
  or
  <a href="//maps.google.com/maps?q={{page.latlng}}">Google Maps</a>
</p>
{% endif %}

{% comment %}
DATE
{% endcomment %}

{% if page.humandate %}
<p id="when">
  <strong>When:</strong>
  {{page.humandate}}
  {% include workshop_calendar.html %}
</p>
{% endif %}

{% comment %}
SPECIAL REQUIREMENTS

Modify the block below if there are any special requirements.
{% endcomment %}
<p id="requirements">
  <strong>Requirements:</strong> Participants must bring a laptop with a
  Mac, Linux, or Windows operating system (not a tablet, Chromebook, etc.). Basic knowledge of UNIX commandline, bash scripting and cluster computing is expected.

</p>

{% comment %}
CONTACT EMAIL ADDRESS

Display the contact email address set in the configuration file.
{% endcomment %}
<p id="contact">
  <strong>Contact</strong>:
  Please email
  {% if page.email %}
  {% for email in page.email %}
  {% if forloop.last and page.email.size > 1 %}
  or
  {% else %}
  {% unless forloop.first %}
  ,
  {% endunless %}
  {% endif %}
  <a href='mailto:{{email}}'>{{email}}</a>
  {% endfor %}
  {% else %}
  to-be-announced
  {% endif %}
  for more information.
</p>

{% comment %}
  SCHEDULE

  Show the workshop's schedule.  Edit the items and times in the table
  to match your plans.  You may also want to change 'Day 1' and 'Day
  2' to be actual dates or days of the week.
{% endcomment %}
<h2 id="schedule">Schedule</h2>

{% if page.carpentry == "swc" %}
  {% include sc/schedule.html %}
{% elsif page.carpentry == "dc" %}
  {% include dc/schedule.html %}
{% elsif page.carpentry == "lc" %}
  {% include lc/schedule.html %}
{% elsif page.carpentry == "academy" %}
  {% include academy/schedule.html %}
{% endif %}

<h2 id="schedule">Schedule</h2>

<div class="row">
  <div class="col-md-6">
    <table class="table table-striped">
      <tr> <td>13:00</td>  <td>Introduction to Spider</td> </tr>
      <tr> <td>13:30</td>  <td>Login to Spider (ssh key troubleshooting)</td> </tr>
      <tr> <td>14:00</td>  <td>Demo of data manager and software manager role</td> </tr>
      <tr> <td>15:00</td>  <td>Coffee</td> </tr>
      <tr> <td>15:15</td>  <td>Submitting jobs to Spider and using collaboration features</td> </tr>
      <tr> <td>16:15</td>  <td>More demos of additional features and Wrap up</td> </tr>
      <tr> <td>17:00</td>  <td>END</td> </tr>
    </table>
  </div>
</div>


