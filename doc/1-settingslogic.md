Gemの概要
---

- 環境毎に定数を定義する

<br>
`app/models/constants.rb`

```
class Constants < Settingslogic
  source "#{Rails.root}/config/constants.yml"
  namespace Rails.env
end
```
<br>
`config/constants.yml`

```
defaults: &defaults
  name: 'ASKA'
  address: 'Minami-Aoyama'

development:
  name: 'CHAGE'
  address: 'Fukuoka'

test:
  <<: *defaults

production:
  <<: *defaults
```

Gemの保存場所
---
<br>

```
$ gem which settingslogic
$ cd $SETTINGSLOGIC_DIR
$ git init
# 変更廃棄のため
```

<br>

