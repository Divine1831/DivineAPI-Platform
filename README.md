# DivineAPI Platform — Upgraded

A responsive developer console for the existing DivineAPI backend.

## Run locally
Open `index.html` in a browser, or use VS Code Live Server. This is a static frontend; no Node build is required.

## API
The frontend currently connects to:
`https://divine-api-seven.vercel.app`

Known routes used:
- `GET /api/status`
- `GET /api/projects`
- `GET /api/auth/me` (documented as an existing route)
- `POST /api/auth/login`
- `POST /api/auth/register`
- `POST /api/auth/forgot-password`

The API Explorer can send GET, POST, PUT, PATCH and DELETE requests to routes on this API. The backend must actually implement a route and allow the frontend origin through CORS for it to work.

## Included interactions
- Responsive sidebar navigation
- Dark/light theme preference
- API request builder with headers and JSON body
- Response viewer, status and elapsed time
- Local request history and activity chart
- Documentation navigation
- Existing API authentication route forms

## Important limitations and security
- Request history is stored in this browser's local storage. It is not server analytics or global API usage.
- API key management, billing, team management, server-side uptime monitoring and usage quotas are not implemented because the current backend routes described to this project do not expose those features. They require real backend endpoints and database policies.
- The authentication form expects the existing API's response shape. Confirm the exact login/register payload and response format against the deployed backend before production use.
- Do not put Supabase service-role keys, private API secrets, passwords or recovery tokens in frontend source code.
- Restrict backend CORS to the deployed frontend origin before public launch.
- This project is a frontend dashboard, not an API gateway or security boundary.
