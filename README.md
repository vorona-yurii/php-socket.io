PHP_SocketIO_Client
===================

EN: PHP client for socket.io (websocket client)

How to use:
```
$data = [
    'user_id' => 123,
    'room' => 321,
    'EIO' => 3,
];
$address = '/socket.io/?' . http_build_query($data);
$io = new SocketIOConnect('127.0.0.1', 8080, $address);
$io->send('chat message', json_encode([
    'chat_id' => 1,
    'user_id' => 123,
    'message' => 'Test message'
]));

```