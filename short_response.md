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

You are designing a system for a community radio station. Three pieces of data
have to live somewhere.

| Data | What the system does with it |
| --- | --- |
| A show, with a title, a host, and a start time | Says whether it is on air right now, and how long until it ends |
| The station's opening hours, keyed by day name | Looked up by day, and never changes while the program runs |
| A listener's pledge, with an amount and a date | Says whether it is still within the 30-day refund window |

For each one, decide whether it should be a **dictionary** or a **class**, and
defend the choice in one sentence that names the behavior involved. One of the
three is a closer call than the other two — say which, and what would change
your mind.

### Your Response

[Write your response here]

## Question 2

A teammate pushes this class and the traceback it produces. They have not
told you which line is wrong.

```py
class Permit:
    def __init__(self, plate, zone):
        plate = plate
        self.zone = zone

    def label(self):
        return f"{self.plate} in zone {self.zone}"
```

```text
Traceback (most recent call last):
  File "main.py", line 9, in <module>
    print(permit.label())
  File "main.py", line 7, in label
    return f"{self.plate} in zone {self.zone}"
AttributeError: 'Permit' object has no attribute 'plate'
```

The traceback points at `label`, and `label` is not the bug. Explain what
`plate = plate` actually does inside `__init__`, why Python raises no error
there, and why the failure surfaces three lines later instead. Name the rule
about `self` that the fix depends on.

### Your Response

[Write your response here]

