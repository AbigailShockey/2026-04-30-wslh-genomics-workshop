---
layout: workshop      # DON'T CHANGE THIS.
# More detailed instructions (including how to fill these variables for an
# online workshop) are available at
# https://carpentries.github.io/workshop-template/customization/index.html
venue: "Wisconsin State Laboratory of Hygiene"        # brief name of the institution that hosts the workshop without address (e.g., "Euphoric State University")
address: "online"      # full street address of workshop (e.g., "Room A, 123 Forth Street, Blimingen, Euphoria"), videoconferencing URL, or 'online'
country: "United States"      # lowercase two-letter ISO country code such as "fr" (see https://en.wikipedia.org/wiki/ISO_3166-1#Current_codes) for the institution that hosts the workshop
language: "en"     # lowercase two-letter ISO language code such as "fr" (see https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) for the workshop
latitude: "0"        # decimal latitude of workshop venue (use https://www.latlong.net/)
longitude: "0"       # decimal longitude of the workshop venue (use https://www.latlong.net)
humandate: "April 29-30, 2026"    # human-readable dates for the workshop (e.g., "Feb 17-18, 2020")
humantime: "9:00 am - 4:30 pm CEST (7:00 am - 2:30 pm UTC)"    # human-readable times for the workshop e.g., "9:00 am - 4:30 pm CEST (7:00 am - 2:30 pm UTC)"
startdate: 2026-04-29      # machine-readable start date for the workshop in YYYY-MM-DD format like 2015-01-01
enddate: 2026-04-30        # machine-readable end date for the workshop in YYYY-MM-DD format like 2015-01-02
instructor: ["Abigail Shockey, PhD", "Christopher Jossart, MS"] # boxed, comma-separated list of instructors' names as strings, like ["Kay McNulty", "Betty Jennings", "Betty Snyder"]
helper: ["", ""]     # boxed, comma-separated list of helpers' names, like ["Marlyn Wescoff", "Fran Bilas", "Ruth Lichterman"]
email: ["first@example.org","second@example.org"]    # boxed, comma-separated list of contact email addresses for the host, lead instructor, or whoever else is handling questions, like ["marlyn.wescoff@example.org", "fran.bilas@example.org", "ruth.lichterman@example.org"]
collaborative_notes:  # optional: URL for the workshop collaborative notes, e.g. an Etherpad or Google Docs document (e.g., https://pad.carpentries.org/2015-01-01-euphoria)
eventbrite:           # optional: alphanumeric key for Eventbrite registration, e.g., "1234567890AB" (if Eventbrite is being used)
what3words:           # optional: what3words (https://what3words.com) address of the workshop venue, without leading slashes e.g. "globe.lessening.computers"
---

<h2 id="general">General Information</h2>

{% comment %}
INTRODUCTION

Edit the general explanatory paragraph below if you want to change
the pitch.
{% endcomment %}

<p>
This workshop teaches the basics of bioinformatics analysis including: use of the command-line and command-line bioinformatics tools to analyze next-generation sequencing data, and connecting to and using cloud computing environments. This workshop will be virtual and instructors will use participatory live coding. Instructors will teach lesson material by typing code, and workshop participants will code alongside instructors. Each lesson will include practical exercises that allow participants to test their knowledge as they learn.
</p>

{% comment %}
AUDIENCE

