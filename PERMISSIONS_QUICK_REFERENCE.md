# WCW CRM - Role & Permission Quick Reference Matrix
## One-Page Permission Summary

**Status:** Ready for PBAC Migration  
**Effective Date:** April 8, 2026

---

## Quick Legend
| Symbol | Meaning |
|--------|---------|
| ✅ | Full Access / Works |
| 🟠 | Partial / Conditional |
| ❌ | No Access / Restricted |
| 🔴 | Not Implemented |

---

## PERMISSION MATRIX - All Features by Role

### DASHBOARD & NAVIGATION

| Feature | Admin | Manager | Sales Rep | Inside Rep | Status |
|---------|-------|---------|-----------|-----------|--------|
| View Dashboard | ✅ All Data | ✅ Team Data | 🟠 Own Region | ✅ All Regions | ✅ |
| Filter Dashboard | ✅ All Regions | ✅ Team | 🟠 Own Only | ✅ All Regions | ✅ |
| Access Settings | ✅ All | ❌ | ❌ | ❌ | 🟠 |
| View Navigation Menu | ✅ All Items | ✅ Most Items | 🟠 Filtered | 🟠 Filtered | ✅ |
| Manage Global Settings | ✅ Yes | ❌ | ❌ | ❌ | 🟠 |

---

### CUSTOMER MANAGEMENT

| Feature | Admin | Manager | Sales Rep | Inside Rep | Status |
|---------|-------|---------|-----------|-----------|--------|
| **View Customers** |
| - List View | ✅ All | ✅ Team | ✅ Own | ✅ All | ✅ |
| - Detail View | ✅ Any | ✅ Team | ✅ Own | ✅ All | ✅ |
| **Create Customer** | ✅ | ✅ | ✅ | ✅ | ✅ |
| **Edit Customer** | ✅ Any | ✅ Any | ✅ Own Only | ✅ Any | ✅ |
| **Delete Customer** | ✅ | ✅ | ✅ Own Only | ✅ | ✅ |
| **Search/Filter** | ✅ All Data | ✅ Team Data | 🟠 Own Data | ✅ All Data | ✅ |

---

### CONTACT MANAGEMENT

| Feature | Admin | Manager | Sales Rep | Inside Rep | Status |
|---------|-------|---------|-----------|-----------|--------|
| **View Contacts** |
| - List View | ✅ All | ✅ Team | ✅ Customer's/Target's | ✅ All | ✅ |
| - Detail View | ✅ Any | ✅ Team | ✅ Own Customer/Target | ✅ All | ✅ |
| **Create Contact** | ✅ | ✅ | ✅ | ✅ | ✅ |
| **Edit Contact** | ✅ Any | ✅ Any | ✅ Own | ✅ Any | ✅ |
| **Delete Contact** | ✅ | ✅ | ✅ Own | ✅ | ✅ |

---

### OPPORTUNITY MANAGEMENT

| Feature | Admin | Manager | Sales Rep | Inside Rep | Status |
|---------|-------|---------|-----------|-----------|--------|
| **View Opportunities** |
| - List View | ✅ All | ✅ Team | ✅ Own | ✅ All | ✅ |
| - Pipeline View | ✅ All | ✅ Team | ✅ Own | ✅ All | ✅ |
| **Create Opportunity** | ✅ | ✅ | ✅ | ✅ | ✅ |
| **Edit Opportunity** | ✅ Any | ✅ Any | ✅ Own Only | ✅ Any | ✅ |
| **Mark Won/Lost** | ✅ | ✅ | ✅ | ✅ | ✅ |
| **Delete Opportunity** | ✅ | ✅ | ✅ Own | ✅ | ✅ |

---

### TASK MANAGEMENT

| Feature | Admin | Manager | Sales Rep | Inside Rep | Status |
|---------|-------|---------|-----------|-----------|--------|
| **View Tasks** | ✅ All | ✅ Team + Own | ✅ Own | ✅ All | ✅ |
| **Create Task** | ✅ | ✅ | ✅ | ✅ | ✅ |
| **Edit Task** | ✅ Any | ✅ Team + Own | ✅ Own | ✅ Any | ✅ |
| **Complete Task** | ✅ | ✅ | ✅ | ✅ | ✅ |
| **Delete Task** | ✅ | ✅ | ✅ Own | ✅ | ✅ |

---

### COMMITMENT MANAGEMENT

| Feature | Admin | Manager | Sales Rep | Inside Rep | Status |
|---------|-------|---------|-----------|-----------|--------|
| **View Commitments** | ✅ All | ✅ Team | ✅ Own | ✅ All | ✅ |
| **Create Commitment** | ✅ | ✅ | ✅ | ✅ | ✅ |
| **Edit Commitment** | ✅ Any | ✅ Team | ✅ Own | ✅ Any | ✅ |
| **Mark Completed** | ✅ | ✅ | ✅ | ✅ | ✅ |

