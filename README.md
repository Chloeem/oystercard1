# oyster_card

## Issues
----

### Type:
NameError:
  uninitialized constant Oystercard

### Where:
./spec/oystercard_spec.rb:1:in `<top (required)>' 

### Line number:
rb:1

### What the error means:
Raised when a given name is invalid or undefined.

### How to solve"
Not pointing to any specifically because there are no lib files containing the class - create
lib files and require in the oystercard_spec.rb


## User-Stories
```
In order to use public transport
As a customer
I want money on my card
```
Behaviour = have a balance

### Notes to self
-----
```
    it 'Raises an error when top up exceeds the limit of £90' do
      maximum_limit = Oystercard::MAXIMUM_LIMIT # Using this approach wont raise the error every time as is the expect
      subject.top_up(maximum_limit)             # that produces the error (£91)
      expect { subject.top_up(1) }.to raise_error("Maximum top up limit of #{maximum_limit} exceeded") #can use the var created in the test itself
    end
```

