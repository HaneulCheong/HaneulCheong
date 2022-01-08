<details>
<summary>above.py</summary>

```python
class Developer:
    def __init__(self, name: str, languages: dict[str, str], favorite: str) -> None:
        if favorite not in languages.keys():
            raise ValueError

        self.name: str = name
        self.languages: dict[str, str] = languages
        self.favorite: str = favorite

    def hello(self) -> list[str]:
        return [
            f"Hi! My name is {self.name}.",
            f"I like to code in {self.favorite}.",
        ]

    def __repr__(self) -> str:
        return f"<Developer '{self.name}'>"
```
</details>

```python
import above


if __name__ == "__main__":
    me: above.Developer = above.Developer(
        name="Haneul Cheong",
        languages={
            "Python": "Intermediate",
            "C#": "Beginner",
            "C": "Barely Remembering Anything",
        },
        favorite="Python",
    )

    for sentence in me.hello():
        print(sentence)
```

<!---
HaneulCheong/HaneulCheong is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
