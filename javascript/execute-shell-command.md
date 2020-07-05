You can execute a shell command using the many utilities from `child_process`.

```js
  const { execSync } = require('child_process');

  // to execute a bash script that is in a directory above synchronously
  execSync('./command.sh', { cwd: path.resolve(__dirname, '../') });
```
