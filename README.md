```python
import datetime
import random
import time
from typing import Any, Literal, Callable, override
from universal import Student

class Fripe(Student, stage="Gymnasium"): # Equiv to HS in other countries
    def __init__(
        self, 
        name: Literal["Fripe", "froop"] = "Fripe",
    ) -> None:
        self.name = name
        self.born_at = float("NaN")
        self.interests = [
            "Programming",
            "Procedural art",
            "3D rendering"
            "Vocaloid",
            "Minecraft",
            "Testing in prod",
            "Game development",
        ]
        self.skills = random.choices(
            self.interests, 
            k=len(self.interests) - (len(self.interests) // 3) # TODO: Improve on this
        )
        self.knowledge: list[Any] = []

    @override
    def do_work(
        self,
        work: Callable[..., Any],
        /,
        due_at: datetime.datetime | None = None,
        *work_args: Any,
        **work_kvargs: Any,
    ) -> Any:
        if due_at is None:
            return
        time.sleep(max(
            0, 
            (due_at - datetime.timedelta(hours=1) - datetime.datetime.now()).total_seconds(),
        ))
        return work(*work_args, **work_kvargs)

    def __call__(self, *args) -> None:
        if random.random() < 0.85:
            self.knowledge.append(args)
        return "uh huh"
```