---

### CALENDAR & SCHEDULE

| Feature | Admin | Manager | Sales Rep | Inside Rep | Status |
|---------|-------|---------|-----------|-----------|--------|
| **View Calendar** | 🟠 Mock Data | 🟠 Mock Data | 🟠 Mock Data | 🟠 Mock Data | 🔴 |
| **Create Meeting** | ✅ | ✅ | ✅ | ✅ | ✅ |
| **View Schedule** | ✅ All | ✅ Team + Own | ✅ Own | ✅ All | ✅ |
| **Create Schedule Entry** | ✅ | ✅ | ✅ | ✅ | ✅ |

---

### TARGET & DAILY ALERTS

| Feature | Admin | Manager | Sales Rep | Inside Rep | Status |
|---------|-------|---------|-----------|-----------|--------|
| **View Targets** | ✅ All | ✅ Team | ✅ Own | ✅ All | ✅ |
| **Create/Edit Target** | ✅ | ✅ | ✅ Own | ✅ | ✅ |
| **Import Prospects** | ✅ | ✅ | ✅ Own | ✅ | ✅ |
| **View Daily Alerts** | ✅ All | ✅ Team | ✅ Own | ✅ All | ✅ |
| **Manage Alerts** | ✅ | ✅ | ✅ | ✅ | ✅ |

---

### ADMINISTRATIVE

| Feature | Admin | Manager | Sales Rep | Inside Rep | Status |
|---------|-------|---------|-----------|-----------|--------|
| **User Management** |
| - View Users | ✅ All | ✅ Team | ❌ | ❌ | ✅ |
| - Create User | ✅ | ❌ | ❌ | ❌ | ✅ |
| - Edit User | ✅ All | ✅ Team | ❌ | ❌ | ✅ |
| - Deactivate User | ✅ | ❌ | ❌ | ❌ | ✅ |
| **Permission Management** | ✅ | ❌ | ❌ | ❌ | 🟠 |
| **Region Management** |
| - View Regions | ✅ All | ✅ Own | 🟠 Own | ✅ All | ✅ |
| - Manage Regions | ✅ | ❌ | ❌ | ❌ | 🟠 |
| **Group Management** |
| - View Groups | ✅ All | ✅ Team | ❌ | ❌ | ✅ |
| - Create/Edit Groups | ✅ | ✅ Team | ❌ | ❌ | 🟠 |
| **Global Settings** | ✅ Organization Level | ❌ | ❌ | ❌ | 🟠 |
| **Impersonation** | ✅ Any Rep | ✅ Any Rep | 🟠 Region Reps | ✅ Any Rep | 🟢 |

---

### IMPERSONATION & CROSS-USER MANAGEMENT

| Action (when selecting another Rep) | Admin | Manager | Sales Rep | Inside Rep | Tagged/Logged |
|-------------------------------------|-------|---------|-----------|------------|---------------|
| **Select Rep (Scope)** | ✅ Global | ✅ Global | 🟠 Region Only | ✅ Global | N/A |
| **View Customers** | ✅ | ✅ | ✅ | ✅ | ✅ |
| **Manage Meetings** | ✅ | ✅ | ✅ | ✅ | ✅ |
| **Create Opportunities** | ✅ | ✅ | ✅ | ✅ | ✅ |
| **Create Commitments** | ✅ | ✅ | ✅ | ✅ | ✅ |
| **Create Tasks** | ✅ | ✅ | ✅ | ✅ | ✅ |
| **Manage Schedule** | ✅ | ✅ | ✅ | ✅ | ✅ |
| **Create Targets** | ✅ | ✅ | ✅ | ✅ | ✅ |
| **Conversion Requests** | ✅ | ✅ | ✅ | ✅ | ✅ |
| **Edit Target's Global Settings** | ❌ | ❌ | ❌ | ❌ | N/A |

---

## FEATURE AVAILABILITY BY ROLE

### 👨‍💼 ADMIN (Role ID: 1)
**Type:** Super Access | **Scope:** Global / All Regions
**Codebase Access:**
- ✅ **Global Settings:** The ONLY role with access to `GLOBAL_SETTINGS_MANAGEMENT_ROLES`.
- ✅ **User Management:** Full CRUD (View, Create, Edit, Delete).
- ✅ **Regional Data:** Bypasses all regional filters in `UserAccessPolicy.php`.
- ✅ **Modules:** Dashboard, Customers, Contacts, Opportunities, Meetings, Tasks, Team Requests, Calendar, Commitments, Targets, Users.
- ✅ **Permissions:** Managed via `ADMIN_PERMISSIONS` in `rolePermissions.config.ts`.
- ✅ **Impersonation:** Can select **Any Rep** (Global) and perform all operational actions.
- ✅ **Global View:** When no rep is selected, sees ALL customers, targets, tasks, and commitments.
- ✅ **Org Settings:** Can edit global settings only in Global View (No Rep selected).

