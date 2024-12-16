# Отчёт по игре

## Описание игры

В данной игре игрок управляет персонажем, который должен преодолевать препятствия, избегать врагов и ловушек, а также добраться до конечной точки уровня. Персонаж может прыгать, двигаться влево и вправо, а также атаковать врагов ближним боем. Игра завершится, если игрок столкнется с врагом или достигнет конечной точки уровня.

## Основной функционал

### Управление
- **Перемещение**: Используются клавиши стрелок:
  - Стрелка вправо: движение вправо.
  - Стрелка влево: движение влево.
  - Стрелка вверх: прыжок (при нахождении на платформе).
  
- **Атака**: Для активации атаки нужно нажать пробел. Зона атаки появляется перед персонажем.

### Персонаж
- **Жизни**: У персонажа есть 3 жизни. При столкновении с врагом жизнь уменьшается на 1, при попадании в ловушку — на 2.
- **Перемещение**: Персонаж может двигаться по экрану, прыжок реализован с использованием вертикальной скорости и гравитации.
- **Атака**: Зона атаки отображается перед персонажем и уничтожает врагов при попадании.

### Локация
- **Размеры локации**: Локация имеет размеры 10000 пикселей по горизонтали и 3000 пикселей по вертикали. Камера следит за движением игрока.
- **Конечная точка**: Игра заканчивается, когда игрок достигает конечной точки уровня, которая отображается зелёным прямоугольником.
  
### Препятствия и враги
- **Платформы**: Платформы расположены на разных высотах и используются для перемещения игрока. Если игрок не находится на платформе, он будет падать.
- **Ловушки**: Ловушки активируются, когда персонаж входит в их область. Ловушки наносят урон (уменьшают жизни на 2) и уничтожаются после активации.
- **Враги**: Враги представлены красными прямоугольниками. При столкновении с врагом жизни игрока уменьшаются на 1. Если жизни заканчиваются, игра завершается.
  
### Камера
- **Привязка камеры**: Камера следует за движением игрока, но ограничена размерами локации, чтобы избежать застревания или бесконечного падения персонажа.

## Структура кода

### 1. Инициализация и настройки
- Инициализация Pygame и создание окна.
- Определение констант и начальных параметров для игрока, врагов, ловушек и платформ.

### 2. Главный игровой цикл
- Обработка событий: управление персонажем, активация атаки, проверка столкновений.
- Обновление положения персонажа с учетом гравитации и прыжков.
- Отображение всех объектов: персонаж, враги, ловушки, платформы, зона атаки.
- Обновление экрана с помощью Pygame.

### 3. Логика игры
- Проверка столкновений с врагами и ловушками.
- Уменьшение жизней при столкновении с врагами или активации ловушки.
- Отталкивание персонажа от врага после столкновения.
- Конец игры при отсутствии жизней или достижении конечной точки.

## Изменения и улучшения
- Добавлена камера, следящая за игроком, с ограничениями по краям экрана.
- Добавлены враги и ловушки, которые влияют на количество жизней игрока.
- Реализована система атаки и уничтожения врагов.


## Заключение

Игра представляет собой простую 2D платформенную игру с элементами преодоления препятствий и боя с врагами. Управление реализовано через клавиши стрелок, с возможностью атаки и прыжков. Игра заканчивается, когда игрок достигает финиша или теряет все жизни.
