<style>
code{color: hotpink};
.code-wrapper{
    padding: 0 !important;
}
pre {
    padding: 0 !important;
}
strong {
    color: white;
}
</style>

# Tutorial: How to use reveal-md

---

### What is reveal.js?
`reveal.js` is a powerful JavaScript library for creating presentations in HTML/CSS

---

#### Example Code
```html
	<body>
		<div class="reveal">
			<div class="slides">
				<section>Slide 1</section>
				<section>Slide 2</section>
			</div>
		</div>
		<script src="js/reveal.js"></script>
		<script>
			Reveal.initialize();
		</script>
	</body>
```

---

#### Slide 1
---
#### Slide 2
---

![dont.gif](images%2Fdont.gif)

---

### Markdown to the rescue!
![markdown.jpeg](images%2Fmarkdown.jpeg)

---
### Markdown refresher
#### `Headings`
```markdown
# H1
## H2
### H3
#### H4
##### H5
###### H6
```

---
# H1
## H2
### H3
#### H4
##### H5
###### H6
---
### Markdown refresher
#### `Formatting`
```markdown
Emphasis with *asterisks* or _underscores_.

Bold, with **asterisks** or __underscores__.

Combined with **asterisks and _underscores_**.

Strikethrough with tildes. ~~Scratch this.~~
```
---
#### `Formatting`
Emphasis with *asterisks* or _underscores_.

Bold, with **asterisks** or __underscores__.

Combined with **asterisks and _underscores_**.

Strikethrough with tildes. ~~Scratch this.~~

---
#### `Lists`
```markdown
> Ordered
1. First ordered list item
2. Another item

> Unordered
* Unordered list can use asterisks
- Or minuses
+ Or pluses
```
---
#### `Lists`
> Ordered
1. First ordered list item
2. Another item

> Unordered
* Unordered list can use asterisks
- Or minuses
+ Or pluses
---
### Final ingredient before 🚀 - `reveal-md`
- `reveal-md`: *Convert existing `markdown` files to `reveal.js` HTML/CSS files and host them on a local server*
---
### Setup we will use
![overview.png](images%2Foverview.png)
---
### Getting started
#### Install `reveal-md`
```bash
npm install -g reveal-md
```
---
### Basic syntax of `reveal-md`
```bash
# 1. Create slides.md with a `# Hello World`
reveal-md slides.md
# 2. Even better: All files (recursively in current dir)
reveal-md .
## 3. Best ✨: Auto-Refresh on change
reveal-md . -w
```
---
### Intermediate syntax
- Use HTML/CSS/Javascript
  - Style tag at the beginning
  - Inline Markdown styling ([docu](https://revealjs.com/markdown/#element-attributes))
---
### Why this is nice?
- Version everything in Git and work together on it!
- Endless possibilities (CSS/HTML/JS)
- Show plugins
- Use ChatGPT for slide generation
---
### Use ChatGPT for slide generation <!-- .slide: data-background-color="#00A67E" -->
---
<!-- .slide: data-background-color="#00A67E" -->
<img style="position: relative; top: 40px;" height="40px" src="images%2Fgpt.png"> ...
- <span style="font-size: larger">🗣</span>️  *Generate me 3 markdown slides for reveal.js which explain the importance of carrot farming in south africa. (Create markdown code snippets, always use a Level 3 header ### for the title), use bullet points and no long sentences, use emojis when appropriate)*
---
### The Importance of Carrot Farming in South Africa 🥕🇿🇦
- Carrots are one of the most widely cultivated vegetables in the world
- South Africa is one of the largest producers of carrots in Africa
- Carrot farming is an important source of income for many farmers in South Africa
---
### Nutritional Value of Carrots 🥕🍎
- Carrots are an excellent source of vitamins and minerals, including vitamin A, potassium, and fiber
- Eating carrots can help improve eye health, lower blood pressure, and boost immunity
- Including carrots in a balanced diet can help prevent chronic diseases like cancer and heart disease
---
### Economic Impact of Carrot Farming in South Africa 💰👨‍🌾
- Carrot farming contributes significantly to South Africa's agricultural sector, which employs over 800,000 people
- Carrot exports generate valuable foreign exchange for the country
- Many small-scale farmers rely on carrot farming for their livelihoods, making it an important driver of rural development in South Africa
---
<!-- .slide: data-background-color="#00A67E" -->

<img style="position: relative; top: 40px;" height="70px" src="images%2Fgpt.png"> ...
- <span style="font-size: larger">🗣</span>️  *Extend the markdown snippets with inline spans and css so that each word carrot is colored in orange*
---
<style>
.carrot {
  font-weight: bold;
  color: orange;
}
</style>
### The Importance of Carrot Farming in South Africa <span class="carrot">🥕</span><span style="color: black;">🇿🇦</span>

- <span class="carrot">Carrots</span> are one of the most widely cultivated vegetables in the world
- South Africa is one of the largest producers of <span class="carrot">carrots</span> in Africa
- <span class="carrot">Carrot</span> farming is an important source of income for many farmers in South Africa
---
```html
<style>
span[style*="color: orange;"] {
  font-weight: bold;
}
</style>
### The Importance of Carrot Farming in South Africa
<span style="color: orange;">🥕</span>
<span style="color: black;">🇿🇦</span>

- <span style="color: orange;">Carrots</span>
are one of the most widely cultivated
vegetables in the world

- South Africa is one of the largest producers of 
<span style="color: orange;">carrots</span> in Africa

- <span style="color: orange;">Carrot</span> farming is an important source of income for many farmers in South Africa
```
---
<!-- .slide: data-background-color="#00A67E" -->

<img style="position: relative; top: 40px;" height="70px" src="images%2Fgpt.png"> ...
- <span style="font-size: larger">🗣</span>️  *Also animate the carrot emoji on the first slide to slightly wiggle (also return markdown with html/css elements)*
---
<style>
  span[style*="color: orange;"] {
    font-weight: bold;
    animation: wiggle 0.5s infinite;
    display: inline-block;
  }

  @keyframes wiggle {
    0% { transform: rotate(-2deg); }
    50% { transform: rotate(2deg); }
    100% { transform: rotate(-2deg); }
  }

</style>
### The Importance of Carrot Farming in South Africa <span style="color: orange;">🥕</span><span style="color: black;">🇿🇦</span>
- <span style="color: orange;">Carrots</span> are one of the most widely cultivated vegetables in the world
- South Africa is one of the largest producers of <span style="color: orange;">carrots</span> in Africa
- <span style="color: orange;">Carrot</span> farming is an important source of income for many farmers in South Africa
---
### New times allow for new games ...
`Proposal`

🎲  *Everyone has 10 minutes time to create a topic he is given randomly and needs to prepare a <span style="color: orange;">3</span> -minute <span style="color: orange;">⏰</span> talk.*
---
### Let's play this next week?
#### Who is interested?
---
### Let's make a poll
We also can do this in reveal.js too
---
## First step
- Visit [vag.app/karaoke](http://vag.app/karaoke) with your phone 📲
---
### Who wants to participate in our PowerPoint Karaoke?
<div class="poll">

- Not this time, I'm good
- Sure, book me in!
- Yes, but I only want to watch...
</div>