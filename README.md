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

2. in lib/main.dart file: add the class definition for the WelcomeScreen widget after the SignUpScreen class:

3. Locate the build() method for the _SignUpFormState class. This is the part of the code that builds the SignUp button. Notice how the button is defined: It’s a TextButton with a blue background, white text that says Sign up and, when pressed, does nothing.enable the button to display the screen and create a method to display it.

4. Update the onPressed property to call the (non-existent) method that will display the welcome screen.
And add the _showWelcomeScreen function inside the State before @override
void _showWelcomeScreen() {
  Navigator.of(context).pushNamed('/welcome');
}
5. Add the /welcome route.
Create the connection to show the new screen. Inside the MaterialApp({routes: }), add the route below '/' (параметр):
'/welcome': (context) => const WelcomeScreen(),