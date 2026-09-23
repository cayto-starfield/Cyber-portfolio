---
layout: default
modal-id: 7
title: Senior Analyst QA ProceSs
img: handlersjournal.png
alt: image-alt

# Add the link to your journal below
project-url:

# Once you've completed your project, update the 'description' below to this one: Provided clear and concise written documentation of cybersecurity events, including detailed event descriptions, tools used, and lessons learned throughout the process.
description: This project is in progress and not ready to be published just yet. Please contact me if you'd like a sneak peek. Otherwise, stay tuned!
---

<h3>Team QA Process SOP</h3>
<p><em>This step-by-step process outlines the key activities and responsibilities involved in the Team QA Process. It ensures a structured approach to quality assurance and integration testing within the development team.</em></p>

<h4>Phase 1: QA Planning</h4>
<table class="qa-portfolio-table">
  <thead>
    <tr>
      <th style="width: 25%;">Task & Step</th>
      <th style="width: 15%;">Owner</th>
      <th style="width: 60%;">Action Items & Guidelines</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>1.1 Create QA Story and 'Test Checklist Creation' Task</strong></td>
      <td><span class="role-badge role-qa">QA Team</span></td>
      <td>
        <ul class="bullet-list">
          <li>In the planning phase, create a QA story that includes a task titled 'Test Checklist Creation'.</li>
          <li>The QA team is responsible for logging the time spent on creating a checklist of tests for all the stories in the current sprint.</li>
          <li>Time spent on this task should not exceed one day.</li>
          <li>The checklist is a Google document shared with and editable by the entire team.</li>
          <li>The checklist serves as a high-level list of verifications, guiding developers in creating integration tests.</li>
          <li>This checklist acts as a fail-safe if full test cases have not yet been created for a feature.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><strong>1.2 Structuring the Test Plan and Test Checklist</strong></td>
      <td><span class="role-badge role-shared">Team</span></td>
      <td>
        <ul class="bullet-list">
          <li>Create a task for organizing how the test plan and test checklist will be structured.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><strong>1.3 Devs' Contribution to the Checklist</strong></td>
      <td><span class="role-badge role-dev">Developers</span></td>
      <td>
        <ul class="bullet-list">
          <li>Developers will also add points to the checklist mentioned above, but only related to the individual stories they will be developing.</li>
          <li>This should be done before starting any development work.</li>
          <li>Create a task on the story, and allocate no more than three hours for this task.</li>
          <li>This is to be completed on the first day of the sprint.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

<h4>Phase 2: Test Data Review & Development</h4>
<table class="qa-portfolio-table">
  <thead>
    <tr>
      <th style="width: 25%;">Task & Step</th>
      <th style="width: 15%;">Owner</th>
      <th style="width: 60%;">Action Items & Guidelines</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>2.1 Review of Test Checklist</strong></td>
      <td><span class="role-badge role-shared">QA & Devs</span></td>
      <td>
        <ul class="bullet-list">
          <li>Once the test checklist is complete, developers can begin development.</li>
          <li>QA will review the checklist and add any points they feel are essential to be covered in the integration test.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><strong>2.2 Writing Detailed Manual Tests</strong></td>
      <td><span class="role-badge role-qa">QA Team</span></td>
      <td>
        <ul class="bullet-list">
          <li>QA will start writing more detailed manual tests, prioritizing stories from highest to lowest priority.</li>
          <li>Test cases will be added to the Moonwalker’s Active Learning test plan Google spreadsheet.</li>
          <li>The location of the test cases will be communicated via Slack.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><strong>2.3 Using Test Cases as Guidelines</strong></td>
      <td><span class="role-badge role-dev">Developers</span></td>
      <td>
        <ul class="bullet-list">
          <li>If test cases are completed before developers begin writing their integration tests, developers should use the completed test cases as guidelines rather than the high-level checklist.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><strong>2.4 Knowledge Sharing with QA</strong></td>
      <td><span class="role-badge role-shared">QA & Devs</span></td>
      <td>
        <ul class="bullet-list">
          <li>It is preferable for developers to have a knowledge-sharing session with QA before writing integration tests.</li>
          <li>Knowledge sharing can reveal scenarios that are invalid or were not initially accounted for and need to be added.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><strong>2.5 Documenting Automated Tests</strong></td>
      <td><span class="role-badge role-dev">Devs / Auto Testers</span></td>
      <td>
        <ul class="bullet-list">
          <li>Developers/QA Automation Testers are required to document on the checklist and/or spreadsheet which points/scenarios they have automated.</li>
          <li>They should specify the location of these automated tests.</li>
          <li>The spreadsheet should have a column titled "Automated," and developers should indicate "yes" or "no" accordingly for each automated test.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>
