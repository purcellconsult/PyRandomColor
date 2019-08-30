## PyRandomColor

PyRandomColor is a simple module that allows pythonistas the ability to select from 150 random colors to add to their turtle graphics.

The package is available on PyPI. To install use the following pip command: 
  
    $ pip install pyrandomcolor

Just like how entertainment would be mundane with just black and white television, the same concept applies to your turtle computer graphics. The turtle module does enable pythonistas the ability to add color via the color function. 

This is great, but sometimes when you’re creating images you’re not exactly sure what colors to use. Or better yet, maybe you just want to experiment and randomly color your graphics to see what works best; after all, seeing is believing.
  
*Ta-da*, this is where the _PyRandomColor_  module comes to the rescue!

## List of Functions


Here’s a quick overview of the functions that’s available for use:
  
`get_random_color()`: Picks any random color.

 `whites_and_pastels()`: Returns a random color that’s within the white and pastel color schemes.

  `grays()`: returns a random color that’s within the gray color scheme.

`blues()`: Returns a random color within the blue color scheme.

`greens()`: Returns a random color within the green color scheme.

`yellows()`: Returns a random color within the yellow color scheme.

`browns()`: Returns a random color within the brown color scheme.

`oranges()`: Returns a random color within the orange color scheme.

`pinks_violets()`: Returns a random color within the pinkish and _violetish_ color scheme.

Color is relatively hard to categorize as there’s many different shades, hues and what not, so experiment with this module the same way a painter experiments with their palette. 

## Code Examples 

    from random_colors import get_random_color
    import turtle
    def random_color_square():
        square = turtle.Turtle()
        square.hideturtle()
        square.pensize(3)   
        square.pencolor(get_random_color())
        square.color(get_random_color(), get_random_color())  
        square.begin_fill()
        for x in range(4):
            square.forward(100)
            square.right(90)
        square.end_fill()
        turtle.done()
        
    random_color_square()

Output:
  


    def random_color_square2(cycles=10):  
        square = turtle.Turtle()  
        go, turn = 100, 90  
      square.hideturtle()  
        square.pensize(3)  # set the border to 3 pixels  
      square.pencolor(get_random_color())  # set border color  
      square.color(get_random_color(), get_random_color())  # set fill and outer color  
      
      for x in range(cycles):  
            for y in range(4):  
                square.forward(go)  
                square.right(turn)  
            go -= 10  
      turtle.done()
    
    random_color_square2

Output


Note, your output may be different from the one generated here as the colors are randomly generated each time. This is an interesting form of art as there's a high probability that each image will have some degree of variance. 
