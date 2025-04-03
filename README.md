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
        "const ${TM_DIRECTORY/^.+[\\/\\\\]+(.*)$/$1/}: React.FC = () => {",
        "  return (",
        "    <IonPage>",
        "      <IonHeader >",
        "        <IonToolbar color='none'>",
        "          <IonButtons slot='start'>",
        "            <IonBackButton color='primary' defaultHref='/' />",
        "          </IonButtons>",
        "            <IonTitle>${TM_DIRECTORY/^.+[\\/\\\\]+(.*)$/$1/}</IonTitle>",
        "        </IonToolbar>",
        "      </IonHeader>",
        "      <IonContent className='ion-padding'></IonContent>",
        "    </IonPage>",
        "  );",
        "};",
        "",
        "export default ${TM_DIRECTORY/^.+[\\/\\\\]+(.*)$/$1/}"
      ],
      "description": "Ionic React page template"
    }
}
```

```json
{
"Ionic React Page for DGk v2": {
        "prefix": "dgkv2",
       "body": [
      "import React from \"react\";",
      "import { IonContent, IonHeader, IonPage, IonToolbar } from \"@ionic/react\";",
      "import PageTitleCaption from \"../../../components/PageTilteCaption\";",
      "import BackButton from \"../../../components/BackButton\";",
      "",
      "const ${TM_DIRECTORY/^.+[\\/\\\\]+(.*)$/$1/}: React.FC = () => {",
      "  return (",
      "    <IonPage>",
      "      <IonHeader mode=\"md\" className=\"ion-no-border\">",
      "        <IonToolbar>",
      "          <BackButton",
      "            color=\"primary\"",
      "            backgroundColor=\"var(--ion-color-tertiary)\"",
      "            onClick={() => {",
      "              history.go(-1);",
      "            }}",
      "          />",
      "        </IonToolbar>",
      "      </IonHeader>",
      "      <IonContent fullscreen className=\"ion-padding\">",
      "        <PageTitleCaption",
      "          title={\"${TM_FILENAME_BASE}\"}",
      "          caption={",
      "            \"${1:View or update your details, set transaction limits, change your PIN and more}\"",
      "          }",
      "        />",
      "      </IonContent>",
      "    </IonPage>",
      "  );",
      "};",
      "",
      "export default ${TM_DIRECTORY/^.+[\\/\\\\]+(.*)$/$1/};"
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
Check [VSCode Docs](https://code.visualstudio.com/docs/editor/userdefinedsnippets) for more.
