My final project for the Intro to Python course by Code First Girls

## Table of contents

- [Overview](#overview)
  - [The Project Brief](#the-project-brief)
  - [Example code](#Example-code)
  - [Links](#links)
- [My Process](#my-process)
  - [What I Learnt](#what-i-learnt)
  - [Continued Development](#continued-development)
- [Author](#author)

## Overview

### The Project Brief
- In this project you'll create a program to search for recipes based on an ingredient. The standard project uses the Edamam Recipe API, but can be changed to use a different API after completing the required tasks.
- You will not need any additional knowledge beyond what is covered in this course to complete this
project.

### Example code

```python
import requests

def recipe_search(ingredient):
# Register to get an APP ID and key https://developer.edamam.com/
app_id = ''
app_key = ''
result = requests.get(
'https://api.edamam.com/search?q={}&app_id={}&app_key={}'.format(ingredient, app_id,

app_key)
)
data = result.json()
return data['hits']

def run():
ingredient = input('Enter an ingredient: ')
results = recipe_search(ingredient)
for result in results:
recipe = result['recipe']
print(recipe['label'])
print(recipe['uri'])
print()

run()
```


### Links

- Edamam API Documentation: [Edamam](https://developer.edamam.com/edamam-docs-recipe-api)

## My Process

### What I learned

- A lot! 
- I wanted to expand on the original code to add in additional search parameters as well as the option to save to a meal plan.
- Initially my worry was that there was a neater way to arrange asking the questions, but I decided for my first project to keep it simple.
- Combining two skills that I had learnt on the course, adding to a csv and user input, were the easiest parts for me, but making sure I had the parameters 
in the code correctly was the biggest hurdle, especially when using data from the API.
- How to use Stack Overflow. At one point I had hit a wall and thought, based what I had learnt on the course, that I had bitten off more than I could chew so asking for help and advice was really useful and gave me the push I needed to work through my problems with my code.

### Continued development

Continue to learn Python concepts now that the course has finished. I have enrolled on a few other courses so will take those whilst studying other areas of Python that I'm not as confident with.

### Useful resources

- [HTML Tree Generator](https://chrome.google.com/webstore/detail/html-tree-generator/dlbbmhhaadfnbbdnjalilhdakfmiffeg) - Generates websites' DOM trees
- [CSS Peeper](https://chrome.google.com/webstore/detail/css-peeper/mbnbehikldjhnfehhnaidhjhoofhpehk?hl=en) - extracts the key CSS elements of a webpage

## Author

- LinkedIn - [Jessica Ashby](https://www.linkedin.com/jessicaashby)
