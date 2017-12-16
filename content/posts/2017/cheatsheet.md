---
title: "Markdown Cheatsheet"
date: 2017-12-09T13:55:37+08:00
categories: ["示例", "測試"]
tags: ["markdown", "cheatsheet"]
toc: true
---


# Standard Markdown


## Inline Markup

We are all in the *gutters*, but `some` of us are looking at the **stars**.

我們都生活在 *陰溝裡* ，但仍有人仰望 **星空** 。長度試試。長度試試。長度試試。長度試試。長度試試。長度試試。長度試試。長度試試。長度試試。長度試試。長度試試。長度試試。長度試試。長度試試。

## Image

![Fedora 26](https://i.imgur.com/QzfKyxm.jpg)


## Code Block

使用 `conda` 創造一個名為 `venv` 的虛擬指令如下：

```
conda create -n tthl python=3.6
source activate tthl
pip install -r requirements.txt
```

## Block Quote

> block quote block quote block quote block quote block quote block quote block
> continued
>
> nest line
>
> > and nested
> >
> > 1. item
> > 2. another item

## Table

超難寫的 Table:

| a | b | c | d | e |
|---|---|---|---|---|
| 1 | 2 | 3 | 4 | 5 |
| 5 | 4 | 3 | 2 | 1 |
| 6 | 6 | 6 | 6 | 6 |

## Hr

text above hr.

-------------

text below hr.

## List

* abc
* def
* another list
    * ijk
    * lmn
* zmd

1. x
2. y
3. z
    1. s
    2. u
4. b


## Hyperlink

This is [an example](http://example.com/ "Title") inline link.
[This link](http://example.net/) has no title attribute.



# Hugo Shortcodes

## Highlight

Inline Highlights:

{{< highlight python "linenos=inline,hl_lines=8 15-17,linenostart=199,noclasses=false" >}}
from pprint import pprint

TC = int(input())
for _ in range(TC):
    cards = []
    for i in range(5):
        nums = [int(x) for x in input().split()]
        cards.append(set(nums))

    # pprint(cards)

    N = int(input())
    for _ in range(N):
        inp = input().split()[1:]
        selects = [ord(x) - ord('A') for x in inp]
        result = set(range(1, 33))
        for i, c in enumerate(cards):
            if i in selects:
                result = result & c
            else:
                complement = set(range(1, 33)) - c
                result = result & complement
        
        # print(inp, result)
        result = list(result)
        
        if len(result) == 0:
            print('Impossible!')
        elif len(result) >= 2:
            print("I don't know!")
        else:
            print(result[0])
{{< / highlight >}}

Table Highlights:

{{< highlight python "linenos=table,linenostart=199,noclasses=false" >}}
from pprint import pprint

TC = int(input())
for _ in range(TC):
    cards = []
    for i in range(5):
        nums = [int(x) for x in input().split()]
        cards.append(set(nums))

    # pprint(cards)

    N = int(input())
    for _ in range(N):
        inp = input().split()[1:]
        selects = [ord(x) - ord('A') for x in inp]
        result = set(range(1, 33))
        for i, c in enumerate(cards):
            if i in selects:
                result = result & c
            else:
                complement = set(range(1, 33)) - c
                result = result & complement
        
        # print(inp, result)
        result = list(result)
        
        if len(result) == 0:
            print('Impossible!')
        elif len(result) >= 2:
            print("I don't know!")
        else:
            print(result[0])
{{< / highlight >}}

## Gists

{{< gist spf13 7896402 >}}

## Figure

{{< figure src="https://i.imgur.com/KdlKPx8.jpg" title="人類衰退之後" width="400" >}}

## Youtube

{{< youtube _J73EqmpZ7k >}}

## Tweet

{{< tweet 877500564405444608 >}}


# Custom Shortcodes

## Jupyter notebook

## Admonition

## Expansion




# Others

## Latex

## AsciiMath