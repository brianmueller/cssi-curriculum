---
  layout: post
  title: Fortune Teller Day 1 Potential Solutions
  language: app-engine
---
# Fortune Teller Boilerplate:
You can fork and clone this repo [here](https://github.com/google-cssi/cssi-6-fortune-teller-first-steps).

We are going to continue working on your fortune-teller apps through additional exercises that will add in user functionality. If you did not get a chance to finish the earlier fortune-teller exercises, feel free to use and build upon the basic, working code in this repo so you can focus on understanding user functionality. The code in this repo will give you access to an 8ball and Fortune Cookie handler that displays a random fortune on two separate templates. In the coming exercises, you will need to add template variables, additional logic, forms and change how static files are handled.

Notice that because multiple handlers need a way to access a message indexed at either a random  or  specific number, a global function, `getMessage()` is defined. `getMessage()` is outside any of the handler classes so that it can be used multiple times:

```
def getMessage(any_list,specificNumber=0):
    # if there is no second parameter passed, then pick a random index
    if specificNumber == 0:
        index = random.randint(0,len(any_list)-1)
    # if there is a specificNumber, then use that to index the messages
    else:
        index = specificNumber
    return any_list[index]
```
