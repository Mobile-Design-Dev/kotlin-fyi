
## Buttons

With { } adding extra-css styling and animations :octicons-squirrel-24:{: .heartbeat }

[:fontawesome-brands-twitter:{: .twitter } Follow @kotlinfyi](https://twitter.com/kotlinfyi){: .md-button .md-button--primary }


## Code

```kotlin linenums="1" hl_lines="2 3"
package fyi.kotlin

fun main(args: Array<String>){
    println("Hello World!")
    println("#Args: " + args.size)
}
```

Or try inline highlighting - it's `#!kotlin fun()`!

## Keys

Use `++` to get keys e.g., ++ctrl++ or ++ctrl+alt+del++

## Tabs

=== "With Icons"

    * :octicons-flame-24: | Sed sagittis eleifend rutrum 
    * :octicons-hourglass-24: | Donec vitae suscipit est 
    * :octicons-squirrel-24: | Nulla tempor lobortis orci 

=== "Just Text"

    1. Sed sagittis eleifend rutrum
    2. Donec vitae suscipit est
    3. Nulla tempor lobortis orci

## Footnotes

Declare it [^1] - and you can have [^2] have multi-line footnotes too.

[^1]: Define it with the same number and a colon to represent this is content!
[^2]:
    Just indent by four spaces if you want a multi-line footnote. Just indent by four spaces if you want a multi-line footnote.Just indent by four spaces if you want a multi-line footnote.


## Formatting

- ==This was marked==
- ^^This was inserted^^
- ~~This was deleted~~
- H~2~0
- A^T^A

## Project layout

    mkdocs.yml    # The configuration file.
    docs/
        index.md  # The documentation homepage.
        ...       # Other markdown pages, images and other files.


## Data Tables

| Method      | Description                          |
| ----------- | ------------------------------------ |
| `GET`       | :material-check:     Fetch resource  |
| `PUT`       | :material-check-all: Update resource |
| `DELETE`    | :material-close:     Delete resource |

## Definition Lists

Are awesome for glossaries!

`Lorem ipsum dolor sit amet`
:   Sed sagittis eleifend rutrum. Donec vitae suscipit est. Nullam tempus
    tellus non sem sollicitudin, quis rutrum leo facilisis.

`Cras arcu libero`
:   Aliquam metus eros, pretium sed nulla venenatis, faucibus auctor ex. Proin
    ut eros sed sapien ullamcorper consequat. Nunc ligula ante.
    
    Duis mollis est eget nibh volutpat, fermentum aliquet dui mollis.
    Nam vulputate tincidunt fringilla.
    Nullam dignissim ultrices urna non auctor.

## Tasklist

custom or clickable checkboxes

- [x] Lorem ipsum dolor sit amet, consectetur adipiscing elit
- [ ] Vestibulum convallis sit amet nisi a tincidunt
    * [x] In hac habitasse platea dictumst
    * [x] In scelerisque nibh non dolor mollis congue sed et metus
    * [ ] Praesent sed risus massa
- [ ] Aenean pretium efficitur erat, donec pharetra, ligula non scelerisque