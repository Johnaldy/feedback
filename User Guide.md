# Partner Engagement Feedback System - User Guide

This guide explains how to use the Partner Engagement Feedback system to collect, submit, and analyze customer feedback on partner-delivered engagements.

## For Partners: Submitting Feedback

### Step 1: Collect Customer Feedback
After completing an engagement with a customer, collect feedback using your preferred method (survey, email, etc.) on the following metrics:
- Overall Customer Satisfaction (1-5 scale)
- Quality of Work/Material (1-5 scale)
- Effectiveness of Communication (1-5 scale)
- Impact/Value of Service (1-5 scale)
- Any additional comments or suggestions

### Step 2: Submit Feedback via GitHub Issue
1. Go to [Submit Partner Feedback](https://github.com/johnaldy/feedback/issues/new?template=partner-feedback.yml)
2. Fill out all required fields in the form:
   - Partner Name (select from dropdown)
   - Date Completed (when the engagement ended)
   - Engagement Type (select from dropdown)
   - Engagement Name (title of the engagement)
   - Engagement Status (current status)
   - Number of Responses Received (how many customers provided feedback)
   - Average scores for all metrics
   - Vertical (region of the customer)
   - Any customer suggestions or comments
   - Recommendations for GitHub
   - Suggested Add-on Products

3. Click "Submit new issue" to record the feedback

### Step 3: Review Average Score
After submission, a GitHub Action will automatically:
- Calculate the overall Average score (average of the 4 metrics)
- Add a comment to the issue with the calculated score
- Apply appropriate labels based on the score

## For Corps Team: Analyzing Feedback

### Viewing Individual Feedback
All feedback submissions are stored as GitHub Issues with the `feedback` label.

### Analyzing Feedback Data
1. Go to the [Partner Engagement Feedback Project](https://github.com/johnaldy/feedback/projects)
2. Use the different views to analyze the data:
   - "Average by Partner" - View feedback scores grouped by partner
   - "All Feedback" - View all feedback submissions in a table format

### Filtering and Searching
You can filter feedback data by:
- Partner (using the Partner field)
- Engagement Type (using the Engagement Type field)
- Average Score category (using labels: Average-excellent, Average-good, Average-average, Average-needs-attention)
- Date range (using the Date Completed field)

### Exporting Data
To export data for further analysis:
1. Go to the Project view
2. Click on the "..." menu
3. Select "Export as CSV"

## Feedback Reminder Process

1. Weekly reminders are sent automatically for engagements that require feedback
2. Partners receive an email with a link to the feedback form
3. Follow-up reminders are sent if feedback is not submitted within 2 weeks

## Technical Support
If you encounter any issues with the feedback system, please contact @Johnaldy or file an issue with the label `support`.
