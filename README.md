## Islamic-tasks
### Все участники тестнета разделены на группы

https://docs.google.com/spreadsheets/d/1jRBe64-WsnLNTHAOLUU5Ed_8CODU60Y4Enm59Bs_d60/edit?usp=sharing
Каждую неделю команда будет делегировать токены последующей группе и соответсвенно будет меняться актив сет для выполнения заданий (1 неделя - 1 группа; вторая -2).
Задания отображаются в https://haqq-val-contest.crew3.xyz/questboard и станут доступны когда наступит неделя вашей группы (в дискорде выдадут роль Project Validator). Делегация от комадны по понедельникам. Дедлайн - воскресенье. На данный момент командой внесены изменения в правила и для выполнения заданий не обязательно быть в актив сете (кроме задания "не попасть в тюрьму" и "аптайм". 

кран ноходиться здесь https://testedge2.haqq.network/
для клейма токенов нам нужно нашу мнемонику которую мы получили при создании кошелька для gentx импортировать в MetaMask (именно в ММ потому как при импорте в кеплер будет другой адресс). Далее переходим по ссылке https://testedge2.haqq.network/ конектим наш ММ и github. Меняем сеть и запрашиваем токены. Кран выдает 5 ISLM раз в 24 часа.

### 1 задание (100 exp) — делегировать любое количество токенов вашему валидатору (хеш транзакции в форму и на всякий случай себе в блокнот)
проверка баланса кошелька
```
haqqd query bank balances <YOUR WALLET>
```
#### 1 ISLM = 1000000000000000000 aISLM
перед выполнением проверьте чтобы в /root/.haqqd/config/app.toml  строка 11 газ стоял "0"
```
haqqd tx staking delegate <YOUR_VALOPER_ADDRESS> 10000000aISLM --from=<YOUR WALLET> --chain-id=haqq_54211-2
```
### 2 задание (100 exp) — вывести реварды с валидатора (хеш двух транзакций в форму и на всякий случай себе в блокнот)
```
haqqd tx distribution withdraw-all-rewards --from=<YOUR WALLET> --chain-id=haqq_54211-2 --gas=auto
```
#Withdraw rewards with commission:
```
haqqd tx distribution withdraw-rewards <YOUR_VALOPER_ADDRESS> --from=<YOUR WALLET> --commission --chain-id=haqq_54211-2
```
### 3 задание (100 exp) — делегировать любое количество токенов любому другому валидатору (хеш транзакции в форму и на всякий случай себе в блокнот)
```
haqqd tx staking delegate <Любой_VALOPER_ADDRESS> 10000000aISLM --from=<YOUR WALLET> --chain-id=haqq_54211-2
```
### Для ределигации следующая команда <srcValidatorAddress> -наш валик; <destValidatorAddress> - валик друга
quicksilverd tx staking redelegate <srcValidatorAddress> <destValidatorAddress> 10000000uqck --from=$WALLET --chain-id=$QUICKSILVER_CHAIN_ID --gas=auto

### 4 задание (150 exp) — обеспечивать безотказную работу узла не ниже 98%
в воскресенье делаем скрин с експлорера где видно наш аптайм. скрин в форму

### 5 задание (200 exp) — изменить своего валидатора (добавьте изображение, добавьте описание и все, что считаете нужным) - скриины до изменений и после добавляем в форму
```
haqqd tx staking edit-validator \
  --moniker=<Наш моникер> \
  --identity=<your_keybase_id> \
  --website="<your_website>" \
  --details="<your_validator_description>" \
  --chain-id=haqq_54211-2 \
  --from=<YOUR WALLET>
```
### 6 задание (200 exp) - не попасть в тюрьму за все время нахождения в активном сете.

###   7 задание (250 exp) - сделать систему мониторинга и оповещения работоспособности ноды и написать об этом публичный гайд.
https://github.com/madnoder/Monitoring-Bot-HAQQ

###   8 задание (250 exp) - не пропустить голосование, которое проведет команда (для мониторинга можно поставить бота от ryssroad)
```
haqqd tx gov vote 1 yes --from <YOUR_WALLET> --chain-id=haqq_54211-2
```
###   9 задание (300 exp) - запилить свою голосвалку (пруф - ваш моникер в голосовалке и ссылка в форму).
```
haqqd tx gov submit-proposal --title="Randomly reward" --description="Ваше предложение" --type="Text" --deposit="11000000aISLM" --from=<name_wallet> --fees 555aISLM
```
###   10 задание (400 exp) - отключить другого валидатора (Try to disable the validator node that is also in the active set with you) (репорт в хецнер что он использует сервак для крипты)

###   11 задание (500 exp) - запилить свой експлорер (ссылку в форму)

###   12 задание (700 exp) - стопнуть сетку (в форме подробно описать как вы этого добились)

###   13 задание (700 exp) - найти ошибки в доках команды

###   14 задание (1000 exp) - найти ошибки в доках на github

###   15 задание (150 exp) - задание доступно с ролью "Админ" в дискорде







