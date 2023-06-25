# Package to create MySQL database types
## Install this package
```bash
npm i mysql2-types-generator
```

## Connect to MySQL database using `mysql2-handler` package
```javascript
// No need to install mysql2 or mysql2-handler packages, they are dependencies of this package for capability reasons
const DB = require('mysql2-handler');
// OR
import DB from 'mysql2-handler';
```

## Import this package
```javascript
const { generateDatabaseTSFile } = require('mysql2-types-generator')
// OR
import { generateDatabaseTSFile } from 'mysql2-types-generator'
```

## Create database connection
```javascript
DB.Connect(() => {
    await generateDatabaseTSFile(DB, 'database-name', 'path/to/newtsfile/') // path/to/newtsfile/ is optional
    // default path is ./Data/types/
    // types filename is DBTypes.database-name.ts
});
```