# Issue Management Automation Workflow

This repository uses an intelligent Issue Management Automation system that automatically triages, categorizes, and responds to all issues.

## 🚀 Features

### Automatic Triage
When you create an issue, the system automatically:
- Assigns category labels based on keywords in the title
- Assigns priority labels based on keywords in the title or body
- Adds initial status labels for tracking
- Creates all necessary labels if they don't exist

### Epic Task Breakdown
Issues with "Epic" in the title automatically get:
- 4 sub-issues created for structured implementation
- A task checklist added to the parent issue
- All sub-tasks linked back to the parent epic
- Proper labels for tracking progress

### Intelligent Responses
You'll receive:
- A welcome message if this is your first issue in the repo
- Type-specific guidance based on the issue category
- Automatic milestone assignment for high-priority items
- Status updates as the issue progresses through triage

## 🏷️ Label System

### Category Labels
- **bug** - Something isn't working
- **enhancement** - New feature or request
- **epic** - Large feature requiring multiple sub-tasks
- **maintenance** - Maintenance and housekeeping tasks

### Priority Labels
Priority is automatically assigned based on keywords:

| Priority | Keywords | Label |
|----------|----------|-------|
| Critical | critical, urgent, production, outage | `priority-critical` |
| High | important, high, blocking | `priority-high` |
| Medium | medium, normal (or no keywords) | `priority-medium` |
| Low | low, nice-to-have, minor | `priority-low` |

### Status Labels
- **needs-triage** - New issue awaiting initial review
- **needs-review** - Triaged and awaiting detailed review
- **first-time-contributor** - Created by first-time contributor

## 📋 Using Issue Templates

We provide three issue templates to help structure your submissions:

### Bug Report
Use this for reporting bugs and issues. Include:
- Clear description of the bug
- Steps to reproduce
- Expected vs actual behavior
- Environment details

### Feature Request / Epic
Use this for new features and enhancements. Include:
- Feature description
- Problem statement
- Proposed solution
- Use cases and benefits

### Maintenance Task
Use this for maintenance and housekeeping. Include:
- Task description
- Task type (refactoring, updates, etc.)
- Scope and reason
- Expected outcome

## 🎯 How to Create Issues

### Creating a Bug Report
```
Title: Bug: [Short description]
Body: Use the bug report template
```

**Example:**
```
Title: Bug: Login form validation not working
```

The system will:
- Add `bug` label
- Detect priority from your description
- Add `needs-triage` → `needs-review` labels
- Post bug report guidelines
- Assign to milestone if high/critical priority

### Creating an Epic
```
Title: Epic: [Feature name]
Body: Use the feature request template
```

**Example:**
```
Title: Epic: Redesign user dashboard interface
```

The system will:
- Add `epic` label
- Detect priority from your description
- Create 4 sub-issues automatically:
  1. Requirements Analysis
  2. Design and Architecture
  3. Implementation
  4. Testing and Documentation
- Add task checklist to parent issue
- Post feature request process guidelines
- Assign to milestone if high/critical priority

### Creating a Maintenance Task
```
Title: [Task description with "maintenance"]
Body: Use the maintenance template
```

**Example:**
```
Title: Weekly maintenance cleanup and refactor
```

The system will:
- Add `maintenance` label
- Detect priority from your description
- Post maintenance guidelines
- Add appropriate status labels

## 🔍 Priority Detection Examples

### Critical Priority
Keywords: critical, urgent, production, outage
```
"This is a critical bug affecting production users"
"Urgent: Server outage detected"
```

### High Priority
Keywords: important, high, blocking
```
"This is a high priority feature request"
"Blocking issue preventing deployment"
"Important: Security vulnerability found"
```

### Medium Priority
Keywords: medium, normal (or default)
```
"This is a medium priority task"
"Normal maintenance work"
```

### Low Priority
Keywords: low, nice-to-have, minor
```
"Low priority enhancement"
"Nice-to-have feature for future"
"Minor UI improvement"
```

## 📊 What Happens Automatically

### When You Create an Issue:
1. ✅ System analyzes title and body for keywords
2. ✅ Category label assigned based on title
3. ✅ Priority label assigned based on title OR body
4. ✅ `needs-triage` label added
5. ✅ First-time contributor check performed
6. ✅ Type-specific response comment posted
7. ✅ Milestone assigned if high/critical priority
8. ✅ Status changed to `needs-review`

### For Epic Issues:
9. ✅ 4 sub-issues created with structured naming
10. ✅ Sub-issues linked to parent epic
11. ✅ Parent issue updated with task checklist
12. ✅ All sub-issues labeled with `enhancement` and `needs-review`

## 🛠️ Workflow Files

- **Workflow:** `.github/workflows/issue-automation.yml`
- **Templates:**
  - `.github/ISSUE_TEMPLATE/bug_report.md`
  - `.github/ISSUE_TEMPLATE/feature_request.md`
  - `.github/ISSUE_TEMPLATE/maintenance_report.md`

## 📈 Monitoring

View workflow runs and automation status:
- **Actions Tab:** https://github.com/quonyabram/mcpmark-cicd/actions
- **Workflow:** "Issue Management Automation"

## 💡 Tips

1. **Use Keywords Wisely:** Include priority keywords naturally in your description
2. **Be Specific:** Clear titles help the automation categorize correctly
3. **Use Templates:** Templates ensure you provide all necessary information
4. **Check Labels:** Review auto-assigned labels and adjust if needed
5. **Track Epics:** Monitor the task checklist to track epic progress

## 🤝 Contributing

This automation system helps maintain consistency and organization. When creating issues:
- Follow the templates
- Use clear, descriptive titles
- Include priority indicators naturally in your description
- Review the auto-assigned labels and milestone

The system is designed to save time while maintaining high-quality issue tracking!

## 📞 Questions?

If you have questions about the automation system or need help:
- Check the workflow runs in the Actions tab
- Review existing issues for examples
- Contact the repository maintainers

---

**Automation Version:** 1.0  
**Last Updated:** 2025-11-21
