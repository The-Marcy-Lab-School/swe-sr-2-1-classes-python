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

Boro Bikes is a bike-share service operating in New York.

The engineering team is deciding between two versions of code that build the same Boro Bikes record. The first builds a dictionary, the
second defines a class.

```py
def make_bike(serial, station, needs_repair):
    return {"serial": serial, "station": station, "needs_repair": needs_repair}

def is_rentable(bike):
    return not bike["needs_repair"]

bike = make_bike("BB4231", "30th Street & 4th Avenue", True)
print(is_rentable(bike)) # False
```

```py
class Bike:
    def __init__(self, serial, station, needs_repair):
        self.serial = serial
        self.station = station
        self.needs_repair = needs_repair
    def is_rentable(self):
        return not self.needs_repair

bike = Bike("BB4231", "30th Street & 4th Avenue", True)
print(bike.is_rentable()) # False
```

Both work but the second approach is what they went with.

In two or three sentences, defend this choice by naming what the second version provides that
the first does not, using the words **encapsulation** and **interface**. To support your argument
give one concrete thing that can go wrong in the first version that cannot go
wrong in the second.

### Response 1

[Write your response here]

## Question 2

Boro Bikes is being rebuilt, and three pieces of data have to live somewhere.

| Data                                                                                             | What the system does with it                                  |
| ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------- |
| A "ride", which includes the member on the ride, the bike, and the length of the ride in minutes | Says whether the ride counts as long, and what the ride costs |
| The dock capacity for each station, keyed by station name                                        | Looked up by name, and never changes while the program runs   |
| A member, with a name and a ride limit                                                           | Says whether they can take another bike out right now         |

For each one, decide whether it should be a **dictionary** or a **class**, and
defend the choice in one sentence that names the behavior involved.

### Response 2

[Write your response here]

## Question 3

```py
class Station:
    def __init__(self, name, capacity):
        self.name = name
        self.capacity = capacity
        self.bikes = []

    def dock(self, bike):
        self.bikes.append(bike)

    def repair_list(self):
        return [bike for bike in self.bikes if bike.needs_repair]

    def _rebalance_overnight(self):
        self.bikes = self.bikes[: self.capacity]
```

Describe this class's **interface**: list the attributes and methods the rest of
the program is meant to use. Then name at least one it should leave alone, and
say what would break if the overnight rebalancing code ran in the middle of the
afternoon.

### Response 3

[Write your response here]
