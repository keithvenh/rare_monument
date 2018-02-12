# A Rare Monument

A Text Adventure Game by the VH Bros

## Markdown Lessons

### Lesson 3 | Links, Bold, Italics and Images

In this lesson spice up our markdown with different styles, as well as how to add links to other pages.

#### Links

Links are quite simple. There are two elements to every link: the text you want to be clickable, and the location you want people to go when the link is clicked. Here is the syntax:

```md
 1 [Your Clickable Text](https://www.yourweblink.com)
 2
 3 [Google](https://www.google.com)
```

It's as simple as that. Put your text inside of brackets ``` [] ```. Put your web address inside parentheses ``` () ```. Don't put a space between them.

[Google](https://www.google.com)

#### Bold Text

Bold, or what is referred to as 'strong emphasis' can be achieved in one of two ways. The first is by surrounding the text you want bold with sets of 2 asterisks. The second is by surrounding the text you want bold with sets of 2 underscores. Observe:

```md
 1 **Bolded By Asterisks**
 2
 3 __Bolded By Underscores__
```

They Both result in the same style:

**Bolded By Asterisks**

__Bolded By Underscores__

#### Italicized Text

Italics, or emphasis, can be achieved in the same manner as bold, except rather than sets of two asterisks or underscore, you only use a set of 1 to surround your text.

```md
 1 *Italicized with Asterisks*
 2
 3 _Italicized with Underscores_
```

The result is the same either way.

*Italicized with Asterisks*

_Italicized with Underscores_

#### Combining Styles

If you need your text to be *both* italicized and bold, you can achieve this by mixing your choice of asterisks and underscores.

```md
 1 **Bold with asterisks, _italicized with underscores_**
 2
 3 __Bold with underscores, *italicized with asterisks*__
 4
 5 *Italicized with asterisks, __bold with underscores__*
 6
 7 _Italicized with underscores, **bold with asterisks**_
 8
 9 **_Bold and Italicized_**
10
11 __*Bold and Italicized*__
12
13 *__Bold and Italicized__*
14
15 _**Bold and Italicized**_
```

Which you choose really depends on your preference, just make sure you match your asterisks and underscores, otherwise you won't achieve the result you desire.

**Bold with asterisks, _italicized with underscores_**

__Bold with underscores, *italicized with asterisks*__

*Italicized with asterisks, __bold with underscores__*

_Italicized with underscores, **bold with asterisks**_

**_Bold and Italicized_**

__*Bold and Italicized*__

*__Bold and Italicized__*

_**Bold and Italicized**_

You can now harness the power of emphasis and strong emphasis, or italics and bold-face fonts!

#### Images

Image syntax is identical to links with the addition of one thing: you start it with an ``` ! ```.

```md
 1 ![Your alt Text](Your Image Location)
```

The other differences are what goes between the ``` [] ``` and the ``` () ```. As seen in the markdown above, alt text goes between the brackets. Alt text is what screen readers use for the visually impaired. It is important to use a good description of your image as alt text to make your site as accessible as possible.

```md
 1 ![VH Bros Logo](Your Image Location)
```

Between the parentheses you will put the location where your image file can be found. This may be a web address like google.com/images, but more likely it is a file stored in the same location as your markdown.

```md
 1 ![VH Bros Logo](../images/vh-bros-logo-dark.png)
```
Here we see something that might be new, the ``` .../images ```. This is called a relative path. It is a way of telling the computer how to find the file based on the location of the file the computer is currently working at. If the image was in the same directory, or folder, you would simply need the image name, but because the images are stored in a separate dirctory, you need to specify how to get to the directory to find the image. Here is an example of how our directory looks:

- rare_monument
  - git_lessons
    - 01-lesson_one.md
    - 02-lesson_two.md
    - 03-lesson_three.md
    - 04-lesson_four.md
    - 05-lesson_five.md
    - README.md
  - images
    - vh-bros-logo-black.png
    - *vh-bros-logo-dark.png*
    - vh-bros-logo-light.png
    - vh-bros-logo-medium.png
    - vh-bros-logo-white.png
  - js_lessons
  - md_lessons
    - 01-lesson_one.md
    - 02-lesson_two.md
    - **03-lesson_three.md**
    - README.md
  - README.md

The file we are currently working in (03-lesson_three.md) is bold, and the image file we need access to (vh-bros-logo-dark.png) is italicized. What we need to do is move from our current director, or folder, (md_lessons), out to our primary directory (rare_monument) and into the images directory. To do this we specify a relative path do this folder.

The ``` .. ``` in the relative path above simply means, go to my parent directory, or the folder above the one we are currently in. In our scenario, this gets us into the rare_monument directory, and then from there we can specify the path to the file we want, which is images/vh-bros-logo-dark.png. This is a convenient way to link to documents that are withing the same parent directory as well. And the good new is that ``` .. ``` can be combined to go back as far as we need. For example, lets say we have the directory structure below:

- numbers
  - one
    - one_one
      - one_one_one
        - one_one_one_one
          - our_file.md
      -one_one_two
    -one_two
  -two
    -two-one
      - our_image.jpg

Let's say we are in the ``` one_one_one_one ``` directory working on ``` our_file.md ``` and want to access ``` our_image.jpg ```. We could combine our ``` .. ``` to get all the way out to the ``` numbers ``` directory and then work our way down to our image file. We would need to four sets of ``` .. ``` separated by slashes. One to go from ``` one_one_one_one ``` (where we currently are) to ``` one_one_one```. A second to go from ``` one_one_one ``` to ``` one_one ```. A third to go from ``` one_one ``` to ``` one ```. And a fourth to go from ``` one ``` to ``` numbers ```. From there, we can simply add the path to our file, which is ``` two/two-one/our_image.jpg ```. So our finally link would look like this:

```bash
../../../../two/two-one/our_image.jpg
```

It is rare that you would need to go so deep with your directories, but it is comforting to know there is an easy way to handle links even if you do.

Now, back to our image. This is where we left it: ``` ![VH Bros Logo](../images/vh-bros-logo-dark.png) ```. We could leave it at this, but there is an option to add a hover text to your images if you desire. To do so, simply add a space between your file path, and put the text you want to display on hover in quotes.

```md
 1 ![VH Bros Logo](../images/vh-bros-logo-dark.png "VH Bros Awesome New Logo!")
 ```

 ![VH Bros Logo](../images/vh-bros-logo-dark.png "VH Bros Awesome New Logo!" )

 And there you have it. A fancy image in your markdown!

This marks the end of your Markdown tutorial. In the last three lessons you learned about headers and paragraphs, ordered lists, unorderd lists and checklists, and now you've learned links, bold, italics and images. You truly are a Markdown Champion! Give yourself a gold star!

Here is a fun tip for the road. If you want to create strikethrough text, surround it with two ``` ~ ```.

```md
 1 ~~strikethrough~~
```

~~strikethrough~~

Give yourself another gold star!