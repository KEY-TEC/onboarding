# 5. Config export / Config import
## Workflow
``` 
drush cex
git add .
git commit -a -m "...."
git pull 
drush cim
```
# 6. config split

$config['config_split.config_split.local']['status'] = TRUE;