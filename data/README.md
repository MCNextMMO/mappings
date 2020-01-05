# Data Mappings

Map Minecraft IDs to Bukkit types/classes. Get types from stable names.

Example JSON to Java enum conversion:

```js
const entities = require('entities.json');

const javaEnum = Object.entries(entities).map(([id, { name, type }]) => `${type}(EntityType.${type}, "${id}", "${name}"),`).join('\n');

console.log(javaEnum);
```
