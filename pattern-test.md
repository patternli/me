---
layout: base
title: "Pattern Test"

cardspecial:
  settings:
    class: 
  list:
    - title: This is my special card
      feature: http://placekitten.com/450/450
      short: it is very special to me
      class: card-special
card:
    settings:
      class: grid-250
    list:
        - title: My first card
          flag: super
          meta: "Date: November 25th 2022 | Location: Bothell"
          short: Has to be great
          feature: http://placekitten.com/350/300
          class:
          links:
            - link: youtube.com
              text: youtube
              class: btn btn-alpha
            - link: amazon.com
              text: amazon
              class: btn btn-text
        - title: My second card
          flag: flash
          meta: "Date: November 26th 2022 | Location: Sammamish"
          short: getting a chai while the walkers walk
          feature: http://placekitten.com/350/200
          class: card-tag
          links:
            - link: youtube.com
              text: youtube
              class: btn btn-zeta
            - link: amazon.com
              text: amazon
              class: btn
        - title: My third card
          meta: "Date: November 26th 2022 | Location: home"
          short: watching moonhaven
          feature: http://placekitten.com/500/300
          flag: Just In!
          links:
            - link: youtube.com
              text: youtube
              class: btn btn-alpha
            - link: amazon.com
              text: amazon
              class: btn
cardleft:
    settings:
      class: grid-250
    list:
        - title: My fourth card
          meta: "Date: November 26th 2022 | Location: home"
          short: |
            still watching moonhaven

            it's awsome
          class: card-left col-2
          feature: http://placekitten.com/350/350
          links:
            - link: youtube.com
              text: youtube
            - link: amazon.com
              text: amazon

---

{% include patterns/card/card.md content=page.cardspecial %}

{% include patterns/card/card.md content=page.card %}

{% include patterns/card/card.md content=page.cardleft %}
