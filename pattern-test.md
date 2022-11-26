---
layout: base
title: "Pattern Test"

card:
    settings:
        class: card-group
        columns: 2
    list:
        - title: My first card
          flag: super
          meta: "Date: November 25th 2022 | Location: Bothell"
          body: Has to be great
          image: http://placekitten.com/300/300
          class: card-left
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
          body: getting a chai while the walkers walk
          image: http://placekitten.com/300/200
          links:
            - link: youtube.com
              text: youtube
              class: btn btn-zeta
            - link: amazon.com
              text: amazon
              class: btn

---


{% include patterns/card/card.md content=page.card %}