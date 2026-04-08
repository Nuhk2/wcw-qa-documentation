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
| View Dashboard | ✅ All Data | ✅ Team Data | ✅ Own Region | ✅ Own Region | ✅ |
| Filter Dashboard | ✅ All Regions | ✅ Team | 🟠 Own Only | 🟠 Own Only | ✅ |
| Access Settings | ✅ All | 🟠 Limited | ❌ | ❌ | 🟠 |
| View Navigation Menu | ✅ All Items | ✅ Most Items | 🟠 Filtered | 🟠 Filtered | ✅ |
| Manage Global Settings | ✅ Yes | 🟠 Team Only | ❌ | ❌ | 🟠 |

---

### CUSTOMER MANAGEMENT

| Feature | Admin | Manager | Sales Rep | Inside Rep | Status |
|---------|-------|---------|-----------|-----------|--------|
| **View Customers** |
| - List View | ✅ All | ✅ Team | ✅ Own | ✅ Own | ✅ |
| - Detail View | ✅ Any | ✅ Team | ✅ Own | ✅ Own | ✅ |
| **Create Customer** | ✅ | ✅ Assign to Team | ✅ Assign to Self | ✅ Assign to Self | ✅ |
| **Edit Customer** | ✅ Any | ✅ Team Only | 🟠 Own Only | 🟠 Own Only | 🟠 |
| **Delete Customer** | ✅ | 🟠 Team Only | ❌ | ❌ | 🟠 |
| **Search/Filter** | ✅ All Data | ✅ Team Data | 🟠 Own Data | 🟠 Own Data | ✅ |
| **Export Customers** | ✅ | ✅ | ✅ | ✅ | 🟠 |

---

### CONTACT MANAGEMENT

| Feature | Admin | Manager | Sales Rep | Inside Rep | Status |
|---------|-------|---------|-----------|-----------|--------|
| **View Contacts** |
| - List View | ✅ All | ✅ Team | ✅ Customer's | ✅ Customer's | ✅ |
| - Detail View | ✅ Any | ✅ Team | ✅ Own Customer | ✅ Own Customer | ✅ |
| **Create Contact** | ✅ | ✅ Team Customers | ✅ Own Customer | ✅ Own Customer | ✅ |
| **Edit Contact** | ✅ Any | ✅ Team's | ✅ Own Customer's | ✅ Own Customer's | ✅ |
| **Delete Contact** | ✅ | 🟠 Team Only | ❌ | ❌ | 🟠 |

---

### OPPORTUNITY MANAGEMENT

| Feature | Admin | Manager | Sales Rep | Inside Rep | Status |
|---------|-------|---------|-----------|-----------|--------|
| **View Opportunities** |
| - List View | ✅ All | ✅ Team | ✅ Own | ✅ Own | ✅ |
| - Pipeline View | ✅ All | ✅ Team | ✅ Own | ✅ Own | ✅ |
| **Create Opportunity** | ✅ | ✅ Assign to Team | ✅ Own | ✅ Own | ✅ |
| **Edit Opportunity** | ✅ Any | ✅ Team Only | 🟠 Own Only | 🟠 Own Only | ✅ |
| **Mark Won/Lost** | ✅ | ✅ Team | ✅ Own | ✅ Own | ✅ |
| **Delete Opportunity** | ✅ | 🟠 Team Only | ❌ | ❌ | 🟠 |

---

### TASK MANAGEMENT

| Feature | Admin | Manager | Sales Rep | Inside Rep | Status |
|---------|-------|---------|-----------|-----------|--------|
| **View Tasks** | ❌ Restricted | ✅ Team + Own | ✅ Own | ✅ Own | 🟠 |
| **Create Task** | ❌ Restricted | ✅ Assign to Team | ✅ Own | ✅ Own | 🟠 |
| **Edit Task** | ❌ Restricted | ✅ Team + Own | ✅ Own | ✅ Own | 🟠 |
| **Complete Task** | ❌ Restricted | ✅ | ✅ | ✅ | 🟠 |
| **Delete Task** | ❌ Restricted | 🟠 Team Only | ❌ | ❌ | 🟠 |

---

### COMMITMENT MANAGEMENT

| Feature | Admin | Manager | Sales Rep | Inside Rep | Status |
|---------|-------|---------|-----------|-----------|--------|
| **View Commitments** | ✅ All | ✅ Team | ✅ Own | ✅ Own | ✅ |
| **Create Commitment** | ✅ | ✅ Assign to Team | ✅ Own | ✅ Own | ✅ |
| **Edit Commitment** | ✅ Any | ✅ Team | ✅ Own | ✅ Own | ✅ |
| **Mark Completed** | ✅ | ✅ | ✅ | ✅ | ✅ |

---

### CALENDAR & SCHEDULE

| Feature | Admin | Manager | Sales Rep | Inside Rep | Status |
|---------|-------|---------|-----------|-----------|--------|
| **View Calendar** | 🟠 Mock Data | 🟠 Mock Data | 🟠 Mock Data | 🟠 Mock Data | 🔴 |
| **Create Meeting** | 🟠 | 🟠 | 🟠 | 🟠 | 🔴 |
| **View Schedule** | ❌ Restricted | ✅ Team + Own | ✅ Own | ✅ Own | 🟠 |
| **Create Schedule Entry** | ❌ Restricted | ✅ Team | ✅ Own | ✅ Own | 🟠 |

