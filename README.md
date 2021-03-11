# Homework02
Just typing some words so it could be different from main branch // для задания 1 и 2
## Part 1
1.Создайте пустой репозиторий на сервисе github.com (или gitlab.com, или bitbucket.com).
2.Выполните инструкцию по созданию первого коммита на странице репозитория, созданного на предыдещем шаге.
3.Создайте файл hello_world.cpp в локальной копии репозитория (который должен был появиться на шаге 2). Реализуйте программу Hello world на языке C++ используя плохой стиль кода. Например, после заголовочных файлов вставьте строку using namespace std;.
```
$ cat > hello_world.cpp <<EOF // создаём исполняемый файл hello_world.cpp который печатает "Hello world"
> #include <iostream>
> using namespace std;
> int main(int argc, char** argv)
> {
> cout << "Hello world";
> }
> EOF
```
4.Добавьте этот файл в локальную копию репозитория.
```
$ git add hello_world.cpp
```
5.Закоммитьте изменения с осмысленным сообщением.
```
$ git commit -m "Added alpha version of hello_world.cpp"
```
6.Измените исходный код так, чтобы программа через стандартный поток ввода запрашивалось имя пользователя. А в стандартный поток вывода печаталось сообщение Hello world from @name, где @name имя пользователя.
```
$ nano hello_world.cpp // открываем редактор чтобы изменить файл
> #include <iostream>
> #include <string>
> using namespace std;
> int main(int argc, char** argv)
> {
> string a;
> cout << "Please insert your name: "
> cin >> a;
> cout << endl << "Hello world from " << a;
> }
```
7.Закоммитьте новую версию программы. Почему не надо добавлять файл повторно git add?
```
$ git commit -a //совершает коммит автоматически индексируя изменения в файлах проекта
> Added printing user's name
```
8.Запуште изменения в удалёный репозиторий.
```
$ git push --set-upstream origin master
```
9.Проверьте, что история коммитов доступна в удалёный репозитории.
```
Доступна: $ git log
```
