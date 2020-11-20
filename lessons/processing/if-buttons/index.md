---
title: Ветвления — создаём кнопки
description: Жмяк-жмяк
---

# Ветвления — создаём кнопки

<iframe width="560" height="315" src="https://www.youtube.com/embed/K8f7Lhy1uHM" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

0:40 как сделать кнопку, «на пальцах»
4:30 делаем кнопку в коде
7:01 текст
11:30 как сделать круглую кнопку

## Примеры кода

<pre>
bg = 0;

def setup():
    size(600,400)
    
def draw():
    global bg
    background(bg)
    #кнопка прямоугольная
    fill(255)
    # левый верхний угол 250 150, размеры 100 на 50
    rect(250,150,100,50) # x от 250 до 250+100, y от 150 до 150 + 50  
    
    
    #круглая кнопка
    ellipse(400,350,70,70) # центр х=400 y=350 диаметр 70, радиус 35
    
    
def mouseClicked():
    global bg
    # если прямоугольная кнопка нажата
    
    if mouseX > 250 and mouseX < 350 and mouseY > 150 and mouseY < 200:
        bg = 255
        
    
    #если круглая кнопка нажата
    xDif = 400 - mouseX
    yDif = 350 - mouseY
    
    if sqrt(xDif*xDif + yDif*yDif) < 35:
        bg = 0

    
</pre>