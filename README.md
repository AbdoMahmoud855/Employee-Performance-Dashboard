# 📊 Employee Performance & Workforce Dashboard

> An interactive Excel dashboard that tells the story of **689 employees** across **5 countries** and **20 departments**, hired between 2016 and 2020. Instead of staring at tables, the dashboard answers real questions: Who is working the most overtime? Where are the pay gaps? Who takes the most leave? How is performance distributed across countries?

---

## 🗂️ Project Contents

| File | Description |
|---|---|
| `Book1.xlsx` | The complete Excel workbook |
| ↳ `Employees` sheet | Raw data (689 rows × 14 columns) |
| ↳ `pivotTable` sheet | All the Pivot Tables that feed the charts |
| ↳ `Employee PerformanceDashboard` sheet | **Page 1** of the dashboard (overview) |
| ↳ `details` sheet | **Page 2** (deeper drill-down) |

**Data columns:** `No` · `Full Name` · `Gender` · `Start Date` · `Years` · `Department` · `Country` · `Center` · `Monthly Salary` · `Annual Salary` · `Job Rate` · `Sick Leaves` · `Unpaid Leaves` · `Overtime Hours`

---

## ❓ Questions This Dashboard Answers

### Page 1: Overview

**KPI cards: "Where do we stand right now?"**
- The company spends **$17M** on salaries.
- It has **689 employees**.
- They worked **9,441 overtime hours**, costing **$155K**.

| Chart | Question | Short Answer |
|---|---|---|
| Hires by Quarter | Does hiring follow a seasonal pattern? | No, hiring is steady. Q2 is highest (181) and Q3 lowest (160). |
| Leave Days by Gender & Country | Who takes the most leave, and from which country? | Men (1,106 days) take more than women (526), and Egypt has the largest share (908), but this reflects headcount, not behavior. |
| Avg Salary by Center | Does one center pay more? | East pays **$2,274**, about 15% above South (**$1,981**). |
| Overtime per Department | Which departments are running at full capacity? | Quality Control and Manufacturing (about 1,700 hours each). |
| Performance Flag per Country | How is performance distributed across countries? | 339 bonuses vs 142 deductions, with similar proportions in every country. |
| Split Gender | What is the gender makeup? | 65% men and 35% women. |

### Page 2: Details

| Chart | Question | Short Answer |
|---|---|---|
| Salary by Dept (Male vs Female) | Is there a pay gap between men and women? | Not company-wide ($14 difference), but yes inside specific departments (e.g., Research Center: $2,051 vs $1,230). |
| Sick Leaves per Department | Where are sick leaves concentrated? | In Manufacturing (197) and the departments with the highest overtime. |
| Top 10 Overtime | Who is carrying the overtime? | 3 of the top 4 are from Quality Control, led by Omar Hishan with 198 hours. |
| Job Rate Distribution | How are job ratings distributed? | 49% of the team sits in the top two tiers (4.5 and 5). |

### Questions That Emerge From Combining Charts

- **Does workload affect health?** Yes. The departments with the most overtime are also the ones with the most sick leave.
- **Is overtime distributed fairly?** No. It is concentrated in a few people and departments.
- **Is evaluation consistent across branches?** Most likely, since Bonus and Deduction ratios are similar in every country.

> 💡 The slicers let you ask any of these questions for a specific slice, for example: *"What does the picture look like for women in the East center?"*

---

## 🎨 Dashboard Design

The dashboard follows a clean, consistent **blue-teal corporate theme** so the numbers stay the focus and nothing competes for attention.

### Color Palette

| Role | Color | Where it's used |
|---|---|---|
| **Header banner** | Teal blue | Title bar at the top of both pages, with a white bold title |
| **KPI cards & filter panel** | Deep navy-teal | Dark backgrounds with white text for maximum contrast |
| **Chart titles** | Bright sky blue | Makes every chart title easy to spot against the light cards |
| **Chart series** | Dark teal + light blue | Two-tone bars and pie slices (e.g., Female = dark, Male = light) |
| **Page background** | Pale blue-gray | Soft canvas that lets the cards stand out |

