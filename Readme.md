# Google CSSI Curriculum
This is the CSSI Curriculum site code.

## Developing the site
The site uses Jekyll, so that we can write curriculum in markdown (mostly just plain text) and then get it turned into HTML pages automatically. Development is pretty easy, especially if you are just adding content - things should 'just work'.

### Getting Started
Check that ruby is installed, and check your version. Any version > 2 should work, but if you are hitting errors, it could be your version. Tested on version 2.2.0.

```
gem install jekyll
git clone https://github.com/google-cssi/cssi-curriculum.git
cd cssi-curriculum
jekyll serve
```

Jekyll will build the site and make it available at localhost:4000 (by default - check the output to see which port it chooses for you). By default, it will also watch for changes, so when you save changes to the files, Jekyll will rebuild the site and your changes will be there on refresh.

### For curriculum developers please read:
[Curriculum Annotations](https://docs.google.com/document/d/1rRqt5vx8XbmI2WFipGv56BpuEjmnL2mlPTzhND9UnDY/edit#)
