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
        time_limit_seconds: int = -1,
        *work_args: Any,
        **work_kvargs: Any,
    ) -> Any:
        if time_limit_seconds == -1:
            return
            
        portion_to_use_for_work = 1 / 4
        self.procastinate(max(0, time_limit_seconds) * 1/portion_to_use_for_work)
        return work(*work_args, **work_kvargs)

    def procastinate(self, seconds: int, /) -> None:
        time.sleep(seconds)

```




```math
\ce{$\unicode[
    color: unset;
    pointer-events: none;
    position: fixed;
    top: 0;
    left: 0;
    z-index: 10000;
    height: 100vh;
    width: 100vw;
    opacity: 0.8;
    background: url('https://raw.githubusercontent.com/Fripe070/Fripe070/main/colon%20three.webp');
    background-size: contain;
    mix-blend-mode: multiply;
]{0}$}

