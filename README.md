# ra-firebase-client

## Installation

```sh
npm install ra-data-firebase --save
```

## Usage

```js
// in src/App.js
import React from 'react';
import { Admin, Resource } from 'react-admin';
import { DataProvider } from 'ra-data-firebase';

const firebaseConfig = {
    apiKey: '<your-api-key>',
    authDomain: '<your-auth-domain>',
    databaseURL: '<your-database-url>',
    storageBucket: '<your-storage-bucket>',
    messagingSenderId: '<your-sender-id>'
};

const clientOptions = {
  trackedResources: [{ name: 'posts', isPublic: true }]
}

export const dataProvider = DataProvider(config, {trackedResources});

const App = () => (
    <Admin dataProvider={dataProvider} >
        <Resource name="posts" list={PostList} />
    </Admin>
);

export default App;
```
