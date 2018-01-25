---
layout: sidebar
title: Stacked navigation
description: Navigation to support deeper content
---

Navigation to support sub-pages within a section
{:.lead}

## Why?
When you need to sign post a user to child pages within a section.

## Usage
- Use in combination with [breadcrumbs]({{ site.baseurl }}{% link components/breadcrumbs.md %})
- to display a secondary navigational hierarchy 
- when you need our users to navigate through subpages or content chapters
- always position to the far left of the interface to maintain consistency
- try to keep navigational links short
- always use an active link to display what page the user is on
- display one level at a time.
- use `aria-current="page"` to highlight the current page
- use `aria-label="navigation name"` or `aria-labelledby="id-here"` on the root `nav` element
- stacked nav expands to fill the available space, so usually wrap in a grid.

## Variants

### Root page current

When the navigation root is the current page:

{% capture root %}
<div class="grid" data-no-inpagenav>
    <div data-g="12 sm:4">
        <nav class="stacked-nav">
            <h2 class="stacked-nav__root">
                <a href="#" aria-current="page">
                    Root link
                </a>
            </h2>

            <ul class="stacked-nav__list">
                <li class="stacked-nav__list-item">
                    <a href="#">
                        Link 1
                    </a>
                </li>
                <li class="stacked-nav__list-item">
                    <a href="#">
                        Link 2
                    </a>
                </li>
                <li class="stacked-nav__list-item">
                    <a href="#">
                        Link 3
                    </a>
                </li>
            </ul>
        </nav>
    </div>
</div>
{% endcapture %}
{% include example.html lang='html' body=root %}

### Sub page current

When a sub page is the current page:

{% capture sub %}
<div class="grid" data-no-inpagenav>
    <div data-g="12 sm:4">
        <nav class="stacked-nav">
            <h2 class="stacked-nav__root">
                <a href="#">
                    Root link
                </a>
            </h2>

            <ul class="stacked-nav__list">
                <li class="stacked-nav__list-item">
                    <a href="#">
                        Link 1
                    </a>
                </li>
                <li class="stacked-nav__list-item">
                    <a href="#" aria-current="page">
                        Link 2
                    </a>
                </li>
                <li class="stacked-nav__list-item">
                    <a href="#">
                        Link 3
                    </a>
                </li>
            </ul>
        </nav>
    </div>
</div>
{% endcapture %}
{% include example.html lang='html' body=sub %}