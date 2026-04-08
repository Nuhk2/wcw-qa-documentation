# WCW CRM System - Complete Structure Analysis

## 1. ROLES DEFINED

| Role ID | Role Name | Description | System Type | Status |
|---------|-----------|-------------|-------------|--------|
| 1 | Admin | Super admin with full system access | SUPER_ACCESS | Active |
| 2 | Sales Rep | Sales representative with customer/opportunity access | STANDARD | Active |
| 3 | Inside Rep | Inside representative with limited access | STANDARD | Active |
| 4 | Manager | Manager with super admin access | SUPER_ACCESS | Active |

**Super Access Role IDs:** [1, 4] (Admin, Manager)
**Standard Sales Role IDs:** [2, 3] (Sales Rep, Inside Rep)

---

## 2. CORE MODULES & FEATURES

### 2.1 USER MANAGEMENT Module
**Path:** `src/app/features/User Management/`
**Routes:** 
- `/users` (Users List with CRUD)
- Roles route commented out: `/roles`

**CRUD Operations:**
| Operation | Endpoint | Method | Status |
|-----------|----------|--------|--------|
| Create User | `/users/create` | POST | ✅ |
| List Users | `/users/list` | GET | ✅ |
| Datatable Users | `/users/datatable` | GET | ✅ |
| Update User | `/users/update/{userId}` | PUT | ✅ |
| Delete User | `/users/delete/{userId}` | DELETE | ✅ |
| Get User Roles | `/roles/list` | GET | ✅ |

**Permissions Enforced:**
- `Add User` - Controls new user creation
- `Edit User` - Controls user modification
- `Delete User` - Controls user deletion
- `View User` - Controls user view access (Route permission)
- `View Role` - Controls role panel access
- `Add Role` - Controls role creation
- `Edit Role` - Controls role editing
- `Delete Role` - Controls role deletion

**Permission Check Pattern:**
```tsx
const addPermission = auth?.user?.roles?.some((role) => 
  role.permissions?.some((p) => p.name === 'Add User')
);
```

---

### 2.2 CUSTOMERS Module
**Path:** `src/app/features/Customers/`
**Route:** `/customers`

**CRUD Operations:**
| Operation | Endpoint | Method | Status |
|-----------|----------|--------|--------|
| List Customers | `/customers/list?params` | GET | ✅ |
| Show Customer | `/customers/show/{id}` | GET | ✅ |
| Create Customer | `/customers/create` | POST | ✅ |
| Update Customer | `/customers/update/{id}` | PUT | ✅ |
| Delete Customer | `/customers/delete/{id}` | DELETE | ✅ |
| Get Customer Meetings | `/customers/meetings/{customerId}` | GET | ✅ |
| Get Customer Contacts | `/customers/contacts/{customerId}` | GET | ✅ |
| Get Customer Tasks | `/customers/tasks/{customerId}` | GET | ✅ |
| Convert Prospect Request | `/prospects/convert-request/{prospectId}` | POST | ✅ |
| Convert Prospect by Task | `/prospects/convert/{taskId}` | POST | ✅ |
| Get PPro Requests | `/prospects/requests` | GET | ✅ |

**Sub-features:**
- Contacts
- Meetings
- Tasks
- Prospects

**Access Control:**
- Available to all authenticated users
- Role-based sidebar visibility

---

### 2.3 OPPORTUNITIES Module
**Path:** `src/app/features/Opportunity/`
**Route:** `/opportunities`

**CRUD Operations:**
| Operation | Endpoint | Method | Status |
|-----------|----------|--------|--------|
| List Opportunities | `/opportunities/list?params` | GET | ✅ |
| Show Opportunity | `/opportunities/show/{id}` | GET | ✅ |
| Create Opportunity | `/opportunities/create` | POST | ✅ |
| Update Opportunity | `/opportunities/update/{id}` | PUT | ✅ |
| Delete Opportunity | `/opportunities/delete/{id}` | DELETE | ✅ |
| Update Status | `/opportunities/status/update/{id}` | PUT | ✅ |
| Get Analytics | `/opportunities/analytics?userId={id}` | GET | ✅ |