Explain who your audience is.  (In particular, tell readers if the
workshop is only open to people from a particular institution.
{% endcomment %}

<p id="who">
  <strong>Who:</strong>
  This workshop is for individuals with little to no prior experience with the command-line, bioinformatics analyses, or cloud computing. 
  However, participants are expected to have some familiarity with biological concepts, including genome sequencing and the the concept of genomic variation.
</p>
<p align="center">
  <strong>You don't need to have any previous knowledge of the tools
  that will be presented at the workshop.</strong>
</p>

{% comment %}
LOCATION

This block displays the address and links to maps showing directions
if the latitude and longitude of the workshop have been set.  You
can use https://www.latlong.net/ to find the lat/long of an
address.
{% endcomment %}

<p id="where">
  <strong>Where:</strong> This training will take place online.
  The instructors will provide you with the information you will need to connect to this meeting.
</p>

{% comment %}
DATE

This block displays the date and links to Google Calendar.
{% endcomment %}
{% if page.humandate %}
<p id="when">
  <strong>When:</strong>
  {{page.humandate}}; {{page.humantime}}
  {% include workshop_calendar.html %}
</p>
{% endif %}

{% comment %}
SPECIAL REQUIREMENTS

Modify the block below if there are any special requirements.
{% endcomment %}
<p id="requirements">
  <strong>Requirements:</strong>
    Participants must have access to the internet and a computer with a
    Mac, Linux, or Windows operating system (not a tablet, Chromebook, etc.).
</p>

{% comment %}
ACCESSIBILITY

Modify the block below if there are any barriers to accessibility or
special instructions.
{% endcomment %}
<p id="accessibility">
  <strong>Accessibility:</strong>
  We are committed to making this workshop
  accessible to everybody. 
</p>
<p>We are dedicated to providing a positive and accessible learning environment for all. 
  We do not require participants to provide documentation of disabilities or disclose any unnecessary personal information. 
  However, we do want to help create an inclusive, accessible experience for all participants. 
  We encourage you to share any information that would be helpful to make your Carpentries experience accessible.
  To request an accommodation for this workshop [...].
</p>
<p>
  <a href="https://glosario.carpentries.org/">Glosario</a> is a multilingual glossary 
  for computing and data science terms. The glossary helps 
  learners attend workshops and use our lessons to make sense of computational and programming jargon written in English by offering it 
  in their native language. Translating data science terms also provides a teaching tool for Carpentries Instructors to reduce barriers 
  for their learners.
</p>

{% comment %}
WORKSHOP RECORDINGS

Modify or remove the block below if you plan to record the workshop.
<p id="recordings">
  <strong>Workshop Recordings:</strong>
  Carpentries workshops are designed to be interactive rather than lecture-based, with lessons that build upon one another.
  To foster a positive online learning environment, we strongly recommend that participants join in real time.
  As a result, workshop recordings are not recommended and may not be available to learners.
</p>
{% endcomment %}

{% comment %}
CONTACT EMAIL ADDRESS

Display the contact email address set in the configuration file.
{% endcomment %}
<p id="contact">
  <strong>Contact:</strong>
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
<p id="roles">
  <strong>Roles:</strong>
  To learn more about the roles at the workshop (who will be doing what),
  refer to <a href="https://carpentries.org/workshop_faq/#what-are-the-roles-of-everyone-participating-in-a-workshop">our Workshop FAQ</a>.
</p>
{% endcomment %}

{% comment %}
WHO CAN ATTEND?

If you would like to specify who can attend the workshop,
you can use the section below.

Move the 'endcomment' tag above the beginning of the following
<p> tag to make this section visible.

Edit the text to match who can attend the workshop. For instance:
- This workshop is open to affiliates to ABC university.
- This workshop is open to the public.
- If you are interested in attending this workshop, contact me@example.com
  for more information

<p id="who-can-attend">
    <strong>Who can attend?:</strong>
    This workshop is open to ....
</p>
{% endcomment %}

<hr/>

{% comment %}
Collaborative Notes

If you want to use an Etherpad, go to

https://pad.carpentries.org/YYYY-MM-DD-site

where 'YYYY-MM-DD-site' is the identifier for your workshop,
e.g., '2015-06-10-esu'.

Note we also have a CodiMD (the open-source version of HackMD)
available at https://codimd.carpentries.org
{% endcomment %}
{% if page.collaborative_notes %}
<h2 id="collaborative_notes">Collaborative Notes</h2>

<p>
We will use this <a href="{{ page.collaborative_notes }}">collaborative document</a> for chatting, taking notes, and sharing URLs and bits of code.
</p>
<hr/>
{% endif %}

{% comment %}
SURVEYS - DO NOT EDIT SURVEY LINKS
{% endcomment %}
<h2 id="surveys">Surveys</h2>
<p>Please be sure to complete these surveys before and after the workshop.</p>
{% if site.carpentry == "incubator" %}
<p><a href="{{ site.incubator_pre_survey }}">Pre-workshop Survey</a></p>
<p><a href="{{ site.incubator_post_survey }}">Post-workshop Survey</a></p>
{% elsif site.incubator_pre_survey or site.incubator_post_survey %}
<div class="alert alert-danger">
WARNING: you have defined custom pre- and/or post-survey links for
a workshop not configured for The Carpentries Incubator
(the value of `curriculum` is not set to `incubator` in `_config.yml`).
Please comment out the `incubator_pre_survey` and `incubator_post_survey` fields
in `_config.yml` or, if this workshop is teaching a lesson in the Incubator,
change the value of `carpentry` to `incubator`.
</div>
{% else %}
<p><a href="{{ site.pre_survey }}{{ site.github.project_title }}">Pre-workshop Survey</a></p>
<p><a href="{{ site.post_survey }}{{ site.github.project_title }}">Post-workshop Survey</a></p>
{% endif %}

<hr/>


{% comment %}
SCHEDULE

Show the workshop's schedule.

Small changes to the schedule can be made by modifying the
`schedule.html` found in the `_includes` folder for your
workshop type (`swc`, `lc`, or `dc`). Edit the items and
times in the table to match your plans. You may also want to
change 'Day 1' and 'Day 2' to be actual dates or days of the
week.

For larger changes, a blank template for a 4-day workshop
(useful for online teaching for instance) can be found in
`_includes/custom-schedule.html`. Add the times, and what
you will be teaching to this file. You may also want to add
rows to the table if you wish to break down the schedule
further. To use this custom schedule here, replace the block
of code below the Schedule `<h2>` header below with
`{% include custom-schedule.html %}`.
{% endcomment %}

<h2 id="schedule">Schedule</h2>

{% include dc/schedule.html %}

{% comment %}
Edit/replace the text above if you want to include a schedule table.
See the contents of the _includes/custom-schedule.html file for an example of
how one of these schedule tables is constructed.
{% endcomment %}

<hr/>

{% comment %}
SETUP

Delete irrelevant sections from the setup instructions.  Each
section is inside a 'div' without any classes to make the beginning
and end easier to find.

This is the other place where people frequently make mistakes, so
please preview your site before committing, and make sure to run
'tools/check' as well.
{% endcomment %}

<h2 id="setup">Setup</h2>

<p>
  To participate in this workshop, you will need an up-to-date web browser and access to the videoconferencing client Zoom. If you have the ability, the instructions for installing Zoom can be found below. If you do not have the ability to install the Zoom client, you can access the workshop using Zoom on your web browser.
</p>

{% comment %}
For online workshops, the section below provides:
- installation instructions for the Zoom client
- recommendations for setting up Learners' workspace so they can follow along
  the instructions and the videoconferencing

If you do not use Zoom for your online workshop, edit the file
`_includes/install_instructions/videoconferencing.html`
to include the relevant installation instructions.
{% endcomment %}


<h3 id="videoconferencing">Install the videoconferencing client</h3>

{% comment %}
Replace the paragraph below with the relevant installation instructions
if you do not use Zoom
{% endcomment %}
<p>
  If you haven't used Zoom before, go to the
  <a href="https://zoom.us/download">official website</a>
  to download and install the Zoom client for your computer.
</p>

<h4>Set up your workspace</h4>

<p>
  In this workshop, you will be learning by "coding along" with the Instructors.
  To do this, you will need to have both the window for the tool
  you will be learning about (in this workshop, the command line)
  and the window for the Zoom video conference client open.
  In order to see both at once,
  we recommend using one of the following set up options:
  <ul>
    <li><strong>Two monitors:</strong> If you have two monitors,
      plan to have the tool you are learning up on one monitor and
      the video conferencing software on the other.</li>
    <li><strong>Two devices:</strong> If you don't have two monitors,
      do you have another device (tablet, smartphone) with a medium to large
      sized screen? If so, try using the smaller device as your video
      conference connection and your larger device (laptop or desktop)
      to follow along with the tool you will be learning about.</li>
    <li><strong>Divide your screen:</strong> If you only have one device
      and one screen, practice having two windows
      (the video conference program and one of the tools you will be using
      at the workshop) open together.
      How can you best fit both on your screen?
      Will it work better for you to toggle between them
      using a keyboard shortcut?
      Try it out in advance to decide what will work best for you.</li>
  </ul>
  This <a href="https://carpentries.org/blog/2020/06/online-workshop-logistics-and_screen-layouts/" target="_blank">blog post</a> includes detailed information on how to set up your screen to follow along during the workshop.
</p>

{% comment%}
CODE OF CONDUCT
{% endcomment %}
<h2 id="code-of-conduct">Code of Conduct</h2>

<p>
Workshop instructors, helpers, and participants are expected to follow are required to conform to the <a href="https://abigailshockey.github.io/2026-04-30-wslh-genomics-workshop/CODE_OF_CONDUCT.html">Code of Conduct</a>.
</p>
