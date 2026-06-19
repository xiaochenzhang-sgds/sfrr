# ⚡ RuleOps — Salesforce Recommendation Rule Manager

> *Because manually hunting through Salesforce rules should be illegal* 🚫

A slick, browser-based tool built for **US** to manage recommendation rules without drowning in Salesforce. Upload a CSV, make your changes, export, done. ✅

---

## 🚀 Live App

👉 **[Open RuleOps](https://xiaochenzhang-sgds.github.io/sfrr)**

> Works best on Chrome. No login. No install. Just vibes. ✨

---

## 🎯 What it does

- 👥 See every team member and their assigned rules at a glance
- ✏️ Edit rule parameters — localities, lead sources, vendor grades, operations, verticals
- ➕ Assign agents to existing rules or spin up brand new ones
- 🚨 Instantly spot agents with **no rules** or **incomplete profiles**
- 🔄 Replace former agents in active rules (bye Jonathan 👋)
- 📤 Export a Salesforce-ready CSV in the exact bulk upload format

---

## 🔄 The Workflow

### After making changes in Salesforce

```
Salesforce export → Upload Rules CSV → Make adjustments → Export CSV → Upload back to Salesforce
```

1. Export your latest rules from Salesforce
2. Click **↑ Upload Rules** in the app
3. Tweak whatever needs tweaking
4. Hit **↓ Export CSV**
5. Import back into Salesforce 🎉

### New joiner? No problem 🙋

1. Find them in the sidebar (they'll have a 🔴 red dot)
2. Click **Edit Profile** → set their account sources & business types
3. Click **+ Assign to existing rule** or **+ New rule**
4. Export & import to Salesforce — done!

### Replacing a former agent 👋

1. Dashboard will shout at you with a red alert
2. Click **Replace agent** → pick someone from the list
3. Export CSV — new agent row appears with blank IDs (Salesforce handles the rest)
4. Manually delete the old agent's record in Salesforce

---

## 📂 Uploading CSVs

| Button | What to upload |
|---|---|
| **↑ Upload Rules** | Your Salesforce rules export (`existing_RR.csv`) |
| **↑ Upload Agents** | Your agent details sheet (`Agent_details.csv`) |

### Rules CSV format
```
Rule Name, Lead Source, Business Type, Vertical, Locality,
Vendor Grade, Applicable for Operation,
Recommendation Agent Name, Sales Agent: Full Name,
Recommendation Rule Agent ID
```
> 💡 `Vertical` is a new column we added — check with your Salesforce admin to map it on first import!

---

## 🗺️ Reference Values

**🔍 Lead Sources**
`Self Sign Up` · `Inbound` · `Own Research` · `Automated LeadGen` · `Import`

**🏢 Verticals**
`Restaurant` · `Shop`

**🍜 Business Types**
`Regular Restaurant` · `Home Based Kitchen` · `Street Food`

**⭐ Vendor Grades**
`AAA` · `AA` · `A` · `B` · `C` · `D` · `Ungraded`

**⚙️ Operations (currently active)**
- AccountRecycling
- OpportunityReassignment
- LeadConversion
- OpportunityAutoAssignment
- NewLeadConversion
- IncompleteSSULeadAutoAssignment
- OpportunityAutoAssignmentFromCase
- SSUAccountAutoAssignment

---

## 🚦 Status Indicators

| Dot | Meaning |
|---|---|
| 🟢 Green | Agent has rules — all good! |
| 🟡 Amber | Agent exists but has no rules assigned yet |
| 🔴 Red | Profile incomplete — no account source set |

---

## 💾 Data & Storage

- Everything lives in your **browser's local storage** — nothing goes to any server 🔒
- Each browser / device saves independently
- Hit **↺** (top right corner) to wipe everything and start fresh from defaults
- The app URL is public — please don't share it externally 🙅

---

## 🛠️ Updating the App

Got a new version of the file? Here's how to swap it in:

1. Go to your repo on GitHub
2. Click **Add file → Upload files**
3. Upload the new `index.html` (or `indexrr.html`)
4. Commit — GitHub Pages updates within ~60 seconds ⏱️

---

## 🧱 Built with

Pure HTML, CSS & vanilla JavaScript — no frameworks, no build tools, no drama.
Icons by [Tabler Icons](https://tabler-icons.io) 🎨

---

*Made with ☕ and mild frustration at manual Salesforce updates.*
