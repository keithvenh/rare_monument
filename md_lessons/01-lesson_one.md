# A Rare Monument

A Text Adventure Game by the VH Bros

## Markdown Lessons

### Lesson 1 | Headings and Paragraphs

Let me start by saying that I am not a markdown expert, but I have found that it is fairly easy to use. In fact, I used it to write all of these lessons. So I will teach you what I know, which is just enough to create these markdown files for our purposes.

Let's begin.

Markdown can be thought of as a way of creating a nice looking text document for the internet. As long as it has a site that can interpret it, that is. Fortunately for us, GitHub has that capability.

Let's start with headings. There are six levels of headings, level one being the most important, six being least. There should only be one level one heading per page. And as you nest headings under another heading you switch to the next level of heading, like this:

# Heading 1

## Heading 2

### Heading 3

## Heading 2

### Heading 3

#### Heading 4

## Heading 2

Creating Headings in Markdown is simple. First, make sure that it is on its own line, and that there is a blank line both ahead of and below it. Second start your line with a number of hashes equal to the level heading you desire. Last, add one space between your hashes and your heading text, like so:

```md
 1 # Heading 1
 2
 3 ## Heading 2
 4
 5 ### Heading 3
 6
 7 #### Heading 4
 8 
 9 ##### Heading 5
10
11 ###### Heading 6
```
Which results in:

# Heading 1

## Heading 2

### Heading 3

#### Heading 4

##### Heading 5

###### Heading 6

Simple, right. Now, paragraphs are just as simple. You need a lin above your paragraph, and a line below your paragraphs, just like with headers, And that's it. Just type your paragraph. Add an extra line between paragraphs to start a new paragraph.

For example:

```md
 1 ## A Heading for My Paragraph
 2
 3 This is my paragraph, and it is quite a doozy.
 4
 5 This is my second paragraph, but it's not as good as my first.
 6
 7 This is my last paragraph. The end.
```

Which results in:

## A Heading for My Paragraph

This is my paragraph, and it is quite a doozy.

This is my second paragraph, but it's not as good as my first.

This is my last paragraph. The end.

Congratulations! You now know as much as I do about Markdown paragraphs and headings!

[DIRECTORY](README.md) | [LESSON 2](02-lesson_two.md)