---

### 👔 MANAGER (Role ID: 4)
**Type:** Super Access | **Scope:** Broad / Team-Wide
**Codebase Access:**
- ✅ **Dashboard:** Broad access (Super Access Role ID).
- ❌ **Global Settings:** Explicitly restricted (not in `GLOBAL_SETTINGS_MANAGEMENT_ROLES`).
- 🟠 **User Management:** Can **View** users but cannot Create, Edit, or Delete (restricted in `MANAGER_PERMISSIONS`).
- ✅ **Regional Data:** Bypasses regional filters in `UserAccessPolicy.php` (Global scope).
- ✅ **Modules:** All operational modules except User CRUD.
- ✅ **Team Coordination:** Can assign tasks and view team schedules.
- ✅ **Impersonation:** Can select **Any Rep** (Global) and perform all operational actions.
- ✅ **Global View:** When no rep is selected, sees ALL customers, targets, tasks, and commitments.
- ❌ **Org Settings:** CANNOT edit global organizational settings.

---

### 📱 SALES REP (Role ID: 2)
**Type:** Standard | **Scope:** STRICTLY Regional (Own Only)
**Codebase Access:**
- ❌ **Global Access:** Blocked by `UserAccessPolicy.php` if region doesn't match.
- ❌ **User/Role Management:** No access to User list or Role configuration.
- ✅ **Dashboard:** Filtered to own region metrics only.
- ✅ **Operational Modules:** Customers, Contacts, Opportunities, Meetings, Tasks, Commitments, Targets.
- ✅ **Personal Tools:** Weekly/Daily Schedule, Daily Alerts (Own data only).
- 🟠 **Targets:** View own targets; create/edit limited to own customer associations.
- ✅ **Impersonation:** Can select **Other Reps (Within Own Region Only)**.
- ✅ **Actions:** Can perform all operational actions for the selected rep (logged with tag).
- ❌ **Org Settings:** No access to global settings.

---

### 🏢 INSIDE REP (Role ID: 3)
**Type:** Standard | **Primary:** Office-based Sales Operations

- ✅ **Office-based customer management:** Global scope in `UserAccessPolicy.php`.
- ✅ **Impersonation:** Can select **Any Rep** (Global) and perform all operational actions.
- ✅ **Actions:** Can perform all operational actions for the selected rep (logged with tag).
- ❌ **Org Settings:** No access to global settings.

---

## PERMISSION STRINGS (Current & Planned)

### Implemented Permissions
```
✅ user.view          - View user list
✅ user.create        - Create new user (Admin only)
✅ user.edit          - Edit user details
✅ user.delete        - Deactivate user (Admin only)
✅ dashboard.view     - Access dashboard
✅ dashboard.filter   - Apply dashboard filters
✅ dashboard.refresh  - Refresh dashboard data
```

### Planned PBAC Permissions (To Implement)
```
🔴 customer.view      - View customers
🔴 customer.create    - Create customer
🔴 customer.edit      - Edit customer
🔴 customer.delete    - Delete customer
🔴 contact.view       - View contacts
🔴 contact.create     - Create contact
🔴 contact.edit       - Edit contact
🔴 contact.delete     - Delete contact
🔴 opportunity.view   - View opportunities
🔴 opportunity.create - Create opportunity
🔴 opportunity.edit   - Edit opportunity
🔴 opportunity.delete - Close/delete opportunity
🔴 task.view          - View tasks
🔴 task.create        - Create task
🔴 task.edit          - Edit/complete task
🔴 task.delete        - Delete task (Manager only)
🔴 commitment.view    - View commitments
🔴 commitment.create  - Create commitment
🔴 commitment.edit    - Edit commitment
🔴 target.view        - View targets
🔴 target.create      - Set targets (Manager/Admin)
🔴 region.view        - View regions
🔴 region.manage      - Manage regions
🔴 group.view         - View groups
🔴 group.manage       - Manage groups
🔴 setting.view       - View settings
🔴 setting.edit       - Edit settings
🔴 permission.view    - View permissions
🔴 permission.manage  - Manage permissions
```

---

## CROSS-FUNCTIONAL ACCESS RULES

### Data Ownership Model
```
👤 Your Own Data
   USER -> Can view/edit own records
          Can view own customer's related data
          Can view own team's data tasks (if Manager)

👥 Team Data
   MANAGER -> Can view team members' data
             Can view team customers
             Can assign tasks to team
             Can set team targets

🏢 Regional/Office Data
   REGION_FILTER -> All users see only their region
   OFFICE_FILTER -> Inside reps see only their office
   
🌍 Global Data
   ADMIN -> Can view all data across all regions
   MANAGER -> Can view all team data across regions
```

