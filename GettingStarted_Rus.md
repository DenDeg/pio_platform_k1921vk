# Быстрый старт с МК серии K1921BK VSCode+Platform.io
Данный репозиторий добавляет поддержку разработки под МК серии K1921BK для PlatformIO  
Используется адаптированный фреймоврк [NIIET k1921vk SDK](https://github.com/kenny5660/framework-k1921vk-sdk), который основан на официальном [SDK от НИИЭТ](https://bitbucket.org/niietcm4/k1921vkx_sdk/src)  

[PlatformIO](https://docs.platformio.org/en/latest//what-is-platformio.html) - Открытая экосистема для IoT разработки.  
Основные возможности PlarformIO:  
* Внутрисхемная отладка через сервер GDB
* Локальная и удаленная прошивка МК
* Статический анализ кода с помощью cppcheck,PVS-Studio и тд. В том числе поддержка проверок MISRA C
* Анализ использования памяти

## Список поддерживаемых МК:
* К1921ВК01Т
* К1921ВК035
* К1921ВК028

## Найстройка среды разработки
1. [Установка Visual Studio Code](https://code.visualstudio.com/)
2. [Установка PlatformIO](https://docs.platformio.org/en/latest/integration/ide/vscode.html#ide-vscode)
3. После успешной утсановки расширения в левом боковом меню появится эмблема  Platform.io, кликаем туда, затем Open. Откроется окно PIO Home.
4. Создаем новый проект (кнопка New Project),
   *    Name - Название проека
   *    Board - Выбираем используемый контроллер (Сейчас доступны Generic K1921VK01T и Generic K1921VK035)
   *    Framework - используемый фреймоврк для разработки, пока доступен только - NIIET k1921vk SDK 
5. Platform io самостоятельно скачает все требуемые библиотеки, компиляторы, openocd и тд.

Примеры проектов можно увидеть: PIO Home > Platforms > K1921VK > Examples  
Или в [репозитории платформы](https://github.com/kenny5660/pio_platform_k1921vk/tree/master/examples)

## Прошивка и отладка
В данный момент отлдака через сервер GDB и прошивка осуществляется с помощью openocd.  
Поддерживаются следующие отладчики:  
* st-link (only SWD)

## Текущие проблемы 
* Прошивка мк происходит только со 2го раза
* Отладчик работает некорректно, если в пути до папки проекта встречаются русские символы