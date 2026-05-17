DeviceCycle — Product Lifecycle Management
DeviceCycle is a comprehensive web application designed to manage the complete lifecycle of hardware devices within an organization. It replaces messy manual tracking systems (like outdated spreadsheets) with a clean, centralized dashboard that provides a full audit trail of every device from registration to decommissioning.

🎯 Key Features
Centralized Dashboard: A live overview of your entire device fleet, including total devices, active counts, firmware version distribution, and alerts for devices running outdated software.
 
Robust Device Management: Easily add, update, and decommission devices. Track essential details such as serial numbers, models, current status, and firmware versions.

Firmware Catalog: Manage and track available firmware versions. The system automatically detects and flags which devices are running outdated builds, ensuring compliance and security.

Comprehensive Change Logs: Every action taken on a device is automatically recorded with a precise timestamp. Whether a device is created, updated, changes status, receives a firmware upgrade, or is deleted, a full history is retained.

Real-time Notifications: An activity panel in the application header displays recent fleet events as they happen.

Role-Based Authentication: Secure JWT-based login system separating user privileges. Administrators can make modifications to the device fleet, while regular users are restricted to read-only access.


🛠️ Technology Stack
The project utilizes a modern, robust full-stack architecture, split into a single-page application frontend and a RESTful API backend.

Frontend (devicecycle-client)
Framework: React 18 built with Vite for fast development and optimized production builds.
Language: TypeScript for type-safe code.
Styling: Tailwind CSS, utilizing its utility-first approach and supporting dark mode aesthetics.
Data Fetching & State: TanStack Query v5 for efficient API data caching and synchronization.
Routing: React Router DOM (v6).
Data Visualization: Recharts for rendering dashboard analytics.
Icons: Lucide React.

Backend (DeviceCycle.Server)
Framework: ASP.NET Core 8 Web API.
ORM: Entity Framework Core 8 for data access.
Database: SQL Server.
Security: ASP.NET Identity combined with JWT (JSON Web Token) Bearer authentication for secure, stateless sessions.

📂 Project Architecture
The repository is structured into two main applications:

text
├── DeviceCycle.Server/     (Backend ASP.NET Core API)
│   ├── Controllers/        # API endpoints
│   ├── Models/             # Entity Framework Core models & DbContext
│   ├── Migrations/         # Database schema migrations
│   └── appsettings.json    # Connection strings and configuration
│
└── devicecycle-client/     (Frontend React Application)
    └── src/
        ├── api/            # Centralized API service calls
        ├── components/     # Reusable UI components
        ├── pages/          # Main views: Dashboard, Devices, Firmware, ChangeLogs, Login
        └── context/        # React Context providers for Auth and Theme
