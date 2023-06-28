# Custom VS Code Snippets

This repository contains a custom VS Code snippet collection

## Installation

Follow these steps:

1. Open Visual Studio Code.
2. On Windows **File > Preferences > Configure User Snippets > New Global Snippets** 
3. On MacOS **(Shift+Cmd+P)**.
4. Paste the JSON file

## Available Snippets

### Ionic React Page

```json
{
  "Ionic React Page": {
    "prefix": "ionic-react-page",
    "body": [
      "import React from 'react';",
      "import {",
      "  IonBackButton,",
      "  IonButtons,",
      "  IonContent,",
      "  IonHeader,",
      "  IonPage,",
      "  IonTitle,",
      "  IonToolbar,",
      "} from '@ionic/react';",
      "",
      "const ${TM_DIRECTORY/.*\\/(.*)$/$1/g}: React.FC = () => {",
      "  return (",
      "    <IonPage>",
      "      <IonHeader >",
      "        <IonToolbar color='none'>",
      "          <IonButtons slot='start'>",
      "            <IonBackButton color='primary' defaultHref='/' />",
      "          </IonButtons>",
      "          <IonButtons slot='end'>",
      "            <IonTitle>${TM_DIRECTORY/.*\\/(.*)$/$1/g}</IonTitle>",
      "          </IonButtons>",
      "        </IonToolbar>",
      "      </IonHeader>",
      "      <IonContent className='ion-padding'></IonContent>",
      "    </IonPage>",
      "  );",
      "};",
      "",
      "export default ${TM_DIRECTORY/.*\\/(.*)$/$1/g}"
    ],
    "description": "Ionic React page template"
  }
}
```

### Typescript React Function Component

```json
{
"Typescript React Function Component": {
    "prefix": "fc",
    "body": [
      "import { FC } from 'react'",
      "",
      "interface ${TM_DIRECTORY/.*\\/(.*)$/$1/g}Props {",
      "  $1",
      "}",
      "",
      "const ${TM_DIRECTORY/.*\\/(.*)$/$1/g}: FC<${TM_DIRECTORY/.*\\/(.*)$/$1/g}Props> = ({$2}) => {",
      "  return <div>${TM_DIRECTORY/.*\\/(.*)$/$1/g}</div>",
      "}",
      "",
      "export default ${TM_DIRECTORY/.*\\/(.*)$/$1/g}"
    ],
    "description": "Typescript React Function Component"
  }
  }
  ```


