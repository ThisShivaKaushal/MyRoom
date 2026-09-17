# 🛋️ My Room
 
A little corner of the internet that looks like my actual desk. Not a "portfolio," not a "dashboard" — just my room, rebuilt in a browser.
 
![preview](./images/preview.png)

## What even is this
 
I got tired of portfolios that look like a resume wearing a website costume. So instead I just... built my room. The desk, the vinyl wall, the shelf with the trophy I definitely still bring up in conversations, the Luffy poster, the plant I'm somehow keeping alive — all of it, sitting there as a page you can actually explore instead of scroll past.


## What's actually in it
 
- **The desk** — laptop, headphones, and an ice-cold Diet Coke, because that's basically the holy trinity of getting anything done
- **The vinyl wall** — a wall of records and posters stacked up behind the desk like a mood board that never got taken down
- **The shelf** — books, a trophy, a little globe, a camera, a tiny Luffy figure standing guard, and a couple of baskets doing the honest work of hiding my clutter
- **The plant** — surviving, against all odds
- **The sneakers** — tucked in the corner because apparently even virtual rooms need virtual shoes on the floor
Every object is its own little element sitting exactly where it sits on my real desk. Nothing here is decorative filler — I picked each piece because it's actually mine.
 
## The hover thing
 
This is the part I'm most proud of, honestly. Hover over any object in the room and everything *else* fades and blurs out — like the rest of the room politely steps back so that one thing gets the spotlight. Move your cursor, the spotlight moves with it.
 
It's a small effect but it's the one that makes the page feel less like a static illustration and more like a room you're actually standing in and looking around.
 
Pure CSS, no JavaScript required:

```css
.coke {
    position: absolute;
    scale: 65%;
    left: 435px;
    top: 350px;
    width: 100px;
    height: auto;
    transition: transform 0.4s ease;
}

.coke:hover {
    transform: scale(1.2);
}

.room:has(.coke:hover)>*:not(.coke):not(.coketext) {
    filter: blur(1px);
    transition: filter 0.4s ease;
}
```

That's genuinely most of the magic. One selector doing the heavy lifting: "if the room is being hovered, blur everything that *isn't* the thing being hovered." Simple, but it makes the whole page feel alive.
 
## Built with
 
**HTML and CSS. That's the whole stack.**
 
No JavaScript. No React, no build tools, no `npm install`ing forty packages to render a plant. Every object is positioned, styled, and animated with plain old CSS — flexbox/absolute positioning for layout, `filter` and `transition` for the hover effect, and a lot of patience getting shadows to look right.
 
I wanted this to be the kind of project you can open in a text editor, read top to bottom, and understand in five minutes. No hidden build step, no config files to decode.
 
## Running it locally

There's nothing to install. That's the whole point.
 
```bash
git clone <your-repo-url>
cd my-room
open index.html
```

## File structure
 
```
my-room/
├── index.html      # the room itself
├── style.css       # everything — layout, positioning, the hover effect
├── assets/         # illustrations / images for each object
├    └──  preview.png      # screenshot for this README & many more
├── icons/          # icons
└── aboutme/        # aboutme page's stuff
     └── aboutme.html        # all the html of aboutme page
     └── aboutme.css         # all the css of aboutme page

```

## License
 
MIT. Take it, remix it, build your own room — just don't try to convince people the Diet Coke can was your idea.