# π§βπ» NextJS ThankQ_FE κ°μ΄λλΌμΈ

### `npm run dev`

Runs the app in the development mode.

### `npm run build`

Builds the app for production to the `out` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

ν°λ―Έλμ npm i λ₯Ό μλ ₯ν΄μ package.jsonμ μλ λΌμ΄λΈλ¬λ¦¬λ₯Ό λ€μ΄ λ°μ ν, \
npm run devλ₯Ό κ°λ° λͺ¨λ μ€ν & npm run build λ₯Ό νμ¬ build μ€ν -> out ν΄λκ° build ν΄λ

### `npm run start`

### `npm run test`

test the app using jest

<br/>
<br/>

# π Quick Start

```bash
cd <Project Name>
npm install
npm run dev
```

your site is now running at `http://localhost:3001`  
Open [http://localhost:3001](http://localhost:3001) to view it in your browser.

# π§ Build Project

```bash
cd <Project Name>
npm install
npm run build
```

`out` folder = `build` folder
<br/>

# π Folder Structure

A quick look at the directories you'll see in this project.

## Root driectory layout

    .
    βββ public              #
    βββ pages               #
    βββ @types              #
    βββ styles              # css
    βββ constants           #
    βββ apis                #
    βββ store               # global state
    βββ components          #
    βββ hooks               # Custom hooks
    βββ utils               #
    βββ README.md           #
    βββ ...

<br/>

## Pages

Each page is associated with a route based on its file name.

    .
    βββ ...
    βββ pages               #
    β   βββ apis            # API endpoint
    β   βββ _app.tsx        # App component to initialize pages
    β   βββ _document.tsx   # Custom document to augment application's <html> and <body> tags
    β   βββ index.tsx       # Parent page
    βββ ...

<br/>

## Styles

Css, theme configuration files are placed into this folder.

    .
    βββ ...
    βββ styles              #
    β   βββ globals.css     #
    β   βββ ...
    βββ ...

<br/>

## Components

Components are independent and reusable bits of code.

    .
    βββ ...
    βββ components          #
    β βββ @Layout           # Page Layout
    β βββ Button ...        # Atomic Components
    β βββ Hooks             # Custom React Hook
    β βββ ...               #
    βββ ...

<br/>

## Api

Api call related functions.
<br/>

## Hooks

Custom hook allows you to extract some components logic into a reusable function that starts with use and that call can other hooks.

    .
    βββ ...
    βββ hooks                #
    β   βββ useHook.tsx      #
    β   βββ ...
    βββ ...

<br/>

## Utils

Small snippets you can use throughout the application. Short and specific functions and constants used throughout application.

<br/>

## π§βπ» React Component

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

# π€ Don't use React.FC

1. μ¬μ©νμ§ μλ νΈμ΄ λ κ°λ¨νκ³  μ΅μν©λλ€.
2. children propμ΄ μ΅μλλ‘ ν¬ν¨λμ΄ props νμμ΄ λͺννμ§ λͺ»ν©λλ€.
3. defaultPropsκ° μ μμ μΌλ‘ λμνμ§ μμ΅λλ€. defaultProps μ¬μ©νμ¬ propsμ μ΄κΈ° κ°μ μ€μ νμ¬λ κ°μ μΈμνμ§ λͺ»ν©λλ€.

<br/>
