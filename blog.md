---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

title: Home
description: Michael Webb (TheRandomMelon)'s official site for all of the *random* things he does.
layout: default
---

<div class="flex flex-row justify-center items-center" style="margin-top: 1rem; width: 100%;">
    <div class="window glass active" style="--window-background-color: #96B844; width: 100%;">
        <div class="title-bar">
            <div class="title-bar-text">Welcome to my blog!</div>
            <div class="title-bar-controls">
                <button aria-label="Minimize"></button>
                <button aria-label="Maximize"></button>
                <button aria-label="Close"></button>
            </div>
        </div>
        <div class="window-body">
            <div class="flex flex-row items-center" style="margin: 1rem;">
                <div class="items-center">
                    <h4 style="font-size: 1.25rem; font-weight: 500; margin-bottom: 0.5rem;">Latest posts</h4>
                    {% for post in site.posts limit:5 %}
                    <div class="flex flex-row sm-flex-column items-center">
                        <div class="window glass active sm-mb-post-preview" style="margin-top: 8px; max-width: calc(228px + 13px); --window-background-color: #96B844;">
                            <div class="title-bar">
                            </div>
                            <div class="window-body" style="width: 228px; height: 128px;">
                                <img src="{{ post.image }}" style="width: 228px; height: 128px;" />
                            </div>
                        </div>
                        <div class="flex flex-col" style="margin-left: 20px;">
                            <h4 style="font-size: 16px; margin-bottom: 4px;">
                                {{ post.title }}
                            </h4>
                            <p style="margin-bottom: 8px;">
                                {{ post.description }}
                            </p>
                            <button style="max-width: 84px;" onclick="window.location.href = '{{ post.url }}';">Read post</button>
                        </div>
                    </div>
                    {% endfor %}
                </div>
            </div>
        </div>
    </div>
</div>