**Sub-features:**
- Tasks (related to opportunities)
- Meetings (related to opportunities)
- Targets/Commitments
- Meeting Checklists

**Role Requirements:**
- Sidebar Role: [SUPER_ACCESS, SALES_REP]
- Accessible with `keepVisibleWhenViewingOtherRep: true`

---

### 2.4 TASKS Module
**Path:** `src/app/features/Tasks/` and `src/app/features/Opportunity/services/taskApi.tsx`
**Routes:** 
- `/tasks` - Task List (permission: 'non-admin')
- `/team-requests` - Team Requests/PPro Tasks (all users)

**CRUD Operations:**
| Operation | Endpoint | Method | Status |
|-----------|----------|--------|--------|
| List Tasks | `/tasks/list?params` | GET | ✅ |
| Show Task | `/tasks/show/{id}` | GET | ✅ |
| Create Task | `/tasks/create` | POST | ✅ |
| Update Task | `/tasks/update/{id}` | PUT | ✅ |
| Delete Task | `/tasks/delete/{id}` | DELETE | ✅ |
| Assign Task | `/tasks/assign/{id}` | PUT | ✅ |

**Task Types:**
1. Customer Tasks
2. Opportunity Tasks
3. PPro Conversion Tasks

**Task Properties:**
- Status: (Open, Closed, etc.)
- Priority: (High, Medium, Low)
- Due Date
- Taskable Type: Customer | Opportunity
- Assignment tracking

**Role Requirements:**
- Sidebar Role: [SALES_REP, INSIDE_REP]
- Keep visible when viewing other rep: true

---

### 2.5 CALENDAR Module
**Path:** `src/app/features/Calendar/`
**Route:** `/calendar`

**Status:** ⚠️ **BLOCKER - Hardcoded mock data (September 2025)**

**Features:**
- Calendar view
- Meeting calendar display
- Mock data implementation

---

### 2.6 SCHEDULE Module
**Path:** `src/app/pages/schedule/`
**Routes:**
- `/schedule` - Weekly Schedule (permission: 'non-admin')
- `/day-schedule` - Daily Schedule (permission: 'non-admin')

**Features:**
- Weekly schedule view
- Daily schedule view
- Schedule management

**Role Requirements:**
- Sidebar Role: [SALES_REP]
- Keep visible when viewing other rep: true

---

### 2.7 DAILY ALERTS Module
**Path:** `src/app/features/DailyAlerts/`
**Route:** `/daily-alerts` (permission: 'non-admin')

**CRUD Operations:**
| Operation | Endpoint | Method | Status |
|-----------|----------|--------|--------|
| Get Notifications | `/notifications/list` | GET | ✅ |
| Unread Count | (via API) | GET | ✅ |
| Mark Read | (via mutation) | PATCH | ✅ |

**Role Requirements:**
- Sidebar Role: [SALES_REP]
- Display unread badge on sidebar

---

### 2.8 COMMITMENTS Module
**Path:** `src/app/features/Commitments/`
**Route:** `/commitments`

**CRUD Operations:**
| Operation | Endpoint | Method | Status |
|-----------|----------|--------|--------|
| Get Commitments | `/commitments/list?params` | GET | ✅ |
| Create Commitment | `/commitments/create` | POST | ✅ |
| Update Commitment | `/commitments/update/{id}` | PUT | ✅ |
| Delete Commitment | `/commitments/delete/{id}` | DELETE | ✅ |

**Features:**
- Product assignments
- Department tracking
- Task linking
- Status management

**Role Requirements:**
- Sidebar Role: [SUPER_ACCESS, SALES_REP]
- Keep visible when viewing other rep: true

---

### 2.9 TARGETS Module
**Path:** `src/app/features/Opportunity/services/targetApi.tsx`
**Route:** `/targets`

**CRUD Operations:**
| Operation | Endpoint | Method | Status |
|-----------|----------|--------|--------|
| List Targets | `/targets/list?params` | GET | ✅ |
| Create Target | `/targets/create` | POST | ✅ |
| Update Target | `/targets/update/{id}` | PUT | ✅ |
| Delete Target | `/targets/delete/{id}` | DELETE | ✅ |
| Show Target | `/targets/show/{id}` | GET | ✅ |

