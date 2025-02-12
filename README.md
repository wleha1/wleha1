## <div align="center">QA Engineer</div>

```python
import pytest

skills = {
    "Тестирование": [
        "Ручное тестирование",
        "Автоматизированное тестирование (в процессе изучения)",
        "Тестирование API (REST, SOAP)",
        "Тестирование базы данных (PostgreSQL)",
    ],
    "Инструменты": [
        "Postman",
        "Jira",
        "DevTools",
        "Kibana",
        "Swagger",
        "Grafana",
        "Kafka",
        "Git",
        "Docker",
        "Selenium"
    ],
    "Языки": [
        "Python (в процессе изучения)",
        "JavaScript"
    ],
    "Дополнительно": [
        "HTML/CSS",
        "React"
    ]
}

def test_skills_exist():
    """Проверяем, что все навыки существуют"""
    expected_skills = {
        "Тестирование": [
            "Ручное тестирование", 
            "Автоматизированное тестирование (в процессе изучения)", 
            "Тестирование API (REST, SOAP)",
            "Тестирование базы данных (PostgreSQL)",
            "Производительное тестирование",
        ],
        "Инструменты": [
            "Postman", 
            "Яндекс Трекер", 
            "DevTools", 
            "Kibana", 
            "Swagger", 
            "Grafana", 
            "Kafka",
            "Git",
            "Docker",
            "Selenium"
        ],
        "Языки": [
            "Python (в процессе изучения)", 
            "JavaScript"
        ],
        "Дополнительно": [
            "HTML/CSS", 
            "React"
        ]
    }

    for category, skills_list in expected_skills.items():
        for skill in skills_list:
            assert skill in skills[category], f"Навык '{skill}' не найден в категории '{category}'"

def test_skills_count():
    """Проверяем количество навыков в каждой категории"""
    assert len(skills["Тестирование"]) == 5, "Неверное количество навыков в тестировании"
    assert len(skills["Инструменты"]) == 10, "Неверное количество инструментов"
    assert len(skills["Языки"]) == 2, "Неверное количество языков"
    assert len(skills["Дополнительно"]) == 2, "Неверное количество дополнительных знаний"
```
