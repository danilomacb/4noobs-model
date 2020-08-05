[Roadmap](../../../README.md)

```ruby
def get_numbers_stack(list)
  stack  = [[0, []]]
  output = []
  until stack.empty?
    index, taken = stack.pop
    next output << taken if index == list.size
    stack.unshift [index + 1, taken]
    stack.unshift [index + 1, taken + [list[index]]]
  end
  output
end
```
