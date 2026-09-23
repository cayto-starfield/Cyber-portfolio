---
layout: default
modal-id: 8
title: UI & Accessibility Test Plan
img: linux.png
alt: image-alt

# Add the link to your journal below
project-url: https://sites.google.com/view/caytonova/see-portfolio/ui-acessibility-test-cases-writing?authuser=0

# Once you've completed your project, update the 'description' below to this one: Provided clear and concise written documentation of cybersecurity events, including detailed event descriptions, tools used, and lessons learned throughout the process.
description: A structured manual test execution plan designed to validate complex frontend web components (such as dynamic data grids and overflow menus) and verify strict Section 508 accessibility compliance. This project ensured the application met federal standards for keyboard-only navigation and inclusive user experience design.
---

<h3>1. Tab Strip & Overflow Menu UI</h3>
<table class="qa-portfolio-table">
  <thead>
    <tr>
      <th>Test ID</th>
      <th>Scenario</th>
      <th>Steps</th>
      <th>Expected Result</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>TS-01</strong></td>
      <td>Hamburger Icon UI & Minimization</td>
      <td>
        <ol class="step-list">
          <li>Open browser in full screen.</li>
          <li>Click the browser 'minimize button'.</li>
        </ol>
      </td>
      <td>The 'Hamburger' overflow icon is displayed and retains proper UI appearance.</td>
    </tr>
    <tr>
      <td><strong>TS-02</strong></td>
      <td>Overflow Menu Animation</td>
      <td>
        <ol class="step-list">
          <li>Click on the 'Hamburger' icon.</li>
        </ol>
      </td>
      <td>Activates the animation of the Overflow menu flyout.</td>
    </tr>
    <tr>
      <td><strong>TS-03</strong></td>
      <td>Pinned Tab Highlighting (Full Screen)</td>
      <td>
        <ol class="step-list">
          <li>Open browser in full screen.</li>
          <li>Click on a tab in the overflow to 'pin' it.</li>
          <li>Click on a horizontal tab to make it active.</li>
        </ol>
      </td>
      <td>Active tab is highlighted. Pinned tab appears to the left of the hamburger icon with matching background color.</td>
    </tr>
    <tr>
      <td><strong>TS-04</strong></td>
      <td>Pinned Tab Highlighting (Minimized)</td>
      <td>
        <ol class="step-list">
          <li>Minimize the browser window.</li>
          <li>Click on a tab in the overflow to 'pin' it.</li>
          <li>Click a horizontal tab to make active.</li>
        </ol>
      </td>
      <td>Active tab is highlighted. Pinned tab is separated from horizontal tabs by a vertical white bar.</td>
    </tr>
  </tbody>
</table>

<h3>2. 508 Compliance (Accessibility Navigation)</h3>
<table class="qa-portfolio-table">
  <thead>
    <tr>
      <th>Test ID</th>
      <th>Scenario</th>
      <th>Steps</th>
      <th>Expected Result</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>ACC-01</strong></td>
      <td>Forward Tab Navigation</td>
      <td>
        <ol class="step-list">
          <li>Press the <code>Tab</code> key repeatedly.</li>
        </ol>
      </td>
      <td>User navigates forward through all page functions and menu bar tabs.</td>
    </tr>
    <tr>
      <td><strong>ACC-02</strong></td>
      <td>Reverse Tab Navigation</td>
      <td>
        <ol class="step-list">
          <li>Press <code>Shift + Tab</code>.</li>
        </ol>
      </td>
      <td>User navigates backward to the previous user function/child tab.</td>
    </tr>
    <tr>
      <td><strong>ACC-03</strong></td>
      <td>Skip to Main Content</td>
      <td>
        <ol class="step-list">
          <li>Navigate to the top of the page.</li>
          <li>Focus on "Skip To the Main Content" tooltip.</li>
          <li>Press <code>Enter</code>.</li>
        </ol>
      </td>
      <td>Focus immediately jumps to the page's main content area.</td>
    </tr>
  </tbody>
</table>

<h3>3. Data Grid UI & Column Resizing</h3>
<table class="qa-portfolio-table">
  <thead>
    <tr>
      <th>Test ID</th>
      <th>Scenario</th>
      <th>Steps</th>
      <th>Expected Result</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>GRID-01</strong></td>
      <td>Column Resizing by Dragging</td>
      <td>
        <ol class="step-list">
          <li>Navigate to an Item List or Popup List.</li>
          <li>Drag a column's resize arrow left or right.</li>
        </ol>
      </td>
      <td>Only the dragged column and the far-right column are affected. All other columns retain original settings.</td>
    </tr>
    <tr>
      <td><strong>GRID-02</strong></td>
      <td>Reset Column Sizes</td>
      <td>
        <ol class="step-list">
          <li>Resize a column.</li>
          <li>Click the resize column icon.</li>
        </ol>
      </td>
      <td>All columns return to their default width settings.</td>
    </tr>
    <tr>
      <td><strong>GRID-03</strong></td>
      <td>Grid Row Color States</td>
      <td>
        <ol class="step-list">
          <li>Navigate to a populated List.</li>
          <li>Hover over a row.</li>
          <li>Check the box on a row.</li>
          <li>Click on a row to select it.</li>
        </ol>
      </td>
      <td>Hover = Red<br>Checked = Blue<br>Selected = Green</td>
    </tr>
  </tbody>
</table>
