## Информация по SFML

### Официальный сайт библиотеки:

https://www.sfml-dev.org/index.php

### Русская информация по бибилиотеке:

https://kychka-pc.ru/

https://kychka-pc.ru/category/sfml/page/5

### Установка:

sudo apt update && sudo apt install libsfml-dev

### Пример простейшей программы:

```
#include <SFML/Graphics.hpp>

int main()
{
    sf::RenderWindow window(sf::VideoMode(200, 200), "SFML works!");
    sf::CircleShape shape(100.f);
    shape.setFillColor(sf::Color::Green);

    while (window.isOpen())
    {
        sf::Event event;
        while (window.pollEvent(event))
        {
            if (event.type == sf::Event::Closed)
                window.close();
        }

        window.clear();
        window.draw(shape);
        window.display();
    }

    return 0;
}
```


### Сборка с помощью gcc:

g++ -c main.cpp


### Создание окончательного исполняемого файла:

g++ main.o -o sfml-app -lsfml-graphics -lsfml-window -lsfml-system