# WCW CRM QA Documentation Index
## Complete Feature Testing & Permission Framework

**Release:** v1.0 (PBAC Migration Ready)  
**Date:** April 8, 2026  
**Status:** 🟢 Ready for QA Execution

---

## 📚 Documentation Package Contents

This comprehensive QA package includes **4 detailed documents** for testing the WCW CRM system before PBAC migration:

### 1. **ROLE_PERMISSIONS_FEATURE_CHECKLIST.md** - Primary QA Document
**100+ Pages | Detailed Feature Matrix**

**What it contains:**
- Complete breakdown of all 17 modules
- Features for each module with role-based access
- Permission requirements for each operation
- Detailed edge cases for testing
- Known issues and blockers
- Pass/fail criteria for each feature
- Test execution recommendations

**Use this when:**
- Planning QA test execution
- Writing individual test cases
- Validating feature completeness
- Documenting known issues
- Creating test reports

**Structure:**
```
├─ System Roles Overview (4 roles)
├─ 17 Module Details:
│  ├─ Auth Module (1.1-1.4)
│  ├─ Dashboard (2.1-2.3)
│  ├─ Customers (3.1-3.6)
│  ├─ Contacts (4.1-4.4)
│  ├─ Opportunities (5.1-5.4)
│  ├─ Tasks (6.1-6.4)
│  ├─ Commitments (7.1-7.4)
│  ├─ Calendar (8.1-8.2)
│  ├─ Schedule (9.1-9.2)
│  ├─ Targets (10.1-10.2)
│  ├─ Daily Alerts (11.1-11.2)
│  ├─ Global Settings (12.1-12.2)
│  ├─ Regions (13.1-13.2)
│  ├─ Groups (14.1-14.2)
│  ├─ User Management (15.1-15.5)
│  ├─ Subscription (16.1-16.2)
│  └─ Layout (17.1-17.3)
├─ Summary Table by Module
├─ Priority Fixes
├─ Testing Execution Guide
└─ Support Information
```

**Key Metrics:**
- 80+ Features mapped
- 4 Roles with access control
- 150+ Edge cases documented
- 10+ Priority fixes identified
- 100% PBAC compatible structure

---

### 2. **PERMISSIONS_QUICK_REFERENCE.md** - One-Page Lookup
**12 Pages | Visual Permission Matrix**

**What it contains:**
- Quick permission matrix for all features
- Permission strings (implemented + planned)
- One-page module summaries
- Access control rules explanations
- Cross-role scenario examples
- Cascade deletion rules
- Field-level permission examples
- Test coordinate recommendations

**Use this when:**
- Quick feature permission lookup
- Understanding role boundaries
- Explaining access to stakeholders
- Writing API permission validations
- Designing PBAC implementation

**Key sections:**
```
✅ Permission Matrix (all features × 4 roles)
✅ Feature availability by role (breakdown)
✅ Permission strings (40+ total)
✅ Access control rules
✅ Cascade deletion workflows
✅ Field-level examples
✅ Cross-functional patterns
✅ Testing coordinates
```

**Quick Stats:**
- 15+ permission matrices
- 40+ permission strings
- 4 role profiles
- 8+ access control rules
- 6 field-level examples

---

### 3. **QA_TEST_EXECUTION_TRACKER.md** - Testing Checklist
**25 Pages | Module-by-Module Tracker**

**What it contains:**
- Test execution checklist for each module
- Role-based testing matrix
- Edge case tracking
- Issue identification form
- Critical blockers dashboard
- Progress metrics
- Sign-off documentation
- Role-based completion tracking

**Use this when:**
- Executing daily test runs
- Tracking test progress
- Documenting issues found
- Creating test reports
- Sign-off validation

**Structure:**
```
├─ Credential setup section
├─ 17 Module test tracking forms:
│  ├─ Feature test matrix
│  ├─ Edge cases checklist
│  ├─ Issues documentation
│  ├─ Sign-off section
│  └─ Test notes area
├─ Cross-module integration tests
├─ Critical blockers summary
├─ Role-based completion tracking
├─ Progress metrics dashboard
└─ Sign-off checklist
```

