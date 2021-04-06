import turtle
import random
import os 

win = turtle.Screen()
win.title('Cannon Shooting game')
win.setup(800, 600)
win.tracer(0)
win.listen()

cannon = turtle.Turtle()
cannon.shape('square')
cannon.shapesize(2,2)
cannon.up()
cannon.color('blue')
cannon.goto(-360, -260)

class Enemy(turtle.Turtle):
    def _init_(self):
        super()._init_(shape='circle')
        self.shapesize(2,2)
        self.up()
        self.color('red')
        self.dx = -0.5
        self.goto(420, random.randint(0,250))


    def move(self):
        self.goto(self.xcor()+self.dx, self.ycor())


class Bullet(turtle.Turtle):
    def _init_(self):
        super()._init_(shape='square')
        self.shapesize(0.2, 0.7)
        self.up()
        self.color('red')
        self.lt(50)
   …
