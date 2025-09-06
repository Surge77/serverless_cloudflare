npm create cloudflare is a scaffolder (project generator)

Cloudflare provides a starter generator (create-cloudflare) to bootstrap Workers, Pages, and Durable Objects projects quickly.

THe command for creating a project with cloudflare

`npm create cloudflare -- my-app` 

or 

`npm create cloudflare@latest my-app`

`npx wrangler login`  - To login into our cloudflare account from the cli Opens your browser to https://dash.cloudflare.com/ (OAuth login).

You log in with your Cloudflare account (email/password or SSO).

`npx wrangler whoami` - Displays your Cloudflare account ID, email, and maybe team info.

Useful to confirm you’re logged in with the right account (especially if you have multiple).

`npm run deploy` - In a Cloudflare project, npm run deploy runs wrangler publish → bundles your Worker → uploads to Cloudflare → attaches resources → serves globally at edge locations.


> Terminal warning solution 

▲ [WARNING] Worker has workers.dev disabled, but 'workers_dev' is not in the config.

  Using fallback value 'workers_dev = true'.

  - In the wrangler.jsonc file just add `"workers_dev": true`


- If we want to deploy a new worker from the same project just change the name from the wrangler.jsonc file and the run the command `npm run deploy` 