# 👋 Hi, I’m Eshwar Reddy Thippeswamy (@ESHWARGEEK)

I am a Computer Science and Engineering student (Class of 2026) at SJM Institute of Technology, passionate about building intelligent full-stack applications and automated systems.

- 👀 **I’m interested in:** Full-stack web development, Generative AI integration, and automated test engineering.
- 🌱 **I’m currently learning:** Advanced applications using Python, TypeScript, React, Node.js, LangChain, and the Google Gemini API.
- 💼 **I'm currently working as:** A Python Automation Intern at Alethea Communications Technologies, focusing on Python automation. I previously completed AI and full-stack internships at KodNest, Tublian, and AICTE.
- 🚀 **Projects I'm proud of:** **CareerNova** (an AI-powered resume analyzer built with React, Express, and Gemini) and **HabitLoop** (a food logging and momentum tracker).
- 🏆 **Milestones:** Top 10 Finalist at the Google Cloud Gen AI Exchange Hackathon and selected for the AWS AI and ML Scholars Program.
- 💞️ **I’m looking to collaborate on:** Open-source AI initiatives (especially Google Summer of Code organizations) and innovative full-stack applications.
- 📫 **How to reach me:** eshwarreddy8382@gmail.com

## 🌍 Open Source Contributions

### [sktime](https://github.com/sktime/sktime) — a unified framework for machine learning with time series

| Type | Contribution | Status |
|------|--------------|--------|
| 🐞 Bug report | [#11785](https://github.com/sktime/sktime/issues/11785) — `IntervalSegmenter` with integer `intervals` silently drops the last time point of every interval | Reported |
| 🔧 Bug fix | [#11787](https://github.com/sktime/sktime/pull/11787) — fix `IntervalSegmenter` dropping last time point of int intervals | 🟡 In review |

**What I found:** When splitting time series into intervals, `IntervalSegmenter` stored interval end points as *inclusive* in `fit`, but sliced them as *exclusive* in `transform`. As a result, the last data point of every interval was lost (25% of the data in the reproducing example). The bug had gone unnoticed since at least 2022.

**What I did:**
- Reproduced and diagnosed the bug, traced it to the inclusive/exclusive mismatch, and confirmed it predates a 2022 refactor of the module
- Fixed the integer path of `_fit` to store exclusive end points, consistent with `iloc` slicing and with `RandomIntervalSegmenter`
- Added a parametrized regression test that fails on `main` and passes with the fix
- Verified the change against sktime's full estimator conformance suite (`check_estimator`)

<!---
ESHWARGEEK/ESHWARGEEK is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