### Concurrent User Restrictions
```
❌ Same customer/opportunity cannot be edited by 2+ users simultaneously
❌ Cannot view another user's private notes or tasks
✅ Can view shared team tasks assigned to you
✅ Can view team member's customer if it's a shared customer
```

### Cascade Rules on Deletion
```
When Customer is deleted:
  ├─ Contacts (cascade delete) ❌ Sales Rep cannot see
  ├─ Opportunities (archive or delete)
  ├─ Tasks (reassign or archive)
  └─ Commitments (mark complete or archive)

When Contact is deleted:
  ├─ Tasks related to contact (mark invalid)
  └─ Commitments (mark complete)

When User is deleted:
  ├─ Assign customers to manager
  ├─ Reassign tasks
  ├─ Archive opportunities
  └─ Reassign commitments
```

---

## KNOWN RESTRICTIONS BY DESIGN

### Why Admin Can't View Tasks
```
Design Decision: Tasks are field-level operations
Admin visibility could compromise field rep independence
Workaround: Manager can view team tasks
```

### Why Admin Can't View Schedule
```
Design Decision: Schedule is personal planning tool
Admin visibility compromises privacy
Workaround: Manager can view team schedules for coordination
```

### Why Admin Can't Access Daily Alerts
```
Design Decision: Alerts are operational indicators for field reps
Admin visibility unnecessary (has dashboard)
Workaround: Daily alerts auto-aggregate to manager
```

### Why Sales Rep Can't Delete Data
```
Design Decision: Maintain audit trail for all field activities
Prevents accidental data loss
Workaround: Admin/Manager can delete if necessary
```

---

## FIELD-LEVEL PERMISSION EXAMPLES

### Example 1: Customer Record Edit
```
Sales Rep Views Customer:
  ├─ Full name ✅ (own)
  ├─ Email ✅
  ├─ Phone ✅
  ├─ Address ✅
  ├─ Billing history ✅
  ├─ Contact history ✅
  ├─ Internal notes ✅ (own)
  ├─ Manager notes ✅ if visible
  └─ Assigned rep ✅ (shows as "Self")

Manager Views Sales Rep's Customer:
  ├─ Full name ✅
  ├─ Email ✅
  ├─ Phone ✅
  ├─ Address ✅
  ├─ Billing history ✅
  ├─ Contact history ✅
  ├─ Internal notes ✅ (team visibility)
  ├─ Manager notes ✅ (full)
  └─ Assigned rep ✅ (shows team member name)

Admin Views Any Customer:
  ├─ All fields ✅
  ├─ Internal notes ✅ (all)
  ├─ System audit ✅
  └─ Can see "masked" fields
```

### Example 2: Permission Change Workflow
```
Current State (RBAC):
1. User has "Sales Rep" role
2. Has implicit access to all sales rep features
3. Restrictions via route-level middleware

New State (PBAC - Planned):
1. User record stores array of permissions
2. Each permission checked at UI and API
3. Example: user.permissions = [
     "customer.view",
     "customer.create",
     "opportunity.view",
     "opportunity.create",
     "opportunity.edit"
   ]
4. Missing: "customer.edit", "opportunity.delete"
5. UI hides "Edit" button for customers
6. API rejects edit request if permission missing
```

---

## TESTING COORDINATES

### Test Each Role Combination
```
4 Roles × 17 Modules × 5 CRUD Operations = 340 Primary Tests
└─ Plus edge cases ≈ 750+ total tests ✅ (Playwright suite)
```

### Recommended Test Execution Order
```
1. Admin full access (baseline)
2. Manager team-scoped access (verify scoping works)
3. Sales Rep own-only access (verify restrictions)
4. Inside Rep variations (document differences)
5. Cross-role scenarios (Admin viewing Sales Rep's data)
6. Permission combos (edge permissions)
```

---

## STATUS SYMBOLS REFERENCE

| Symbol | Color | Meaning | Action |
|--------|-------|---------|--------|
| ✅ | Green | Fully Implemented & Working | Use in production |
| 🟡 | Yellow | Partial/Issues | Document limitations |
| 🔴 | Red | Not Implemented | Mark as blocker |
| 🟠 | Orange | In Progress/Design | Plan completion |
| ❌ | Red X | No Access / Restricted | Works as designed |

---

**Last Updated:** April 8, 2026  
**Next Update:** Post-PBAC Migration (Target: April 15, 2026)  
**Repository:** WCW CRM Frontend - Playwright Test Suite  
**Maintained By:** QA Team
