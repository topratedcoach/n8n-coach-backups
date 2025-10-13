# TopRatedCoachAI Workflow Backups

> Automated daily backups of all n8n workflows tagged with "TopRatedCoachAI"

## 📊 Backup Summary

- **Last Updated**: 2025-10-13 07:00:35 UTC
- **Total Workflows**: 1
- **Active Workflows**: 1
- **Repository**: [topratedcoach/n8n-coach-backups](https://github.com/topratedcoach/n8n-coach-backups)
- **Backup Frequency**: Daily at 3:00 AM UTC

---

## 📋 Workflow Index

### 1. 🔔 Post Call Webhook Trigger

- **Workflow ID**: `5q23rjNh39FQdAxa`
- **Status**: ✅ Active
- **Last Backup**: 2025-10-13 07:00:35 UTC
- **File**: [backups/top-rated-coach-ai/5q23rjNh39FQdAxa.json](./backups/top-rated-coach-ai/5q23rjNh39FQdAxa.json)
- **Direct Link**: [View on GitHub](https://github.com/topratedcoach/n8n-coach-backups/blob/main/backups/top-rated-coach-ai/5q23rjNh39FQdAxa.json)

---

## 🔧 How to Use These Backups

### Restore a Workflow to n8n

1. Navigate to **backups/top-rated-coach-ai/** folder above
2. Click on any workflow file
3. Click the **Raw** button on GitHub
4. Copy the entire JSON content
5. In n8n:
   - Go to **Workflows** → **Add workflow**
   - Click **Import from URL or File**
   - Paste the JSON and click **Import**

### View Workflow History

Each workflow file maintains its complete version history in Git:

```bash
# View all changes to a specific workflow
git log backups/top-rated-coach-ai/{workflow-id}.json

# Compare two versions  
git diff HEAD~5 HEAD backups/top-rated-coach-ai/{workflow-id}.json

# See what changed in a specific commit
git show {commit-hash}
```

### Search for Workflows

- **In this README**: Press `Ctrl+F` and search by workflow name
- **In GitHub**: Press `t` to open file finder and search
- **In Git**: `git log --all --grep="workflow-name"`

---

## 📁 Repository Structure

```
n8n-coach-backups/
├── README.md                      ← You are here
└── backups/
    └── top-rated-coach-ai/
        ├── 5q23rjNh39FQdAxa.json  (Post Call Webhook Trigger)
        ├── CcHBrELrSsWhXNYT.json  (PreCall Initial Data)
        ├── E7kXqgU4iMB7Gzl5.json  (Delete USER - DANGER)
        └── ... (1 total workflow files)
```

---

## 🎯 Key Features

### ✅ Stable Filenames
Files are named by workflow ID (e.g., `5q23rjNh39FQdAxa.json`) which:
- **Never changes** even when you rename the workflow
- **Prevents duplicates** when workflow names change
- **Maintains clean Git history** for each workflow

### 📝 Complete Backups
Each backup includes:
- All nodes and their configurations
- Connections between nodes
- Workflow settings and metadata
- Credential references (IDs only, not actual secrets)

### 📚 Version History
Every change is tracked:
- See exactly what changed in each backup
- Compare any two versions
- Restore to any previous state

### 🤖 Auto-Generated
This README updates automatically:
- Regenerated with each backup run
- Always shows current workflow names
- Automatically sorted alphabetically

---

## ⚠️ Important Notes

### Security
- ✅ Workflow files contain credential **IDs** only
- ❌ Actual credentials (passwords, API keys) are **never** backed up
- ✅ Safe to store in public/private repositories

### File Naming Convention
- **Format**: `{workflow-id}.json`
- **Example**: `5q23rjNh39FQdAxa.json`
- **Benefit**: Renaming a workflow updates the same file (no duplicates)
- **Workflow name**: Stored inside the JSON and in this README

### Backup Scope
- ✅ Only workflows tagged with **"TopRatedCoachAI"**
- ✅ Includes both active and inactive workflows
- ❌ Workflows without this tag are not backed up

---

## 🚀 Automation Details

### The Backup Workflow

This backup system is built using n8n itself:

- **Workflow Name**: Backup TopRatedCoachAI Workflows to GitHub
- **Workflow ID**: `vunHkbizyUk9GJ61`
- **Schedule**: Daily at **3:00 AM UTC**
- **Execution Time**: ~30-60 seconds

### Backup Process

1. **Discovery**: Finds all workflows with tag "TopRatedCoachAI"
2. **Export**: Gets complete workflow JSON from n8n API
3. **Prepare**: Converts to Base64 for GitHub API
4. **Check**: Determines if file exists (update vs create)
5. **Commit**: Uploads to GitHub with descriptive commit message
6. **Index**: Updates this README with current workflow list
7. **Report**: Sends success/error summary

### Recent Runs

- **Last Successful Run**: 2025-10-13 07:00:35 UTC
- **Workflows Backed Up**: 1
- **Status**: ✅ All workflows backed up successfully

---

## 📊 Statistics

### Overall
- **Total Workflows**: 1
- **Active**: 1
- **Inactive**: 0

### By Category
- **Triggers & Webhooks**: 1

---

## 🔧 Configuration

### Environment Variables Required

```bash
GITHUB_OWNER="topratedcoach"
GITHUB_REPO="n8n-coach-backups"
```

### Credentials Required

1. **n8n API Credentials**
   - Access to workflow list and details
   - Used by "Get All n8n Workflows" node

2. **GitHub OAuth2 Credentials**  
   - Repository write access
   - Used by all GitHub nodes

---

## 📞 Support & Troubleshooting

### Common Issues

**❓ README not updating**
- Check: GitHub credentials have write permission
- Check: Repository name and owner are correct
- Solution: Run workflow manually and check execution logs

**❓ Workflows showing as "Unknown"**
- Check: "Prepare GitHub File Data" node is passing metadata
- Solution: Verify `workflowName` and `workflowId` in node output

**❓ Backup failed for some workflows**
- Check: Execution logs for specific errors
- Check: GitHub API rate limits
- Solution: Review error summary in workflow output

### Need Help?

1. Check the backup workflow execution logs in n8n
2. Verify all credentials are properly configured
3. Ensure environment variables are set correctly
4. Review the [n8n documentation](https://docs.n8n.io)

---

## 🎨 Customization

Want to modify this backup system? Here's what you can customize:

### Change Backup Location
Edit `filePath` in "Prepare GitHub File Data" node:
```javascript
filePath = `your-custom-path/${fileName}`
```

### Change Schedule
Edit cron expression in "Schedule Trigger" node:
```
0 3 * * *  → Daily at 3 AM
0 */6 * * * → Every 6 hours
0 0 * * 0  → Weekly on Sunday
```

### Filter Different Workflows
Edit tag filter in "tags: "YourCustomTag"
```

---

## 📜 License & Usage

These backups are for internal use of the TopRatedCoachAI n8n instance. 

- ✅ Safe to clone/fork for your own n8n backup needs
- ✅ Modify and adapt as needed
- ❌ Workflow credentials are not included (by design)

---

*This README is auto-generated by the n8n backup workflow.*  
*Last updated: 2025-10-13 07:00:35 UTC*  
*Maintained by: n8n Backup Automation*
