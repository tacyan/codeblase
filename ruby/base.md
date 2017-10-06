# rubyのコードを書いて行きます。

## httpリクエスト

```
10.times do |i|
  client = Faraday.new(:url => "https://example.com")
  # 証明書無効化
  client.ssl[:verify] = false
  res = client.post "/hosts?apikey=xxxxxxxx", {
    "service_group_name": "std",
    "uuid": "#{SecureRandom.uuid}",
    "ip": "127.0.0.1",
    "item_id": "1234",
    "domain": "test.co-bonnou.com",
    "status": 0
  }
  body = JSON.parse res.body
  pp body
end
```

## 九九

```
(1..9).each do |x|
    puts "#{x}の段"
    (1..9).map do |y|
        puts x * y
    end
end
```