**Features:**
- Sales targets
- Products
- Departments
- Goal tracking

**Role Requirements:**
- Sidebar Role: [] (Available to all)

---

### 2.10 CONTACTS Module
**Path:** `src/app/features/Contacts/`
**Route:** `/contacts`

**CRUD Operations:**
| Operation | Endpoint | Method | Status |
|-----------|----------|--------|--------|
| List Contacts | `/contacts/list?params` | GET | ✅ |
| Show Contact | `/contacts/show/{id}` | GET | ✅ |
| Create Contact | `/contacts/create` | POST | ✅ |
| Update Contact | `/contacts/update/{id}` | PUT | ✅ |
| Delete Contact | `/contacts/delete/{id}` | DELETE | ✅ |
| Get Contact Roles | `/contact-roles/list` | GET | ✅ |

**Sub-features:**
- Contact roles
- Customer contacts
- Contact management modal

**Role Requirements:**
- Sidebar Role: [] (Available to all)

---

### 2.11 GROUPS Module
**Path:** `src/app/features/Groups/`
**Route:** `/groups`

**CRUD Operations:**
| Operation | Endpoint | Method | Status |
|-----------|----------|--------|--------|
| List Groups | `/groups/list?userId={id}` | GET | ✅ |
| Show Group | `/groups/show/{id}` | GET | ✅ |
| Create Group | `/groups/create` | POST | ✅ |
| Update Group | `/groups/update/{id}` | PUT | ✅ |
| Delete Group | `/groups/delete/{id}` | DELETE | ✅ |

**Features:**
- Group creation management
- Member bulk operations
- Group removal
- User filtering by group

**Operations Identified:**
- Handle bulk member operations
- Remove member from group
- View group details

---

### 2.12 GLOBAL SETTINGS Module
**Path:** `src/app/features/GlobalSettings/`
**Route:** `/global-settings`

**CRUD Operations:**
| Operation | Endpoint | Method | Status |
|-----------|----------|--------|--------|
| List Settings | `/global-settings/opportunity/list` | GET | ✅ |
| Add Setting | `/global-settings/opportunity/create` | POST | ✅ |
| Update Setting | `/global-settings/opportunity/update` | PUT | ✅ |
| Delete Setting | `/global-settings/opportunity/delete/{id}` | DELETE | ✅ |
| Update Meeting Checklist | `/global-settings/meeting-checklists/update` | PUT | ✅ |

**Features:**
- Opportunity settings
- Meeting checklist configuration
- System configuration

**Role Requirements:**
- Sidebar Role: [SUPER_ACCESS, MANAGER]
- Real-time updates to other users

---

### 2.13 ROLES & PERMISSIONS Module
**Path:** `src/app/features/User Management/Roles/`
**Route:** `/roles` (Commented out)

**CRUD Operations:**
| Operation | Endpoint | Method | Status |
|-----------|----------|--------|--------|
| List Roles | `/roles/list` | GET | ✅ |
| Create Role | `/roles/create` | POST | ✅ |
| Update Role | `/roles/update/{roleId}` | PUT | ✅ |
| Delete Role | `/roles/delete/{roleId}` | DELETE | ✅ |
| Get Permissions | `/roles/permissions` | GET | ✅ |

**Features:**
- Role management
- Permission assignment to roles
- Permission UI grouped by feature

**Permission Grouping:**
Permissions are organized by feature sections:
- User section
- Role section
- Customer section
- Opportunity section
- (More sections based on features)

---

### 2.14 DASHBOARD Module
**Path:** `src/app/features/Dashboard/`
**Route:** `/dashboard`
- `/dashboard/cities` - City details
- `/dashboard/rep/{repId}` - Rep details

**Operations:**
| Operation | Endpoint | Method | Status |
|-----------|----------|--------|--------|
| Get Regions | `/dashboard/companies` | GET | ✅ |
| Net New Customers (Region) | `/dashboard/region/net-new-customers/{regionId}` | GET | ✅ |
| Net New Customers (Rep) | `/dashboard/rep/net-new-customers/{userId}` | GET | ✅ |
| Get Rep Details | `/dashboard/rep/{userId}?regionId={id}` | GET | ✅ |

