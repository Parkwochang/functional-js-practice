# 🧑‍💻 NextJS ThankQ_FE 가이드라인

### `npm run dev`

Runs the app in the development mode.

### `npm run build`

Builds the app for production to the `out` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

터미널에 npm i 를 입력해서 package.json에 있는 라이브러리를 다운 받은 후, \
npm run dev를 개발 모드 실행 & npm run build 를 하여 build 실행 -> out 폴더가 build 폴더

### `npm run start`

### `npm run test`

test the app using jest

<br/>
<br/>

# 🚀 Quick Start

```bash
cd <Project Name>
npm install
npm run dev
```

your site is now running at `http://localhost:3001`  
Open [http://localhost:3001](http://localhost:3001) to view it in your browser.

# 🔧 Build Project

```bash
cd <Project Name>
npm install
npm run build
```

`out` folder = `build` folder
<br/>

# 📁 Folder Structure

A quick look at the directories you'll see in this project.

## Root driectory layout

    .
    ├── public              #
    ├── pages               #
    ├── @types              #
    ├── styles              # css
    ├── constants           #
    ├── apis                #
    ├── store               # global state
    ├── components          #
    ├── hooks               # Custom hooks
    ├── utils               #
    ├── README.md           #
    └── ...

<br/>

## Pages

Each page is associated with a route based on its file name.

    .
    ├── ...
    ├── pages               #
    │   ├── apis            # API endpoint
    │   ├── _app.tsx        # App component to initialize pages
    │   ├── _document.tsx   # Custom document to augment application's <html> and <body> tags
    │   └── index.tsx       # Parent page
    └── ...

<br/>

## Styles

Css, theme configuration files are placed into this folder.

    .
    ├── ...
    ├── styles              #
    │   ├── globals.css     #
    │   └── ...
    └── ...

<br/>

## Components

Components are independent and reusable bits of code.

    .
    ├── ...
    ├── components          #
    │ ├── @Layout           # Page Layout
    │ ├── Button ...        # Atomic Components
    │ ├── Hooks             # Custom React Hook
    │ └── ...               #
    └── ...

<br/>

## Api

Api call related functions.
<br/>

## Hooks

Custom hook allows you to extract some components logic into a reusable function that starts with use and that call can other hooks.

    .
    ├── ...
    ├── hooks                #
    │   ├── useHook.tsx      #
    │   └── ...
    └── ...

<br/>

## Utils

Small snippets you can use throughout the application. Short and specific functions and constants used throughout application.

<br/>

## 🧑‍💻 React Component

- **Extensions:** Use .tsx extension for React components.

- **Filename:** Use PascalCase for filenames. E.g., ReservationCard.tsx.

- **Reference Naming:** Use PascalCase for React components and camelCase for their instances.

  ```tsx
  // bad
  import reservationCard from './ReservationCard';

  // g
  import ReservationCard from './ReservationCard';

  // bad
  const ReservationItem = <ReservationCard />;

  // g
  const reservationItem = <ReservationCard />;
  ```

  <br/>
  <br/>

# 🤔 Don't use React.FC

1. 사용하지 않는 편이 더 간단하고 익숙합니다.
2. children prop이 옵셔널로 포함되어 props 타입이 명확하지 못합니다.
3. defaultProps가 정상적으로 동작하지 않습니다. defaultProps 사용하여 props의 초기 값을 설정하여도 값을 인식하지 못합니다.

<br/>
