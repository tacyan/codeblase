# slackのincoming-webhookを使用する

url
https://slack.com/services/new/incoming-webhook

curl
```
curl -X POST --data-urlencode "payload={\"chanQnel\": \"#general\", \"username\": \"webhookbot\", \"text\": \"This is posted to #general and comes from a bot named webhookbot.\", \"icon_emoji\": \":ghost:\"}" https://hooks.slack.com/services/xxxx/xxx/xxxx
```

curlテスト

```
$ curl -X POST "https://hooks.slack.com/services/XXX/XXX/XXX" -d 'payload={
  "channel": "#general",
  "username": "my_bot",
  "text": "test",
  "icon_emoji": ":ghost:"
}'
```

controller

```
function send_to_slack($message) {
  $webhook_url = 'https://hooks.slack.com/services/XXXXXXXXX/XXXXXXXXX/XXXXXXXXXXXXXXXXXXXXXXXX';
  $options = array(
    'http' => array(
      'method' => 'POST',
      'header' => 'Content-Type: application/json',
      'content' => json_encode($message),
    )
  );
  $response = file_get_contents($webhook_url, false, stream_context_create($options));
  return $response === 'ok';
}

$message = array(
  'username' => 'Bot',
  'text' => 'fooooo!!!',
);

send_to_slack($message);
```


使えそうな記事

https://qiita.com/monhan/items/d95ad6e4e698da9e6593
