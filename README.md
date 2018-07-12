<html>
<body>
<h3>FAIR SCREENING</h3>
<p>Fair Screening is an application built in Docassemble designed to help rental tenants in the United States to obtain, and in some cases amend, their tenant screening reports.</p>
<p>To see Fair Screening in action, visit https://www.fairscreening.com.</p>

<h3>HOW IT WORKS</h3>
<p>The application is split up into two interviews, fairscreening_request_report.yml and fairscreening_followup.yml. In request_report, the application follows these steps:<p>

<ol>
<li>Determine whether user is eligible to obtain a copy of their screening report.</li>
<li>If eligible, collect personal information.</li>
<li>Assemble personal information into a request letter to one or more screening companies.</li>
<li>Fax request letter to one or more screening companies.</li>
</ol>

<p>In fairscreening_followup, the application follows these steps:</p>

<ol>
<li>Make sure user has received a copy of their screening report in the mail.</li>
<li>Check each type of issue with a report to see if the user is experiencing that issue.</li>
<li>For each matching issue, collect specific data.</li>
<li>Output data on all matching issues into an Action Plan and present action plan to the user for download.</li>
</ol>

<h3>LIMITATIONS</h3>
<p>Currently, the application allows tenants from anywhere in the US to obtain their report, but only tenants who applied for housing in Illinois can amend their report. This is because the application is customized to Illinois law. However, those rules can be modified or expanded to work with any US jurisdiction.</p>

<h3>STATIC FILES</h3>
<p>hide_source.js: Javascript code to hide the source button. You'll want to include this file in Production.</p>

<h3>SOURCES</h3>
<p>company_info.yml: YML file with the list of screening companies, their names and contact information.</p>

<h3>INTEGRATIONS</h3>
<p>Twilio: Fair Screening uses the Twilio fax API (beta) to fax requests for screening reports. You'll need to set up a Twilio account and include the following directives in the Docassemble config file:</p>

<p>twilio:<br>
  fax: True<br>
  account sid: *include account sid from Twilio*<br>
  auth token: *include token from Twilio*<br>
  number: *include fax number from Twilio, number should be formatted like "+18004445555"*
  </p>
  
<p>Mailgun: Fair Screening uses the Mailgun API to send notification emails to the user. You don't have to use Mailgun to send emails, but if you want to, you'll need to set up a Mailgun account and include the following directives in the Docassemble config file:</p>

<p>mail:<br>
  default sender: *include name and email* <br>
  mailgun api key: *include mailgun api key* <br>
  mailgun domain: mg.yourdomain.com
  </p>
  
<p>Google Maps: Fair Screening uses the Google Maps API for address autocomplete. This function is not required, but if you want to include this, you'll need to set up a Google account and include the following directive in the Docassemble config file:</p>

<p>google:<br>
  google maps api key: *include google maps api key*</p>

<h3>DOCASSEMBLE</h3>
<p>For more information on Docassemble, visit https://www.docassemble.org</p>

<h3>QUESTIONS OR FEEDBACK?</h3>
<p>Email me at tobyfranklin@gmail.com.</p>
</body>
</html>
