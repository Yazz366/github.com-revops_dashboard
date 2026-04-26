# github.com-revops_dashboard
Dashboard originally built as a Claude Artifact, now hosted on GitHub.
# Stllr RevOps Dashboard

A lightweight, browser-based Revenue Operations (RevOps) dashboard designed to track UGC production, brand pipelines, and team operations across daily, weekly, and quarterly levels.

Built as a single HTML application with no backend required.

---

## Overview

The Stllr RevOps Dashboard centralizes:

- Brand-level production tracking  
- Content pipeline visibility (from briefing to posting)  
- Task and team management  
- Weekly to quarterly rollups  
- Video credit tracking per brand  

It mirrors internal Google Sheets workflows while adding structured visualization, automation logic, and improved usability.

---

## Core Modules

### Daily Ops (Main View)
- Spreadsheet-style interface (Stage × Brand)
- Tracks content production stages:
  - Posted on social
  - Remixed
  - Approved
  - Pending approval
  - Reshooting / editing
  - Filming
  - Scripting
  - Shipment
  - Creative direction setup
  - Creator onboarding
  - No creator
  - No brief

Primary use: day-to-day production tracking and pipeline visibility.

---

### Task Board
- Kanban-style task management
- Columns:
  - Pending
  - In Progress
  - Blocked
  - Done
- Includes:
  - Priority (High / Normal / Low)
  - Due dates
  - Assigned account manager
  - Notes

Primary use: operational execution and follow-ups.

---

### Weekly Rollup
- Aggregated data from completed weeks
- Stage distribution analysis
- Week-over-week comparison

---

### Monthly and Quarterly Rollups
- Performance trends over time
- Pipeline health visibility
- Production velocity insights

---

### Brand Video Credit Report
Tracks:
- Active videos
- Credit videos
- Total allocation

Primary use: monitor delivery versus commitments and utilization.

---

### RevOps Report
- High-level performance overview
- Combines pipeline metrics, stage distribution, and brand performance

---

### Archive System
- Completed weeks become read-only
- Used as the data source for rollups
- Can be reopened if needed

---

## Key Features

### Week Management
- Create new weeks
- Clone structure from previous week
- Rename and delete weeks
- Mark weeks as completed
- Automatic labeling (e.g. W17 Apr 21)

---

### Brand Management
Each brand includes:
- Account manager (AM)
- Solution type:
  - PREMIER
  - PAYG
  - INFLUENCERS
- Status:
  - On track
  - At risk
  - Blocked
- Video metrics:
  - Active
  - Credit
  - Total

---

### Pipeline Tracking
- Visual pipeline representation
- Stage-level aggregation
- Conversion visibility across stages

---

### Export Functionality
- Export selected weeks
- CSV download
- Multi-week selection support

---

### Dark Mode
- Toggle between light and dark themes
- Preference stored locally

---

### Local Storage Persistence
All data is stored in the browser:
- Weeks
- Archived weeks
- Active week state
- UI preferences

No backend or database is required.

---

## Data Structure

### Week Object
```json
{
  "id": "string",
  "label": "W16 Apr 14",
  "year": 2026,
  "weekNum": 16,
  "completed": false,
  "brands": [],
  "tasks": []
}
