## intro-sinatra

- `mkdir sinatra-test`

- `cd sinatra-test`

- `touch app.rb`

- `gem install sinatra`

- ~~~ruby
  # app.rb
  require 'sinatra'
  
  get '/' do
      'Hello world! welcome'
  end
  ~~~

- `ruby app.rb -o -$IP`

### 서버 자동 실행 방법

- `gem install "sinatra-contrib"`
- `require "sinatra/reloader"`





