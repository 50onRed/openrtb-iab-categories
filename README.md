# OpenRTB IAB categories

This repository contains a list of OpenRTB IAB categories in JSON format.

The list was generated from OpenRTB 2.4 [specification](http://www.iab.com/wp-content/uploads/2016/03/OpenRTB-API-Specification-Version-2-4-FINAL.pdf) using the following Python script:

```python
from collections import OrderedDict
import json

raw_categories = ''  # TODO: copy/paste here a list of IAB categories from OpenRTB specification
categories = OrderedDict()

for line in raw_categories.splitlines():
    iab_id, iab_name = line.split(' ', 1)
    categories[iab_id] = iab_name

print(json.dumps(categories, indent=4))
```
