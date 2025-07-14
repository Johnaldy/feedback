# Partner Engagement Feedback System - Implementation Guide

This document provides step-by-step instructions for implementing the Partner Engagement Feedback System.

## Prerequisites
- Admin access to the github/services repository
- GitHub Actions enabled on the repository
- Permissions to create GitHub Projects

## Implementation Steps

### 1. Add Issue Template

1. Create the `.github/ISSUE_TEMPLATE` directory in the repository if it doesn't exist
2. Add the `partner-feedback.yml` file to this directory
3. Commit and push the changes

### 2. Set Up GitHub Actions

1. Create the `.github/workflows` directory if it doesn't exist
2. Add the following workflow files:
   - `process-feedback.yml` - For processing submitted feedback
   - `feedback-reminder.yml` - For sending automated reminders

3. Configure the required secrets for email sending:
   - Go to Repository Settings > Secrets and Variables > Actions
   - Add the following secrets:
     - `MAIL_USERNAME` - Email username for sending reminders
     - `MAIL_PASSWORD` - Email password or app password

### 3. Set Up GitHub Project

1. Run the `setup-feedback-project.js` script:
   ```bash
   npm install @octokit/core @octokit/graphql
   # Update the script with your GitHub token
   node scripts/setup-feedback-project.js
   ```

2. Alternatively, create the project manually:
   - Go to the github/services repository
   - Click on Projects > New project
   - Create a project named "Partner Engagement Feedback Tracker"
   - Add custom fields for:
     - AVG Score (Number)
     - Partner (Single select)
     - Engagement Type (Single select)
     - Date Completed (Date)
   - Create views for:
     - AVG Score by Partner (Board layout)
     - AVG Score Timeline (Roadmap layout)
     - All Feedback (Table layout)

### 4. Set Up Dashboard (optional)

1. Create the docs/feedback-dashboard directory
2. Add the provided files:
   - `index.html` - Main dashboard page
   - `js/dashboard.js` - Dashboard functionality

3. Enable GitHub Pages:
   - Go to Repository Settings > Pages
   - Set the source to the main branch, /docs folder
   - Save the configuration

### 5. Create Labels

Create the following labels in the repository:
- `feedback` - For all feedback submissions
- `avg-excellent` - For AVG scores ≥ 4.5
- `avg-good` - For AVG scores ≥ 4.0
- `avg-average` - For AVG scores ≥ 3.0
- `avg-needs-attention` - For AVG scores < 3.0

### 6. Documentation

1. Add the documentation file:
   - `docs/partner-feedback-guide.md`

2. Share the guide with the Corps team and partners

## Verification

After implementation, verify the system works correctly:

1. Submit a test feedback issue
2. Verify the AVG score is calculated correctly
3. Check that the issue appears in the project
4. Confirm the dashboard displays data correctly (if implemented)
5. Test the reminder workflow using manual dispatch

## Maintenance

Regularly review and update the system:

1. Adjust the form fields as needed
2. Update partner and engagement type options
3. Refine the dashboard visualizations
4. Monitor and troubleshoot any issues

## Contact

For questions or issues with the implementation, contact @Johnaldy.
