# sinatra template

## How to Install

```
$ bundle install --path vendor/bundle
```

## How to Test

* All files

```
$ bundle exec rspec spec
```

* Only specific file

```
$ bundle exec rspec spec/hello_spec.rb
```

## How to Run

```
$ bundle exec rackup -o 0.0.0.0 -p 8080
```

## How to Run as a unicorn process

You can use sinatra app as a unicorn process.<br>
And if you use default **config/unicorn.rb** settings, it can be used directory by accessing http://localhost:3000

* Start unicorn process<br>
  *You can change app environment (ex. development, production, etc.) using ``-E`` option.

```
$ bundle exec unicorn -c config/unicorn.rb -D -E development
```

* Stop unicorn process

```
$ kill -QUIT `cat ./tmp/pids/unicorn.pid`
```

* Restart unicorn process

```
$ kill -HUP `cat ./tmp/pids/unicorn.pid`
```

* Slow restart unicorn process

```
$ kill -USR2 `cat ./tmp/pids/unicorn.pid`
```

## References
1. Sinatra, http://www.sinatrarb.com/, Online; accessed 19-July-2016. 
2. rbenvを用いたruby環境構築手順（CentOS7.1） - Qiita, http://qiita.com/ksugawara61/items/e3bb87d5e0dd49d20c8f, Online; accessed 14-September-2016.
3. ruby+rbenv+sinatraの環境構築 - Qiita, http://qiita.com/ksugawara61/items/c1a0572353668c58e87a, Online; accessed 14-September-2016.
4. Unicorn設定のまとめ - Qiita, https://qiita.com/syou007/items/555062cc96dd0b08a610, Online; accessed 27-June-2019.
