---
title: Go does not need generics
date: '2019-03-07'
spoiler: Do we stand on the right side of history.
---

## A little of context

Urs Holzle, the Head of Infrastructure in Google says:

> Keeping things simple and yet scalable is actually the biggest challenge"

Google had struggled with that problem ìn 2007 with an enormous codebase, hundreds of developer and the most important thing is `45-minute build`. Why is it important, we'll get to that later.

During one of those 45-minute builds, they talked about a bunch of features will be included in C++ 11, at that point. Rob Pike who later become one of Golang's creators ask himself:

> Did the C++ committee really believe what was wrong with C++ was that it didn't have enough features?

It got them thinking about creating a new language where they should simplify the features instead of adding them.

Eventually, the idea of Go born on September 2007. Two years later, Go marked November 10th, 2009 as its official birthday.

So Go was designed for `speed of compilation` and `simplicity of the language`.

## Go philosophy

Most of other languages evolve themselves by adding new features, but in Rob's point of view, adding features would not make them better but bigger. It also makes them much more complicated and become similar to other languages.

Go, however, is a different language. Go doesn't try to be like other languages. Since 2012, when Go 1.0 is released, the language is fixed, nothing has been changed since then. No features which can change the language has been added. The code you wrote back then still work with current Go version.

People might say that without adding features, Go will become a boring language. But what is more important? More fun to write or fewer things to maintain? Adding feature will not only add complexity to the language but also drop the readability of the syntax.

A list of NO's in Go design is a long list which contains not only generics but also ternary operation, pointer arithmetic,... .These features missing because it doesn't fit, because it affects compilation speed, or because it would make the language too complicated.

Therefore, if your favorite features are missing, and you really need to use them. Go try them on another language. Because after all, Go is just a language. We will need different languages for different problems.

## Do we stand on the right side of history ?

By the time Erlang's first appearance years ago, concurrency was kind of a myth back then. Some languages thinked it is essential to have them as a first class feature and some didn't. Python stood on the `don't buy it` side. But slowly, the usage of concurrency increases.

Then NodeJS and Go were created, highlighted the need for concurrency as a first-class concept, They have shown that concurrency is a must. Python has missed that boat, they stood on the wrong side of history.

Since Go 1.0 is launch in 2009, people don't know whether they need generic or not. By that time, newborn languages like Rust, Swift have proved that have some kinds of generic is useful.

We all know that adding it to Go will make it much more complicated language and increase compilation time which are two things Go was designed to address. But we also know that not adding generic would be a mistake make Go stand on the wrong side of history as Python did. There are reasons for people sticking with Go: simplicity, scalability, compilation time, ... .The question is do we really able to pay the cost for adding generics. If we want to use generic, use Rust or some other language which are support it.

If it has to come to a Yes/No question whether we should add Generic into the language or not. For me, it is a big fat NO, we don't need generic in Go.