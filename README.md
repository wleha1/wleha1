## Frontend 

```javascript
const frontendSkills = {
    name: "Егор",
    age: 18,
    location: "Санкт-Петербург",
    skills: {
        languages: ["JavaScript", "HTML", "CSS", "Sass"],
        frameworks: ["React", "Node.js"],
        tools: ["Vite", "Git", ]
    },
    displaySkills: function() {
        console.log("Мои навыки во фронтенд разработке:");
        for (const category in this.skills) {
            console.log(`\n${category.charAt(0).toUpperCase() + category.slice(1)}:`);
            this.skills[category].forEach(skill => {
                console.log(`- ${skill}`);
            });
        }
    }
};

frontendSkills.displaySkills();
```

## QA Engineer

```python
import pytest

skills = {
    "Тестирование": [
        "Ручное тестирование",
        "Автоматизированное тестирование",
        "Тестирование API"
    ],
    "Инструменты": [
        "Postman",
        "Jira",
        "pytest"
    ],
    "Языки": [
        "Python",
        "JavaScript",
        "MySQL"
    ]
}

def test_skills_exist():
    """Проверяем, что все навыки существуют"""
    expected_skills = {
        "Тестирование": ["Ручное тестирование", "Автоматизированное тестирование", "Тестирование API"],
        "Инструменты": ["Postman", "Jira", "Selenium", "pytest"],
        "Языки": ["Python", "JavaScript"]
    }
    
    for category, skills_list in expected_skills.items():
        for skill in skills_list:
            assert skill in skills[category], f"Навык '{skill}' не найден в категории '{category}'"

def test_skills_count():
    """Проверяем количество навыков в каждой категории"""
    assert len(skills["Тестирование"]) == 3, "Неверное количество навыков в тестировании"
    assert len(skills["Инструменты"]) == 3, "Неверное количество инструментов"
    assert len(skills["Языки"]) == 2, "Неверное количество языков"
```
