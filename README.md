# Islamic-tasks
## Все участники тестнета разделены на группы
```
https://docs.google.com/spreadsheets/d/1jRBe64-WsnLNTHAOLUU5Ed_8CODU60Y4Enm59Bs_d60/edit?usp=sharing
Каждую неделю команда будет делегировать токены последующей группе и соответсвенно будет меняться актив сет для выполнения заданий (1 неделя - 1 группа; вторая -2).
Задания отображаются в https://haqq-val-contest.crew3.xyz/questboard и станут доступны когда наступит неделя вашей группы (в дискорде выдадут роль Project Validator). Делегация от комадны по понедельникам. Дедлайн - воскресенье.

### 1 задание (100 exp) — делегировать любое количество токенов вашему валидатору (хеш транзакции в форму и на всякий случай себе в блокнот)
```
haqqd tx staking delegate <YOUR_VALOPER_ADDRESS> 10000000aISLM --from=<YOUR WALLET> --chain-id=haqq_54211-2 --gas=auto --fees 250aISLM
```
### 2 задание (100 exp) — вывести реварды с валидатора (хеш двух транзакций в форму и на всякий случай себе в блокнот)
```
haqqd tx distribution withdraw-all-rewards --from=<YOUR WALLET> --chain-id=haqq_54211-2 --gas=auto --fees 250aISLM
```
### 3 задание (100 exp) — вывести реварды с валидатора (хеш транзакции в форму и на всякий случай себе в блокнот)
```
haqqd tx staking delegate <Любой_VALOPER_ADDRESS> 10000000aISLM --from=<YOUR WALLET> --chain-id=haqq_54211-2 --gas=auto --fees 250aISLM
```
### 4 задание (150 exp) — обеспечивать безотказную работу узла не ниже 98%
в воскресенье делаем скрин с експлорера где видно наш аптайм. скрин в форму

### 5 задание (200 exp) — изменить своего валидатора (добавьте изображение, добавьте описание и все, что считаете нужным) - скриины до изменений и после добавляем в форму

```
haqqd tx staking edit-validator \
  --moniker=$NODENAME \
  --identity=<your_keybase_id> \
  --website="<your_website>" \
  --details="<your_validator_description>" \
  --chain-id=$STRIDE_CHAIN_ID \
  --from=$WALLET
```
### 6 задание (200 exp) - не попасть в тюрьму за все время нахождения в активном сете.


###   7 задание (250 exp) - сделать систему мониторинга и оповещения работоспособности ноды и написать об этом публичный гайд.

