# Ruby Code Snippets

```ruby
# count objects group by value
[1] pry(main)> [:a, :b, :b, :c, :c, :c].tally
=> {:a=>1, :b=>2, :c=>3}
```

```ruby
# pretty print hash
[4] pry(main)> puts JSON.pretty_generate(a: {b: 1, c: 2})
{
  "a": {
    "b": 1,
    "c": 2
  }
}
```