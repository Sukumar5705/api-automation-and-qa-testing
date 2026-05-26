# Automation & QA Developer Assessment

This repository contains the completed submission for the Automation & QA Developer Take-Home Skills Assessment. The project focuses on web application QA testing, API integration, workflow automation using n8n, conditional logic handling, and notification-based monitoring workflows.

Assignment Reference: :contentReference[oaicite:0]{index=0}

---

# Repository Contents

| File | Description |
|---|---|
| `Task1_QA_Report_Sukumar.pdf` | QA testing report containing identified bugs, severity levels, and root-cause analysis |
| `Task2_Workflow_Sukumar.json` | Exported n8n workflow JSON for API automation and Telegram alert integration |
| `README.md` | Documentation for both tasks |
| `/screenshots` | Workflow execution screenshots and QA screenshots |

---

# Task 1 – Web App QA & Debug Report

## Application Tested
Conduit / RealWorld Demo Application

## Objective
The objective of Task 1 was to manually test a web application built using AI-assisted development tools and identify functional, UI/UX, validation, accessibility, and security-related issues.

Assignment Requirement Reference: :contentReference[oaicite:1]{index=1}

---

## Testing Scope

The following workflows were manually tested:

- User Registration
- Login
- Article Creation
- Article Interaction
- Navigation
- Logout Flow

---

## Major Issues Identified

### 1. Poor UI Readability
- Low text contrast reduced readability and accessibility.

### 2. Weak Password Validation
- Extremely weak passwords such as `12345` and `abc` were accepted.

### 3. Invalid Email Acceptance
- Malformed email addresses were accepted during registration.

### 4. Incorrect Focus Styling
- Entire containers received thick black borders on interaction.

### 5. Inconsistent UI Design
- Outdated visual hierarchy and inconsistent styling reduced usability.

Detailed report available in:
`Task1_QA_Report_Sukumar.pdf`

Report Reference: :contentReference[oaicite:2]{index=2}

---

## Root Cause Analysis

A detailed root-cause analysis was performed on the weak password validation issue. The analysis explains:
- why the issue occurs,
- potential security risks,
- frontend/backend validation gaps,
- recommended fixes.

Root Cause Section Reference: :contentReference[oaicite:3]{index=3}

---

# Task 2 – n8n API Integration Workflow

## Objective

The objective of Task 2 was to build an automated workflow in n8n that:
- fetches public API data,
- transforms and filters data,
- enriches results using a second API call,
- applies conditional logic,
- sends automated notifications,
- handles errors gracefully.

Assignment Requirement Reference: :contentReference[oaicite:4]{index=4}

---

# Workflow Overview

The workflow automates cryptocurrency market monitoring using CoinGecko APIs and Telegram notifications.

## Workflow Structure

```text
Schedule Trigger
      ↓
Get Top Crypto Coins
      ↓
Filter Top 5 Coins
      ↓
Get Bitcoin Details
      ↓
IF Condition (24h price drop threshold)
      ↓
Telegram Alert Notification
