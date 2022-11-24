# edrys_module-markdown-it

With this module you can define tasks with Markdown-it.
Additionally it adds support for:

* __Katex:__ `$formula$` or `$$formula$$`
* __PlantUML:__

  ```` markdown
  ```plantuml
  Bob -> Alice : hello
  ```
  ````

* __DOT:__

  ```` markdown
  ```dot
  digraph example1 {
    1 -> 2 -> { 4, 5 };
    1 -> 3 -> { 6, 7 };
  }
  ```
  ````

* __ditaa:__

  ```` markdown
  ```ditaa
  +--------+   +-------+    +-------+
  |        +---+ ditaa +--> |       |
  |  Text  |   +-------+    |diagram|
  |Document|   |!magic!|    |       |
  |     {d}|   |       |    |       |
  +---+----+   +-------+    +-------+
      :                         ^
      |       Lots of work      |
      +-------------------------+
  ```
  ````

Import the following URL to your document:

```
https://cross-lab-project.github.io/edrys_module-markdown-it/index.html
```

## Configuration

To simplify the usage, we provide the example in Yaml and not in JSON, you have to convert it by your own.
You can modify only the general configuration, it will be presented to all and if you add different strings to other roles teacher/students/station, then this content will be presented additionally.

``` yaml
|-
  # Main Document

  This document will be shown to all users,
  except if you add additional roles,
  then this will be used as the fallback.

  Additional html content is also possible

  <iframe
    width="560"
    height="315"
    src="https://www.youtube.com/embed/BdKyq56Cijo"
    title="YouTube video player"
    frameborder="0"
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
    allowfullscreen
  ></iframe>

  next to formulas: $\frac{12}{x}$

  and next to diagrams:

    ```dot
  digraph example1 {
    1 -> 2 -> { 4, 5 };
    1 -> 3 -> { 6, 7 };
  }
```
