# Sass Notes : 

## Variables : 
 ```
 $var : 0 ; 
 ```

## For Loop :
 ```
 @for $i from 1 through 3 {
    .container>div:nth-child(#{$i})
     {
        // background-color: rgba(255,192,203 , 1/$i);
         background-color: red;
      }
  }
 ```
 ```
@for $i from 1 through 10 {
    $num:$num+1;
    .container>div:nth-child(#{$i})
    {
      
      background-color: rgba(255,192,203 , 1/$i);

    }
    .container>div:nth-child(#{$i}):hover
    {
        background-color: rgba(255,192,203 , $i/10);
    }
}
```
----
## Functions:
```
@function division($num1 , $num2)
{
  $result:$num1/$num2;
  @return $result;
}

@for $i from 1 through 10 {
    .container>div:nth-child(#{$i})
    {
      background-color: rgba(255,192,203 , division(1,$i));
     //background-color: red;
    }
}
```
----
## Mixins :
```
@mixin divStyle {
    background-color: pink;
    height: 50px;
    width:50px;
    display: flex;
    justify-content: center;
    align-items: center;
}
div{
    @include divStyle;
  
}
```
----
## Librairies : 
```
@use "sass:math";

.container {
  display: flex;
}

article[role="main"] {
  width: math.div(600px, 960px) * 100%;
}

aside[role="complementary"] {
  width: math.div(300px, 960px) * 100%;
  margin-left: auto;
}
```
----

## Import :
```
// foundation/_code.scss
code {
  padding: .25em;
  line-height: 0;
}

// style.scss
@import 'foundation/code', '.............';

```

Documentation [Sass Website]:(https://sass-lang.com/documentation)



    


