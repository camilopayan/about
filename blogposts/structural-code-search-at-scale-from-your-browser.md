---
title: Structural code search. At scale. From your browser.
author: Rijnard van Tonder
authorUrl: https://twitter.com/rvtond
publishDate: 2020-01-08T10:00-07:00
tags: [blog]
slug: structural-code-search-at-scale-from-your-browser
heroImage: https://TODO
published: true
---

It's not every day that you get to talk about something new that hasn't quite
been done before. Today that something is structural code search, a richer way
for searching code. And we're making available at scale.

## So what _is_ structural code search?

Structural code search is the idea that you can search for _syntactic
structures_ in code that correspond more closely to a program's underlying
concrete syntax tree. For example, `for` loops in Rust look something like
this:

```rust
for var in expression {
    code
}
```

and the `code` part can itself be nested in further code blocks containing more
`for` loops, `if` statements, and so on. If we wanted to match all of the
`code` block contents and search for patterns inside it, our search engine must
understand that `code` is contained inside the _balanced_ braces `{ ... }`.
This is exactly what parsers do: they understand syntax that delineate code
blocks, and turn them into tree data structures. But most code search today is
not based on true parsing or tree data structures: it's based on matching
literal strings and regular expressions. We could search for strictly richer
and more interesting patterns if today's search tools _also_ treated programs
in their truer tree form. So today we're making it possible to perform
structural search queries in Sourcegraph, at scale, from your browser.

## What can I use structural search for?

## When you should use structural search

## Resources

This idea of structural matching is not new. There is an immense amount of work
out there on parsing and query tools for syntax trees. Most compilers today
offer a library or visitor framework used by, e.g., linters or static
analyzers. You might be familiar with some of the following tools that are
relate to Sourcegraph's structural search:

- Intellij [SSR](https://www.jetbrains.com/help/idea/structural-search-and-replace.html)
- coccinelle (only C / some Java)
- gogrep (only Go)
- various grammar and parser generator based tools 
 - tree-sitter (query syntax trees efficiently)
 - cobra

At Sourcegraph we're continually looking to improve developer tools, and to
integrate existing tools like these. We currently...

## What's next for structural search?

We significant improvements planned:

- ...

Happy searching!

