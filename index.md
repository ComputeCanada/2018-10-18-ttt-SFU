---
layout: workshop      # DON'T CHANGE THIS.
carpentry: "FIXME"    # what kind of Carpentry (must be either "lc" or "dc" or "swc")
venue: "Simon Fraser University, Instructor Training"        # brief name of host site without address (e.g., "Euphoric State University")
address: "Rm 7010, Research Commons, W.A.C. Bennett Library, Burnaby"      # full street address of workshop (e.g., "Room A, 123 Forth Street, Blimingen, Euphoria")
country: "ca"      # lowercase two-letter ISO country code such as "fr" (see https://en.wikipedia.org/wiki/ISO_3166-1)
language: "en"     # lowercase two-letter ISO language code such as "fr" (see https://en.wikipedia.org/wiki/ISO_639-1)
latlng: "49.279664, -122.918841"       # decimal latitude and longitude of workshop venue (e.g., "41.7901128,-87.6007318" - use https://www.latlong.net/)
humandate: "October 18 & 19"    # human-readable dates for the workshop (e.g., "Feb 17-18, 2020")
humantime: "9am to 5pm"    # human-readable times for the workshop (e.g., "9:00 am - 4:30 pm")
startdate: 2018-10-18      # machine-readable start date for the workshop in YYYY-MM-DD format like 2015-01-01
enddate: 2018-10-19        # machine-readable end date for the workshop in YYYY-MM-DD format like 2015-01-02
instructor: ["John Simpson"] # boxed, comma-separated list of instructors' names as strings, like ["Kay McNulty", "Betty Jennings", "Betty Snyder"]
helper: [""]     # boxed, comma-separated list of helpers' names, like ["Marlyn Wescoff", "Fran Bilas", "Ruth Lichterman"]
email: ["john.simpson@computecanada.ca"]    # boxed, comma-separated list of contact email addresses for the host, lead instructor, or whoever else is handling questions, like ["marlyn.wescoff@example.org", "fran.bilas@example.org", "ruth.lichterman@example.org"]
collaborative_notes:  http://pad.software-carpentry.org/2018-10-18-ttt-SFU           # optional: URL for the workshop collaborative notes, e.g. an Etherpad or Google Docs document
eventbrite:           # optional: alphanumeric key for Eventbrite registration, e.g., "1234567890AB" (if Eventbrite is being used)
---

{% comment %} See instructions in the comments below for how to edit specific sections of this workshop template. {% endcomment %}

{% comment %}
  HEADER

  Edit the values in the block above to be appropriate for your workshop.
  If the value is not 'true', 'false', 'null', or a number, please use
  double quotation marks around the value, unless specified otherwise.
  And run 'make workshop-check' *before* committing to make sure that changes are good.
{% endcomment %}

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

<!--
  INTRODUCTION
  Edit the general explanatory paragraph below if you want to change
  the pitch.
-->

<p>
  The course is aimed at everyone who is
  interested in becoming a better teacher. In particular, this training
  is aimed at those who want to become <a href="{{ site.swc_site }}">Software Carpentry</a>
  and <a href="{{ site.dc_site }}">Data Carpentry</a>
  instructors, run workshops and contribute to the Carpentry training
  materials. You don't currently have to be an instructor or a
  teacher to attend this workshop, but you do need to be willing and
  committed to becoming one and to improving your teaching techniques.
</p>

<p>
  <a href="{{ site.swc_site }}">Software Carpentry</a>
  and <a href="{{ site.dc_site }}">Data Carpentry</a>'s mission is to
  help scientists and engineers get more research done in less time
  and with less pain by teaching them basic lab skills for scientific
  computing.  This hands-on two-day workshop covers the basics of
  educational psychology and instructional design, and looks at how to
  use these ideas in both intensive workshops and regular classes.
</p>
<p>
  The workshop is a mix of lectures and hands-on lessons where you
  practice giving a short lesson using approaches learned and
  implement some of the teaching techniques which we will discuss.
  This is training for teaching, not technical training; you do not
  need any particular technical background, and we will not be
  teaching that. This workshop is based on the constantly revised and
  updated
 <a href="{{ site.training_site }}">curriculum</a>.
</p>

{% comment %}
  LOCATION

  This block displays the address and links to maps showing directions
  if the latitude and longitude of the workshop have been set.  You
  can use https://itouchmap.com/latlong.html to find the lat/long of an
  address.
{% endcomment %}
{% if page.latlng %}
<p id="where">
  <strong>Where:</strong>
  {{page.address}}.
  Get directions with
  <a href="//www.openstreetmap.org/?mlat={{page.latlng | replace:',','&mlon='}}&zoom=16">OpenStreetMap</a>
  or
  <a href="//maps.google.com/maps?q={{page.latlng}}">Google Maps</a>.
</p>
{% endif %}

{% comment %}
  DATE

  This block displays the date and links to Google Calendar.
{% endcomment %}
{% if page.humandate %}
<p id="when">
  <strong>When:</strong>
  {{page.humandate}}.
  {% include workshop_calendar.html %}
</p>
{% endif %}

{% comment %}
  SPECIAL REQUIREMENTS

  Modify the block below if there are any special requirements.
{% endcomment %}
<p>
  <strong>Requirements:</strong> Participants should bring a laptop
  that is Internet connected and has a functioning browser.  If you
  have it, a device for recording audio and video (mobile phones and
  laptops are OK) is useful as throughout the two days, we are going
  to record one another teaching in pairs or threes.  It does not have
  to be high-quality, but it should be good enough that you can
  understand what someone is saying.
