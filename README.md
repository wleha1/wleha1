## <div align="center">QA Engineer</div>

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
        "JavaScript"
    ]
}

def test_skills_exist():
    """Проверяем, что все навыки существуют"""
    expected_skills = {
        "Тестирование": ["Ручное тестирование", "Автоматизированное тестирование", "Тестирование API"],
        "Инструменты": ["Postman", "Jira", "pytest"],
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
