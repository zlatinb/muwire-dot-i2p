---
layout: wikipage
permalink: /i2pd.html
---

# I2Pd instructions

If you are running I2Pd you need to enable the `I2CP` interface which is not enabled by default.  To do that, you need to edit your `$HOME/.i2pd/i2pd.conf` file and add the following lines:

```
[i2cp]
enabled=true
address=127.0.0.1
port=7654
```

If your I2Pd router is running on a different IP you may need to adjust the interface address accordingly.

You need to restart the I2Pd daemon after making these changes.
