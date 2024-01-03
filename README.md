# Movie Browser Frontend

A React/TypeScript client for signing in and managing a personal movie collection through list, create, edit, image-upload, and delete flows.

## Application flow

```text
sign in -> movie list -> create movie
                      -> edit movie
                      -> delete movie
```

Routes live in `src/routes/Router.tsx`, API access in `src/services/api.ts`, reusable fields in `src/components`, and form validation schemas in `src/schemas`.

## Local setup

```bash
cp .env_sample .env
npm install
npm start
```

Configure the API URL expected by the Axios client and start the matching backend separately. The full-stack version is available in [`movie-collection-organizer`](https://github.com/alirazawatoo/movie-collection-organizer).

## Boundaries

- Authentication and persistence depend on the external API.
- `src/pages/Movies.test.tsx` provides focused page coverage, not end-to-end assurance.
- Image behavior depends on the backend upload contract.
