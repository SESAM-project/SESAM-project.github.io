---
# Leave the homepage title empty to use the site title
title:
date: 2022-10-24
type: landing

sections:
  - block: hero

    content:
      title: |
        **SE**cure software engineering through **S**ensible **A**uto**M**ation

      image:
        filename: welcome_b.png
        postion: center
        size: cover

      text: |
        <br>
        SESAM aims to develop a comprehensive framework that enhances key development practices by integrating security seamlessly and sensibly. The project will focus on minimizing the disruption to developers’ workflows through automation and intelligent tool support.
        <br>
        The project is supported by the <a href="https://www.kks.se">KK Foundation</a>.
      
        
  - block: collection
    content:
      title: Latest Posts
      subtitle:
      text:
      count: 5
      filters:
        author: ''
        category: ''
        exclude_featured: false
        publication_type: ''
        tag: ''
      offset: 0
      order: desc
      page_type: post
    design:
      view: card
      columns: '1'
  
  # - block: markdown
  #   content:
  #     title:
  #     subtitle: ''
  #     text:
  #   design:
  #     columns: '1'
  #     background:
  #       image: 
  #         filename: welcome.jpg
  #         filters:
  #           brightness: 1
  #         parallax: false
  #         position: center
  #         size: cover
  #         text_color_light: true
  #     spacing:
  #       padding: ['20px', '0', '20px', '0']
  #     css_class: fullscreen

#- block: collection
#   content:
#     title: Project Publications
#     text: "Here you will find the latest publications from the SESAM project."
#     count: 5
#     filters:
#       folders:
#         - publication
#       publication_type: 'article'
#   design:
#     view: citation
#     columns: '1'

  - block: markdown
    content:
      title:
      subtitle:
      text: |
        {{% cta cta_link="./people/" cta_text="Meet the consortium →" %}}
    design:
      columns: '1'
---
