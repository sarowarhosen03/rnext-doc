# 1.5 - Basics of React Components: Importing & Exporting Components

\***\*Export and Import:\*\***

when we create a component and want to use it in another file, we can use the **export** and **import** statements provided by JavaScript to export our component from one file and import it into another.

There are two types of export/import systems.

1. Default Export
2. Namee Export
  
## **Default export/import**

when we use default export, we can import it with the same name or set our own choosing name. That time we don't need to use any {}.

```jsx
export default function Profile() {
  return <img src="https://i.imgur.com/MK3eW3Am.jpg" alt="Katherine Johnson" />;
}

import Profile from "./pathname";
or;
import MyProfile from "./pathname";
```

## **Name export/import**

when we use name export that time we have to import it with the same name inside {}. But we can rename it. That time we use (as) to rename.

```jsx
export function Profile() {
  return <img src="https://i.imgur.com/MK3eW3Am.jpg" alt="Katherine Johnson" />;
}

import { Profile } from "./pathname";
or;
import { Profile as MyProfile } from "./pathname";
```

note: we can use default and name export/import together.

Any component that you export by default can be exported with whatever name you choose. For instance, you can use any name you choose when importing the Profile Component.
```jsx
import Component from './components/Profile'
```
