# Short Responses

For this short response assignment, aim to write a response with the following
qualities (your instructor will give you feedback on these areas):

- [ ] Addresses all parts of the prompt
- [ ] Accurately uses relevant technical terminology
- [ ] Is free of grammar and spelling mistakes (double check with Grammarly!)
- [ ] Uses markdown to enhance readability (preview in VS Code with
      Command/Control + Shift + V)
- [ ] Is easy to comprehend

Write your response in the space provided. Make sure to preview your markdown
to check how it is rendered before submitting.

## Question 1

Boro Bikes is being rebuilt, and three pieces of data have to live somewhere.

| Data | What the system does with it |
| --- | --- |
| A ride, with a member, a bike, and the minutes | Says whether it counts as long, and what it costs |
| The dock capacity for each station, keyed by station name | Looked up by name, and never changes while the program runs |
| A member, with a name and a ride limit | Says whether they can take another bike out right now |

For each one, decide whether it should be a **dictionary** or a **class**, and
defend the choice in one sentence that names the behavior involved. One of the
three is a closer call than the other two — say which, and what would change
your mind.

### Your Response

[Write your response here]

## Question 2

A teammate pushes this class and the traceback it produces. They have not told
you which line is wrong.

```py
class Bike:
    def __init__(self, serial, station):
        serial = serial
        self.station = station

    def label(self):
        return f"{self.serial} at {self.station}"
```

```text
Traceback (most recent call last):
  File "main.py", line 9, in <module>
    print(bike.label())
  File "main.py", line 7, in label
    return f"{self.serial} at {self.station}"
AttributeError: 'Bike' object has no attribute 'serial'
```

The traceback points at `label`, and `label` is not the bug. Explain what
`serial = serial` actually does inside `__init__`, why Python raises no error
there, and why the failure surfaces three lines later instead. Name the rule
about `self` that the fix depends on.

### Your Response

[Write your response here]

