# Enterprise User Management System

A comprehensive, multi-tenant user management platform built with React 18, featuring role-based access control, advanced analytics, and enterprise-grade architecture. This system demonstrates modern frontend development practices with a fully functional demo environment.

[![React](https://img.shields.io/badge/React-18.2+-61DAFB?style=flat&logo=react&logoColor=white)](https://reactjs.org/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-3.3+-38B2AC?style=flat&logo=tailwind-css&logoColor=white)](https://tailwindcss.com/)
[![Zustand](https://img.shields.io/badge/Zustand-4.4+-000000?style=flat&logo=zustand&logoColor=white)](https://zustand-demo.pmnd.rs/)
[![Vite](https://img.shields.io/badge/Vite-4.4+-646CFF?style=flat&logo=vite&logoColor=white)](https://vitejs.dev/)

---

## 🌟 Key Features

### 🔐 Authentication & Authorization
- **Role-Based Access Control (RBAC)**: Three-tier system (System Admin, Tenant Admin, User)
- **Session Management**: Persistent authentication with localStorage
- **Protected Routes**: Route-level access control based on user roles
- **Demo Credentials**: Ready-to-use test accounts for different roles

### 🏢 Multi-Tenant Architecture
- **Tenant Isolation**: Data separation between tenants using mock APIs
- **Tenant Onboarding**: Multi-step wizard for new tenant setup
- **Tenant Configuration**: Settings and preferences management
- **Global Tenant Management**: System admin oversight

### 👥 User Management
- **CRUD Operations**: Create, read, update, delete users via mock API
- **Role Assignment**: Role and privilege management
- **User Profiles**: Profile management with tabbed interface
- **Activity Tracking**: Mock user session and activity data

### 🏗️ Organization Management
- **Hierarchical Structure**: Parent-child organization relationships
- **Department Management**: Multi-level organizational hierarchies
- **Industry Categorization**: Organization classification
- **Contact Management**: Organization contact information

### ⚖️ Legal Entity Management
- **Entity Types**: Support for corporations, LLCs, partnerships, etc.
- **Compliance Tracking**: Monitor compliance status
- **Jurisdictional Management**: Multi-jurisdiction support

### 🛡️ Security & Privileges
- **Granular Permissions**: Privilege control system
- **Role Templates**: Pre-defined role configurations
- **Security Center**: Security monitoring interface
- **Privilege Categories**: Organized permission structures

### 📊 Analytics & Reporting
- **Chart.js Integration**: Interactive analytics dashboards
- **Data Visualizations**: User growth trends, role distributions, activity heatmaps
- **CSV Export**: Export functionality for user growth data
- **Role-specific Analytics**: Different dashboards per user role

### 🔧 System Administration
- **System Monitoring**: Health and performance tracking interface
- **API Management**: REST API endpoint management interface
- **Security Center**: Security event management
- **System Configuration**: Global system settings
- **Global Reports**: Cross-tenant reporting

### 🎨 User Experience
- **Responsive Design**: Mobile-first approach with Tailwind CSS
- **Loading States**: LoadingSpinner component with feedback
- **Error Handling**: ErrorBoundary implementation
- **Toast Notifications**: React Hot Toast integration

---

## 🛠️ Technology Stack

| Category | Technology | Version | Purpose |
|----------|------------|---------|---------|
| **Framework** | React | 18.2+ | Frontend framework |
| **Routing** | React Router | 6.8+ | Client-side routing |
| **State Management** | Zustand | 4.4+ | Global state management |
| **Styling** | Tailwind CSS | 3.3+ | Utility-first CSS framework |
| **Forms** | React Hook Form | 7.45+ | Form state management |
| **Charts** | Chart.js | 4.0+ | Data visualization |
| **Icons** | Lucide React | 0.263+ | Icon library |
| **Notifications** | React Hot Toast | 2.4+ | Toast notifications |
| **Build Tool** | Vite | 4.4+ | Build tool and dev server |

---

## 🚀 Quick Start

### Prerequisites
- **Node.js**: Version 16.x or higher
- **npm**: Version 8.x or higher (or yarn)

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd user-management-system
   ```

2. **Install dependencies**
   ```bash
   npm install
   # or
   yarn install
   ```

3. **Start the development server**
   ```bash
   npm run dev
   # or
   yarn dev
   ```

4. **Open your browser**
   Navigate to `http://localhost:5173`

### Build for Production
```bash
npm run build
npm run preview  # Preview production build locally
```

---

## 👤 Demo Credentials

The application includes three demo accounts showcasing different role capabilities:

| Role | Email | Password | Access Level |
|------|-------|----------|--------------|
| **System Administrator** | `admin@techcorp.com` | `admin123` | Global system management |
| **Tenant Administrator** | `sarah.manager@techcorp.com` | `manager123` | Tenant-specific management |
| **Regular User** | `mike.developer@techcorp.com` | `user123` | Personal profile and organization access |

---

## 📁 Project Structure

```
src/
├── components/                 # Reusable UI components
│   ├── charts/                # Data visualization components
│   │   └── AdvancedDataVisualization.jsx
│   ├── common/                # Shared components
│   │   └── LoadingSpinner.jsx
│   ├── layout/                # Layout components
│   │   ├── DashboardLayout.jsx
│   │   └── RoleBasedNavigation.jsx
│   └── modals/                # Modal components
│       ├── CreateOrganizationModal.jsx
│       ├── DeleteConfirmationModal.jsx
│       ├── EditOrganizationModal.jsx
│       └── TenantOnboardingWizard.jsx
├── hooks/                     # Custom React hooks
│   ├── useAnalytics.js
│   └── useAuth.js
├── pages/                     # Route-based page components
│   ├── dashboards/           # Role-specific dashboards
│   │   ├── SystemAdminDashboards.jsx
│   │   └── TenantAdminDashboard.jsx
│   ├── roles/                # Role management
│   │   └── RoleManagement.jsx
│   ├── system/               # System admin pages
│   │   ├── APIManagement.jsx
│   │   ├── GlobalReports.jsx
│   │   ├── GlobalUserManagement.jsx
│   │   ├── LegalEntityManagement.jsx
│   │   ├── PrivilegeManagement.jsx
│   │   ├── SecurityCenter.jsx
│   │   ├── SystemConfiguration.jsx
│   │   └── SystemMonitoring.jsx
│   ├── tenant/               # Tenant admin pages
│   │   ├── LegalEntityManagement.jsx
│   │   ├── Notifications.jsx
│   │   ├── OrganizationManagement.jsx
│   │   ├── PrivilegeManagement.jsx
│   │   ├── TenantReports.jsx
│   │   └── TenantSettings.jsx
│   ├── Dashboard.jsx
│   ├── LoginPage.jsx
│   ├── OrganizationManagement.jsx
│   ├── SystemUsersPage.jsx
│   ├── TenantManagement.jsx
│   └── UserPortal.jsx
├── services/                 # API services and mock data
│   ├── analyticsApi.js
│   ├── mockApi.js
│   └── systemAdminMockApi.js
├── store/                    # Zustand stores
│   └── authStore.js
├── App.jsx                   # Main application component
├── App.css                   # Global styles
├── index.css                 # Tailwind imports
└── main.jsx                  # Application entry point
```

---

## 🎯 Feature Implementation

### System Administrator Features
- **Global Tenant Management**: Tenant CRUD operations with onboarding wizard
- **System Analytics**: Dashboard with Chart.js visualizations
- **API Management**: Interface for API endpoint management
- **Security Center**: Security event monitoring interface
- **System Configuration**: Global settings management
- **System Monitoring**: Performance tracking interface

### Tenant Administrator Features
- **User Management**: User CRUD operations within tenant
- **Organization Management**: Hierarchical organization structure
- **Role Management**: Role and privilege assignment
- **Legal Entity Management**: Legal entity CRUD operations
- **Tenant Analytics**: Tenant-specific reporting dashboard
- **Tenant Settings**: Tenant configuration management

### User Features
- **User Portal**: Tabbed interface for personal management
- **Profile Management**: Personal profile editing
- **Organization View**: Access to organization information
- **Legal Entity Access**: View associated legal entities
- **Activity Tracking**: Personal activity monitoring
- **Security Settings**: Password and security preferences

---

## 🔧 Implementation Details

### State Management (Zustand)
- **Authentication Store**: Persistent auth state with localStorage
- **Role-based State**: User role and permission management
- **Session Persistence**: Automatic session restoration

### Routing (React Router v6)
- **Protected Routes**: Role-based route protection
- **Dynamic Navigation**: Role-specific navigation menus
- **Route Guards**: Access control implementation

### UI Components
- **Modal System**: Reusable modal patterns for CRUD operations
- **Loading States**: LoadingSpinner component for async operations
- **Error Boundaries**: ErrorBoundary class component in UserPortal
- **Toast Notifications**: React Hot Toast for user feedback

### Mock API Implementation
- **Realistic Data**: Mock data with relationships
- **Network Delays**: Simulated API response times
- **Error Simulation**: Mock error scenarios
- **CRUD Operations**: Full Create, Read, Update, Delete operations

---

## 📊 Analytics Implementation

### Chart.js Integration
- **User Growth Charts**: Line charts with real Chart.js implementation
- **Role Distribution**: Doughnut charts showing role breakdowns
- **Activity Heatmaps**: Custom heatmap visualization
- **Performance Metrics**: Real-time metric cards

### Export Features
- **CSV Export**: User growth data export functionality
- **Report Generation**: Template-based report creation

---

## 🔒 Security Implementation

### Authentication
- **Demo Credentials**: Email-based role detection in authStore
- **Session Management**: localStorage-based session persistence
- **Route Protection**: RoleProtectedRoute component implementation
- **Access Control**: Component-level permission checking

### Input Validation
- **Form Validation**: React Hook Form with validation rules
- **Error Handling**: Comprehensive error message display
- **Data Sanitization**: Input cleaning and validation

---

## 🚀 Deployment

### Build Configuration
```bash
# Build for production
npm run build

# Preview production build
npm run preview
```

### Static Hosting Ready
The application is configured for deployment to:
- Vercel
- Netlify  
- GitHub Pages
- Any static hosting platform

---

## ⚠️ Current Limitations

### What's NOT Implemented
- **Testing**: No unit tests, integration tests, or E2E tests
- **Real Backend**: Only mock APIs, no actual backend integration
- **Real-time Features**: No WebSocket or live updates
- **Advanced Security**: Basic client-side security only
- **Internationalization**: No multi-language support
- **Performance Monitoring**: No real analytics tracking

### Mock Data Only
- All data is stored in localStorage
- No real database integration
- API calls are simulated with timeouts
- No actual user authentication

---

## 🤝 Contributing

1. **Fork the repository**
2. **Create a feature branch**: `git checkout -b feature/amazing-feature`
3. **Commit your changes**: `git commit -m 'Add amazing feature'`
4. **Push to the branch**: `git push origin feature/amazing-feature`
5. **Open a Pull Request**

---

## 📞 Support

For questions and support:
- **Email**: deepanshik825@gmail.com
- **GitHub Issues**: For bug reports and feature requests

---

## 📄 License

This project is licensed under the MIT License.

---

<div align="center">

**Built with ❤️ for enterprise user management**

*A comprehensive demo showcasing modern React development patterns*

</div>
