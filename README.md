HR-Analytics-Dashboard
An interactive 4-page Power BI dashboard analyzing employee  attrition across 594 employees
An interactive 4-page Power BI dashboard that analyzes employee attrition across 594 employees. It helps HR teams understand who is leaving, when they leave, and why — by breaking attrition down by job role, tenure, age, gender, marital status, department, overtime, business travel, and salary.

📌 Key Insights
Metric	Value
👥 Total Employees	594
✅ Active Employees	448
🚪 Attrition Count	146
📉 Attrition Rate	24.6%
💰 Avg Monthly Income	4K
🎂 Average Age	28
📅 Average Tenure	5.04 years

🔍 What the data reveals
Highest attrition occurs in Year 1 of tenure — 41 employees left within their first year.
Laboratory Technicians have the highest attrition by job role (44 leavers), followed by Research Scientists (34) and Sales Executives (28).
A secondary spike appears at Year 10 (10 leavers), suggesting a mid-career retention issue.
Overtime, business travel frequency, and lower salary slabs are strongly correlated with higher attrition.

🖥️ Dashboard Pages
Page 1 — Overview
KPI cards + attrition by job role + attrition by years at company, with global slicers.

Page 2 — Attrition KPIs
High-level attrition rate and count with breakdown visuals by gender, age group, department, overtime, business travel, salary slab, job role, and salary distribution.

Page 3 — Detailed Breakdown
Drill-down analysis across multiple dimensions for deeper HR investigation.

Page 4 — Insights 
Summary of findings.

🛠️ Skills & Tools Used
Power Query

Data cleaning and transformation

Creating custom Age Groups and Salary Slabs

DAX Measures

Attrition Rate

Attrition Count

Active Employees

Average Tenure

Average Monthly Income

Power BI Features

Interactive visuals (bar, line, donut, matrix, card)

Slicers (Age Group, Department, Over Time, Gender)

Drill-through pages

Navigation buttons

Custom dashboard design

🎛️ Interactive Slicers
Every visual on the dashboard is filtered simultaneously by:

Age Group

Department

Over Time

Gender

📈 DAX Measures (Preview)
dax
Attrition Count = 
CALCULATE(
    COUNT(HR[EmployeeNumber]),
    HR[Attrition] = "Yes"
)

Attrition Rate = 
DIVIDE([Attrition Count], [Total Employees], 0)

Active Employees = 
CALCULATE(
    COUNT(HR[EmployeeNumber]),
    HR[Attrition] = "No"
)

Average Tenure = 
AVERAGE(HR[YearsAtCompany])

Average Monthly Income = 
AVERAGE(HR[MonthlyIncome])
Full list of measures available in dax/measures.md.

💡 Recommendations
Based on the analysis, HR teams should consider:

Strengthen onboarding & first-year engagement — most attrition happens in Year 1.

Review compensation for Laboratory Technicians and Research Scientists — the two highest-attrition roles.

Manage overtime — employees working overtime show significantly higher attrition.

Address the Year-10 spike — introduce mid-career growth and retention programs.

Travel policy review — frequent business travelers leave more often.

🤝 Contributing
Contributions, suggestions, and feedback are welcome!

Fork the repo

Create a feature branch (git checkout -b feature/improvement)

Commit changes (git commit -m "Add improvement")

Push and open a Pull Request

📄 License
This project is licensed under the MIT License — see the LICENSE file for details.

👤 Author
Your Name

GitHub: @your-username

LinkedIn: Your Profile

⭐ If you found this project useful, please give it a star!

📝 What to do next:
Copy the README above into a file named README.md

Replace <your-username>, Your Name, and LinkedIn with your details

Add your screenshots to docs/screenshots/

Upload your .pbix into powerbi/

Want me to also write the .gitignore and dax/measures.md files to complete the repo? Just say the word 👍

whatare you doing
Sorry — I may have gone too far! 😅

You asked me to write the full README.md for your GitHub repo, so that's what I did in my last message — I wrote a complete, ready-to-use README for your HR Analytics Dashboard project.

But I also added a bunch of extra stuff (repo structure, next steps, offers to write more files). If that felt like too much, that's on me.

Let me reset. Just tell me what you actually want:

✅ Just the README.md → (already done above, you can copy it)

📝 README + .gitignore + dax/measures.md

🚀 Step-by-step git commands to push everything to GitHub

🤔 Something else entirely

What do you need?

Unable to render code block i upload pdf in attach files section it says this
Ah, I understand now! You're trying to upload your PDF into GitHub's web interface, and when you drag it into the "attach files" section, GitHub shows:

"Unable to render code block"

That's a GitHub rendering limitation, not an error with your file. Here's what's happening and how to fix it 👇

🔍 Why this happens
When you upload a PDF (or .pbix, .zip, images with unusual content) to GitHub's "attach files" box in an Issue, Comment, or README editor, GitHub tries to preview/render it inline.

Your PDF contains:

Tables that look like code blocks (the "1 1 1 1..." rows on page 3)

Images/screenshots

Mixed formatting

GitHub's markdown renderer gets confused and throws: "Unable to render code block" because it thinks your PDF content is broken markdown/code.

✅ The Fix — Don't use "attach files"
Instead, upload the PDF properly as a repository file:

Option 1: Upload via GitHub web UI (easiest)
Go to your repo on github.com

Click "Add file" → "Upload files"

Drag your PDF into the upload area (not the comment/attach box)

Put it in a folder like docs/ → e.g. docs/HR_Analytics_Dashboard.pdf

Scroll down → Commit changes

✅ This stores the PDF as a real file — no rendering issues.

Option 2: Reference it in README (correct way)
In your README.md, link to the file instead of attaching it:

markdown
## 📄 Project Report

[Download the full HR Analytics Dashboard PDF](docs/HR_Analytics_Dashboard.pdf)
Or embed a preview:

markdown
[![Dashboard PDF](docs/screenshots/page1.png)](docs/HR_Analytics_Dashboard.pdf)
Option 3: Upload via Git command line
bash
git add docs/HR_Analytics_Dashboard.pdf
git commit -m "Add project PDF report"
git push origin main
⚠️ Also — GitHub doesn't render .pbix files
Just so you know: GitHub cannot preview Power BI .pbix files either. It will store them, but visitors can only download them. That's why having screenshots in your README is important — people can see the dashboard without opening Power BI.



markdown
![Page 1](docs/screenshots/page1.png)

📄 [View full PDF report](docs/HR_Analytics_Dashboard.pdf)
Quick question so I can help precisely:
Are you trying to upload the PDF into the README, or as a separate file in the repo?

Is this in the "Add file → Upload files" section, or the comment/issue box?

Tell me which screen you're on and I'll walk you through it step by step 👍

