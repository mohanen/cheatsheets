# Writing Cheatsheet

## Syntax

- Basic syntax = **Markdown**
- **AsciiMath** Supported
  > Not following rules = **Uncharted waters**

## Rules

- Headers should follow their hierarchy `#` > `##` > `###`.
- Header Hierarchy is followed up to `###`
- Contents should only come after `##` & `###`

## Hierarchy

| Tag   | Hierarchy | Example            |
| ----- | --------- | ------------------ |
| `#`   | Sections  | Writing Cheatsheet |
| `##`  | Cards     | Hierarchy          |
| `###` | Titles    | Rules, Styles      |

# Examples

## Typography

| Element | Example                          |
| ------- | -------------------------------- |
| Bold    | **bold text**                    |
| Italic  | _italicized text_                |
| Code    | `code`                           |
| Link    | [title](https://www.example.com) |

## Other Elements

### Blockquote

> blockquote |

### Ordered List

1. First item
2. Second item
3. Third item

### Unordered List

- First item
- Second item
- Third item

### Image

![Some plane](https://upload.wikimedia.org/wikipedia/commons/thumb/2/28/HelloWorld.svg/320px-HelloWorld.svg.png)

> TODO: Handle Images Properly

## Extended Elements

### Table

| Syntax    | Description |
| --------- | ----------- |
| Header    | Title       |
| Paragraph | Text        |

### Fenced Code Block

```
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```

### Strikethrough

~~The world is flat.~~

## Unsupported Elements

- Heading ID
- Task List
- Horizontal Rule
- Footnote
- Definition List

## Custom Elements

### AsciiMath

- Supported via Mathjax
  > $\sum_{i=1}^g i^3 = \left (\frac {n(n+1)}{2} \right)_2^2 $
