# A Rare Monument

A Text Adventure Game by the VH Bros

## Markdown Lessons

### Lesson 2 | Lists and More Lists 

In this lesson, we will learn how to make three types of lists: Unordered, or bulleted, lists; Ordered, or numbered, lists, and checklists.

#### Unordered Lists 

An unordered list is simply a list where the order doesn't matter, such as a grocery list or a to-do list. We would usually represent these with bullet points. To make an unordered list, simply begin a new paragraph, then start your line with a dash. Follow your dash with a single space and then add your list item. For example:

```
 1 - List Item 1
 2 - List Item 2
 3 - List Item 3
```

This would result in:

- List Item 1
- List Item 2
- List Item 3

You get the idea. Now, the nice thing about lists is that you can have nested lists, similar to an outline. To do so, simply indent the nested item with 2 spaces, and type out your list item like normal. For example:

```
 1 - List Item 1
 2 - List Item 2
 3   - List Item 2-1
 4   - List Item 2-2
 5 - List Item 3
 6   - List Item 3-1
 7     - List Item 3-1-1
 8 - List Item 4
```

This would result in:

- List Item 1
- List Item 2
  - List Item 2-1
  - List Item 2-2
- List Item 3
  - List Item 3-1
    - List Item 3-1-1
- List Item 4

Pretty Simple, right? (Note: For an unordered list you can begin your line with ``` - ```, ``` * ```, or ``` + ```)

#### Ordered Lists 

The good news is that ordered lists follow the same pattern, the only differences being that you start your line with a number followed by a period, and to nest items you have to indent them with four spaces, like so:

```
 1 1. List Item 1
 2 2. List Item 2
 3     1. List Item 2-1
 4     2. List Item 2-2
 5 3. List Item 3
 6     1. List Item 3-1
 7         1. List Item 3-1-1
 8 4. List Item 4
```

Which gives us:

1. List Item 1
2. List Item 2
    1. List Item 2-1
    2. List Item 2-2
3. List Item 3
    1. List Item 3-1
        1. List Item 3-1-1
4. List Item 4

Again, pretty simple, isn't it?

#### Checklists

Checklists are a little more complicated, but not much. They are essentially an unordered list with a little special magic added to the beginning. These types of list are specially supported by GitHub. Observe:

```
 1 - [ ] Incomplete Task 1
 2 - [ ] Incomplete Task 2
 3   - [ ] Incomplete Subtask 2-1
 4 - [x] Complete Task 1
 5   - [x] Complete Subtask 1-1
 6 - [ ] Incomplete Task 3
 ```

 Which Yields:

- [ ] Incomplete Task 1
- [ ] Incomplete Task 2
  - [ ] Incomplete Subtask 2-1
- [x] Complete Task 1
  - [x] Complete Subtask 1-1
- [ ] Incomplete Task 3 

Its pretty simple, but just to make it more explicit, here are the patterns. 

For an incomplete taks it goes:

``` - ``` ``` space ``` ``` [ ``` ``` space ``` ``` ] ``` ``` space ``` ``` YOUR TASK ```

For a complete taks it goes:

``` - ``` ``` space ``` ``` [ ``` ``` x ``` ``` ] ``` ``` space ``` ``` YOUR TASK ```

As for subtasks: indent by 2 spaces. That's really all there is to it. You now know how to make unordered lists, ordered lists and checklists in markdown. One last thing to note, however is that you can mix one list with a different sublist of a different type, I'm sure you can figure out how it is done.

```
 1 1. Ordered Item 1
 2   - Unordered Sub Item
 3   - Unordered Sub Item
 4 2. Ordered Item 2
 5     1. Ordered Sub Item
 6 3. Ordered Item 3
 7
 8
 9 - Unordered Item 1
10   1. Ordered Sub Item
11   2. Ordered Sub Item
12 - Unordered Item 2
13   - Unordered Sub Item
14 - Unordered Item 3
```

1. Ordered Item 1
  - Unordered Sub Item
  - Unordered Sub Item
2. Ordered Item 2
    1. Ordered Sub Item
3. Ordered Item 3
- Unordered Item 1
    1. Ordered Sub Item
    2. Ordered Sub Item
- Unordered Item 2
  - Unordered Sub Item
- Unordered Item 3

Easy enough? Good. Here is a review:

Unordered List: ``` - ``` ``` space ``` ``` YOUR TASK ```

Ordered List: ``` 1. ``` ``` space ``` ``` YOUR TASK ```

Incomplete Checklist: ``` - ``` ``` space ``` ``` [ ``` ``` space ``` ``` ] ``` ``` space ``` ``` YOUR TASK ```

Complete Checklist: ``` - ``` ``` space ``` ``` [ ``` ``` x ``` ``` ] ``` ``` space ``` ``` YOUR TASK ```

And that is all you need to know about lists!

[DIRECTORY](README.md) | [LESSON 1](01-lesson_one.md) | [LESSON 3](03-lesson_three.md)