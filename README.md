# Rapport

Reporting solution for Elixir using EEx templates, HTML and CSS built to support printing.

## Installation

If [available in Hex](https://hex.pm/docs/publish), the package can be installed
by adding `rapport` to your list of dependencies in `mix.exs`:

```elixir
def deps do
  [
    {:rapport, "~> 0.1.0"}
  ]
end
```

## Basic Usage

```elixir
template = """
<section class="sheet padding-10mm">
  <article><%= @hello %></article>
</section>
"""
html_report =
  Rapport.new(template)
  |> Rapport.set_field(:hello, "Inline template")
  |> Rapport.generate_html
```

## Credits

The following people have contributed ideas, documentation, or code to Librex:

* Richard Nyström
* Sergey Chechaev

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request
