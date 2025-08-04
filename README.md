  adeetya-u - Visual Studio Code \* { margin: 0; padding: 0; box-sizing: border-box; } body { font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; background: #1e1e1e; color: #cccccc; overflow: hidden; } /\* Title Bar \*/ .title-bar { height: 30px; background: #3c3c3c; display: flex; align-items: center; justify-content: space-between; padding: 0 10px; font-size: 13px; } .window-controls { display: flex; gap: 5px; } .control-btn { width: 12px; height: 12px; border-radius: 50%; cursor: pointer; } .control-btn.close { background: #ff5f57; } .control-btn.minimize { background: #ffbd2e; } .control-btn.maximize { background: #28ca42; } .title-text { color: #cccccc; font-size: 13px; } /\* Main Container \*/ .vscode-container { display: flex; height: calc(100vh - 52px); position: relative; } /\* Activity Bar \*/ .activity-bar { width: 48px; background: #333333; border-right: 1px solid #444444; display: flex; flex-direction: column; align-items: center; padding: 10px 0; } .activity-item { width: 48px; height: 48px; display: flex; align-items: center; justify-content: center; cursor: pointer; margin-bottom: 5px; border-left: 2px solid transparent; position: relative; } .activity-item:hover { background: #2a2d2e; } .activity-item.active { background: #094771; border-left-color: #0078d4; } .activity-item svg { fill: #cccccc; width: 24px; height: 24px; } /\* Side Panel \*/ .side-panel { width: 300px; background: #252526; border-right: 1px solid #3e3e42; display: flex; flex-direction: column; } .panel-header { height: 35px; background: #2d2d30; display: flex; align-items: center; padding: 0 15px; font-size: 11px; text-transform: uppercase; color: #cccccc; font-weight: 600; letter-spacing: 0.5px; } .file-explorer { flex: 1; overflow-y: auto; } .folder { padding: 8px 16px; display: flex; align-items: center; font-size: 13px; color: #cccccc; cursor: pointer; } .folder:hover { background: #2a2d2e; } .folder-icon { margin-right: 8px; color: #dcb67a; } .file-item { padding: 6px 32px; display: flex; align-items: center; font-size: 13px; color: #cccccc; cursor: pointer; position: relative; } .file-item:hover { background: #2a2d2e; } .file-item.active { background: #094771; color: #ffffff; } .file-icon { margin-right: 8px; width: 16px; height: 16px; display: flex; align-items: center; justify-content: center; } .file-icon svg { width: 16px; height: 16px; } /\* VS Code File Icons \*/ .icon-markdown { fill: #519aba; } .icon-typescript { fill: #3178c6; } .icon-json { fill: #cbcb41; } .icon-package { fill: #8cc84b; } .icon-folder { fill: #dcb67a; } /\* Main Editor Area \*/ .editor-area { flex: 1; display: flex; flex-direction: column; } .tab-bar { height: 35px; background: #2d2d30; border-bottom: 1px solid #3e3e42; display: flex; align-items: center; } .tab { height: 35px; padding: 0 16px; display: flex; align-items: center; background: #1e1e1e; border-right: 1px solid #3e3e42; cursor: pointer; font-size: 13px; gap: 8px; } .tab.active { background: #1e1e1e; border-bottom: 2px solid #0078d4; } .tab-close { width: 16px; height: 16px; border-radius: 3px; display: flex; align-items: center; justify-content: center; font-size: 10px; color: #969696; } .tab-close:hover { background: #3e3e42; } .editor-content { flex: 1; background: #1e1e1e; padding: 20px; overflow-y: auto; font-family: 'Consolas', 'Courier New', monospace; font-size: 14px; line-height: 1.6; } .editor-content.welcome { display: flex; flex-direction: column; align-items: center; justify-content: center; font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; } .welcome-content { text-align: center; max-width: 500px; } .welcome-title { font-size: 28px; color: #cccccc; margin-bottom: 30px; font-weight: 300; } .shortcuts-section { text-align: left; margin-top: 30px; } .shortcut-item { display: flex; justify-content: space-between; align-items: center; padding: 12px 0; border-bottom: 1px solid #3e3e42; font-size: 14px; } .shortcut-keys { background: #3e3e42; padding: 4px 8px; border-radius: 3px; font-size: 11px; font-family: 'Consolas', 'Courier New', monospace; color: #cccccc; } .code-content { display: none; } .code-content.active { display: block; } .line-numbers { float: left; width: 50px; text-align: right; padding-right: 10px; color: #6e7681; user-select: none; } .code-line { margin-bottom: 2px; } .keyword { color: #569cd6; } .string { color: #ce9178; } .comment { color: #6a9955; } .property { color: #9cdcfe; } .number { color: #b5cea8; } .function { color: #dcdcaa; } /\* Status Bar \*/ .status-bar { height: 22px; background: #0078d4; display: flex; align-items: center; justify-content: space-between; padding: 0 10px; font-size: 12px; color: #ffffff; } .status-left, .status-right { display: flex; align-items: center; gap: 15px; } .status-item { display: flex; align-items: center; gap: 5px; cursor: pointer; } .status-item:hover { background: rgba(255, 255, 255, 0.1); padding: 2px 4px; border-radius: 2px; } /\* VS Code Icons \*/ .vscode-icon { width: 16px; height: 16px; fill: currentColor; } /\* Chat Pane (Cursor AI Style) \*/ .chat-pane { width: 350px; background: #252526; border-left: 1px solid #3e3e42; display: flex; flex-direction: column; } .chat-header { height: 35px; background: #2d2d30; display: flex; align-items: center; padding: 0 15px; font-size: 13px; color: #cccccc; font-weight: 600; border-bottom: 1px solid #3e3e42; } .chat-content { flex: 1; padding: 15px; overflow-y: auto; display: flex; flex-direction: column; } .chat-welcome { background: #2d2d30; border-radius: 8px; padding: 15px; margin-bottom: 15px; border-left: 3px solid #0078d4; } .chat-welcome h4 { color: #0078d4; margin-bottom: 8px; font-size: 14px; } .chat-welcome p { color: #cccccc; font-size: 12px; line-height: 1.4; margin-bottom: 8px; } .chat-input-container { padding: 15px; border-top: 1px solid #3e3e42; } .chat-input-wrapper { position: relative; background: #1e1e1e; border: 1px solid #3e3e42; border-radius: 6px; display: flex; align-items: flex-end; } .chat-input { flex: 1; background: transparent; border: none; color: #cccccc; font-size: 14px; padding: 12px 40px 12px 12px; resize: none; font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; outline: none; min-height: 20px; max-height: 100px; } .chat-input::placeholder { color: #6e7681; } .send-button { position: absolute; right: 8px; bottom: 8px; width: 28px; height: 28px; background: #0078d4; border: none; border-radius: 4px; cursor: pointer; display: flex; align-items: center; justify-content: center; transition: background 0.2s; } .send-button:hover { background: #106ebe; } .send-button:disabled { background: #3e3e42; cursor: not-allowed; } .send-button svg { width: 16px; height: 16px; fill: #ffffff; } .contact-options { display: flex; gap: 8px; margin-top: 10px; } .contact-btn { padding: 6px 12px; background: #0e639c; border: none; border-radius: 4px; color: #ffffff; font-size: 11px; cursor: pointer; text-decoration: none; display: flex; align-items: center; gap: 4px; transition: background 0.2s; } .contact-btn:hover { background: #1177bb; } .contact-btn svg { width: 12px; height: 12px; fill: currentColor; } /\* Cursor AI Style Input Options \*/ .input-options { display: flex; gap: 8px; margin-bottom: 10px; padding: 0 15px; } .option-btn { padding: 4px 8px; background: #3e3e42; border: none; border-radius: 4px; color: #cccccc; font-size: 11px; cursor: pointer; display: flex; align-items: center; gap: 4px; transition: background 0.2s; } .option-btn:hover { background: #4e4e52; } .option-btn.active { background: #0078d4; color: #ffffff; } .option-btn svg { width: 12px; height: 12px; fill: currentColor; } /\* Terminal Pane \*/ .terminal-pane { height: 200px; background: #1e1e1e; border-top: 1px solid #3e3e42; display: flex; flex-direction: column; } /\* Editor Container to hold both editor and terminal \*/ .editor-container { flex: 1; display: flex; flex-direction: column; } .terminal-header { height: 35px; background: #2d2d30; display: flex; align-items: center; padding: 0 15px; font-size: 13px; color: #cccccc; font-weight: 600; border-bottom: 1px solid #3e3e42; } .terminal-content { flex: 1; padding: 10px; font-family: 'Consolas', 'Courier New', monospace; font-size: 12px; line-height: 1.1; color: #cccccc; overflow-y: auto; } .terminal-line { margin-bottom: 0px; white-space: pre-wrap; } .terminal-prompt { color: #4ec9b0; } .terminal-command { color: #dcdcaa; } .terminal-output { color: #cccccc; } .terminal-error { color: #f44747; } .terminal-success { color: #4ec9b0; }

adeetya-u — portfolio

EXPLORER

📁 PORTFOLIO

Welcome.md

TS

About.ts

TS

Skills.ts

TS

Projects.ts

JSON

Analytics.json

JSON

Contact.json

Welcome.md

×

Adeetya Upadhyay
================

Full Stack Developer & ML Engineer | UIUC Student

![Adeetya's GitHub Stats](https://github-readme-stats.vercel.app/api?username=adeetya-u&show_icons=true&theme=dark&bg_color=252526&title_color=4ec9b0&text_color=cccccc&icon_color=0078d4&border_color=3e3e42&hide_border=true&show_owner=true&rank_icon=github)

![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=adeetya-u&layout=donut&theme=dark&bg_color=252526&title_color=4ec9b0&text_color=cccccc&border_color=3e3e42&hide_border=true&langs_count=6)

#### TECHNICAL SKILLS

Languages:

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54) ![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white) ![C++](https://img.shields.io/badge/c++-%2300599C.svg?style=for-the-badge&logo=c%2B%2B&logoColor=white) ![R](https://img.shields.io/badge/r-%23276DC3.svg?style=for-the-badge&logo=r&logoColor=white) ![SQL](https://img.shields.io/badge/mysql-%2300f.svg?style=for-the-badge&logo=mysql&logoColor=white) ![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E) ![TypeScript](https://img.shields.io/badge/typescript-%23007ACC.svg?style=for-the-badge&logo=typescript&logoColor=white) ![HTML5](https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white) ![CSS3](https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white) ![Bash](https://img.shields.io/badge/shell_script-%23121011.svg?style=for-the-badge&logo=gnu-bash&logoColor=white) ![COBOL](https://img.shields.io/badge/cobol-%23005AA0.svg?style=for-the-badge&logo=cobol&logoColor=white) ![JCL](https://img.shields.io/badge/jcl-%23FF6B35.svg?style=for-the-badge&logo=ibm&logoColor=white)

Frameworks:

![React](https://img.shields.io/badge/react-%2320232a.svg?style=for-the-badge&logo=react&logoColor=%2361DAFB) ![NodeJS](https://img.shields.io/badge/node.js-6DA55F?style=for-the-badge&logo=node.js&logoColor=white) ![Express.js](https://img.shields.io/badge/express.js-%23404d59.svg?style=for-the-badge&logo=express&logoColor=%2361DAFB) ![Flask](https://img.shields.io/badge/flask-%23000.svg?style=for-the-badge&logo=flask&logoColor=white) ![FastAPI](https://img.shields.io/badge/FastAPI-005571?style=for-the-badge&logo=fastapi) ![Redux](https://img.shields.io/badge/redux-%23593d88.svg?style=for-the-badge&logo=redux&logoColor=white) ![GraphQL](https://img.shields.io/badge/-GraphQL-E10098?style=for-the-badge&logo=graphql&logoColor=white)

Cloud Platforms:

![AWS](https://img.shields.io/badge/AWS-%23FF9900.svg?style=for-the-badge&logo=amazon-aws&logoColor=white) ![Azure](https://img.shields.io/badge/azure-%230072C6.svg?style=for-the-badge&logo=microsoftazure&logoColor=white) ![Google Cloud](https://img.shields.io/badge/GoogleCloud-%234285F4.svg?style=for-the-badge&logo=google-cloud&logoColor=white)

Systems & Architecture:

![PostgreSQL](https://img.shields.io/badge/postgres-%23316192.svg?style=for-the-badge&logo=postgresql&logoColor=white) ![MongoDB](https://img.shields.io/badge/MongoDB-%234ea94b.svg?style=for-the-badge&logo=mongodb&logoColor=white) ![SQLite](https://img.shields.io/badge/sqlite-%2307405e.svg?style=for-the-badge&logo=sqlite&logoColor=white)

Data and ML:

![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white) ![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white) ![scikit-learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white) ![TensorFlow](https://img.shields.io/badge/TensorFlow-%23FF6F00.svg?style=for-the-badge&logo=TensorFlow&logoColor=white) ![PyTorch](https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?style=for-the-badge&logo=PyTorch&logoColor=white)

Tools:

![Git](https://img.shields.io/badge/git-%23F05033.svg?style=for-the-badge&logo=git&logoColor=white) ![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white) ![GitHub Actions](https://img.shields.io/badge/github%20actions-%232671E5.svg?style=for-the-badge&logo=githubactions&logoColor=white) ![Postman](https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white) ![Figma](https://img.shields.io/badge/figma-%23F24E1E.svg?style=for-the-badge&logo=figma&logoColor=white)

### CURRENT FOCUS

Building ML pipelines, full-stack applications, and AI-powered solutions. Expected graduation May 2027.

Champaign, IL UIUC Actively Building

#### FEATURED PROJECTS

![TutorSwap Project](https://github-readme-stats.vercel.app/api/pin/?username=CS222-UIUC&repo=team-69-project&theme=dark&bg_color=252526&title_color=4ec9b0&text_color=cccccc&icon_color=0078d4&border_color=3e3e42&hide_border=true)

![Portfolio Repo](https://github-readme-stats.vercel.app/api/pin/?username=adeetya-u&repo=adeetya-u&theme=dark&bg_color=252526&title_color=4ec9b0&text_color=cccccc&icon_color=0078d4&border_color=3e3e42&hide_border=true)

![ReverseDCF Project](https://github-readme-stats.vercel.app/api/pin/?username=adeetya-u&repo=ReverseDCF&theme=dark&bg_color=252526&title_color=4ec9b0&text_color=cccccc&icon_color=0078d4&border_color=3e3e42&hide_border=true)

![GitHub Pages Portfolio](https://github-readme-stats.vercel.app/api/pin/?username=adeetya-u&repo=adeetya-u.github.io&theme=dark&bg_color=252526&title_color=4ec9b0&text_color=cccccc&icon_color=0078d4&border_color=3e3e42&hide_border=true)

[Email](mailto:adeetya.upadhyay@gmail.com) [LinkedIn](https://www.linkedin.com/in/adeetya-upadhyay/) [GitHub](https://github.com/adeetya-u)

Acta, Non Verba

1  
2  
3  
4  
5  
6  
7  
8  
9  
10  
11  
12  
13  
14  
15  
16  
17  
18  
19  
20  
21  
22  
23  
24  
25  
26  
27  
28  
29  
30

// About.ts - Developer Profile

interface Developer {

name: string;

role: string;

location: string;

education: string\[\];

interests: string\[\];

}

const developer: Developer = {

name: "Adeetya Upadhyay",

role: "Full Stack Developer & ML Engineer",

location: "Champaign, IL",

education: \[

"B.S. Computer Science & Advertising | UIUC | GPA: 3.80",

"B.S.L.A.S. Econometrics & Quantitative Economics | UIUC | GPA: 4.00"

\],

interests: \[

"Machine Learning Engineering",

"Full Stack Development",

"AI-powered Solutions",

"Cloud Architecture"

\],

status: "🔥 Actively building",

expectedGraduation: "May 2027"

};

export default developer;

1  
2  
3  
4  
5  
6  
7  
8  
9  
10  
11  
12  
13  
14  
15  
16  
17  
18  
19  
20  
21  
22  
23  
24  
25  
26  
27  
28  
29  
30  
31  
32  
33  
34  
35

// Skills.ts - Technical Skills & Expertise

interface TechStack {

languages: string\[\];

frameworks: string\[\];

cloud: string\[\];

databases: string\[\];

tools: string\[\];

}

const myTechStack: TechStack = {

languages: \[

"Python", "TypeScript", "JavaScript",

"Java", "C++", "R", "SQL", "COBOL", "JCL"

\],

frameworks: \[

"React", "Node.js", "Flask",

"FastAPI", "TensorFlow", "PyTorch"

\],

cloud: \[

"AWS (EC2, S3, RDS, Lambda)",

"Azure (Functions, Data Factory)",

"GCP (BigQuery, Pub/Sub)"

\],

databases: \[

"PostgreSQL", "SQLite", "MongoDB"

\],

tools: \[

"Git", "Docker", "CI/CD",

"Kubernetes", "Apache Spark"

\]

};

export { myTechStack };

1  
2  
3  
4  
5  
6  
7  
8  
9  
10  
11  
12  
13  
14  
15  
16  
17  
18  
19  
20  
21  
22  
23  
24  
25  
26  
27  
28  
29  
30  
31  
32  
33  
34  
35  
36  
37  
38  
39  
40

// Projects.ts - Portfolio Projects

interface Project {

name: string;

description: string;

techStack: string\[\];

status: "active" | "completed" | "in-development";

}

const projects: Project\[\] = \[

{

name: "TutorSwap Platform",

description: "Full-stack peer tutoring platform with AI-powered matching",

techStack: \["React", "Flask", "PostgreSQL", "Socket.IO"\],

status: "in-development"

},

{

name: "AI Grant Matcher",

description: "AI chatbot matching nonprofits with grants",

techStack: \["React", "Redux", "Flask", "OpenAI API"\],

status: "active"

},

{

name: "ML Forecasting Engine",

description: "Time-series forecasting for infrastructure predictions",

techStack: \["Python", "TensorFlow", "Apache Spark"\],

status: "completed"

},

{

name: "Enterprise Automation Tools",

description: "SAP integration and process automation suite",

techStack: \["Java", "SAP", "z/OS", "COBOL"\],

status: "active"

}

\];

export { projects };

1  
2  
3  
4  
5  
6  
7  
8  
9  
10  
11  
12  
13  
14  
15  
16  
17  
18  
19  
20  
21  
22  
23  
24  
25  
26  
27  
28  
29  
30

{

"name": "Adeetya Upadhyay",

"contact": {

"email": "adeetya.upadhyay@gmail.com",

"linkedin": "linkedin.com/in/adeetya-upadhyay",

"github": "github.com/adeetya-u"

},

"location": "Champaign, IL",

"availability": "Open to opportunities",

"experience": \[

{

"role": "Lead Consultant",

"company": "OTCR Consulting"

},

{

"role": "Senior Consultant",

"company": "Illinois Business Consulting"

}

\],

"currentlyLearning": \[

"Advanced PyTorch",

"Kubernetes",

"System Design"

\],

"motto": "Acta, non Verba"

}

1  
2  
3  
4  
5  
6  
7  
8  
9  
10  
11  
12  
13  
14  
15  
16  
17  
18  
19  
20  
21  
22  
23  
24  
25  
26  
27  
28  
29  
30  
31  
32  
33

{

"github": {

"username": "adeetya-u",

"totalCommits": 1247,

"publicRepos": 31,

"stars": 156,

"followers": 94,

"currentStreak": 87

},

"languageStats": {

"HTML": "89.37%",

"Python": "8.55%",

"CSS": "2.08%"

},

"activity": {

"today": 8,

"thisWeek": 52,

"thisMonth": 187

},

"codingTime": {

"totalHours": 2847,

"thisWeek": 52,

"averagePerDay": 7.4

},

"goals2025": \[

"365 day commit streak",

"10 major projects",

"1000 GitHub stars",

"Open source contributions"

\]

}

TERMINAL

adeetya@portfolio:~$ git status

On branch main Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean

adeetya@portfolio:~$ npm run dev

\> portfolio@1.0.0 dev > next dev

ready - started server on 0.0.0.0:3000, url: http://localhost:3000

✓ Ready in 1.2s

adeetya@portfolio:~$ python ml\_model.py

Loading TensorFlow model...

Model accuracy: 94.2%

✓ Model training completed

adeetya@portfolio:~$ docker build -t portfolio .

Sending build context to Docker daemon 2.048kB

Step 1/8 : FROM node:18-alpine

Step 2/8 : WORKDIR /app

✓ Successfully built portfolio:latest

adeetya@portfolio:~$ git push origin main

Enumerating objects: 5, done.

Counting objects: 100% (5/5), done.

✓ To https://github.com/adeetya-u/adeetya-u.git

✓ main -> main

adeetya@portfolio:~$ \_

Chat with Me

#### 👋 Hi there!

I'm Adeetya Upadhyay, a Full Stack Developer and ML Engineer.

Feel free to reach out if you'd like to:

*   Discuss a project collaboration
*   Ask about my experience
*   Talk about job opportunities
*   Just say hello!

[Email](mailto:adeetya.upadhyay@gmail.com) [LinkedIn](https://www.linkedin.com/in/adeetya-upadhyay/)

@ Active Tab Image

∞ Agent Auto

main

0

0

@adeetya-u

156 stars

3,298 hrs 48 mins

// Interactive functionality for VS Code portfolio document.addEventListener('DOMContentLoaded', function() { // File content mapping const fileContents = { 'Welcome.md': 'welcome-content', 'About.ts': 'about-content', 'Skills.ts': 'skills-content', 'Projects.ts': 'projects-content', 'Analytics.json': 'analytics-content', 'Contact.json': 'contact-content' }; // Tab content mapping with SVG icons (using multi-files icon for all) const tabIcons = { 'Welcome.md': '<svg viewBox="0 0 16 16" width="16" height="16" fill="#cccccc"><path d="M2 2a2 2 0 0 1 2-2h8a2 2 0 0 1 2 2v12a2 2 0 0 1-2 2H4a2 2 0 0 1-2-2V2zm2-1a1 1 0 0 0-1 1v12a1 1 0 0 0 1 1h8a1 1 0 0 0 1-1V2a1 1 0 0 0-1-1H4z"/><path d="M3 4.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1 0-1zm0 2h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1 0-1zm0 2h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1 0-1zm0 2h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1 0-1z"/><path d="M1.5 1.5A1.5 1.5 0 0 1 3 0h3a1.5 1.5 0 0 1 1.5 1.5v3A1.5 1.5 0 0 1 6 6H3a1.5 1.5 0 0 1-1.5-1.5v-3z" opacity="0.7"/><path d="M9.5 7.5A1.5 1.5 0 0 1 11 6h3a1.5 1.5 0 0 1 1.5 1.5v3A1.5 1.5 0 0 1 14 12h-3a1.5 1.5 0 0 1-1.5-1.5v-3z" opacity="0.5"/></svg>', 'About.ts': '<svg viewBox="0 0 16 16" width="16" height="16" fill="#cccccc"><path d="M2 2a2 2 0 0 1 2-2h8a2 2 0 0 1 2 2v12a2 2 0 0 1-2 2H4a2 2 0 0 1-2-2V2zm2-1a1 1 0 0 0-1 1v12a1 1 0 0 0 1 1h8a1 1 0 0 0 1-1V2a1 1 0 0 0-1-1H4z"/><path d="M3 4.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1 0-1zm0 2h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1 0-1zm0 2h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1 0-1zm0 2h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1 0-1z"/><path d="M1.5 1.5A1.5 1.5 0 0 1 3 0h3a1.5 1.5 0 0 1 1.5 1.5v3A1.5 1.5 0 0 1 6 6H3a1.5 1.5 0 0 1-1.5-1.5v-3z" opacity="0.7"/><path d="M9.5 7.5A1.5 1.5 0 0 1 11 6h3a1.5 1.5 0 0 1 1.5 1.5v3A1.5 1.5 0 0 1 14 12h-3a1.5 1.5 0 0 1-1.5-1.5v-3z" opacity="0.5"/></svg>', 'Skills.ts': '<svg viewBox="0 0 16 16" width="16" height="16" fill="#cccccc"><path d="M2 2a2 2 0 0 1 2-2h8a2 2 0 0 1 2 2v12a2 2 0 0 1-2 2H4a2 2 0 0 1-2-2V2zm2-1a1 1 0 0 0-1 1v12a1 1 0 0 0 1 1h8a1 1 0 0 0 1-1V2a1 1 0 0 0-1-1H4z"/><path d="M3 4.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1 0-1zm0 2h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1 0-1zm0 2h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1 0-1zm0 2h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1 0-1z"/><path d="M1.5 1.5A1.5 1.5 0 0 1 3 0h3a1.5 1.5 0 0 1 1.5 1.5v3A1.5 1.5 0 0 1 6 6H3a1.5 1.5 0 0 1-1.5-1.5v-3z" opacity="0.7"/><path d="M9.5 7.5A1.5 1.5 0 0 1 11 6h3a1.5 1.5 0 0 1 1.5 1.5v3A1.5 1.5 0 0 1 14 12h-3a1.5 1.5 0 0 1-1.5-1.5v-3z" opacity="0.5"/></svg>', 'Projects.ts': '<svg viewBox="0 0 16 16" width="16" height="16" fill="#cccccc"><path d="M2 2a2 2 0 0 1 2-2h8a2 2 0 0 1 2 2v12a2 2 0 0 1-2 2H4a2 2 0 0 1-2-2V2zm2-1a1 1 0 0 0-1 1v12a1 1 0 0 0 1 1h8a1 1 0 0 0 1-1V2a1 1 0 0 0-1-1H4z"/><path d="M3 4.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1 0-1zm0 2h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1 0-1zm0 2h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1 0-1zm0 2h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1 0-1z"/><path d="M1.5 1.5A1.5 1.5 0 0 1 3 0h3a1.5 1.5 0 0 1 1.5 1.5v3A1.5 1.5 0 0 1 6 6H3a1.5 1.5 0 0 1-1.5-1.5v-3z" opacity="0.7"/><path d="M9.5 7.5A1.5 1.5 0 0 1 11 6h3a1.5 1.5 0 0 1 1.5 1.5v3A1.5 1.5 0 0 1 14 12h-3a1.5 1.5 0 0 1-1.5-1.5v-3z" opacity="0.5"/></svg>', 'Analytics.json': '<svg viewBox="0 0 16 16" width="16" height="16" fill="#cccccc"><path d="M2 2a2 2 0 0 1 2-2h8a2 2 0 0 1 2 2v12a2 2 0 0 1-2 2H4a2 2 0 0 1-2-2V2zm2-1a1 1 0 0 0-1 1v12a1 1 0 0 0 1 1h8a1 1 0 0 0 1-1V2a1 1 0 0 0-1-1H4z"/><path d="M3 4.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1 0-1zm0 2h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1 0-1zm0 2h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1 0-1zm0 2h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1 0-1z"/><path d="M1.5 1.5A1.5 1.5 0 0 1 3 0h3a1.5 1.5 0 0 1 1.5 1.5v3A1.5 1.5 0 0 1 6 6H3a1.5 1.5 0 0 1-1.5-1.5v-3z" opacity="0.7"/><path d="M9.5 7.5A1.5 1.5 0 0 1 11 6h3a1.5 1.5 0 0 1 1.5 1.5v3A1.5 1.5 0 0 1 14 12h-3a1.5 1.5 0 0 1-1.5-1.5v-3z" opacity="0.5"/></svg>', 'Contact.json': '<svg viewBox="0 0 16 16" width="16" height="16" fill="#cccccc"><path d="M2 2a2 2 0 0 1 2-2h8a2 2 0 0 1 2 2v12a2 2 0 0 1-2 2H4a2 2 0 0 1-2-2V2zm2-1a1 1 0 0 0-1 1v12a1 1 0 0 0 1 1h8a1 1 0 0 0 1-1V2a1 1 0 0 0-1-1H4z"/><path d="M3 4.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1 0-1zm0 2h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1 0-1zm0 2h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1 0-1zm0 2h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1 0-1z"/><path d="M1.5 1.5A1.5 1.5 0 0 1 3 0h3a1.5 1.5 0 0 1 1.5 1.5v3A1.5 1.5 0 0 1 6 6H3a1.5 1.5 0 0 1-1.5-1.5v-3z" opacity="0.7"/><path d="M9.5 7.5A1.5 1.5 0 0 1 11 6h3a1.5 1.5 0 0 1 1.5 1.5v3A1.5 1.5 0 0 1 14 12h-3a1.5 1.5 0 0 1-1.5-1.5v-3z" opacity="0.5"/></svg>' }; // Get DOM elements const fileItems = document.querySelectorAll('.file-item'); const editorContent = document.getElementById('editor-content'); const tabElement = document.querySelector('.tab'); let tabIcon = tabElement.querySelector('svg'); const tabName = tabElement.querySelector('span'); // Add click listeners to file items fileItems.forEach(item => { item.addEventListener('click', function() { const fileName = this.querySelector('span:last-child').textContent; // Skip if clicking on folder if (fileName === 'PORTFOLIO') return; // Remove active class from all file items fileItems.forEach(f => f.classList.remove('active')); // Add active class to clicked item this.classList.add('active'); // Update tab if (tabIcons\[fileName\]) { tabIcon.outerHTML = tabIcons\[fileName\]; // Re-query the SVG element after replacing outerHTML tabIcon = tabElement.querySelector('svg'); tabName.textContent = fileName; } // Show corresponding content showContent(fileName); }); }); function showContent(fileName) { // Hide all content const allContent = document.querySelectorAll('#editor-content > div'); allContent.forEach(content => { content.style.display = 'none'; }); // Remove welcome class from editor editorContent.classList.remove('welcome'); // Show selected content const contentId = fileContents\[fileName\]; if (contentId) { const contentElement = document.getElementById(contentId); if (contentElement) { contentElement.style.display = 'block'; // Add welcome class back for welcome content if (contentId === 'welcome-content') { editorContent.classList.add('welcome'); } } } } // Add hover effects to activity bar items const activityItems = document.querySelectorAll('.activity-item'); activityItems.forEach(item => { item.addEventListener('click', function() { // Remove active class from all items activityItems.forEach(i => i.classList.remove('active')); // Add active class to clicked item this.classList.add('active'); }); }); // Add click functionality to status bar items const statusItems = document.querySelectorAll('.status-item'); statusItems.forEach(item => { item.addEventListener('click', function() { const text = this.textContent.trim(); if (text.includes('@adeetya-u')) { window.open('https://github.com/adeetya-u', '\_blank'); } else if (text.includes('stars')) { window.open('https://github.com/adeetya-u?tab=repositories', '\_blank'); } }); }); // Add window control functionality const closeBtn = document.querySelector('.control-btn.close'); const minimizeBtn = document.querySelector('.control-btn.minimize'); const maximizeBtn = document.querySelector('.control-btn.maximize'); closeBtn.addEventListener('click', function() { if (confirm('Are you sure you want to close this portfolio?')) { window.close(); } }); minimizeBtn.addEventListener('click', function() { // Simulate minimize (just a visual effect) document.body.style.transform = 'scale(0.1)'; document.body.style.opacity = '0'; setTimeout(() => { document.body.style.transform = 'scale(1)'; document.body.style.opacity = '1'; }, 1000); }); maximizeBtn.addEventListener('click', function() { if (document.fullscreenElement) { document.exitFullscreen(); } else { document.documentElement.requestFullscreen(); } }); // Keyboard shortcuts document.addEventListener('keydown', function(e) { if (e.ctrlKey) { switch(e.key) { case 'p': case 'P': e.preventDefault(); // Simulate command palette alert('Command Palette (Ctrl+P)\\n\\nAvailable files:\\n• Welcome.md\\n• About.ts\\n• Skills.ts\\n• Projects.ts\\n• Analytics.json\\n• Contact.json'); break; case 'l': case 'L': e.preventDefault(); alert('Language changed to TypeScript/JSON'); break; case 'm': case 'M': e.preventDefault(); document.body.classList.toggle('light-mode'); break; } } }); // Chat functionality const chatInput = document.getElementById('chat-message'); const sendButton = document.getElementById('send-button'); // Enable/disable send button based on input chatInput.addEventListener('input', function() { sendButton.disabled = this.value.trim() === ''; }); // Handle send button click sendButton.addEventListener('click', function() { const message = chatInput.value.trim(); if (message) { // Create email with the message const subject = encodeURIComponent('Portfolio Contact - Message from Website'); const body = encodeURIComponent(\`Hi Adeetya,\\n\\n${message}\\n\\nBest regards,\\n\[Your Name\]\`); const emailUrl = \`mailto:adeetya.upadhyay@gmail.com?subject=${subject}&body=${body}\`; // Open email client window.location.href = emailUrl; // Clear the input chatInput.value = ''; sendButton.disabled = true; // Show success message const originalPlaceholder = chatInput.placeholder; chatInput.placeholder = 'Email opened! Thanks for reaching out!'; setTimeout(() => { chatInput.placeholder = originalPlaceholder; }, 3000); } }); // Handle Enter key in chat input chatInput.addEventListener('keydown', function(e) { if (e.key === 'Enter' && !e.shiftKey) { e.preventDefault(); if (!sendButton.disabled) { sendButton.click(); } } }); // Auto-resize textarea chatInput.addEventListener('input', function() { this.style.height = 'auto'; this.style.height = Math.min(this.scrollHeight, 100) + 'px'; }); // Initialize send button as disabled sendButton.disabled = true; // Initialize with Welcome.md active showContent('Welcome.md'); });