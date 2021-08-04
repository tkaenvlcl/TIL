# Markdown grammar

***

## 1. Heading  ```#```

The more #, the smaller the letter  
There's up to level 6

``` 
# Heading level 1
## Heading level 2
### Heading level 3
```

# Heading level 1

## Heading level 2

### Heading level 3

***

## Emphasis  ```*``` ```**``` ```***```

```
*Italic*
**Bold**
***Bold with Italic***
```

*Italic*  
**Bold**  
***Bold with Italic***

***

## 3. Block Quote  ```>```

```
> This is block quote
>
>> Block quotes can be nested
```

> This is block quote
>> Block quotes can be nested
>>- Block quotes can contain other .md elements
>>- But not all elements can be used

***

## 4. Ordered Lists ```1.```

The numbers don’t have to be in numerical order, but the list should start with the number one.

```
1. First item
1. Second item
1. Third item
1. Fourth item
```

1. First item
2. Second item
3. Third item
4. Fourth item

```
1. First item
2. Second item
3. Third item
    1. Indented item
    2. Indented item
4. Fourth item
```

1. First item
2. Second item
3. Third item
    1. Indented item
    2. Indented item
4. Fourth item

***

## 5. Unordered Lists : ```-``` ```*``` ```+```

You can use dashes(-), asterisks(*), or plus signs(+)

```
- First item
- Second item
- Third item
- Fourth item
```

- First item
- Second item
- Third item
- Fourth item

```
+ First item
+ Second item
+ Third item
    * Indented item
    * Indented item
+ Fourth item
```

+ First item
+ Second item
+ Third item
    * Indented item
    * Indented item
+ Fourth item

***

## 6. Code Blocks ````  ``` ````

````
```python  
print("Hello world!") 
```
````

``` python  
print("Hello world!") 
```  

***

## 7. Links

```
[Google](https://www.google.co.kr "Google")
```

[Google](https://www.google.co.kr "Google")

```
<https://www.google.co.kr>
```

<https://www.google.co.kr>

```
You are the dancing queen  
Young and sweet  
Only seventeen  
[Dancing queen][1]

[1]: <https://www.youtube.com/watch?v=xFrGuyw1V8s> "Youtube"
```

You are the dancing queen  
Young and sweet  
Only seventeen  
[Dancing queen][1]

[1]: <https://www.youtube.com/watch?v=xFrGuyw1V8s> "Youtube"

***

## 8. Image ```!```

```
![markdown_logo](https://raw.github.com/dcurtis/markdown-mark/master/png/208x128.png)
```

![markdown_logo](https://raw.github.com/dcurtis/markdown-mark/master/png/208x128.png)

***

## 9. Table ```|```

### 9.1 Structure

```
| First Header  | Second Header | Third Header         |
| :------------ | :-----------: | -------------------: |
| First row     | Data          | Very long data entry |
| Second row    | **Cell**      | *Cell*               |
| Third row     | Cell that spans across two columns  ||
```

| First Header  | Second Header | Third Header         |
| :------------ | :-----------: | -------------------: |
| First row     | Data          | Very long data entry |
| Second row    | **Cell**      | *Cell*               |
| Third row     | Cell that spans across two columns  ||

### 9.2 Alignment

```
| Header One | Header Two | Header Three | Header Four |
| ---------- | :--------- | :----------: | ----------: |
| Default    | Left       | Center       | Right       |
```

| Header One | Header Two | Header Three | Header Four |
| ---------- | :--------- | :----------: | ----------: |
| Default    | Left       | Center       | Right       |

### 9.3 Column spanning

```
| Column 1 | Column 2 | Column 3 | Column 4 |
| -------- | :------: | -------- | -------- |
| No span  | Span across three columns    |||
```

| Column 1 | Column 2 | Column 3 | Column 4 |
| -------- | :------: | -------- | -------- |
| No span  | Span across three columns    |||
