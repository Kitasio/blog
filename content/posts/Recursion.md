---
title: "Recursion"
date: 2022-08-25T13:46:47+03:00
draft: false
featuredImage: "/lungi3.jpg"
---

## A recursive function is a function that calls itself.

Every recursive function _has two parts_: the __base case__, and the __recursive case__. The recursive case is when the function calls itself. The base case is when the function doesn’t call itself again ... so it doesn’t go into an infinite loop.

-   Recursion is when a function calls itself.
-   Every recursive function has two cases: the base case and the recursive case.
-   A stack has two operations: push and pop.
-   All function calls go onto the call stack.
-   The call stack can get very large, which takes up a lot of memory.

_Recursive function stores it's state on the stack, in contrast to storing it in a variable

Some simple recursive functions in Elixir:
```elixir
defmodule Recursive do
  def sum([]), do: 0
  def sum([head | tail]), do: head + sum(tail)

  def count([]), do: 0
  def count([_ | tail]), do: 1 + count(tail)

  def max([x]), do: x
  def max([head | tail]), do: get_max(head, max(tail))
  defp get_max(x, y) when x > y, do: x
  defp get_max(_, y), do: y

  def sort(list) when length(list) < 2, do: list
  def sort([pivot | tail]) do
    {less, greater} = Enum.split_with(tail, &(&1 <= pivot))
    sort(less) ++ [pivot | sort(greater)]
  end
end

IO.inspect(Recursive.sort([10,2,6,44,3]))
```

## Example
Lets look at a specific recursive function
```elixir
  def sum([]), do: 0
  def sum([head | tail]), do: head + sum(tail)
```

Here's how it looks visually given we pass `sum([2,4,6])`
![visual recursion](/recursion.png)

With recursion the _state is saved on the stack_, as oposed to a loop where you would save state in an empty list, heres how the stack looks before anything is executed
![function on the stack](/stack.png)

When the program hits the _base case_ 
```elixir
  def sum([]), do: 0 # base case
```

it will _start executing_, and __pop values off the stack__ in a _LIFO_ (last in first out) manner:
```elixir
   sum([head | tail]), do: 6 + 0 # 6 goes to prev call
|> sum([head | tail]), do: 4 + 6 # 10 goes to prev call
|> sum([head | tail]), do: 2 + 10 # last function popped off the stack, done
```

Same example from Grokking Algorithms book:
![example from a book Grokking Algorithms](/grokking_example.png)

