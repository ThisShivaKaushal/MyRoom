# My Room

This room is where my favorite belongings live and where I spend most of my time. But today, the doors are wide open—because I’m officially making my room public!


## Descrption
 
 I was completely bored by portfolio websites, because if you make it simple, then for people it is not worth it. For this reason, you have to make a flashy one with a ton of animation, which people with low-end mobiles are not able to open. Because of this reason, I chose to make a unique one. I just duplicated my room into a web-playable website. Now you can interact with my room—just hover on any object, like when our eyes focus on anything then everything gets blurred, the same principle I applied here. And yeah, this is the brief of my project. And also, when you click on the laptop, then you will transfer to my about me page, where you can know a lot of stuff.

### Screenshots

 ![preview](./images/preview.png)
 ![preview](./images/preview1.png)


## What's actually in it
 
- **The desk** — laptop, headphones, and an ice-cold Diet Coke, because that's basically the holy trinity of getting anything done
- **The vinyl wall** — a wall of records and posters stacked up behind the desk like a mood board that never got taken down
- **The shelf** — books, a trophy, a little globe, a camera, a tiny Luffy figure standing guard, and a couple of baskets doing the honest work of hiding my clutter
- **The plant** — surviving, against all odds
- **The sneakers** — tucked in the corner because apparently even virtual rooms need virtual shoes on the floor

 
## The hover thing
 
This is the part I'm most proud of, honestly. Hover over any object in the room and everything *else* fades and blurs out — like the rest of the room politely steps back so that one thing gets the spotlight. 

 
Pure CSS:

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

 
## Built with
 
**HTML and CSS. That's the whole stack.**
 
I used HTML and CSS only to build this project because this is easy for me to write, and I am friendly with it, so I used this.
 
## Running it locally

 
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