### Layout

**Page 1: Overview**

<img width="1403" height="713" alt="image" src="https://github.com/user-attachments/assets/a546ceca-9106-4a2b-9468-78106f48de17" />




**Page 2: Details**

<img width="1191" height="625" alt="image" src="https://github.com/user-attachments/assets/ed587180-1856-4195-a20d-9bf9c21f0602" />


---

## 🎛️ Filters (Slicers), Left Side of Both Pages

The slicers control **every chart at once**, so you can zoom into any slice of the company:

- **Start Date (Year):** 2016 → 2020
- **Job Rate:** job rating from 1 (lowest) to 5 (highest)
- **Gender:** Female / Male
- **Unpaid Leaves:** number of unpaid leave days
- **Center:** East / Main / North / South / West

> 💡 **Try it:** select `Center = East` and `Gender = Female` and watch the whole dashboard retell the story for just that group.

---

# 📄 Page 1: Overview

## 🔢 Part 1: KPI Cards

> **The story:** The moment you open the dashboard, these numbers tell you "where we stand" in five seconds.

| Card | Value | The Story |
|---|---|---|
| 💰 **Total Net Salary** | **$17,063,373** | The total the company spends on salaries. A big number that frames the scale of everything that follows. |
| 👥 **Number Of Employees** | **689** | The size of the whole team. Every later analysis is measured against this number. |
| ⏱️ **Total Overtime Hours** | **9,441 hours** | The team worked over 9,000 extra hours, about **13.7 hours per employee** on average. The key question: is this heavy workload or weak planning? |
| 💵 **TotalOverTimePay** | **$155,095.14** | What the company paid for those extra hours: about **$16.43 per overtime hour** on average (155,095 ÷ 9,441). Roughly **0.9%** of the total salary bill, so overtime is a small cost but a big workload signal. |

> ℹ️ **Extra figures from the pivot sheet:** average monthly salary **$2,068** · average Job Rate **3.59 out of 5** · total overtime pay **$155,095**.

---

## 📈 Chart 1: Number of Hires by Quarter

**Type:** Line chart · **Question:** Does hiring follow a seasonal pattern?

> **The story:** The company hires **at a steady rhythm all year**. Q2 is the busiest with **181** hires, followed by Q4 with **180**, then Q1 with **168**. Q3 is the quietest with **160**.
>
> The curve forms a wave, but the gap between the highest and lowest quarter is only about **21 hires**. There is no sharp "hiring season"; recruitment is continuous and balanced.

**Takeaway:** Summer (Q3) is the calmest hiring period. If you plan a recruitment drive, Q2 is when the company is already most active.

---

## 🏖️ Chart 2: Total Leave Days by Gender and Country

**Type:** Clustered column with data labels · **Question:** Who takes the most leave, and from which country?

> **The story:** Total leave days are **1,632**. Men took **1,106 days** versus **526 days** for women.
>
> But **before concluding that men take more leave**, remember that men make up **65%** of the workforce. Much of the gap comes from headcount, not behavior.
>
> **Egypt** accounts for the largest share (**908 days**), followed by the UAE (**372**), Saudi Arabia (**191**), Syria (**134**), and Lebanon (**27**). That makes sense: Egypt has **379** employees, more than half the team.

> The data labels make the split easy to read. **Men:** Egypt **579**, UAE **272**, Saudi Arabia **125**, Syria **121**, Lebanon **9**. **Women:** Egypt **329**, UAE **100**, Saudi Arabia **66**, Lebanon **18**, Syria **13**.

**Takeaway:** Absolute numbers can mislead. A better metric is "leave days per employee" for each country.

---

## 💵 Chart 3: Average Monthly Salary by Center

**Type:** Column chart · **Question:** Does one center pay more than the others?

> **The story:** Four centers are very close in monthly average (between **$1,981** and **$2,069**), but **the East center** clearly stands out at **$2,274**, roughly **$200** above the rest.
>
> The lowest is **South** at **$1,981**. The gap between East and South is about **15%**.

