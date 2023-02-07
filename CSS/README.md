# What is CSS? 

The are styles and colors for the web.

# What is a Selector? 

This is a form to select a element and modify by CSS. The kind of selector depends of this modify. There are: 

    - tags: p, span, body. *1 point*
    - .Class: class = 'title'   *10 points*
    - #id: id ='my-favorite'    *100 points*


# What is BEM : Block Element Modifier? 

There are rules to do the CSS more easy. 

Only classes. They use the model in components.

Structure: .block__element--modifier. 

*Block*: independent parts of the web site. They have sense by themselves. And we can reuse this use. 

    .block

    Example: .header
             .my-block-compound. 
            
            We have a button. We can give this name like'button'. Or a post/like a instagram post. Use can reuse a post.  

            A menu of a website: .menu-

*Elements*: is dependent to block. And no has sense by himself.

    .block__element

    Example: the elements in a menu. We can use elements to modify him. 

        .menu {} 

        .menu__logo {}

        .menu__button {}

    Attention: 
        
        We can confuse element with block.  For find a solution for that, we can ask us: That part of the code is independent of the rest? 

        Elements doesn't have subElements. They are uniques. 

*Modifiers*: they exists to change the appearance and behavior (comportamiento) to blocks and elements. 

    - .block--modifier, for modify a block
        Example: button--primary || button--secondary

    - .block__element--modifier, for modify a element

   Example: modify the font size, .title | .title--size-regular | .title--size-big

   *Attention*: they never stay alone. 

# Pseudo-classes and Pseudo-elements

    Pseudo classes: it modify to special status of element.

    Pseudo-elements: it modify a part of element.

    Example: 

        - CSS:    
            /* Pseudo class: change the element when is hover and activate*/
            .main-nav__item a:hover {
                color: blue; 
            }.main-van__item a:active {
                color: red;
            }

            /* Pseudo element: put that element after a element */
            .main-nav__item a::after{
                content: " | ";
            }

# Anatomy of rules: 

--> Selector 
p {                                 }
    color : red; --> property value }   ---> declaration
}  --> property                     } 



# Box Model: 

All in HTML are boxes, we use that boxes to create websites. 
                    
- Margin: its a external space on element. Example:  <-- | a | -->

- Border: border, we can modify it. 
                                                           
- Padding: its a internal space in element. Example: | --> a <-- | its like backfill (relleno). 

- Content: img, txt, video

    - Width: the size of the content. The large. 

    - Height: the size of the content. The high. 

Always need to put in the codes: 

*{
    box-sizing: border-box; --> Sum padding (but not margin) and width of elements to give only one result.  
    margin: 0;
    padding: 0;
}


# Herencia | Heritage 

Example: 

    HTML:
        <goku>
            <goten>
                
            </goten>
        </goku>
    CSS:
        goku {
            hair : 'Hair-goku'; 
        }

        goten {
            hair: inherit; 
        }

# Selector Specificity 

    1. Important : .Styles browser .CSS Styles .!important 
    2. Specificity : 
    3. Sources order :

    Where can I see the specificity? in the console. If u see, u can determinate what kind of select you are using. 

# Combinators:

## Adjacent Siblings (hermano cercano)

    h2 + p {
        ... Put this styles to *the next* element (p) to h2
    }

## General Sibling (Hermano general)

    h2 ~ p {
        ... Put this styles to *all next* element (p) to h2
    }

## Child

    div > p {
        ... where the dad is div and the direct child is p
    }


## descendant 

    div p {
        ... all elements (p) inside div
    }

## p:first-child 

    <div> *<p>*

    Examples: 

    :last-child selects all last-child elements.

    span:last-child selects all last-child span elements.

    ul li:last-child selects the last li elements inside of any ul.

## :nth-child

    Examples: 

    :nth-child(8) selects every element that is the 8th child of another element.

    div p:nth-child(2) selects the second p in every div


# Units - dimensions (medidas)

## Absolutes: 

    There are absolutes units into window. *Pixels* are defined and not change with the window size

    *px*.

## Relatives 

    They change with window size.

### REM: 


    html {
        font-size: 62.5%; /* 10px*/  
    }


    p {
        font-size: 1.6rem; /* 16px*/
    }

# Min/Max width

*Rule*: When we will need to use min-max for width, we always should to use width (%) in the base (In percent). 

    section {
        width: 80%;
        
    *Rule* 
        min-width: 320px;
        max-width: 600px;
        
    *grow like u want*   
        min-height: 500px;

        background-color: #F48484;
        /* Center auto position */
        margin: 0 auto; 
    }


# Position

The form to manipulate the contends, boxes, elements in HTML. 

The defect position is static. 

- Static

We can use top, left, right, bottom 
- Absolute 
- Relative
- Fixed
- Sticky

Example: 

    .content {
        border: 2px black dotted;
        display: inline-block;
    }

    .content__box {
        display: inline-block;
        background-color: brown;
        width: 100px;
        height: 100px;
    }

    .content__box:nth-child(2) {
        position: relative;
        top: 20px;
        background-color: indianred;
    }