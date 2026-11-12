# React Tenant Lookup

The frontend repository for a Microsoft Entra tenant lookup project, intended to work with the [Express Tenant Lookup API](https://github.com/Syed-Jawad1412/Express-Tenant-Lookup).

The project is described as supporting domain-to-tenant ID lookup, bulk lookup and CSV export. The current repository contains the React package configuration and dependency lockfile, but the application source is missing, so these interface features cannot yet be verified from this checkout.

## Technology stack

- React and React DOM
- Create React App (`react-scripts`)
- React Testing Library

See `package.json` and `package-lock.json` for the recorded dependency versions.

## Repository status

The `src/` and `public/` folders are not currently committed. This checkout is incomplete and cannot start or build the frontend until the original application files are restored.

Do not treat generated placeholder components as the original implementation. Restore the actual source, including `src/index.*`, the app components and `public/index.html`, then check any API configuration against the backend.

## Available scripts

After restoring the missing source and reviewing compatibility with a supported Node.js release:

```sh
npm ci
npm start
```

Other scripts declared in the package configuration:

```sh
npm test
npm run build
```

`npm start` is the Create React App development command. `npm run build` creates a production bundle when the required source files are present. No passing build or test result is claimed for the incomplete checkout.

## Backend integration

The associated backend provides:

- `GET /api/tenant-smart?domain=example.com`
- `POST /api/tenant-bulk` with a JSON `domains` array

It listens on port `5000` by default. The frontend API URL must be confirmed from the restored source. Backend lookup results may use a guessed `.onmicrosoft.com` fallback; display and validate the resolved domain when implementing the interface.

## Next steps

1. Restore the original `src/` and `public/` folders.
2. Verify single and bulk lookup flows against the backend.
3. Confirm CSV export and document the actual user interface.
4. Add screenshots, test instructions and a live demo link when available.

## License

No project license file is currently included. Confirm licensing before redistributing the application.
