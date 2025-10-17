# Lab 3 Complete a Web API -- Project Report

## Description of Changes
The first step was to create tests verifying safe and idempotent REST endpoints in the file EmployeeController.
- POST: A setUp block was added to simulate ``save()`` returning different IDs on consecutive calls. The test also verifies that ``save()`` is called exactly twice, and that delete and other read methods are not called.
- GET: A setUp block was added to simulate ``findById(id)`` returning an employee object when id is 1, and an empty object when id is 2. The test verifies that ``findById(1)`` is called exactly twice and findById(2) once, while save, delete, and other read methods are not called.
- PUT: A setUp block was added to simulate ``findById(id)`` returning an empty object on the first call and an employee object on the second call. ``save()`` was also simulated to return the created employee object. The test verifies that save() is called exactly twice.
- DELETE: A setUp block with justRun was added to allow ``deleteById(id)`` to be called. The test verifies that ``deleteById(id)`` is called exactly twice, and that save and other read methods are not called.

## Technical Decisions
In this practice, no technical decisions regarding deployment were made, as the deployment followed the instructions provided in the lab documentation. The only decision made was to run ktlintFormat to fix code style violations.
## Learning Outcomes
During this practice, I learned the difference between safe, idempotent, and non-idempotent methods, and how to verify them in tests. MockK was used to simulate specific behaviors in the tests.
## AI Disclosure
### AI Tools Used
- ChatGPT

### AI-Assisted Work
ChatGPT was used to correct grammatically error of this report.
Approximately 10% of the report text was generated with AI assistance.
All code provided by ChatGPT was manually reviewed and adapted to the project context, ensuring consistency with the lab practice and guidance.

### Original Work
Everything else was developed by the developer following the practical guide.