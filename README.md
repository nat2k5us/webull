# webull api usage instructions

## https://www.webull.com/


[<img src="https://miro.medium.com/max/1476/1*KGh1GBqI9R0TfSsSPHGpNg.png" width="200px">](https://www.buymeacoffee.com/nat2k5usW)

## INstall webull lib

```bash
pip install webull

pip install pytest requests_mock
```

# Step 1
- login
```python
from webull import webull # for paper trading, import 'paper_webull'

wb = webull()
wb.login('youremail@gmail.com', 'paswd')

# or 
from webull import webull # for paper trading, import 'paper_webull'

wb = webull()
wb.login('+1-1112223333', 'pa$$w0rd') # phone must be in format +[country_code]-[your number]

```

# Place an order
```python
from webull import webull
wb = webull()
wb.login('youremail@gmail.com', 'paswd')

wb.get_trade_token('123456')
wb.place_order(stock='TSLA', price=190.0, qty=12)
```
# Order Status
```python
from webull import webull
wb = webull()
wb.login('youremail@gmail.com', 'paswd')

wb.get_trade_token('123456')
orders = wb.get_current_orders()
```
# Cancel order 
```python
from webull import webull
wb = webull()
wb.login('youremail@gmail.com', 'paswd')

wb.get_trade_token('123456')
wb.cancel_all_orders()
```

## References
- <https://github.com/tedchou12/webull/wiki>