**Important Information:**
- Ready for 4 QA engineers (one per role)
- 17 separate module tracker sections
- Integration test section
- Critical blocker tracking with priority
- Weekly progress metrics
- Final sign-off pages

---

### 4. **SYSTEM_STRUCTURE_ANALYSIS.md** - Reference (from subagent)
**5 Pages | Codebase Architecture**

**What it contains:**
- Complete system structure analysis
- Role definitions and hierarchy
- Module architecture overview
- API endpoints documented
- Permission enforcement locations
- Gaps in current implementation
- PBAC readiness assessment

**Use this when:**
- Understanding system architecture
- Debugging permission issues
- Planning PBAC implementation
- Understanding API contracts
- Validating permission framework

---

## 🎯 HOW TO USE THESE DOCUMENTS

### Quick Start (5 minutes)
1. **Read:** PERMISSIONS_QUICK_REFERENCE.md (pages 1-3)
2. **Understand:** The 4 roles and their access levels
3. **Reference:** Permission matrix for quick lookups

### Full Test Planning (30 minutes)
1. **Study:** ROLE_PERMISSIONS_FEATURE_CHECKLIST.md (Module 1-3)
2. **Review:** Critical issues section
3. **Map:** Your testing responsibilities

### Daily QA Execution (ongoing)
1. **Use:** QA_TEST_EXECUTION_TRACKER.md
2. **Check:** PERMISSIONS_QUICK_REFERENCE.md for clarifications
3. **Reference:** ROLE_PERMISSIONS_FEATURE_CHECKLIST.md for edge cases
4. **Report:** Issues back to tracker form

### Pre-Release Validation (2 hours)
1. **Verify:** All modules in tracker show ✅
2. **Confirm:** All critical blockers resolved
3. **Check:** PBAC implementation complete
4. **Sign:** Sign-off section in tracker

---

## 📊 TESTING RESPONSIBILITY MATRIX

### Recommended QA Team Allocation

```
QA Engineer #1 - Role: ADMIN
├─ Test modules: 1,2,3,5,10,12,13,14,15
├─ Verify: Full access, global settings management
├─ Focus: Restricted features (Tasks, Schedule, Alerts)
└─ Document: Can-do vs cannot-do patterns

QA Engineer #2 - Role: MANAGER  
├─ Test modules: 1,2,3,4,5,6,7,8,9,11
├─ Verify: Team scoping, team member access
├─ Focus: Cascade restrictions, team data
└─ Document: Team boundaries, data visibility

QA Engineer #3 - Role: SALES REP
├─ Test modules: 1,2,3,4,5,6,7,8,9,11
├─ Verify: Own-data-only access
├─ Focus: Cross-rep restrictions, data isolation
└─ Document: Access denials, permission edge cases

QA Engineer #4 - Role: INSIDE REP
├─ Test modules: 1,2,3,4,5,6,7,9,11
├─ Verify: Office-based operations
├─ Focus: Variations from Sales Rep
└─ Document: Role-specific differences

QA Lead
├─ Coordinate: Cross-module integration tests
├─ Prioritize: Critical blocker fixes
├─ Aggregate: All test results
└─ Validate: Sign-off checklist
```

---

## 🔄 SUGGESTED TEST EXECUTION FLOW

### Phase 1: Setup (Day 1, 2 hours)
```bash
1. Create test accounts (4 roles)
   └─ Use tracker: QA_TEST_EXECUTION_TRACKER.md → Section: Test Credential Setup

2. Verify login works
   └─ Reference: ROLE_PERMISSIONS_FEATURE_CHECKLIST.md → Module 1 (Auth)

3. Verify each role dashboard access
   └─ Reference: PERMISSIONS_QUICK_REFERENCE.md → Dashboard & Navigation

4. Document any blockers
   └─ Use: QA_TEST_EXECUTION_TRACKER.md → Module 2 form
```

