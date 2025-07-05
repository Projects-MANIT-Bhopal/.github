# Yogananda1504-group: Attendance Management & Report Generation System .(ATM-RGS)

## Overview

This group contains a suite of interconnected projects that together form a comprehensive attendance reporting system. The system allows for efficient tracking, processing, and visualization of attendance data.

| Project | Description | Type |
|---------|-------------|------|
| [Attendance Backend](#attendance-backend) | Backend for capturing and storing attendance data | Backend |
| [Attendance Input Taking](#attendance-input-taking) | Frontend for capturing attendance data | Frontend |
| [AttendanceReport2](#attendancereport2) | Backend service for attendance report generation | Backend |
| [Frontend-ReportGeneration](#frontend-reportgeneration) | User interface for the attendance reporting system | Frontend |
| [MCP_ATMS](#mcp_atms) | MCP Server that interfaces with the attendance report system | Server |
| [gitlab-profile](#gitlab-profile) | Group profile configuration | Configuration |

## System Architecture

```
                                ┌──────────────────┐
                                │  MongoDB Database│
                                └───────┬───┬──────┘
                                        │   │
                  ┌───────────────────┐ │   │ ┌───────────────────┐
                  │ Attendance Backend│◄┘   └►│ AttendanceReport2 │
                  │        ▲          │       │     (Backend)     │
                  └────────┼──────────┘       └─────────┬─────────┘───┐
                           │                            │             │
┌────────────────────┐     │                   ┌────────┴────────┐    │
│ Attendance Input   │◄────┘                   │  MCP_ATMS Server│    │
│ Taking (Frontend)  │                         │  (Report Based) │    │ 
└────────────────────┘                         └────────┬────────┘    │
                                                        │             │
                                                        ▼             ▼
                                ┌─────────────────────────────────────┐
                                │     Frontend-ReportGeneration       │
                                └─────────────────────────────────────┘
```

## Project Details

### Attendance Backend

Backend system responsible for capturing and storing attendance data. This component handles the actual attendance-taking process, including check-ins, absences, and related data. It directly interacts with the MongoDB database for storing raw attendance data.

**Key Features:**
- Attendance tracking and recording
- User authentication for attendance
- Absence management
- Real-time attendance data collection
- MongoDB database operations for attendance data

### Attendance Input Taking

Frontend application for capturing attendance data from users. This component provides the interface for check-ins, check-outs, and other attendance-related actions.

**Key Features:**
- User-friendly check-in/check-out interface
- Authentication for attendance verification
- Real-time status updates
- Leave application interface
- Mobile-responsive design for field use

### AttendanceReport2

Backend service responsible for processing and generating attendance reports based on data from the MongoDB database. This component handles all report processing, calculations, and report generation logic.

**Key Features:**
- Data processing and aggregation from MongoDB
- Report generation algorithms
- API endpoints for frontend access
- Advanced database queries and analytics

### Frontend-ReportGeneration

The MANT's own Report Generation Software for the Attendance system. This is the user interface that allows users to interact with the attendance reporting system.

**Key Features:**
- User-friendly interface for generating reports
- Visual representations of attendance data
- Filtering and customization options
- Responsive design for multiple devices

### MCP_ATMS

MCP Server for the Attendance Report 2 system. This server component manages communication between different parts of the system and handles various server-side operations on basis of of processed NLP Queries by a LLM Model. It also interfaces with the Attendance Input Taking frontend.



### gitlab-profile

Configuration and profile settings for the group.

## Getting Started

To get started with the attendance reporting system:

1. Set up MongoDB database
2. Deploy the Attendance Backend for data collection
3. Set up the MCP_ATMS server component
4. Deploy the AttendanceReport2 backend service
5. Configure and launch the Frontend-ReportGeneration interface
6. Configure and launch the Attendance Input Taking interface
7. Connect all components using the provided configuration settings

For detailed setup instructions, refer to each project's individual README file.

## Development

Each project follows its own development workflow. 

