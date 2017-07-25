# nexmotest



https://raw.githubusercontent.com/NathanDFriend/nexmotest/master/nexmo.json


APP_JWT="$(nexmo jwt:generate ./private.key \
application_id=5371cc3a-61d2-41ec-bd82-cb8697430369)"

curl -X POST https://api.nexmo.com/v1/calls\
  -H "Authorization: Bearer "$APP_JWT\
  -H "Content-Type: application/json"\
  -d '{"to":[{"type": "phone","number": 17038500198}],
      "from": {"type": "phone","number": 18882895803},
      "answer_url":["https://raw.githubusercontent.com/NathanDFriend/nexmotest/master/nexmo.json"]}'