### Phase 2: Module Testing (Days 2-5, 4 hours/day)
```
For each module:
1. Assign to primary QA engineer
2. Open ROLE_PERMISSIONS_FEATURE_CHECKLIST.md for that module
3. Open QA_TEST_EXECUTION_TRACKER.md for that module
4. Execute test checklist with all 4 roles:
   ├─ Run each feature test
   ├─ Execute edge cases
   ├─ Document issues in tracker form
   └─ Mark pass/fail in matrix
5. Reference PERMISSIONS_QUICK_REFERENCE.md for permission questions
```

### Phase 3: Integration Testing (Days 3-5, 2 hours/session)
```
1. Use tracker: QA_TEST_EXECUTION_TRACKER.md → Cross-Module Integration Tests
2. Reference: ROLE_PERMISSIONS_FEATURE_CHECKLIST.md → Testing Execution Guide
3. Test complex workflows across modules
4. Document with expected vs actual results
```

### Phase 4: Validation (Day 6, 4 hours)
```
1. Run full Playwright suite:
   └─ npm run test:playwright (756 tests)

2. Compare results vs manual testing
   └─ Reference: PERMISSIONS_QUICK_REFERENCE.md → Permission matrix

3. Verify all critical blockers resolved:
   └─ Use: QA_TEST_EXECUTION_TRACKER.md → Critical Blockers Summary

4. Executive sign-off:
   └─ Complete: QA_TEST_EXECUTION_TRACKER.md → Sign-off Checklist
```

---

## 🎓 TESTING SCENARIOS BY USER JOURNEY

### Scenario 1: Sales Rep Daily Workflow
**Test using:** ROLE_PERMISSIONS_FEATURE_CHECKLIST.md | TRACKER (Sales Rep column)

```
Sales Rep Jim's Day:
1. Login via auth module
   └─ Validate: Login form works, credentials accepted
   └─ Test: Session persists on refresh

2. View dashboard (own region only)
   └─ Validate: Filters show only own region
   └─ Test: Cannot see other regions even if available

3. Create new customer
   └─ Validate: Can create, assigned to self
   └─ Test: Email validation, duplicate detection

4. Add contact to customer
   └─ Validate: Can add, cannot delete
   └─ Test: Duplicate email per customer prevented

5. Create opportunity
   └─ Validate: Can create and edit, cannot delete
   └─ Test: Probability validation, amount validation

6. View own tasks/commitments
   └─ Validate: See only own
   └─ Test: Cannot see manager's tasks

7. View/manage own alerts
   └─ Validate: Can dismiss, snooze, resolve
   └─ Test: Alert count updates

Edge Cases: Try accessing manager's customer, delete own customer (should fail),
edit prospect probability to 150% (should reject)
```

### Scenario 2: Manager Weekly Oversight
**Test using:** ROLE_PERMISSIONS_FEATURE_CHECKLIST.md | TRACKER (Manager column)

```
Manager Lisa's Week:
1. View team dashboard data
   └─ Validate: See all team members' regions
   └─ Test: Cannot modify other regions

2. Create task for team member Jim
   └─ Validate: Can assign ownership, type selection
   └─ Test: Jim receives notification

3. Review team's opportunities
   └─ Validate: See all team opps
   └─ Test: Can edit team opps, cannot delete

4. View team member performance targets
   └─ Validate: Can set targets
   └─ Test: Team member sees assigned target

5. Edit team settings
   └─ Validate: Can modify team-level settings
   └─ Test: Cannot modify global settings

6. User management for team
   └─ Validate: Can view team, cannot create users
   └─ Test: Cannot deactivate team members

Edge Cases: Try changing own role, delete team member's customer,
edit global settings (should be restricted)
```

