---
meta1: here is an example of some metadata
meta2: you can sort and index files based on metadata
meta3: you can hide this metadata using the arrow next to "Properties"
meta4: you can have different types of metadata - like dates!
meta 5:
---
#hereisanexampleoftags #youcanusetagstosortandfilterpages
## Headings

Use hashtags to create headings:

# Heading 1
## Heading 2
### Heading 3

## Text Formatting

- *Italic*: _Italic_
- **Bold**: __Bold__
- ***Bold and Italic***: ___Bold and Italic___

## Lists

### Unordered List

- Item 1
- Item 2
  - Subitem 2.1
  - Subitem 2.2

### Ordered List

1. First item
2. Second item
   1. Subitem 2.1
   2. Subitem 2.2

## Links

[Link to Obsidian](https://obsidian.md)
[[Research Overview]]
## Images
![[Pasted image 20240123163530.png]]

## Quotes

> This is a blockquote.

## Code

Inline code: `code`

Code block:

```python
def hello_world():
    print("Hello, world!")
```

You can copy straight from code blocks by clicking the button on the right 
Very useful if you need to copy commands or code quickly - like the following Shell commands

```shell
@reboot ( sleep 15 ; /usr/bin/socat -d -d pty,raw,echo=0 pty,raw,echo=0 )
@reboot ( sleep 20 ; /usr/bin/socat -v udp4-datagram:192.168.2.86:3000 open:/dev/pts/1,raw,nonblock,waitlock=/tmp/s0.locak,echo=0,b115200,crnl )
```


# LaTeX Rendering Example

## Inline Math

This is an example of inline math: $(E=mc^2)$. You can use single dollar signs for inline math.

## Display Math

For display math, use double dollar signs:

$$
\int_{0}^{\infty} e^{-x^2} \,dx = \frac{\sqrt{\pi}}{2}
$$

## Mathematical Symbols

Some mathematical symbols:

- $(\alpha, \beta, \gamma)$
- $(\sum_{i=1}^{n} i^2)$
- $(\frac{1}{2})$
- $(\sqrt{2})$
- $(\Rightarrow)$

## Equations with Numbering


$$a^2 + b^2 = c^2$$


This is a numbered equation.

## Matrices

Matrices:

$$\begin{bmatrix}
    1 & 2 \\
    3 & 4
\end{bmatrix}
$$

## Greek Letters

Some Greek letters: $$(\alpha, \beta, \gamma, \delta, \epsilon)$$
## Fractions

A fraction: $$(\frac{3}{4})$$
## Callouts
These can help draw emphasis on information (and look pretty too)

> [!info] > Here's a callout block. > It supports **Markdown**, [[Welcome|note links]], and embedded files > ![[Pasted image 20240123163530.png]]

> [!tip] Callouts can have custom titles > Like this one.

> [!faq]- Are callouts foldable? 
> Yes! In a foldable callout, the contents are hidden when the callout is collapsed.

> [!question] Can callouts be nested? 
> > [!todo] Yes!, they can. 
 > > > [!example] You can even use multiple layers of nesting.

>[!info] You can even put equations in callouts
>Black-Scholes Option Pricing Model
>Non-dividend paying stock
>
>$$C=S^{x}\times N(d_{1})-PV(K)\times N(d_{2})$$
>
>$$S^{x}=S-PV(Div)$$
>$$d_{1}=\frac{ln(\frac{S^{x}}{PV(K)})}{\sigma \sqrt{T}}+\frac{\sigma \sqrt{T}}{2}$$
>
>$$d_{2}=d_{1}-\sigma \sqrt{T}$$
>


**There's many different kinds of callouts** - see https://help.obsidian.md/Editing+and+formatting/Callouts#Supported+types for examples