**Takeaway:** East is the standout center on pay. The open question is why: higher-level roles, more experience, or a geographic premium?

> ✅ The Y-axis now starts at zero, so the bars are honest. The consequence: the five centers look much closer than before, and East's lead (about 15% over South) is visible but modest. The numbers tell the story better than the bars here, so consider adding data labels.

---

## ⏰ Chart 4: Total Overtime Per Department

**Type:** Column chart · **Question:** Which departments are running at full capacity?

> **The story (from the actual overtime data):** Two departments dominate the picture:
> - **Quality Control: 1,700 hours**
> - **Manufacturing: 1,699 hours**
>
> Together they account for more than **35%** of all overtime. Next come Account Management (**1,264**), Quality Assurance (**771**), and Facilities/Engineering (**605**).
>
> The lowest departments (Green Building, Research/Development) barely need overtime at all.

**Takeaway:** Quality Control and Manufacturing are the "pressure core" of the company, and likely candidates for additional headcount.

> ✅ The chart now correctly plots `Sum of Overtime Hours`, so the values on screen (1,700 / 1,699 / 1,264…) match the story above.

---

## 🏆 Chart 5: Performance Flag per Country

**Type:** Horizontal bar · **Question:** How is performance distributed across countries?

> **The story:** Each employee carries one of three performance flags:
> - 🟢 **Bonus:** Egypt **181** · UAE **80** · Saudi Arabia **51** · Syria **23** · Lebanon **4**
> - 🟡 **Safe Zone:** Egypt **121** · UAE **42** · Saudi Arabia **24** · Syria **17** · Lebanon **4**
> - 🔴 **Deduction:** Egypt **77** · UAE **34** · Saudi Arabia **15** · Syria **13** · Lebanon **3**
>
> In total: **339 bonuses** versus **142 deductions**, roughly **2.4 employees earning a bonus for every one facing a deduction**. A healthy signal.

**Takeaway:** The proportions are similar across countries (about 49% Bonus overall), which suggests evaluation criteria are applied consistently across branches.

---

## 🥧 Chart 6: Split Gender

**Type:** Pie chart · **Question:** What is the gender makeup of the company?

> **The story:** The team is **65.17% men** (449 employees) and **34.83% women** (240 employees).
>
> That's roughly two women for every four men. The gap exists, but a 35% share for women is reasonable for manufacturing-heavy industries.

**Takeaway:** If the goal is better balance, hiring should focus on departments where women are least represented.

---

# 📄 Page 2: Details

> **The overall story:** If Page 1 is the "view from above," this page is the "microscope." It zooms in on differences between departments and individuals.

---

## ⚖️ Chart 7: Average Monthly Salary by Department, Male vs Female

**Type:** Clustered column · **Question:** Is there a pay gap between men and women?

