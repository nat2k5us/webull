# webull api usage instructions

## https://www.webull.com/

https://www.buymeacoffee.com/nat2k5usW

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
wb.login('test@test.com', 'pa$$w0rd')
```