---

### TARGET & DAILY ALERTS

| Feature | Admin | Manager | Sales Rep | Inside Rep | Status |
|---------|-------|---------|-----------|-----------|--------|
| **View Targets** | ✅ All | ✅ Team | ✅ Own | ✅ Own | ✅ |
| **Create/Edit Target** | ✅ | ✅ Team | ❌ | ❌ | ✅ |
| **View Daily Alerts** | ❌ Restricted | ✅ Team | ✅ Own | ✅ Own | ✅ |
| **Manage Alerts** | ❌ Restricted | ✅ | ✅ | ✅ | ✅ |

---

### ADMINISTRATIVE

| Feature | Admin | Manager | Sales Rep | Inside Rep | Status |
|---------|-------|---------|-----------|-----------|--------|
| **User Management** |
| - View Users | ✅ All | 🟠 Team | ❌ | ❌ | ✅ |
| - Create User | ✅ | ❌ | ❌ | ❌ | ✅ |
| - Edit User | ✅ All | 🟠 Team | ❌ | ❌ | ✅ |
| - Deactivate User | ✅ | ❌ | ❌ | ❌ | ✅ |
| **Permission Management** | 🔴 Not Impl | 🔴 Not Impl | ❌ | ❌ | 🔴 |
| **Region Management** |
| - View Regions | ✅ All | 🟠 Own | 🟠 Own | 🟠 Own | ✅ |
| - Manage Regions | ✅ | 🟠 Own | ❌ | ❌ | 🟠 |
| **Group Management** |
| - View Groups | ✅ All | 🟠 Team | ❌ | ❌ | ✅ |
| - Create/Edit Groups | ✅ | 🟠 Team | ❌ | ❌ | 🟠 |
| **Global Settings** | ✅ | 🟠 | ❌ | ❌ | 🟠 |

---

## FEATURE AVAILABILITY BY ROLE

### 👨‍💼 ADMIN (Role ID: 1)
**Type:** Super Access | **Primary:** System Administration

**All Modules Accessible:**
- ✅ Dashboard (all data)
- ✅ Customers (create, read, update, delete)
- ✅ Contacts (full access)
- ✅ Opportunities (full access)
- ❌ Tasks (restricted by design)
- ✅ Commitments (full)
- 🟠 Calendar (mock data issue)
- ❌ Schedule (restricted)
- ✅ Targets (create for others)
- ❌ Daily Alerts (restricted)
- ✅ User Management (full)
- ✅ Permissions (framework ready)
- ✅ Regions (manage all)
- ✅ Groups (manage all)
- ✅ Settings (all settings)

**Restrictions:**
- Cannot view Tasks (by design)
- Cannot view Schedule (by design)
- Cannot view Daily Alerts (by design)
- Cannot manage own permissions (prevent privilege escalation)

---

### 👔 MANAGER (Role ID: 4)
**Type:** Super Access | **Primary:** Team Oversight & Approval

**All Modules Accessible (with team scope):**
- ✅ Dashboard (team + regional data)
- ✅ Customers (team customers, can assign)
- ✅ Contacts (team customers' contacts)
- ✅ Opportunities (team opps)
- ✅ Tasks (view team + own)
- ✅ Commitments (team)
- 🟠 Calendar (team meetings - mock data)
- ✅ Schedule (view team + own)
- ✅ Targets (assign to team)
- ✅ Daily Alerts (team alert dashboard)
- 🟠 User Management (view/edit team users)
- 🔴 Permissions (framework ready, not fully implemented)
- 🟠 Regions (manage own regions)
- 🟠 Groups (manage team groups)
- 🟠 Settings (limited settings)

**Restrictions:**
- Cannot create users
- Cannot delete teammates
- Cannot modify own role
- Cannot access competitor data (if regional filtering enforced)

---

### 📱 SALES REP (Role ID: 2)
**Type:** Standard | **Primary:** Field Sales Operations

**Modules with Limited Access:**
- ✅ Dashboard (own region only)
- ✅ Customers (own customers)
- ✅ Contacts (own customers' contacts)
- ✅ Opportunities (own opportunities)
- ✅ Tasks (own tasks only)
- ✅ Commitments (own commitments)
- 🟠 Calendar (own meetings - mock data)
- ✅ Schedule (own schedule)
- ✅ Targets (view own targets)
- ✅ Daily Alerts (own alerts)

**No Access:**
- ❌ User Management
- ❌ Permission Management
- ❌ Region Management
- ❌ Groups Management
- ❌ Global Settings
- ❌ Cannot delete anything
- ❌ Cannot create users
- ❌ Cannot view team members' data (by design)

**Can Manage:**
- Own Customers (create, edit, not delete)
- Own Contacts (create, edit, not delete)
- Own Opportunities (create, edit, close)
- Own Tasks (create, edit, complete, not delete)
- Own Commitments (create, edit, mark complete)

---

### 🏢 INSIDE REP (Role ID: 3)
**Type:** Standard | **Primary:** Office-based Sales Operations

**Same as Sales Rep + Office Scope:**
- ✅ All Sales Rep features
- ✅ Customer order processing
- ✅ Office-based customer management

**Differences from Sales Rep:**
- Can create customers for office-based operations
- Can manage customer billing
- Limited travel/field access

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