> **The story:** Company-wide the gap is **nearly zero**: women **$2,059** vs men **$2,073** (a difference of just **$14**). But drill into departments and the picture changes completely:
>
> **Departments where women earn more:**
> - Environmental Health/Safety: women **$2,852** vs men **$1,757** 🔺
> - Major Mfg Projects: **$2,778** vs **$1,921**
> - Facilities/Engineering: **$2,599** vs **$2,120**
>
> **Departments where men earn more:**
> - Environmental Compliance: men **$2,720** vs women **$2,031**
> - Training: **$2,472** vs **$2,030**
> - Research Center: **$2,051** vs **$1,230** 🔻 (the largest gap in men's favor)
>
> The highest-paying department on average is **Human Resources ($2,556)**; the lowest is **Research Center ($1,887)**.

**Takeaway:** The company-wide average hides large gaps inside individual departments. The balanced total exists because the gaps cancel each other out.

> ⚠️ **Caution:** Some departments are small (e.g., Environmental Health/Safety), so one employee can swing the average. Also, **Manufacturing Admin** has men only.

---

## 🤒 Chart 8: Sick Leaves per Department

**Type:** Column chart · **Question:** Where are sick leaves concentrated?

> **The story:** Total sick leave is **1,109 days**. **Manufacturing** leads with **197 days**, followed by Account Management (**143**), Quality Control (**135**), Quality Assurance (**124**), and Facilities/Engineering (**117**).
>
> These are largely the same departments with the highest overtime. **Not a coincidence**: the departments under the most pressure also take the most sick leave.
>
> At the other end, Green Building (**6**) and Research/Development (**7**) are the calmest.

**Takeaway:** There is a clear link between workload and sick leave. That alone justifies reviewing workloads in Manufacturing and Quality Control.

---

## 👤 Table: Top 10 — Overtime Hours

**Type:** Pivot table · **Question:** Who is carrying the overtime?

> **The story:**
>
> | # | Name | Department | Overtime Hours |
> |---|---|---|---|
> | 1 | Omar Hishan | Quality Control | **198** |
> | 2 | Ailya Sharaf | Major Mfg Projects | **192** |
> | 3 | Ghadir Hmshw | Quality Control | **183** |
> | 4 | Farahad Husayn | Quality Control | 153 |
> | 5 | Muhamad Alrifaei | Account Management | 153 |
> | 6 | Muhamad Eurul | Quality Assurance | 148 |
> | 7 | Ahmad Bikri | Manufacturing | 121 |
> | 8 | Iin Alhalaliu | Sales | 116 |
> | 9 | Riad Sahalul | Training | 111 |
> | 10 | Bilal Jalal | Manufacturing Admin | 109 |
>
> **Three of the top four** are from **Quality Control**. The top employee logged **198** extra hours, about **25 full working days** (assuming 8-hour days).

**Takeaway:** Overtime is **concentrated in a few people**. That is both a risk (burnout) and an opportunity (redistributing work).

---

## 🎯 Chart 9: Job Rate Distribution (1 = low, 5 = high)

**Type:** Pie chart · **Question:** How are job ratings distributed?

> **The story (from the data):**
>
> | Job Rate | Employees | Share |
> |---|---|---|
> | 5 | 215 | 31.2% |
> | 3 | 208 | 30.2% |
> | 4.5 | 124 | 18.0% |
> | 2 | 72 | 10.4% |
> | 1 | 70 | 10.2% |
>
> About **49% of the team** sits in the top two tiers (4.5 and 5), and only **20%** in the bottom two. The average rating is **3.59 out of 5**, and the distribution leans toward high performance.

**Takeaway:** A strong team. The group to watch is the **142 employees** in the lowest two tiers, especially those in high-overtime departments.

> ✅ The pie now plots `Count of Job Rate`, so the slices (70 / 72 / 208 / 124 / 215) match the table above.

---

# 🧩 The Whole Story in 6 Sentences

1. The company has **689 employees** and spends **$17M** on salaries.
2. Hiring is **steady** throughout the year, with Q2 the highest.
3. **Egypt** is the core (55% of the team), with the UAE second.
4. The **East center** pays roughly 10-15% more than the others.
5. **Quality Control and Manufacturing** are the biggest pressure points: overtime plus sick leave.
6. The overall male/female pay gap is zero, but it is **large inside specific departments**.

## 🧰 Tools Used

- **Microsoft Excel:** Pivot Tables · Pivot Charts · Slicers
- **Calculated fields:** Average Job Rate · Total Overtime Pay · Female% · Performance Flag
- **Dashboard design:** icons + shapes + navigation arrows (⬅️ ➡️) between the two pages

## 🚀 How to Use the Dashboard

1. Open `Book1.xlsx` and go to the **Employee PerformanceDashboard** sheet.
2. Use the **slicers** on the left to filter the data.
3. Click the **➡️ arrow** to go to the details page.
4. Click the **⬅️ arrow** to go back.
5. If you change the data: **Data → Refresh All**.

---

<p align="center">⭐ If you like this dashboard, leave a star on the project!</p>
