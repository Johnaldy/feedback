# Partner Engagement Feedback System

A system for collecting, tracking, and analyzing customer feedback on partner-delivered engagements.

## Overview

This repository implements a feedback collection and analysis system using GitHub's native features:
- **Issue Templates** for structured feedback collection
- **GitHub Actions** for automatic CSAT calculation and processing
- **GitHub Projects** for visualization and analysis

## How It Works

1. Partners collect feedback from customers after engagements
2. Partners submit feedback using the standardized issue template
3. GitHub Actions automatically calculate CSAT scores and apply labels
4. Feedback data is visualized in the GitHub Project board
5. Weekly reminders are sent for outstanding feedback collection

## Getting Started

### For Partners Submitting Feedback

1. Go to [Submit New Feedback](https://github.com/johnaldy/partner_feedback/issues/new?template=partner-feedback.yml)
2. Fill out all required fields with the customer feedback data
3. Submit the issue

### For Team Members Analyzing Feedback

1. View all feedback in the [Issues tab](https://github.com/johnaldy/partner_feedback/issues?q=is%3Aissue+label%3Afeedback)
2. Use the [Project board](https://github.com/johnaldy/partner_feedback/projects) for visualization and analysis
3. Filter feedback by partner, engagement type, or CSAT score using labels

## Documentation

For detailed instructions on using this system, please see the [Partner Feedback Guide](docs/partner-feedback-guide.md).

## Implementation Details

This system uses the following GitHub features:
- Issue Templates
- GitHub Actions
- GitHub Projects
- GitHub Labels

## Contributing

If you have suggestions for improving this feedback system, please open an issue with the `enhancement` label.