### Scenario 3: Admin System Management
**Test using:** ROLE_PERMISSIONS_FEATURE_CHECKLIST.md | TRACKER (Admin column)

```
Admin Charlie's System Maintenance:
1. View system-wide dashboard
   └─ Validate: See all regions, all reps
   └─ Test: No filtering applied

2. User management
   └─ Validate: Create, edit, deactivate any user
   └─ Test: Cannot delete own account

3. Global settings
   └─ Validate: Can change all system settings
   └─ Test: Changes apply immediately

4. Permission management (PBAC prep)
   └─ Validate: Framework ready, not fully implemented
   └─ Test: Document expected behavior

5. Region & group management
   └─ Validate: Can create, edit, delete
   └─ Test: Reassign data before delete

6. Audit trail review
   └─ Validate: See all system changes
   └─ Test: Cannot modify audit log

Restrictions to Verify: Cannot view Tasks, Schedule, or Daily Alerts
(by design - confirm this is intentional)
```

---

## 🐛 CRITICAL BLOCKERS NEEDING FIXES

Before marking QA complete, these MUST be resolved:

### 1. **Calendar Module - Mock Data Issue** 🔴 CRITICAL
**Severity:** BLOCKING  
**Current State:** Hardcoded September 2025 data only  
**Expected:** Show current month with backend data

**To Test:**
1. Open calendar module
2. Verify month/year displayed (should be current)
3. Verify meetings show current/real data
4. Verify API is being called (check network tab)

**Document in Tracker:** QA_TEST_EXECUTION_TRACKER.md → Module 8 (Calendar)

### 2. **Subscription - Email Verification Disabled** 🔴 CRITICAL
**Severity:** BLOCKING  
**Current State:** Email verification workflow incomplete  
**Expected:** New users can verify email, access system

**To Test:**
1. Attempt to verify email (check if available)
2. Verify verification email sent
3. Test verification link (valid & expired)
4. Test resend verification button

**Document in Tracker:** QA_TEST_EXECUTION_TRACKER.md → Module 16 (Subscription)

### 3. **Authentication - Token Management** 🟡 HIGH
**Severity:** HIGH (Session Management)  
**Current State:** No token refresh or invalidation  
**Expected:** Auto-refresh on expiration, 401 redirect to login

**To Test:**
1. Wait for token to expire
2. Verify auto-refresh triggers (if implemented)
3. Verify invalid token redirects to login
4. Test logout revokes token (backend)

**Document in Tracker:** QA_TEST_EXECUTION_TRACKER.md → Module 1 (Auth)

### 4. **User Management - PBAC Not Implemented** 🟡 HIGH
**Severity:** HIGH (Pre-migration prep)  
**Current State:** Framework ready, permission assignment not working  
**Expected:** Admin/Manager can grant/revoke permissions to users

**To Test:**
1. Attempt to manage user permissions (should fail or show framework)
2. Document current UI/UX for permissions
3. Verify permission framework structure correct
4. Test prepared for PBAC implementation

**Document in Tracker:** QA_TEST_EXECUTION_TRACKER.md → Module 15 (User Management)

---

## 📈 SUCCESS CRITERIA FOR QA SIGN-OFF

### All of These Must Be True:

✅ **All 17 modules tested** with each of 4 roles  
✅ **756 Playwright tests passing** (regression)  
✅ **All critical blockers resolved** (4 items above)  
✅ **All edge cases documented** (150+ scenarios)  
✅ **No unauthorized access found** (security validated)  
✅ **Performance acceptable** (< 3s per page)  
✅ **PBAC structure verified** (ready for implementation)  
✅ **All test results documented** in QA_TEST_EXECUTION_TRACKER.md  
✅ **QA team sign-off** obtained  
✅ **Tech lead review** completed  

### QA Report Deliverables:

1. ✅ Completed QA_TEST_EXECUTION_TRACKER.md with all modules
2. ✅ List of issues found with priority & owner
3. ✅ Proof of all 756 Playwright tests passing
4. ✅ PBAC implementation checklist status
5. ✅ Sign-off documentation completed

