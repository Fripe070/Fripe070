<h3>Hi, I'm Fripe! <img src="https://raw.githubusercontent.com/twitter/twemoji/master/assets/svg/1f44b.svg" height="16"></h3>

```python
import time
from datetime import datetime
from typing import Any, Literal, Callable


class Fripe(Student):
    def __init__(self, name: Literal["Fripe", "froop"] = "Fripe") -> None:
        self.name = name
        self.born_at = datetime.min
        self.skills = []

    def do_work(
        self,
        work: Callable,
        /,
        time_limit_seconds: int | None = None,
        *work_args: Any,
        **work_kvargs: Any,
    ) -> Any:
        if time_limit_seconds is None:
            return
            
        time.sleep(max(0, time_limit_seconds) * 3/4)
        return work(*work_args, **work_kvargs)

```
