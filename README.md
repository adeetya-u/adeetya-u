<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>adeetya-u - VS Code</title>
    <style>
        body { margin: 0; font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; }
        .vscode-container { display: flex; height: 100vh; background: #1e1e1e; color: #cccccc; }
        .sidebar { width: 300px; background: #252526; border-right: 1px solid #333; }
        .main-content { flex: 1; background: #1e1e1e; }
        .sidebar-header { padding: 10px; font-size: 11px; text-transform: uppercase; color: #888; font-weight: bold; }
        .file-explorer { padding: 0; }
        .file-item { padding: 8px 20px; cursor: pointer; display: flex; align-items: center; font-size: 13px; }
        .file-item:hover { background: #2a2d2e; }
        .file-item.active { background: #094771; }
        .file-icon { margin-right: 8px; }
        .welcome-screen { padding: 40px; text-align: center; }
        .welcome-title { font-size: 24px; margin-bottom: 30px; color: #cccccc; }
        .shortcuts { text-align: left; max-width: 400px; margin: 0 auto; }
        .shortcut-item { display: flex; justify-content: space-between; align-items: center; padding: 10px 0; border-bottom: 1px solid #333; }
        .shortcut-keys { background: #333; padding: 4px 8px; border-radius: 3px; font-size: 11px; }
        .status-bar { position: fixed; bottom: 0; left: 0; right: 0; height: 22px; background: #0078d4; display: flex; align-items: center; justify-content: space-between; padding: 0 10px; font-size: 12px; }
    </style>
</head>
<body>

<div class="vscode-container">
    <!-- Sidebar -->
    <div class="sidebar">
        <div class="sidebar-header">📁 PORTFOLIO</div>
        <div class="file-explorer">
            <div class="file-item active">
                <span class="file-icon">🏠</span>
                <span>Welcome.md</span>
            </div>
            <div class="file-item">
                <span class="file-icon">👨‍💻</span>
                <span>About.ts</span>
            </div>
            <div class="file-item">
                <span class="file-icon">🛠️</span>
                <span>Skills.ts</span>
            </div>
            <div class="file-item">
                <span class="file-icon">🚀</span>
                <span>Projects.ts</span>
            </div>
            <div class="file-item">
                <span class="file-icon">📊</span>
                <span>Analytics.json</span>
            </div>
            <div class="file-item">
                <span class="file-icon">🌐</span>
                <span>Contact.json</span>
            </div>
        </div>
    </div>

    <!-- Main Content -->
    <div class="main-content">
        <div class="welcome-screen">
            <h1 class="welcome-title">Welcome to My Portfolio!</h1>
            
            <div class="shortcuts">
                <div class="shortcut-item">
                    <span>To view pages</span>
                    <span class="shortcut-keys">CTRL + P</span>
                </div>
                <div class="shortcut-item">
                    <span>To change theme</span>
                    <span class="shortcut-keys">CTRL + T</span>
                </div>
                <div class="shortcut-item">
                    <span>To toggle mode</span>
                    <span class="shortcut-keys">CTRL + M</span>
                </div>
            </div>
        </div>
    </div>
</div>

<!-- Status Bar -->
<div class="status-bar">
    <div>
        <span>👤 @adeetya-u</span>
        <span style="margin-left: 20px;">🔥 85+ followers</span>
        <span style="margin-left: 20px;">⭐ 120+ stars</span>
    </div>
    <div>
        <span>⏰ coding: 2,397 hrs 23 mins</span>
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