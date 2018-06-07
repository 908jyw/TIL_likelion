## Ruby

### 0. 개요

1. 루비는 순수 객체 지향 언어이다.
2. 모든것이 객체
3. Ruby on Rails 프레임 워크 등장으로 유명

### 1. puts vs print

~~~ ruby
3.times {print "hello"} # => hellohellohello
3.times {puts "hellp"} # => hello
					 # => hello
					 # => hello
~~~

> puts 는 개행문자 포함 ( > 사용하여 주석문 생성가능)

### 2. p vs puts

~~~ ruby
string = "hello"
puts string # => hello => nil
p string # => "hello"
~~~

### 3. Naming conventions

- 변수
  - snake_case
- 상수
  - CONSTANT
- 클래스
  - CamelCase

### 4. pry

- 설치
  - `gem install pry`
- 실행
  - `pry`



### 5. inline statement

~~~ ruby
# if 문
puts "a=0" if a == 0 # a=0	
puts "a=0" if a == 1 # 출력안됨

# while 문
c = 0
result = c += 2 while c < 50
puts result # 50
    
puts "hi" if 0 # hi
~~~

### 6. case

~~~ ruby
case name
when "chang2" then puts "hi chang2"
when "tak" then puts "hi tak"
else puts "hi"
end
~~~

### 7. method

- 대부분의 언어

  - 클래스 안 : function
  - 클래스 밖 : method

- 루비에서는 모든 function은 method

- ~~~ ruby
  # 루비에서의 method 선언
  def simple
    puts "simple!!"
  end  
  => :simple
  
  # 루비에서의 
  def asdf()
    puts "asdf"
  end  
  => :asdf
  ~~~

- ~~~ruby
  # 루비에서는 return이 없을때 마지막 연산 값을 리턴합니다.
  def add2(a,b)
    a+b  
  end  
  => :add2
  add2(1,2)
  => 3
  
  # return을 선택적으로 사용할 수 있습니다.
  def divide(a,b)
    return "I don't think so" if b == 0
    a/b
  end  
  => :divide
  ~~~

- 기본 매개변수

- ~~~ruby
  def factorial(n)
      n == 0 ? 1: n * factorial(n-1)
  end
  factorial # ArgumentError: wrong number of arguments (given 0, expected 1)
  
  
  # 기본 매개변수 등록
  def factorial_d(n=5)
      n == 0 ? 1: n * factorial(n-1)
  end
  factorial_d # 120
  ~~~



### 8. block

~~~ruby
3.times { puts "hello" }
3.times do |asdf|
  puts asdf	# 이부분이 block
end
0
1
2
~~~

~~~ ruby
def hihi
    return "No block" unless block_given?
    yield
end

hihi # => "No block"
hihi {puts "hihi"} #=> hihi

~~~

### 9. String

~~~ ruby
a = "안녕하세요. \n 멋사입니다."
=> "안녕하세요. \n 멋사입니다."
b = '안녕하세요. \n 멋사입니다.'                                                                                
puts a
안녕하세요. 
 멋사입니다.
=> nil
puts b
안녕하세요. \n 멋사입니다.
=> nil
name = "Schang2"
=> "Schang2"
a = "#{name}님 안녕하세요"                                              
=> "Schang2님 안녕하세요"
~~~







### class 만드는 법

~~~ ruby
class Integer
def dollar
self*1100
end  
end  
~~~