</p>
<p>
  Please note that after this course is over, you will be asked to do
  three short follow-up exercises online in order to finish qualifying
  as an instructor: the details are available at
  <a href="{{ site.training_site }}/checkout/">{{ site.training_site }}/checkout/</a>.
  If you have any questions about the workshop, the reading material,
  or anything else, please get in touch.
</p>
<p align="center">
  <em>
    All participants are required to abide by Software
    Carpentry's <a href="{{ site.swc_site }}/conduct/">Code of Conduct</a>.
  </em>
</p>
</p>

{% comment %}
  ACCESSIBILITY

  Modify the block below if there are any barriers to accessibility or
  special instructions.
{% endcomment %}
<p id="accessibility">
  <strong>Accessibility:</strong> We are committed to making this workshop
  accessible to everybody.
  The workshop organizers have checked that:
</p>
<ul>
  <li>The room is wheelchair / scooter accessible.</li>
  <li>Accessible restrooms are available.</li>
</ul>
<p>
  Materials will be provided in advance of the workshop and
  large-print handouts are available if needed by notifying the
  organizers in advance.  If we can help making learning easier for
  you (e.g. sign-language interpreters, lactation facilities) please
  get in touch (using contact details below) and we will
  attempt to provide them.
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

<hr/>

{% comment %} 
 SURVEYS - DO NOT EDIT SURVEY LINKS 
{% endcomment %}
<h2 id="surveys">Surveys</h2>
<p>Please be sure to complete these surveys before and after the workshop.</p>
{% if site.carpentry == "swc" %} 
<p><a href="{{ site.swc_pre_survey }}{{ site.github.project_title }}">Pre-workshop Survey</a></p>
<p><a href="{{ site.swc_post_survey }}{{ site.github.project_title }}">Post-workshop Survey</a></p>
{% elsif site.carpentry == "dc" %}
<p><a href="{{ site.dc_pre_survey }}{{ site.github.project_title }}">Pre-workshop Survey</a></p>
<p><a href="{{ site.dc_post_survey }}{{ site.github.project_title }}">Post-workshop Survey</a></p>
{% elsif site.carpentry == "lc" %}
<p><a href="{{ site.lc_pre_survey }}{{ site.github.project_title }}">Pre-workshop Survey</a></p>
<p><a href="{{ site.lc_post_survey }}{{ site.github.project_title }}">Post-workshop Survey</a></p>
{% endif %}

<hr/>

<h2 id="preparation" name="preparation">Preparation</h2>

<p>
  Please read the following before the workshop begins:
</p>
<ol>
  <li><a href="{{ site.training_site }}/papers/science-of-learning-2015.pdf">The Science of Learning</a></li>
</ol>
<p>
  Please also read through <em>one</em> of the episodes below
  carefully, so that you can do some exercises based on it on the
  first day of the class.
</p>
<div class="row">
  <div class="col-md-6">
    <p><strong>Data Carpentry</strong></p>
    <ul>
      <li><a href="{{ site.dc_site }}/OpenRefine-ecology-lesson/01-working-with-openrefine">Faceting and Clustering in OpenRefine</a></li>
      <li><a href="{{ site.dc_site }}/sql-ecology-lesson/01-sql-basic-queries">Basic Queries in SQL</a></li>
      <li><a href="{{ site.dc_site }}/R-ecology-lesson/02-starting-with-data.html">Starting with Data in R</a></li>
      <li><a href="{{ site.dc_site }}/python-ecology-lesson/01-starting-with-data">Starting with Data in Python</a></li>
    </ul>
  </div>
  <div class="col-md-6">
    <p><strong>Software Carpentry</strong></p>
    <ul>
      <li><a href="{{ site.swc_pages }}/shell-novice/03-create/">Working with Files and Directories in the Unix Shell</a></li>
      <li><a href="{{ site.swc_pages }}/git-novice/04-changes/">Tracking Changes in Git</a></li>
      <li><a href="{{ site.swc_pages }}/sql-novice-survey/01-select/">Selecting Data in SQL</a></li>
      <li><a href="{{ site.swc_pages }}/python-novice-inflammation/02-loop/">Repeating Actions with Loops in Python</a></li>
      <li><a href="{{ site.swc_pages }}/r-novice-gapminder/05-data-structures-part2/">Exploring Data Frames in R</a></li>
    </ul>
  </div>
</div>

<hr/>

<h2 id="materials" name="materials">Training Materials and Schedule</h2>

<p>
  Please see <a href="{{ site.training_site }}">this site</a> for course material and tentative schedule.
</p>

{% comment %}
  Collaborative Notes

  If you want to use an Etherpad, go to

      http://pad.software-carpentry.org/YYYY-MM-DD-site

  where 'YYYY-MM-DD-site' is the identifier for your workshop,
  e.g., '2015-06-10-esu'.
{% endcomment %}
{% if page.collaborative_notes %}
<p id="collaborative_notes">
  We will use this <a href="{{page.collaborative_notes}}">collaborative document</a> for chatting, taking notes, and sharing URLs and bits of code.
</p>
{% endif %}

<hr/>

<p>
  Registration is via the form that may be found 
  <a href="https://www.lib.sfu.ca/help/publish/research-data-management/carpentries-application-form">HERE</a>.  
  Please come ready to participate fully both days.  While there will be some lecture-based content this course is designed to be very interactive, especially on the second day.</li>
</ol>
    </p>
