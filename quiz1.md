1. 請說明 Fixnum (整數) 和 Float (浮點數) 之間的差異

	#### ANS:
	Fixnum (整數):整數。
	Float (浮點數):小數。


2. 今天有兩個字串：

```ruby
str1 = "Hallo Welt!" 
str2 = " NTU Rails 261!"
```
請說明以下兩個印出字串的方式的不同處：
```ruby
puts str1 + str2
puts "#{str1}#{str2}"
```

	#### ANS:
	前者使用 + 號連結兩個字串會多耗記憶體；
	後者為字串內插(string interpolation)較有效率。


3. 請解釋 array 和 hash 的不同處

	#### ANS:
	array：用 index number 呼叫值，例如：使用 array[1] 取出 array 的第二個值。例如：
	```ruby
	schedule = ["CS50" , "Ruby on Rails" , "Java Programming"]
	puts schedule[1] 
	#印出位於[1]的 "Ruby on Rails"
	```
	hash：由鍵(key)與值(value)構成，主要差別在於可以使用 key 取得相對應的 value。例如
	```ruby
	schedule = {
	  Mon: "CS50",
	  Tue: "Ruby on Rails",
	  Wed: "Java Programming",
	}
	puts schedule[:Tue]
	#印出與 schedule["Tue"] 相對應的 "Ruby on Rails"
	```


4. 請寫一段 code 從 [1, "a string", 3.14, [1,2,3,4]] 這個陣列找出所有非字串的值

	#### ANS:
	```ruby
	my_array = [1, "a string", 3.14, [1,2,3,4]] 
	my_array.each {|item| puts "#{item}" if item.class != String}
	```

5. 請列出兩種產出亂數的方法

	#### ANS:
	```ruby
	#方法一
	n = rand(1..100)
	#方法二
	n = (1..100).to_a.shuffle.first
	```


6. 請把 hoemowrk1 程式碼裡的裡面的使用者輸入兩個數字的方式和輸贏的判斷式改寫成 method

	#### ANS: 
	程式碼請至此網址
	https://github.com/anndoko/ntu_ror_266_quiz1/blob/master/rock_paper_scissors_game_def.rb


7. 以下這段程式碼：
```ruby
((1 > 3)&&(true == true))||(!!!false)
```
會執行出什麼結果？ 請試試不用 irb 算出結果

	#### ANS: 
	true


8. 請問 binding.pry 是什麼？ 要如何使用它？

	#### ANS: 
	ruby 的 debugger 套件，在程式碼中加入 binding.pry，即可在執行的時候攔截。


9. 下面的一段程式碼，請嘗試用其他方法把 if...else...end 簡化成一行
```ruby
var = 5

if var >= 5
  return "var is greater than or equal to 5"
else
  return "var is less than 5"
end
```

	#### ANS:
	```ruby
	var >= 5? "var is greater than or equal to 5" : "var is less than 5"
	```