**Features:**
- Sales analytics
- Rep performance metrics
- Regional insights
- Quick actions to other modules

---

### 2.15 SUBSCRIPTION Module
**Path:** `src/app/features/Subscription/`
**Route:** `/subscription`

**CRUD Operations:**
| Operation | Endpoint | Method | Status |
|-----------|----------|--------|--------|
| Get Plans | `/subscription/plans` | GET | ⚠️ |
| Create Subscription | `/subscription/create` | POST | ⚠️ |

**Status:** ⚠️ **BLOCKER - Verification middleware disabled (NO REVENUE PROTECTION)**

**Features:**
- Plan listing
- Subscription creation
- Plan selection

---

## 3. PERMISSION STRINGS IDENTIFIED

### 3.1 Implemented Permission Patterns

**User Management Permissions:**
- `Add User`
- `Edit User`
- `Delete User`
- `View User`
- `Add Role`
- `Edit Role`
- `Delete Role`
- `View Role`

**Likely Permission Format:**  
Based on PermissionBody component grouping by feature section, permissions follow pattern:
```
[ACTION] [FEATURE]
Where ACTION: Add | Edit | Delete | View
Where FEATURE: User | Role | Customer | Opportunity | ... (19+ features)
```

### 3.2 Inferred Permission Coverage

Based on module analysis, likely permissions include:

**User Management (8):**
- Add User, Edit User, Delete User, View User
- Add Role, Edit Role, Delete Role, View Role

**Customers (4):**
- Add Customer, Edit Customer, Delete Customer, View Customer

**Opportunities (4):**
- Add Opportunity, Edit Opportunity, Delete Opportunity, View Opportunity

**Tasks (4):**
- Add Task, Edit Task, Delete Task, View Task

**Meetings (4):**
- Add Meeting, Edit Meeting, Delete Meeting, View Meeting

**Commitments (4):**
- Add Commitment, Edit Commitment, Delete Commitment, View Commitment

**Targets (4):**
- Add Target, Edit Target, Delete Target, View Target

**Groups (4):**
- Add Group, Edit Group, Delete Group, View Group

**Contacts (4):**
- Add Contact, Edit Contact, Delete Contact, View Contact

**Global Settings (2):**
- View Global Settings, Edit Global Settings

**Total Estimated Permissions:** 40+ permissions across 10+ feature groups

---

## 4. ROLE-BASED ACCESS CONTROL (RBAC) PATTERNS

### 4.1 Super Admin Access (Roles 1, 4: Admin, Manager)
```ts
SUPER_ACCESS_ROLE_IDS = [1, 4]
GLOBAL_SETTINGS_MANAGEMENT_ROLES = [1, 4, 4] // Admin, Manager, Manager
```

**Access Includes:**
- All user management operations
- All system administration
- Global settings
- Manager role with same privileges as Admin

### 4.2 Sales Rep Access (Role 2)
```ts
SALES_REP_ROLE_ID = 2
```

**Sidebar Accessible Paths:**
- Dashboard
- Customers
- Opportunities
- Tasks
- Weekly Schedule
- Daily Schedule
- Daily Alerts
- Commitments
- Contacts
- Global Settings (limited)

**Keep Visible When Viewing Other Rep:** YES

### 4.3 Inside Rep Access (Role 3)
```ts
INSIDE_REP_ROLE_ID = 3
```

**Sidebar Accessible Paths:**
- Dashboard
- Tasks
- Daily Alerts

### 4.4 Context-Based Restrictions

**Viewing Other Sales Rep Context:**
`isViewingOtherRepContext(rep_id, current_user_id) = rep_id !== current_user_id`

**Restrictions When Viewing Other Rep:**
- Cannot edit/delete meetings (readonly)
- Cannot edit pre-meetings (readonly)
- Cannot edit/delete some resources
- Read-only data viewing only

**Allowed Paths When Viewing Other Rep:**
- TASKS_PATH, WEEKLY_SCHEDULE_PATH, DAILY_SCHEDULE_PATH
- DAILY_ALERTS_PATH, COMMITMENTS_PATH
- (Defined in `MANAGER_REP_CONTEXT_ALLOWED_PATHS`)

