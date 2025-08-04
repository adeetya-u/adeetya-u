<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>adeetya-u - Visual Studio Code</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: #1e1e1e;
            color: #cccccc;
            overflow: hidden;
        }
        
        /* Title Bar */
        .title-bar {
            height: 30px;
            background: #3c3c3c;
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 0 10px;
            font-size: 13px;
        }
        
        .window-controls {
            display: flex;
            gap: 5px;
        }
        
        .control-btn {
            width: 12px;
            height: 12px;
            border-radius: 50%;
            cursor: pointer;
        }
        
        .control-btn.close { background: #ff5f57; }
        .control-btn.minimize { background: #ffbd2e; }
        .control-btn.maximize { background: #28ca42; }
        
        .title-text {
            color: #cccccc;
            font-size: 13px;
        }
        
        /* Main Container */
        .vscode-container {
            display: flex;
            height: calc(100vh - 52px);
        }
        
        /* Activity Bar */
        .activity-bar {
            width: 48px;
            background: #333333;
            border-right: 1px solid #444444;
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 10px 0;
        }
        
        .activity-item {
            width: 48px;
            height: 48px;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            margin-bottom: 5px;
            border-left: 2px solid transparent;
            position: relative;
        }
        
        .activity-item:hover {
            background: #2a2d2e;
        }
        
        .activity-item.active {
            background: #094771;
            border-left-color: #0078d4;
        }
        
        .activity-item svg {
            fill: #cccccc;
            width: 24px;
            height: 24px;
        }
        
        /* Side Panel */
        .side-panel {
            width: 300px;
            background: #252526;
            border-right: 1px solid #3e3e42;
            display: flex;
            flex-direction: column;
        }
        
        .panel-header {
            height: 35px;
            background: #2d2d30;
            display: flex;
            align-items: center;
            padding: 0 15px;
            font-size: 11px;
            text-transform: uppercase;
            color: #cccccc;
            font-weight: 600;
            letter-spacing: 0.5px;
        }
        
        .file-explorer {
            flex: 1;
            overflow-y: auto;
        }
        
        .folder {
            padding: 8px 16px;
            display: flex;
            align-items: center;
            font-size: 13px;
            color: #cccccc;
            cursor: pointer;
        }
        
        .folder:hover {
            background: #2a2d2e;
        }
        
        .folder-icon {
            margin-right: 8px;
            color: #dcb67a;
        }
        
        .file-item {
            padding: 6px 32px;
            display: flex;
            align-items: center;
            font-size: 13px;
            color: #cccccc;
            cursor: pointer;
            position: relative;
        }
        
        .file-item:hover {
            background: #2a2d2e;
        }
        
        .file-item.active {
            background: #094771;
            color: #ffffff;
        }
        
        .file-icon {
            margin-right: 8px;
            width: 16px;
            height: 16px;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        /* Main Editor Area */
        .editor-area {
            flex: 1;
            display: flex;
            flex-direction: column;
        }
        
        .tab-bar {
            height: 35px;
            background: #2d2d30;
            border-bottom: 1px solid #3e3e42;
            display: flex;
            align-items: center;
        }
        
        .tab {
            height: 35px;
            padding: 0 16px;
            display: flex;
            align-items: center;
            background: #1e1e1e;
            border-right: 1px solid #3e3e42;
            cursor: pointer;
            font-size: 13px;
            gap: 8px;
        }
        
        .tab.active {
            background: #1e1e1e;
            border-bottom: 2px solid #0078d4;
        }
        
        .tab-close {
            width: 16px;
            height: 16px;
            border-radius: 3px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 10px;
            color: #969696;
        }
        
        .tab-close:hover {
            background: #3e3e42;
        }
        
        .editor-content {
            flex: 1;
            background: #1e1e1e;
            padding: 40px;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
        }
        
        .welcome-content {
            text-align: center;
            max-width: 500px;
        }
        
        .welcome-title {
            font-size: 28px;
            color: #cccccc;
            margin-bottom: 30px;
            font-weight: 300;
        }
        
        .shortcuts-section {
            text-align: left;
            margin-top: 30px;
        }
        
        .shortcut-item {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 12px 0;
            border-bottom: 1px solid #3e3e42;
            font-size: 14px;
        }
        
        .shortcut-keys {
            background: #3e3e42;
            padding: 4px 8px;
            border-radius: 3px;
            font-size: 11px;
            font-family: 'Consolas', 'Courier New', monospace;
            color: #cccccc;
        }
        
        /* Status Bar */
        .status-bar {
            height: 22px;
            background: #0078d4;
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 0 10px;
            font-size: 12px;
            color: #ffffff;
        }
        
        .status-left,
        .status-right {
            display: flex;
            align-items: center;
            gap: 15px;
        }
        
        .status-item {
            display: flex;
            align-items: center;
            gap: 5px;
            cursor: pointer;
        }
        
        .status-item:hover {
            background: rgba(255, 255, 255, 0.1);
            padding: 2px 4px;
            border-radius: 2px;
        }
        
        /* VS Code Icons */
        .vscode-icon {
            width: 16px;
            height: 16px;
            fill: currentColor;
        }
    </style>
</head>
<body>

<!-- Title Bar -->
<div class="title-bar">
    <div class="window-controls">
        <div class="control-btn close"></div>
        <div class="control-btn minimize"></div>
        <div class="control-btn maximize"></div>
    </div>
    <div class="title-text">adeetya-u — portfolio</div>
    <div></div>
</div>

<!-- Main VS Code Interface -->
<div class="vscode-container">
    <!-- Activity Bar -->
    <div class="activity-bar">
        <div class="activity-item active" title="Explorer">
            <svg viewBox="0 0 24 24">
                <path d="M10 4H4c-1.11 0-2 .89-2 2v12c0 1.11.89 2 2 2h16c1.11 0 2-.89 2-2V8c0-1.11-.89-2-2-2h-8l-2-2z"/>
            </svg>
        </div>
        <div class="activity-item" title="Search">
            <svg viewBox="0 0 24 24">
                <path d="M15.5 14h-.79l-.28-.27C15.41 12.59 16 11.11 16 9.5 16 5.91 13.09 3 9.5 3S3 5.91 3 9.5 5.91 16 9.5 16c1.61 0 3.09-.59 4.23-1.57l.27.28v.79l5 4.99L20.49 19l-4.99-5zm-6 0C7.01 14 5 11.99 5 9.5S7.01 5 9.5 5 14 7.01 14 9.5 11.99 14 9.5 14z"/>
            </svg>
        </div>
        <div class="activity-item" title="Source Control">
            <svg viewBox="0 0 24 24">
                <path d="M12,3C7.58,3 4,6.58 4,11C4,15.42 7.58,19 12,19C16.42,19 20,15.42 20,11C20,6.58 16.42,3 12,3M8,9.5A1.5,1.5 0 0,1 9.5,8A1.5,1.5 0 0,1 11,9.5A1.5,1.5 0 0,1 9.5,11A1.5,1.5 0 0,1 8,9.5M13,14.5A1.5,1.5 0 0,1 14.5,13A1.5,1.5 0 0,1 16,14.5A1.5,1.5 0 0,1 14.5,16A1.5,1.5 0 0,1 13,14.5Z"/>
            </svg>
        </div>
        <div class="activity-item" title="Run and Debug">
            <svg viewBox="0 0 24 24">
                <path d="M8,5.14V19.14L19,12.14L8,5.14Z"/>
            </svg>
        </div>
        <div class="activity-item" title="Extensions">
            <svg viewBox="0 0 24 24">
                <path d="M20.5,11H19V7C19,5.89 18.1,5 17,5H13V3.5A2.5,2.5 0 0,0 10.5,1A2.5,2.5 0 0,0 8,3.5V5H4C2.89,5 2,5.89 2,7V10.8H3.5C5,10.8 6.2,12 6.2,13.5C6.2,15 5,16.2 3.5,16.2H2V20C2,21.11 2.89,22 4,22H7.8V20.5C7.8,19 9,17.8 10.5,17.8C12,17.8 13.2,19 13.2,20.5V22H17C18.11,22 19,21.11 19,20V16H20.5A2.5,2.5 0 0,0 23,13.5A2.5,2.5 0 0,0 20.5,11Z"/>
            </svg>
        </div>
    </div>

    <!-- Side Panel -->
    <div class="side-panel">
        <div class="panel-header">
            EXPLORER
        </div>
        <div class="file-explorer">
            <div class="folder">
                <span class="folder-icon">📁</span>
                <span>PORTFOLIO</span>
            </div>
            <div class="file-item active">
                <div class="file-icon">📄</div>
                <span>Welcome.md</span>
            </div>
            <div class="file-item">
                <div class="file-icon">🟦</div>
                <span>About.ts</span>
            </div>
            <div class="file-item">
                <div class="file-icon">🟦</div>
                <span>Skills.ts</span>
            </div>
            <div class="file-item">
                <div class="file-icon">🟦</div>
                <span>Projects.ts</span>
            </div>
            <div class="file-item">
                <div class="file-icon">🟨</div>
                <span>Analytics.json</span>
            </div>
            <div class="file-item">
                <div class="file-icon">🟨</div>
                <span>Contact.json</span>
            </div>
            <div class="file-item">
                <div class="file-icon">🟩</div>
                <span>package.json</span>
            </div>
            <div class="file-item">
                <div class="file-icon">📄</div>
                <span>README.md</span>
            </div>
        </div>
    </div>

    <!-- Editor Area -->
    <div class="editor-area">
        <div class="tab-bar">
            <div class="tab active">
                <span>📄</span>
                <span>Welcome.md</span>
                <div class="tab-close">×</div>
            </div>
        </div>
        
        <div class="editor-content">
            <div class="welcome-content">
                <h1 class="welcome-title">Welcome to My Portfolio!</h1>
                
                <div class="shortcuts-section">
                    <div class="shortcut-item">
                        <span>Show all pages</span>
                        <span class="shortcut-keys">CTRL + P</span>
                    </div>
                    <div class="shortcut-item">
                        <span>Change language</span>
                        <span class="shortcut-keys">CTRL + L</span>
                    </div>
                    <div class="shortcut-item">
                        <span>Toggle mode</span>
                        <span class="shortcut-keys">CTRL + M</span>
                    </div>
                </div>
            </div>
        </div>
    </div>
</div>

<!-- Status Bar -->
<div class="status-bar">
    <div class="status-left">
        <div class="status-item">
            <span>🌿</span>
            <span>main</span>
        </div>
        <div class="status-item">
            <span>❌</span>
            <span>0</span>
        </div>
        <div class="status-item">
            <span>⚠️</span>
            <span>0</span>
        </div>
    </div>
    <div class="status-right">
        <div class="status-item">
            <span>👤</span>
            <span>@adeetya-u</span>
        </div>
        <div class="status-item">
            <span>⭐</span>
            <span>120+ stars</span>
        </div>
        <div class="status-item">
            <span>⏰</span>
            <span>2,397 hrs 23 mins</span>
        </div>
    </div>
</div>

</body>
</html>

---

# 👨‍💻 About Me

```typescript
const developer = {
    name: "Adeetya Upadhyay",
    pronouns: "he/him",
    location: "Champaign, IL",
    
    education: [
        "B.S. Computer Science & Advertising | UIUC | GPA: 3.80",
        "B.S.L.A.S. Econometrics & Quantitative Economics | UIUC | GPA: 4.00"
    ],
    
    currentFocus: [
        "Building ML pipelines",
        "Full-stack applications", 
        "AI-powered solutions"
    ],
    
    specialties: [
        "Machine Learning Engineering",
        "Full Stack Development", 
        "AI Integration",
        "Cloud Architecture"
    ],
    
    expectedGraduation: "May 2027",
    status: "🔥 Actively building"
};

export default developer;
```

## 🔗 Quick Links
- 💼 [LinkedIn](https://www.linkedin.com/in/adeetya-upadhyay/)
- 📧 [Email](mailto:adeetya.upadhyay@gmail.com)
- 🐙 [GitHub](https://github.com/adeetya-u)
- 📞 **+1 (765) 977-2984**

---

# 🛠️ Skills & Technologies

```typescript
interface TechStack {
    languages: string[];
    frameworks: Framework[];
    cloud: CloudPlatform[];
    databases: Database[];
    tools: DevTool[];
}

const myStack: TechStack = {
    languages: [
        "Python", "Java", "C++", "JavaScript",
        "TypeScript", "R", "SQL", "HTML", "CSS",
        "Bash", "COBOL", "JCL"
    ],
    
    frameworks: [
        { name: "React", type: "frontend" },
        { name: "Node.js", type: "runtime" },
        { name: "Flask", type: "backend" },
        { name: "FastAPI", type: "backend" },
        { name: "TensorFlow", type: "ml" },
        { name: "PyTorch", type: "ml" }
    ],
    
    cloud: ["AWS", "Azure", "GCP"],
    databases: ["PostgreSQL", "SQLite", "NoSQL"],
    tools: ["Git", "Docker", "CI/CD", "Microservices"],
    specialties: ["ML Engineering", "Full Stack", "AI Integration"]
};

export { myStack };
```

### 💻 **Languages & Technologies**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=flat&logo=java&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=flat&logo=c%2B%2B&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=flat&logo=typescript&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=flat&logo=react&logoColor=61DAFB)
![Node.js](https://img.shields.io/badge/Node.js-43853D?style=flat&logo=node.js&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=flat&logo=flask&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat&logo=amazon-aws&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat&logo=tensorflow&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat&logo=pytorch&logoColor=white)

---

# 🚀 Featured Projects

```python
class ProjectPortfolio:
    def __init__(self):
        self.current_projects = {
            "tutorswap": {
                "status": "in_development",
                "timeline": "Jan 2025 - May 2025",
                "tech_stack": [
                    "React", "Flask", 
                    "PostgreSQL", "Socket.IO", "Docker"
                ],
                "features": [
                    "Logloss matching algorithm",
                    "AI-assisted chat",
                    "Real-time tutoring sessions",
                    "Profile management"
                ],
                "description": "Full-stack peer tutoring platform"
            },
            
            "ai_grant_matcher": {
                "status": "active",
                "timeline": "Aug 2024 - Present", 
                "purpose": "AI chatbot matching nonprofits with grants",
                "tech_stack": ["React", "Redux", "Flask", "OpenAI API"],
                "deployment": "AWS",
                "features": ["Guided Q&A", "Personalized recommendations"]
            }
        }
    
    def get_specialties(self):
        return [
            "ML Pipelines", 
            "Full Stack Development",
            "AI-powered Solutions",
            "Cloud Architecture"
        ]
```

### 🎯 **What I Build**
- 🧠 **ML Engineering** - Predictive models and data pipelines
- 🌐 **Full Stack Apps** - End-to-end web applications  
- 🤖 **AI Integration** - Smart features and automation
- ☁️ **Cloud Solutions** - Scalable infrastructure

---

# 📊 GitHub Analytics

```json
{
    "developer": "adeetya-u",
    "totalCommits": "500+",
    "languageStats": {
        "Python": "35%",
        "JavaScript": "28%", 
        "TypeScript": "15%",
        "Java": "12%",
        "Other": "10%"
    },
    "contributionLevel": "very_high",
    "preferredStack": [
        "React + Flask",
        "ML + Cloud", 
        "Python + TypeScript"
    ],
    "status": "actively_building",
    "currentProjects": [
        "TutorSwap Platform",
        "AI Grant Matcher",
        "ML Forecasting Models"
    ]
}
```

### 🏆 **Achievements**
- 🔥 Current Streak: 45+ days
- 📚 Public Repos: 15+
- ⭐ Total Stars: 120+
- 👥 Followers: 85+

### 📈 **Recent Activity**
- **Today**: 8 contributions
- **This Week**: 42 contributions  
- **This Month**: 187 contributions

<div align="center">

![GitHub Stats](https://github-readme-stats.vercel.app/api?username=adeetya-u&show_icons=true&theme=vs-dark&hide_border=true&bg_color=1e1e1e&icon_color=58a6ff&text_color=c9d1d9&title_color=58a6ff)

![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=adeetya-u&layout=compact&theme=vs-dark&hide_border=true&bg_color=1e1e1e&text_color=c9d1d9&title_color=58a6ff)

</div>

---

# 🌐 Contact & Connect

```json
{
    "name": "Adeetya Upadhyay",
    "contact": {
        "email": "adeetya.upadhyay@gmail.com",
        "phone": "+1 (765) 977-2984",
        "linkedin": "linkedin.com/in/adeetya-upadhyay",
        "github": "github.com/adeetya-u"
    },
    "location": "Champaign, IL",
    "availability": "Open to opportunities",
    "interests": [
        "Machine Learning Engineering",
        "Full Stack Development",
        "AI-powered Solutions", 
        "Cloud Architecture"
    ],
    "education": {
        "university": "University of Illinois Urbana-Champaign",
        "degrees": [
            "B.S. Computer Science & Advertising (GPA: 3.80)",
            "B.S. Econometrics & Quantitative Economics (GPA: 4.00)"
        ],
        "graduation": "May 2027"
    },
    "status": "actively_building",
    "motto": "Always coding, always learning, always growing"
}
```

### 🏆 **Leadership Experience**
- 📊 **OTCR Consulting** - Lead Consultant
- 💼 **Illinois Business Consulting** - Senior Consultant

### 🚀 **Currently Learning**
- Advanced PyTorch
- Kubernetes  
- System Design

### 📊 **Quick Stats**
- 🔥 GitHub Streak: 45+ days
- ⭐ Profile Views: 5000+
- 📂 Public Repos: 15+
- 🤝 Open to Collaborate

---

<div align="center">

### 🚀 **Ready to Connect?**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/adeetya-upadhyay/)
[![Gmail](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:adeetya.upadhyay@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/adeetya-u)

![Profile Views](https://komarev.com/ghpvc/?username=adeetya-u&color=0078d4&style=flat&label=Profile+Views)

**Thanks for visiting! Always coding, always learning, always growing** 🚀

</div>