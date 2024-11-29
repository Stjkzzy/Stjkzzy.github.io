---
tags:
 github
---
发现无法启用github的强制https，这是因为cloudflare默认启用了http/dns代理功能，也就是cdn代理，导致github无法查看生成https证书所需的dns记录，对于指向github的任何dns记录，都要禁用该选项，才能启用Enforce HTTPS。

不过你在的cloudflare上直接启用https即可，这里本来就要利用它的cdn来进行访问加速。
