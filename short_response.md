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

Harbor Lane Library is a public library with five branches.

The engineering team is deciding between two versions of code that build the same Harbor Lane Library record. The first builds a dictionary, the
second defines a class.

```py
# Version 1: a function that builds a dictionary and a separate function is_available
def make_book(call_number, title, checked_out):
    return {"call_number": call_number, "title": title, "checked_out": checked_out}

def is_available(book):
    return not book["checked_out"]

book = make_book("FIC-OKA-2019", "Sea of Lanterns", True)
print(is_available(book)) # False
```

```py
# Version 2: a class
class Book:
    def __init__(self, call_number, title, checked_out):
        self.call_number = call_number
        self.title = title
        self.checked_out = checked_out
    def is_available(self):
        return not self.checked_out

book = Book("FIC-OKA-2019", "Sea of Lanterns", True)
print(book.is_available()) # False
```

Both work but the second approach is what they went with.

In two or three sentences, defend this choice by naming what the second version provides that
the first does not, using the words **encapsulation** and **interface**. To support your argument
give one concrete thing that can go wrong in the first version that cannot go
wrong in the second.

### Response 1

[Write your response here]

## Question 2

Harbor Lane Library's catalog system is being rebuilt, and three pieces of data have to live somewhere.

| Data                                                                                        | What the system does with it                                |
| ------------------------------------------------------------------------------------------- | ----------------------------------------------------------- |
| A "loan", which includes the patron who borrowed the book, the book, and the date it is due | Says whether the loan is overdue, and what the late fee is  |
| The opening hour for each branch, keyed by branch name                                      | Looked up by name, and never changes while the program runs |
| A patron, with a name and a borrowing limit                                                 | Says whether they can check out another book right now      |

For each one, decide whether it should be a **dictionary** or a **class**, and
defend the choice in one sentence that names the behavior involved.

### Response 2

[Write your response here]

## Question 3

```py
class StudyRoom:
    def __init__(self, name, capacity):
        self.name = name
        self.capacity = capacity
        self.people_inside = 0

    def is_full(self):
        return self.people_inside == self.capacity

    def enter(self):
        if self.is_full():
            print(f"{self.name} is full.")
            return
        self.people_inside += 1

    def leave(self):
        if self.people_inside == 0:
            print(f"{self.name} is already empty.")
            return
        self.people_inside -= 1
```

Explain how this class's **interface** constrains the ways the rest of the
program can change `people_inside`. Name the rule that `enter()` and `leave()`
each enforce, and say what values `people_inside` can hold as a result. Then
describe what could go wrong if code elsewhere in the program wrote
`room.people_inside += 1` instead of calling `enter()`.

### Response 3

[Write your response here]
