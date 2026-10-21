# medium-mern

A React front end for a Medium-style reading header, with a placeholder Node server.

**Status:** Stub. `server.js` is an empty file, the React client renders only a header component inside `App.js`, and there are no tests.

## The problem

The project is an early attempt at a Medium-style publishing and reading site. The only part that exists in the code is the top navigation bar that such a site would show.

## What it does

- Header bar with search, bookmark, notification and flag icons (`client/src/Components/Header.js`).
- User avatar with a context menu, and a notification dropdown with its own menu (`UserContextMenu`, `NotificationContextMenu`).
- A theme switch function in the header that listens for changes to the system colour scheme.
- Styles split into partials for colours, variables, globals and the header (`client/src/Styles/`).

## How it's built

- Client: React 17 created with Create React App (`react-scripts` 4.0.3), `react-feather` icons and Sass.
- Server: a root `package.json` with `"start": "node server.js"`, but `server.js` is empty.
- Architecture decision: colours and sizes live in separate Sass partials (`__colors.scss`, `__variable.scss`), so the header styles use shared tokens.

## Running it locally

```bash
cd client
npm install
npm start    # react-scripts start
npm run build
```

The root `npm start` runs the empty `server.js` and exits without serving anything.

## What's left

- `server.js` is empty, so there is no API, database or article storage.
- `App.js` renders only `Header`. There are no article, profile or feed pages.
- No tests: the root `test` script is the npm placeholder, and the client has no test files.
- The client uses React 17 and react-scripts 4.0.3, which are old releases.
