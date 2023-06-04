---
layout: default
nav_order: 1
has_children: false
permalink: /wiki/Product-Specification/Geometry/
parent: Product Specification
grand_parent: Product Pipeline 
title: Geometry
---

# Geometry
{: .no_toc }


## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}


---


<iframe width="560" height="315" src="https://www.youtube.com/embed/tvaRgmhT-wU" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>{: .center-image }

---

## Object Naming Convention	

### Naming assets with a single object:

> A single object must be named with the prefix "**Product_**", followed by the products `UPC`. <br>

![Geometry_ObjectNamingConvention_01.jpg]( /wiki/Product-Pipeline/01_Specification/Geometry_ObjectNamingConvention_02.png){: .center-image }

Name used on asset with only one object.
{: .figure }

---

### Naming assets with more than one object:

The linked parent group/helper must be named with the prefix of "**Product_**", followed by the products `UPC`. <br>

![Geometry_ObjectNamingConvention_01.jpg]( /wiki/Product-Pipeline/01_Specification/Geometry_ObjectNamingConvention_03.png){: .center-image }

Example of a product with more than one object.
{: .figure }



> Assets with More than one object must be grouped/linked to a helper. Click [here]( /wiki/Product-Specification/Geometry/#geometry) for more details.
{: .note}

> ---

### Naming examples
<br>

| Object type | Object Naming Example                    |
|:---|:-----------------------------|
|Root parent object (**or single existing object**)|**Product_**888750194923   |
|Sub-object - **Source of Duplication**|YoghurtPot |
|sub-Object - **Duplicate (reusing UVs)**| YoghurtPot**.001**, YoghurtPot**.002** etc...|

```mermaid

---
title: "Naming Flowchart"
---
flowchart RL
	2(["More than one object?"]) ---|"No"| 1["Name the object:\n #quot;Product_xxxxxxxxxxxxxx#quot;"]
	794047["Sub-Objects should be\n given a descriptive name:\n e.g. #quot;Bottle_Transparent#quot;"] --- 898692["Root linked parent\n (group/helper)\n should be named:\n #quot;Product_xxxxxxxxxxxxxx#quot;"]
	794047 --- 729043(["Is the sub-object\n cloned from another, reusing UV space?"])
	2 ---|"Yes"| 898692
	729043 ---|"no"| 966363["Do nothing"]
	729043 ---|"Yes"| 353669["Sub-objects that are cloned  \n should be named with no\nnumber: e.g. Bottle "]
	921865["Sub-objects reusing UV\n space need to be named\n with the suffix #quot;.#quot;\n followed by numbering:\n e.g. #quot;Bottle.001#quot;, #quot;Bottle.002#quot;,\n #quot;Bottle.003#quot; etc."] --- 353669

%% Mermaid Flow Diagram Link
%% Keep this link to make future edits to your diagram
%% https://www.mermaidflow.app/flowchart#N4IgZgNg9g7iBcoB2UAmBTAzgg2qGAlqgC4AWCATAAwAcANCKegQOanEICMnFDRCITiAYAHKJgLECUJAlAAPBABYAbPRABPBAGYAnDQB0K4ydMntAXwaoAhsRtyQEGwCN0EAQDkbAW3QACMgCoFwArdABjYngAHlQCADcAPgAyJBdMEQBuAB0QAAUAJzQAVyiAfXkq6pqavJiAenjk4RBCmyQAa0wAEXaYWUQrEBEbQvQkYgAlDs6EKmt+gGViDQh0BGJCkvRh1ZEN+DbI+yQWdc80DdFxSWkkAEEMqAgS4kOFZTUGLXg9QzMgOMlgYmHcJ3QqAQYBsEDBixsLBYBDO0NhYKs+CIZEoVAWjGYbA48E4VCUfChRworTEEikMkcingAHZtCofpRdCphrZ7I5nG4PEcALJQcaBUgdfwyYJhE4Afla7S6vX6g2Aw1G40mMy68wRMBWa0OWx2oNW62w8BwAF09hoDgIRAQIBBLhgabd6Y9nq93oyEKz2ZpOdzQeCopC0XD0AikSiWNGMXQsSRyPBqOomKx2FweBSBDR9CpdNSbnT7gH4Kp1L8KMYjECzCCQPtDscoh1zuh3dcQLyHIgnK53AIplAoMR-BAUZ1If4tRNiHFEql0pksgAKFjFEoiBpMCAHQoAShXyTSGWymFIUBKEFQ-jc-iQvkhsSaq-Pa6vuQKxVQMpiEqWpQKqepP2SRpmiSVpMAtLBcBtBhlW6PobAGORNTGJddTmeB8VQZYEM2bZdnDdZI0pGEY3LO4ZCeTAXjeD4QCZGsOQzBsm2bHl2njVF4Bo5NUxxDNaAYbMiTzXgQH4I5mV0JQyWZT0KwZIcmSDTjOCUTgDG0QyjOMoylHtR0jnGTszguK5WgHfkRyFEAlhKFwAFoAHk5SiTB-BvO8HyfdBv0vDdkQSCZ-BsfwMEwCJCgIEQpEil831iGCwuydADBYAx-DyAAhSdiHWcoABVlUyHDJggmDoNXOCEKtW0UNmVUMPVbDtWmWZ9X7YjjVInZhjBSj3mo9FYxGL17kY5j-U0wM2R0vSDJMjbtDMuNkUE4TyNE9NqHxKTcxJMkCwUihdDJbQ1Po9U2OUUsdNJRseJMHk7EHUABVHI4AEk-KCfy3PckJwiiUL12yCJoCQecwGKHxopQIJCjofxxhKCQzn8ABVAA1fzRgidB5QalpzWNFrkLadr0MwoZRBq3q9QIg0jXWYbyNbB122dV1ezgiMJqTabaQe+a-VY9iXpDEk3o+0w+MRXbEyEqbMRAQg01xLNCTO7hZPkkAuRUNk7ro70q2OnS8S+vkhz+5yeigF9J1IBMmpppC2pVRmupZnq8P6oiMK5k0yPM9srNObthYoiFJtomb1J9JiZdtvF7aoVWBI1-btd1sTM0kw3iWNy6QG0ABWNkS3um2lvE-FflrzhtAMzhdFrqhFNJZlmQoGgY4EOOu1sj1rG+xzBQEVyPIhk5gclKccP8OGZVQLKsl36HfwC+9H2fV8-EfQgyA9ymkm-JASh8NxCngfwcry-xiuIUr0H3yDYOpy0ft6YBzVFhYOuE+ocwGhHEi8BTS8zGsnHm1s5q+hYtnNuCAO5d20D3PuA9+7D1Hjtb2msYzF2xEdCSBIcyV3zHJSkZsKCcBoCoWuTdKwtw4greuVB3ofTHpZE4k8ex2Rnk7X6TkF5g2Xr5LG6AcYJgJoTA+G5qpkxfOgecxB3anzfKgG+qjsiX1IBKAImAShgDAAQeQBUQAGDql+TKMMshgBeNAGA84XAaBfA-J+CYPz1Wcb+N++UiolXWAYPEnA8iY3CV-SJeIKCxMMcEjc8Tv5RKoNoPIr9iARAMDfH2gDrR01Qh1JmGpwE6kgYRQa3M4HRyTlRcWKCGJoMWp8as3weHaD4crYw+d1biwsHTSELBELWlAG2AQEQcY6J8K0HwYw5yFBWGMYkIAoAHFkAwZZhRVkAFEkCMO2RMVoKJ3jtCiPcAA6pQ3EADWLwWKHOe5esSSjTvIUMmAgywgCYiUH56AAASHRUANMEK0ewhQJmbKEAwGFcKwUnMhf8024z0DuRLEoZkKhuD4OZEoVoHQCDLLFmQ+E-ZZ5DngkNa0AKthQDnPAAAxC4TgHKXAqBAHTAgmBDnxCkHtKaDAXZeCgCAYYAAvAGJz0BMlJPiRBLTKUHT5hZEAcz4JQEWXslZ6A1kws2Wc3ZIB9lHJOQIU1FzJiGpsDcmQ7zS7KtgaAF5zL0DOvTJwL5QLfkKSUipOC3yyYoohe2BFrYxhwsLMWUs0KY3oGIOGtFFzGGYvcjQOu9YlDaBoBQWuzIo2kvJVGNV4ifqMvpTgRlrz0Bsq5ZynldoGCyvlYqnOALRblqLimDV7ZtULKWQao1GzrU7JHQcw1xzTmTr4Ha653pvWPOrQ091TK3kPM+aCUN7ZFLKVxSG-1oLwVpsRUmzZw8bp5sTbC5NqbI3poEJmnFXIqAqCUBQJQBaSVIDJXYXtorqUSLXYcWtHqWXss5c23lMq5UYE7cqntKcRIDtmfM3VU7VnrMKCa+d5rR2zonechdVyHXLu3dQJ5jhINeu3b63dJ6-nHuBY+ljF772bKLKwhNnHkVnqfdXV9X6i3MhoB+4NDBS2AdQ9NBytLYEQc3Q26DXKW18AFUK0h+0xVSKOAATUQvBjtXAu0qopX26Z-MMM6r1YR6dY68MkbNRamdVqjg2rI-ax1SAV3iRo4p+t-nGMAr3QIa9t1WNhsExx6NXGBDm0tnegTqKhMMJfagCZ2KVCFr0F+-QnAeXSf-WWuTlbaNKbrZ6xtMHuW8s04Ku4IrU7iqOCgKVbaEMKrM8h8aQHyH9pmUcIdWH9WOdw-h0jDnLVzum5cnzlGPnUbA5V4LDG-XAoi9dKLTG2OxapCl5NAg64N10EdlNB2oXCay1i1kelcUftxR3P9AHLPAYUxumt1WoNNvq3yrTzXC7AbayAIz2ATOId68097g3rOatG-ZtzTmpuuaIx5rZBGFtLruVR119KN3rY+aFwFW2jilhYWw6Lp60sCCjUi47RxTvGHO-xh9V30UZtu+5S2X61B4jxcSkrb2BtUs+6thldHavqbg110z50+tILVaMhgCQCDoBgGIZzLcuQGBrHmoruhdLRODL8Hg+kh4SdZLXPN+Xa5tonIsgiBhmRFpoLXAt2bC212OhQCwPICCInaD4YUyabA9BpaAeIcdOEgCmAAGVaEjGQxBhR2CuY4KQ38vC+CUQAMQ8RESUzmA8x8irTBgERdV+EmBXrVzhMBglpsMflhz5Ba+IPkDo7hPKTsaWaEA5wQiwkFRM8qNmhyAVhMgpwKJ0Dj81ZnfgDBMVp8cwv9sXmtUvDFAINTsHhhD5cLCXsG-M8T47PHKefYq-QEKHvvEj+qCtGPxEToO47wnIAMI7-v0cVlVigBYAL+YoGAhQP+d+D+T+z+DALgoBhq5UXsb+CMjeAgS+UImmEeN4ouuwFgQAA

```

If sub-objects are present, they must always have a unique name. Make sure only to append the suffix with a dot "." (e.g. "Bottle.001") if the sub-object in question is reusing UV space from another object in the scene.


> Objects named with the suffix **".001"**, **".002"** etc are ignored in the baking process after model upload. If correct naming isn't used, your model may fail QA.
{: .warning }

<br>

---

## Object Hierarchy
<br>

---

## Object Transform
<br>

---

## Dimensions
<br>

All product models must conform to

> dsdsd
{ .note }

---

## Mesh
<br>