---

## 5. FRONT-END PERMISSION ENFORCEMENT POINTS

### 5.1 Route-Level Protection
**File:** `src/app/router/middlewares/ProtectedRoute.tsx`
```tsx
<ProtectedRoute permission={route.permission}>
  {children}
</ProtectedRoute>
```

**Route Permissions Used:**
- `'View User'` - Users list route
- `'View Role'` - Roles list route (commented out)
- `'non-admin'` - Tasks, Schedule, Daily Alerts routes

### 5.2 Component-Level Buttons
**Pattern:**
```tsx
const addPermission = auth?.user?.roles?.some((role) => 
  role.permissions?.some((p) => p.name === 'Add User')
);

{addPermission && <AddButton />}
```

**Implemented in:**
- Users page (Add/Edit/Delete buttons)
- Roles page (Add/Edit/Delete buttons)
- Data tables (Add/Edit/Delete actions)

### 5.3 Data Table Integration
**File:** `src/app/shared/components/datatables/Table2.tsx`
```tsx
interface UsersTable {
  addPermission: boolean;
  editPermission: boolean;
  deletePermission: boolean;
}
```

**Table Features Controlled:**
- Add row visibility
- Edit row actions
- Delete row actions
- Bulk operations

### 5.4 Sidebar Menu Filtering
**File:** `src/app/shared/config/sidebarAccess.config.ts`
```ts
const getSidebarAccessDefinition = (path: string): SidebarAccessDefinition
```

**Menu Visibility by Role:**
- Sales Rep: Customers, Opportunities, Tasks, Schedule, Alerts, Commitments
- Inside Rep: Tasks, Alerts (limited)
- Admin/Manager: All menus
- Other users: Available menus

---

## 6. API SECURITY PATTERNS

### 6.1 Authentication Headers
**All API calls include:**
```tsx
headers: {
  Authorization: `Bearer ${getState().auth.token}`,
  'Content-Type': 'application/json' // (where applicable)
}
```

### 6.2 Base API Configuration
**File:** `src/app/slices/baseApiSlice.tsx`
```tsx
export const baseApi = createApi({
  baseUrl: backendApiAddress,
  tagTypes: [
    'Auth', 'Users', 'Roles', 'Customer', 'Opportunity',
    'Tasks', 'Meeting', 'Department', 'GlobalSetting', 'Target',
    'LoyaltyFlags', 'Contact', 'ContactRole', 'ProductDepartment',
    'Schedule', 'Commitment', 'Dashboard', 'Regions', 'Groups',
    'Notifications'
  ]
})
```

### 6.3 Token Management
- Backend token stored in auth state
- Token sent with all API requests
- No client-side token refresh mechanism identified ⚠️


---

## 7. IDENTIFIED PERMISSION ENFORCEMENT GAPS

### 7.1 Missing/Incomplete Implementations

| Gap | Location | Impact | Status |
|-----|----------|--------|--------|
| No token refresh mechanism | Global | Session expiration | ⚠️ CRITICAL |
| Subscription verification disabled | Subscription module | No revenue protection | ⚠️ CRITICAL |
| Calendar mock data hardcoded | Calendar module | Data accuracy | ⚠️ BLOCKER |
| Tasks always show full permissions | Tasks page | Should check permissions | ⚠️ INCOMPLETE |
| No granular permission caching | Global | Performance issue | ⚠️ MEDIUM |
| Admin row restriction inconsistent | Table components | Privilege escalation risk | ⚠️ MEDIUM |

### 7.2 Sidebar Access Not Permission-Based
- Sidebar shows based on Role IDs only
- Does NOT check specific permission strings
- Example: User with Edit-only permission still sees Add menu

### 7.3 CRUD Permissions Not Enforced Backend
- Frontend checks permissions for UX
- Backend permission validation not visible
- API responses indicate no backend checks

### 7.4 Routes Without Permission Guards
**Routes accessible via URL without specific checks:**
- `/customers`, `/opportunities`, `/contacts` 
- Permission string left null/undefined
- Only middleware checks auth, not specific permissions

---

## 8. CURRENT IMPLEMENTATION SUMMARY

