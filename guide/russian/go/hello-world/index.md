---
title: Hello World in Go
localeTitle: Привет, мир в Go
---
Для установки Go на компьютере, загрузите его установку из [здесь](https://golang.org/dl/) и установите ее, следуя [инструкции](https://golang.org/doc/install) по [установке](https://golang.org/doc/install) .

## Программа First Go

Создайте файл с именем `main.go` и добавьте в него следующий код:

```go
package main // Package declaration 
 
 import "fmt" // Importing packages 
 
 // Function declaration 
 func main() { 
    fmt.Println("Hello, World!") 
 } 
```

Теперь запустите указанную выше программу с терминала / командной строки. Для этого откройте Terminal / Command Line и перейдите в каталог, в котором присутствует `main.go` Сначала скомпилируйте программу и запустите `go build main.go` Затем запустите команду `go run main.go` чтобы запустить программу. Вы должны увидеть вывод, похожий на следующий вывод:
```
$ go build main.go 
 $ go run main.go 
 Hello, World! 
```

## Анализ

### Объявление пакета

```go
package main 
```

В go каждая программа связана с «пакетом» или набором связанных программ. Заметным исключением является специальный пакет «main», который указывает на то, что он должен запускать следующую программу.

### импорт
```
import “fmt” 
```

Если вы хотите использовать функции из других пакетов, вам необходимо их импортировать. Существуют определенные пакеты, разработанные сторонними разработчиками (называемые «стандартной библиотекой»), и их можно найти на странице https://golang.org/pkg/. В этом случае нам нужен пакет «fmt» для нашего оператора печати (см. Ниже).

### Объявление функции

```go
func main() { 
 } 
```

Функции являются основой любой программы в go. Они могут иметь аргументы и возвращать значения, но `main` функция не выполняет ни одну из них. Он действует как «точка входа», или где go сначала запускает вашу программу. Мы хотим, чтобы наша программа Hello World печаталась, поэтому мы хотим разместить здесь наш код.

### Распечатать заявление

```go
fmt.Println("Hello, world!") 
```

Go не требует точек с запятой в конце строк, поскольку корреспондент добавляет их автоматически. Пакет `fmt` (который мы импортировали выше!) Имеет функцию `Println` , которую мы вызываем с помощью `.` синтаксис. Мы передаем аргументы функции между parens. В этом случае аргумент - это строка, которую мы хотим напечатать ( `"Hello, world!"` ). Обратите внимание, что сама строка заключена в кавычки.

Теперь, когда у вас есть необходимые инструменты, выходите и делайте свои собственные программы Go! Лучший способ учиться - экспериментировать. Если вам когда-нибудь понадобится помощь, попробуйте отличную документацию по ходу: https://golang.org/doc/