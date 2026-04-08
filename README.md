# WCW CRM QA Documentation & Testing Framework

> **Complete QA documentation, permission matrix, and feature checklist for WCW CRM v1.0**

[![QA Status](https://img.shields.io/badge/QA%20Status-Ready%20for%20Testing-green)](./docs/index.md)
[![GitHub Pages](https://img.shields.io/badge/View%20Docs-GitHub%20Pages-blue)](https://nuhk2.github.io/wcw-qa-documentation/)
[![Test Suite](https://img.shields.io/badge/Tests-756%20Playwright%20Tests-brightgreen)](./docs/index.md)
[![Roles](https://img.shields.io/badge/Roles-4%20(Admin%20%7C%20Manager%20%7C%20Sales%20Rep%20%7C%20Inside%20Rep)-informational)](./docs/index.md)
[![Modules](https://img.shields.io/badge/Modules-17%20Total-informational)](./docs/index.md)

## 📖 Documentation Package

This repository contains **comprehensive QA documentation** for testing the WCW CRM system before PBAC migration (Target: April 15, 2026).

### 🎯 Start Here

**→ [QA Documentation Master Index](./QA_DOCUMENTATION_INDEX.md)** - Complete guide to all documents

### Primary Documents

1. **[📋 QA Test Execution Tracker](./QA_TEST_EXECUTION_TRACKER.md)** - Daily testing checklist with module forms
2. **[✅ Feature Checklist](./ROLE_PERMISSIONS_FEATURE_CHECKLIST.md)** - Complete 17-module feature matrix (45k+)
3. **[⚡ Permission Quick Reference](./PERMISSIONS_QUICK_REFERENCE.md)** - One-page permission matrices
4. **[🏗️ System Analysis](./SYSTEM_STRUCTURE_ANALYSIS.md)** - System architecture and roles

### View Online

🌐 **[GitHub Pages Live Site](https://nuhk2.github.io/wcw-qa-documentation/)**

## 📊 What's Included

| Item | Count | Details |
|------|-------|----------|
| **Modules** | 17 | Dashboard, Customers, Contacts, Opportunities, Tasks, Commitments, Calendar, Schedule, Targets, Alerts, Settings, Regions, Groups, User Mgmt, Subscription, Layout, Auth |
| **Roles** | 4 | Admin (Super), Manager (Team), Sales Rep (Own), Inside Rep (Own) |
| **Features** | 80+ | Complete feature matrix with role access control |
| **Edge Cases** | 150+ | Documented test scenarios |
| **Tests** | 756 | Playwright automation tests |
| **Permissions** | 40+ | Current (7 implemented) + Planned (33 for PBAC) |

## 🚀 Quick Start

### For QA Testing
```
1. Open: QA_TEST_EXECUTION_TRACKER.md
2. Choose your role: Admin, Manager, Sales Rep, or Inside Rep
3. Follow the module forms
4. Use PERMISSIONS_QUICK_REFERENCE.md for clarifications
5. Reference ROLE_PERMISSIONS_FEATURE_CHECKLIST.md for edge cases
```

### For Developers
```
1. Review: SYSTEM_STRUCTURE_ANALYSIS.md
2. Understand: ROLE_PERMISSIONS_FEATURE_CHECKLIST.md (Module 15: User Mgmt)
3. Plan: PBAC migration using permission strings
4. Implement: 40+ permission strings across 17 modules
```

## 🚨 Critical Blockers (Must Fix Before Release)

🔴 **Calendar Module** - Hardcoded mock data (September 2025)  
🔴 **Subscription** - Email verification workflow disabled  
🟡 **Auth** - Token refresh not implemented  
🟡 **User Management** - PBAC permissions not implemented  

See [QA_TEST_EXECUTION_TRACKER.md](./QA_TEST_EXECUTION_TRACKER.md) for details.

## 👥 Testing by Role

### 👨‍💼 Admin (Super Access - System Wide)
- Global settings, user management, regions, groups
- Restricted: Tasks, Schedule, Daily Alerts (by design)
- [View Admin Scenarios](./QA_DOCUMENTATION_INDEX.md)

### 👔 Manager (Super Access + Team Scope)
- Team oversight, approval workflows, performance targets
- Restricted: Cannot create users or change own role
- [View Manager Scenarios](./QA_DOCUMENTATION_INDEX.md)

### 📱 Sales Rep (Own Data Only)
- Customer, opportunity, task, commitment management
- Restricted: Cannot delete, cannot view team members' data
- [View Sales Rep Scenarios](./QA_DOCUMENTATION_INDEX.md)

### 🏢 Inside Rep (Office Operations)
- Same as Sales Rep with office-based focus
- Restricted: Same access restrictions as Sales Rep
- [View Inside Rep Scenarios](./QA_DOCUMENTATION_INDEX.md)

## ✅ Testing Success Criteria

- [ ] All 17 modules tested with each of 4 roles
- [ ] 756 Playwright tests passing
- [ ] All critical blockers resolved
- [ ] All edge cases documented
- [ ] No unauthorized access found
- [ ] Performance < 3s per page load
- [ ] PBAC structure validated
- [ ] QA team sign-off obtained
- [ ] Tech lead review completed

## 🧪 Automated Testing

```bash
# Run all 756 tests
npm run test:playwright

# View results
npx playwright show-report

# Run specific module
npm run test:playwright tests/modules/customers.spec.ts
```

## 🗂️ Repository Structure

```
wcw-qa-documentation/
├── docs/index.md                            # GitHub Pages homepage
├── QA_DOCUMENTATION_INDEX.md               # Master navigation guide
├── ROLE_PERMISSIONS_FEATURE_CHECKLIST.md  # 45k+ 17-module feature matrix
├── PERMISSIONS_QUICK_REFERENCE.md         # One-page permission lookups
├── QA_TEST_EXECUTION_TRACKER.md           # Testing execution forms
├── SYSTEM_STRUCTURE_ANALYSIS.md           # System architecture
├── _config.yml                            # GitHub Pages Jekyll config
├── README.md                              # This file
└── .gitignore
```

## 📖 Documentation Overview

| Document | Purpose | Details |
|----------|---------|----------|
| Master Index | Navigation | How to use all documents, workflows, scenarios |
| Feature Checklist | Reference | All 17 modules, 80+ features, edge cases |
| Tracker | Daily Use | Module-by-module test forms and progress |
| Quick Reference | Lookup | Permission matrices, access rules, field examples |
| System Analysis | Architecture | Roles, modules, structure, API endpoints |

## 🔗 Links

- **📱 GitHub Pages:** [nuhk2.github.io/wcw-qa-documentation](https://nuhk2.github.io/wcw-qa-documentation/)
- **📦 GitHub Repo:** [github.com/Nuhk2/wcw-qa-documentation](https://github.com/Nuhk2/wcw-qa-documentation)
- **❓ Issues:** [Report problems](https://github.com/Nuhk2/wcw-qa-documentation/issues)
- **💬 Discussions:** [Ask questions](https://github.com/Nuhk2/wcw-qa-documentation/discussions)

## 📋 Document Maintenance

| Document | Owner | Frequency |
|----------|-------|----------|
| QA_TEST_EXECUTION_TRACKER.md | QA Lead | Daily (during testing) |
| ROLE_PERMISSIONS_FEATURE_CHECKLIST.md | QA Engineer | Per feature |
| PERMISSIONS_QUICK_REFERENCE.md | QA Engineer | Per permission change |
| SYSTEM_STRUCTURE_ANALYSIS.md | Tech Lead | Per sprint |
| docs/index.md | QA Lead | Per release |

## 🤝 Contributing

To update documentation:

```bash
git clone https://github.com/Nuhk2/wcw-qa-documentation.git
cd wcw-qa-documentation

# Make changes to markdown files
# Then commit and push
git add .
git commit -m "Update: [component] - [description]"
git push origin main
```

GitHub Pages will auto-update within seconds!

## 📞 Support

### I want to...
- **Start testing:** Open [QA_TEST_EXECUTION_TRACKER.md](./QA_TEST_EXECUTION_TRACKER.md)
- **Understand permissions:** Open [PERMISSIONS_QUICK_REFERENCE.md](./PERMISSIONS_QUICK_REFERENCE.md)
- **Learn all features:** Open [ROLE_PERMISSIONS_FEATURE_CHECKLIST.md](./ROLE_PERMISSIONS_FEATURE_CHECKLIST.md)
- **Get started:** Open [QA_DOCUMENTATION_INDEX.md](./QA_DOCUMENTATION_INDEX.md)
- **Understand system:** Open [SYSTEM_STRUCTURE_ANALYSIS.md](./SYSTEM_STRUCTURE_ANALYSIS.md)

---

**Repository:** [Nuhk2/wcw-qa-documentation](https://github.com/Nuhk2/wcw-qa-documentation)  
**Created:** April 8, 2026  
**Target Completion:** April 15, 2026  
**Status:** 🟢 Ready for QA Testing  

*Made with ❤️ for Quality Assurance*