---

## 🔧 USING THE PLAYWRIGHT AUTOMATION

**756 automated tests already written and configured**

### Run All Tests:
```bash
cd /Applications/XAMPP/xamppfiles/htdocs/wcw-frontend
npm run test:playwright
```

### Run Specific Module Tests:
```bash
npm run test:playwright tests/modules/authentication.spec.ts
npm run test:playwright tests/modules/customers.spec.ts
npm run test:playwright tests/modules/calendar.spec.ts
# etc...
```

### View HTML Report:
```bash
npx playwright show-report
```

### Run with Debug UI:
```bash
npm run test:playwright:ui
```

### Integration with QA Tracker:
1. Run: `npm run test:playwright` (756 tests)
2. Check: All tests passing? Update tracker: ✅
3. Check: Some tests failing? Document in tracker: ⚠️
4. Reference: ROLE_PERMISSIONS_FEATURE_CHECKLIST.md for manual edge cases not covered by automation

---

## 📞 SUPPORT & QUESTIONS

### If you find a feature not working:

1. **Check:** ROLE_PERMISSIONS_FEATURE_CHECKLIST.md (list of known issues)
2. **Verify:** Is it marked as "Not Implemented"? → Expected
3. **Test:** Does Playwright test cover it? → Check test output
4. **Document:** Add to QA_TEST_EXECUTION_TRACKER.md → Critical Blockers
5. **Escalate:** If blocking, add to sign-off review

### If you're unsure about permissions:

1. **Quick lookup:** PERMISSIONS_QUICK_REFERENCE.md (matrices)
2. **Detailed explanation:** ROLE_PERMISSIONS_FEATURE_CHECKLIST.md (feature sections)
3. **Test it:** Use QA credentials to verify
4. **Document:** Note findings in tracker

### If you find a security issue:

1. **Report:** To security team immediately
2. **Test:** Does Playwright catch it ? Review test_error_context
3. **Document:** Current behavior vs expected behavior
4. **Escalate:** Block release until fixed

---

## 📋 DOCUMENT USAGE QUICK REFERENCE

| Question | Use This Document | Section |
|----------|------------------|---------|
| What can each role do? | PERMISSIONS_QUICK_REFERENCE.md | Permission Matrix |
| What's the edge case for feature X? | ROLE_PERMISSIONS_FEATURE_CHECKLIST.md | Module section |
| How do I test module Y? | QA_TEST_EXECUTION_TRACKER.md | Module form |
| What are the critical issues? | QA_TEST_EXECUTION_TRACKER.md | Blockers Summary |
| How are permissions enforced? | PERMISSIONS_QUICK_REFERENCE.md | Access Rules |
| Where are API endpoints? | SYSTEM_STRUCTURE_ANALYSIS.md | APIs section |
| What's the architecture? | SYSTEM_STRUCTURE_ANALYSIS.md | Structure section |
| How do I sign off QA? | QA_TEST_EXECUTION_TRACKER.md | Sign-off section |

---

## ✅ FINAL CHECKLIST BEFORE STARTING

- [ ] Read this index document (you are here!)
- [ ] Access to test credentials (create if needed)
- [ ] Laptop with VS Code & terminal open
- [ ] Can run: `npm run test:playwright`
- [ ] Can open: Browser to http://localhost:5173
- [ ] Have: 3-4 QA engineers (one per role minimum)
- [ ] Can access: Backend staging API (wcwstagingapi.nerdflow.cloud)
- [ ] Have: All 4 documents open and printed/bookmarked
- [ ] Understand: 17 modules to test
- [ ] Know: 4 critical blockers to track
- [ ] Ready: To start testing!

---

**Documentation Package Complete**  
**Ready for QA Execution**  
**Expected Duration:** 5-7 business days  
**Target Completion:** April 15, 2026  

**For Questions:** Refer to this index first!
