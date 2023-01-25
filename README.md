# web_site
# signin_example
https://docs.flutter.dev/get-started/codelab-web

Это простое веб-приложение, отображающее экран входа. 
Экран содержит три текстовых поля: 
- имя, 
- фамилия и 
- имя пользователя. 
Когда пользователь заполняет поля, в верхней части области входа появляется анимация индикатора выполнения. 
Когда все три поля заполнены, индикатор выполнения отображается зеленым цветом по всей ширине области входа, а кнопка «Sign up» становится доступной. 
При нажатии кнопки «Sign up» в нижней части экрана появляется Wellcome-экран.

Step 0: Get the starter web app
Step 1: Show the Welcome screen
Step 2: Enable sign in progress tracking
Step 2.5: Launch Dart DevTools
Step 3: Add animation for sign in progress

[Step 0] Get the starter web app
Класс [SignUpForm] представляет собой виджет с состоянием. 
Это означает, что виджет хранит информацию, которая может меняться, 
напр., вводимые пользователем данные или данные из канала.

Поскольку сами виджеты являются immutable (не могут быть изменены после создания), Flutter хранит информацию о состоянии в сопутствующем классе, называемом Stateclass. В этой лабораторной работе все ваши изменения будут внесены в закрытый [_SignUpFormState] класс.

1. in lib/main.dart file: add the class definition for the WelcomeScreen widget after the SignUpScreen class:

2. enable the button to display the screen and create a method to display it.