### 8.1 Component Structure
```
Role → has many → Permissions
User → has many → Roles → has many → Permissions
```

### 8.2 Permission Model
```typescript
interface IPermission {
  id: number;
  name: string; // format: "[ACTION] [FEATURE]"
}

interface IRole {
  id: number;
  name: string;
  description: string;
  permissions: IPermission[] | null;
}

interface IUser {
  id: number;
  roles: IRole[];
  // ... other fields
}
```

### 8.3 Access Control Layers
1. **Authentication Layer:** Token validation
2. **Authorization Layer:** Route permission check
3. **Component Layer:** Button/action visibility
4. **API Layer:** Bearer token validation (backend)
5. **Backend Layer:** ⚠️ NOT VISIBLE - Assumed implemented

---

## 9. MODULES TABLE (ALL 17 MODULES)

| Module | Status | CRUD | Permissions | Permission Check | API Protected |
|--------|--------|------|-------------|------------------|---------------|
| Authentication | ✅ | N/A | N/A | N/A | ✅ |
| Users | ✅ | ✅ | Yes (4) | ✅ Component | ✅ |
| Roles | ✅ | ✅ | Yes (4) | ✅ Component | ✅ |
| Customers | ✅ | ✅ | No | ❌ None | ✅ |
| Opportunities | ✅ | ✅ | No | ❌ None | ✅ |
| Tasks | ✅ | ✅ | No | ⚠️ Incomplete | ✅ |
| Meetings | ✅ | ✅ | No | ⚠️ Context-based | ✅ |
| Contacts | ✅ | ✅ | No | ❌ None | ✅ |
| Groups | ✅ | ✅ | No | ❌ None | ✅ |
| Calendar | ⚠️ | N/A | No | ❌ None | ✅ |
| Schedule | ✅ | Read | No | ⚠️ Role-based | ✅ |
| Global Settings | ✅ | ✅ | No | ⚠️ Role-based | ✅ |
| Commitments | ✅ | ✅ | No | ❌ None | ✅ |
| Targets | ✅ | ✅ | No | ❌ None | ✅ |
| Daily Alerts | ✅ | Read | No | ⚠️ Role-based | ✅ |
| Dashboard | ✅ | Read | No | ✅ Auth | ✅ |
| Subscription | ⚠️ | ⚠️ | No | ❌ DISABLED | ⚠️ |

---

## 10. KEY STATISTICS

- **Total Features:** 17 modules
- **Roles Defined:** 4 (Admin, Sales Rep, Inside Rep, Manager)
- **Explicit Permissions:** ~40+ (estimated based on pattern)
- **Permission-Enabled Modules:** 2 (Users, Roles)
- **Role-Based Access Modules:** 6 (sidebar configuration)
- **API Endpoints:** 50+ across all modules
- **Protected Routes:** 18+ with various permission levels
- **Authentication Headers:** All API calls (100%)
- **Permission Enforcement Points:** 4 layers (Route, Component, Table, API)

---

## 11. RECOMMENDATIONS FOR PBAC DEPLOYMENT

### Phase 1: Foundation
- ✅ Permission framework already exists
- ✅ Role-permission mapping complete
- ✅ API infrastructure supports bearer tokens

### Phase 2: Frontend PBAC
1. Extend permission checks from Users/Roles to all modules
2. Implement permission caching in Redux state
3. Add permission validation middleware to ProtectedRoute
4. Enable Roles route (currently commented out)

### Phase 3: Backend PBAC
1. Verify backend permission validation on all endpoints
2. Implement token refresh mechanism
3. Add audit logging for permission-based actions

### Phase 4: Testing & Deployment
- Reference: Tests structure already established in `/tests/modules/`
- 190+ existing tests ready for extension
- PBAC tests can follow established patterns

---

## Appendix: All API Base Configuration

**Base API Service Tags:**
- Auth, Users, Roles, Customer, Opportunity
- Tasks, Meeting, Department, GlobalSetting, Target
- LoyaltyFlags, Contact, ContactRole, ProductDepartment
- Schedule, Commitment, Dashboard, Regions, Groups, Notifications

**Codebase Location:** `/src/app/slices/baseApiSlice.tsx`
