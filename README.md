# Ідентифікатори
Ідентифікатори це послідовність Unicode символів.
* ідентифікатор має починатися або з літери або з знаку нижнього підкреслювання, але не з цифри.
* ідетифікатори можуть містити цифри але цифра не повинна бути першим симоволом ідентифікатора.
* ідентифікатор може складатися лише виключно з Unicode символів.
* ключові слова (keywords) не можуть використовуватися в якості ідентифікатора
* ідентифікатор який містить тільки один символ і цей символ нижне підкреслювання називаеться пустий ідентифікатор (blank identifier)
* якщо ідентифікатор починаеться з великої літери то такий ідентифікатор називаеться експортованим (exported identifier) в інших мовах програмування такий ідентифікатор відомий як (public)
* якщо ідентифікатор починаеться з маленької літери то такий ідентифікатор називаеться НЕ експортованим (non-exported identifier) в інших мовах програмування такий ідентифікатор відомий як (private)
### Приклади не валідних ідентифікаторів:
```go
// починаються з цифри
123
3apples

// містять Unicode символи які не є літерами або цифрами
a.b
*ptr
$name
a@b.c

// є ключивими словами (keywords).
type
range
```
Усього в мові golang є 25 ключових слів (keywords)
{% code lineNumbers="true" %}
```go
break     
default      
func    
interface  
select
case      
defer        
go      
map        
struct
chan      
else         
goto    
package    
switch
const     
fallthrough  
if      
range      
type
continue  
for          
import  
return     
var
```
{% endcode %}

Розглянемо код наведений нижче. Тут ми створюємо нову змінну яка має назву з однієї літери "a". Цей код буде працювати як і очікувалося, ніяких підступних сюрпризів тут не буде.

```go
package main
import "fmt"

func main() {
	var a int = 0
	fmt.Println(a)
}
```

Так як тип int не є ключовим словом в мові програмування Go то ми можемо створити змінну з тамим іменем. Цей приклад синтетичний і здається що нічого страшного в цьому не має, але це може стати причиною інших помилок.

```go
package main
import "fmt"

func main() {
	var int int = 0
	fmt.Println(int)
}
```

## Welcome to MyAPI

Welcome to MyAPI! Here you'll find all the documentation you need to get up and running with the MyAPI API.

## Want to jump right in?

Feeling like an eager beaver? Jump in to the quick start docs and get making your first request:

{% content-ref url="quick-start.md" %}
[quick-start.md](quick-start.md)
{% endcontent-ref %}

## Want to deep dive?

Dive a little deeper and start exploring our API reference to get an idea of everything that's possible with the API:

{% content-ref url="reference/api-reference/" %}
[api-reference](reference/api-reference/)
{% endcontent-ref %}
