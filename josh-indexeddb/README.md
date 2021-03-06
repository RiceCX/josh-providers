# IndexedDB Provider for JOSH

The IndexedDB provider uses javascript IndexedDB api to store a database in browser

### Running the installer

In your project folder, you should be able to install using this command:

```
npm i @joshdb/indexeddb
** OR **
yarn add @joshdb/indexeddb
```

## Usage

Using the IndexedDB provider goes as such:

```js
const Josh = require('josh');
const JoshIndexedDB = require('@joshdb/indexeddb');

const db = new Josh({
  name: 'testing',
  provider: JoshIndexedDB,
  // See below for all provider options.
  providerOptions: {},
});

db.defer.then(async () => {
  console.log(`Connected, there are ${await db.size} rows in the database.`);
});
```

## Provider Options

Here is a list of full options this provider supports:

| Param             | Type                | Description                 |
| ----------------- | ------------------- | --------------------------- |
| [providerOptions] | <code>Object</code> | The Provider Options Object |
