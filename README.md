Pahunch Ledger

Helping communities organise essential needs when mountain roads are disrupted.

Pahunch Ledger is a mobile friendly prototype designed around a community resilience problem: when mountain roads become disrupted, access to essential services such as medicines, healthcare, education and supplies can be affected.

The prototype allows users to record an affected essential service, estimate the number of people affected, assign an urgency level, and organise reports into a priority list using a transparent scoring rule.

Live demo: https://mukktaa.github.io/Pahunch-Ledger/

Problem Statement

Mountain communities can face difficulties accessing essential services when roads are disrupted by landslides, severe weather or other incidents. Organising information about affected needs may help communities understand which issues require attention.

Pahunch Ledger explores a simple way to structure this information. It is a prototype for demonstration and further development, not a replacement for official disaster reporting or emergency response systems.

Proposed Solution

The prototype provides:

- A form for recording a village or area and an affected essential service.
- Urgency selection and an estimate of the number of people affected.
- Optional details about the disruption.
- Automatic priority scoring.
- A priority list ordered by score.
- Local browser storage so reports persist after a page refresh on the same browser and device.
- A function to clear locally saved demo reports.

Technology Stack

- HTML for page structure and form elements.
- CSS for styling and responsive presentation.
- JavaScript for form handling, score calculation, sorting and deletion.
- Browser Local Storage for saving demo reports on the user's device.
- GitHub for source-code hosting.
- GitHub Pages for publishing the prototype.

The current version does not require a backend server or database.

Priority Scoring Method

The prototype uses an experimental rule:

Priority score = (Urgency × 2) + Impact points

Urgency values

- High = 3
- Medium = 2
- Low = 1

Impact points

- 100 or more people affected = 3 points
- 20–99 people affected = 2 points
- Fewer than 20 people affected = 1 point

Example

A high-urgency report affecting 120 people receives a score of:

(3 × 2) + 3 = 9

A low-urgency report affecting 5 people receives a score of:

(1 × 2) + 1 = 3

Reports with higher scores appear first. This rule is experimental and is not an official disaster assessment standard.

How to Use the Prototype

1. Open the live demo.
2. Enter a village or area.
3. Select the affected essential service and urgency.
4. Enter an estimated number of people affected.
5. Add optional details, if necessary.
6. Submit the report to the priority list.
7. Review the calculated score and report order.
8. Refresh the page to check local persistence.
9. Use the clear button to remove saved demo reports.

Please use fictional information for demonstrations. Do not enter personal or sensitive information.

Architecture

The prototype follows a simple browser-based workflow:

1. Input: The user enters information through the report form.
2. Processing: JavaScript validates the required fields and calculates a score using the defined rule.
3. Prioritisation: Reports are sorted by their calculated scores.
4. Storage: Reports are saved in the browser's Local Storage.
5. Display: The priority list shows the reports and their scores.
6. Deletion: The user can clear the saved demo reports.

All of these operations take place in the browser. The current prototype does not transmit reports to a central server.

Testing

The following functional checks have been performed on the prototype:

Test| Expected result| Result
Priority scoring| Example reports receive scores of 9 and 3| Passed
Priority sorting| Higher-scoring report appears first| Passed
Persistence| Reports remain after refreshing the page| Passed
Clear reports| Reports disappear and remain deleted after refresh| Passed

These are manual functional tests, not a formal independent evaluation.

Limitations

- Reports are stored only in the current browser on the current device.
- Reports are not shared or synchronised between users.
- The prototype does not verify reported incidents.
- It does not provide live road conditions.
- It does not notify authorities or emergency services.
- The priority score is experimental and must not be treated as an official emergency assessment.
- The current version has not been validated through a real-world community deployment.

Do not rely on this prototype for emergency decisions. Contact official services in an emergency.

Future Scope

Possible future improvements include:

- Secure, shared reporting with appropriate access controls.
- Offline-first support and reliable synchronisation when connectivity returns.
- Local-language support.
- Accessibility improvements.
- Community feedback and usability testing.
- Carefully designed verification workflows.
- Consultation with disaster-management professionals to evaluate the prioritisation method.

These are proposed improvements, not features currently implemented.

Responsible Use of AI

AI assistance was used during development for coding guidance, explanations and documentation support. The prototype was manually tested using sample reports. Any AI generated code or content should be reviewed and understood by the project author.

Licence

This project is released under the MIT License. See the "LICENSE" file for details.
