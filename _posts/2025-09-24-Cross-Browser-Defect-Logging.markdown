---
layout: default
modal-id: 9
title: Cross Browser Defect Logging
img: handlersjournal.png
alt: image-alt

# Add the link to your journal below
project-url: https://sites.google.com/view/caytonova/see-portfolio/xbrower-defect-triaging?authuser=0

# Once you've completed your project, update the 'description' below to this one: Provided clear and concise written documentation of cybersecurity events, including detailed event descriptions, tools used, and lessons learned throughout the process.
description: This project is in progress and not ready to be published just yet. Please contact me if you'd like a sneak peek. Otherwise, stay tuned!
---

<h3>1. Cross-Browser Functional Defects (Firefox)</h3>
<p><em>Highlighting high-priority cross-browser UI and functional defects discovered during testing.</em></p>
<table class="qa-portfolio-table">
  <thead>
    <tr>
      <th>Defect ID</th>
      <th>Component</th>
      <th>Priority</th>
      <th>Description</th>
      <th>Environment</th>
      <th>Status</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>DEF-001</strong></td>
      <td>Tab Strip</td>
      <td><strong>High</strong></td>
      <td>Arrows to the right aren't level with the rest of the text.</td>
      <td>FF 33 (Win)</td>
      <td><span class="status-badge status-rft">Ready for Test</span></td>
    </tr>
    <tr>
      <td><strong>DEF-002</strong></td>
      <td>Document Tab</td>
      <td><strong>Critical</strong></td>
      <td>From the Document item list: Dragging the arrow in Browser window does not resize browser pane.</td>
      <td>FF 33 (Win)</td>
      <td><span class="status-badge status-done">Done</span></td>
    </tr>
    <tr>
      <td><strong>DEF-003</strong></td>
      <td>Viewer</td>
      <td><strong>Critical</strong></td>
      <td>Resize bar between viewer window and coding layout doesn't resize (Vertical resizing works).</td>
      <td>FF 33 (Win/Mac)</td>
      <td><span class="status-badge status-done">Done</span></td>
    </tr>
    <tr>
      <td><strong>DEF-004</strong></td>
      <td>Modals</td>
      <td><strong>Critical</strong></td>
      <td>Complex modal buttons do nothing on click. Simple "close" modals function normally.</td>
      <td>FF 33 (Win/Mac)</td>
      <td><span class="status-badge status-rft">Ready for Test</span></td>
    </tr>
    <tr>
      <td><strong>DEF-005</strong></td>
      <td>Pivot</td>
      <td><strong>High</strong></td>
      <td>Pivot hangs indefinitely; "Cancel Request" link does not work on same modal.</td>
      <td>FF 33 (Win/Mac)</td>
      <td><span class="status-badge status-dev">In Dev</span></td>
    </tr>
    <tr>
      <td><strong>DEF-006</strong></td>
      <td>List View</td>
      <td><strong>Critical</strong></td>
      <td>Fields with a large amount of text overflow into other columns; affects Date Fields.</td>
      <td>FF 33 (Win/Mac)</td>
      <td><span class="status-badge status-done">Done</span></td>
    </tr>
    <tr>
      <td><strong>DEF-007</strong></td>
      <td>Layouts</td>
      <td><strong>Critical</strong></td>
      <td>Checkboxes cannot be toggled on/off. Clicking one reloads the page, preventing saving objects with a required Yes/No field.</td>
      <td>FF 33 (Win/Mac)</td>
      <td><span class="status-badge status-rft">Ready for Test</span></td>
    </tr>
    <tr>
      <td><strong>DEF-008</strong></td>
      <td>Popup picker</td>
      <td><strong>High</strong></td>
      <td>"Set" button for single-object popup pickers doesn't work (happens on any select field with single choice).</td>
      <td>FF 33 (Win/Mac)</td>
      <td><span class="status-badge status-done">Done</span></td>
    </tr>
    <tr>
      <td><strong>DEF-009</strong></td>
      <td>Production Sets</td>
      <td><strong>High</strong></td>
      <td>Console buttons "Check for Conflicts" and "Run Production" are clickable but do not execute.</td>
      <td>FF 33 (Win/Mac)</td>
      <td><span class="status-badge status-done">Done</span></td>
    </tr>
    <tr>
      <td><strong>DEF-010</strong></td>
      <td>Document Viewer</td>
      <td><strong>High</strong></td>
      <td>Unicode is not being rendered correctly in extracted text mode.</td>
      <td>FF 33 (Win/Mac)</td>
      <td><span class="status-badge status-open">Open</span></td>
    </tr>
  </tbody>
</table>

<h3>2. Architectural Root Causes</h3>
<p><em>Core JavaScript incompatibilities categorized across multiple areas of the application.</em></p>
<table class="qa-portfolio-table">
  <thead>
    <tr>
      <th>Root Cause</th>
      <th>Risk Level</th>
      <th>Description & Impact</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>No support for <code>window.event</code></strong></td>
      <td>High</td>
      <td>Found in 60+ lines across 28 files (JS functions and VB controls). Requires one-by-one refactoring of both the function call and the function itself to prevent breaking all browsers.</td>
    </tr>
    <tr>
      <td><strong>No support for <code>event.srcElement</code></strong></td>
      <td>High</td>
      <td>Found in 44 lines across 19 files. In Chrome/IE, the event contains <code>srcElement</code> or mouse offset. In FF, the event is undefined, requiring the triggering function to pass it explicitly.</td>
    </tr>
    <tr>
      <td><strong>No support for styling scroll bars</strong></td>
      <td>Low</td>
      <td>Requires implementing custom JS scrollbars (or a library) or altering CSS, which could negatively impact Chrome and IE rendering.</td>
    </tr>
  </tbody>
</table>

<h3>3. JavaScript Console Exceptions</h3>
<p><em>Browser console errors mapped to specific user trigger actions.</em></p>
<table class="qa-portfolio-table">
  <thead>
    <tr>
      <th>Exception / Error</th>
      <th>Triggering Action</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><code>TypeError: window.event is undefined</code></td>
      <td>
        <ul class="bullet-list">
          <li>Clicking the Security icon on item list view pages.</li>
          <li>Opening 'Build Layout' icon from DynamicObject 'Edit Page'.</li>
          <li>Clicking 'Edit Permissions' from 'Export these objects' view.</li>
          <li>Clicking "Set" button on a multi-list filter.</li>
          <li>Clicking filter dropdowns or vertical tabs.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><code>TypeError: e is undefined</code></td>
      <td>
        <ul class="bullet-list">
          <li>Resizing columns is jerky and throws this console error.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><code>ReferenceError: event is not defined</code></td>
      <td>
        <ul class="bullet-list">
          <li>Clicking an ellipsis in the Document Review Coding Pane.</li>
          <li>Clicking a date/time popup picker in a layout.</li>
          <li>Checking/unchecking a checkbox while editing a document.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><code>TypeError: n.originalEvent.srcElement is undefined</code></td>
      <td>
        <ul class="bullet-list">
          <li>Clicking on the column "Date Type" or "Fact" under Fact Manager -> New Fact tabs.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><code>TypeError: this._doc is undefined</code></td>
      <td>
        <ul class="bullet-list">
          <li>Clicking 'Undo', 'Redo', 'TextFontColor', or 'Cancel' in MessageOfTheDay Instance Details.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>
