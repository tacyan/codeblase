# elixirの基礎を書いて行きます。

## fizzbuzz

```
defmodule FizzBuzz do
  defmacrop is_fizz(n) do
    quote do: rem(unquote(n), 3) === 0
  end

  defmacrop is_buzz(n) do
    quote do: rem(unquote(n), 5) === 0
  end

  def stream do
    Stream.iterate(1, &(&1 + 1))
    |> Stream.map(fn (n) when is_fizz(n) and is_buzz(n) -> "FizzBuzz"
                     (n) when is_fizz(n) -> "Fizz"
                     (n) when is_buzz(n) -> "Buzz"
                     (n) -> Integer.to_string(n)
                  end)
  end
end

FizzBuzz.stream
|> Enum.take(16)
|> IO.inspect
```
