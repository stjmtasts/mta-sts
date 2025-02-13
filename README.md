# MTA-STS on GitHub Pages

SPECIAL THANKS TO JIMEH: [https://github.com/jimeh/mta-sts-on-github-pages/tree/main]

Template repository for hosting `mta-sts.YOURDOMAIN/.well-known/mta-sts.txt` on GitHub Pages.

For more information about MTA-STS, including details of required DNS record setup and options available, please see this article: [https://www.security.gov.uk/policy-and-guidance/set-up-tls-rpt-and-mta-sts/]

SPECIAL THANKS TO JIMEH: [https://github.com/jimeh/mta-sts-on-github-pages/tree/main]

## Usage

- Add a `CNAME` DNS record at `mta-sts.YOURDOMAIN` pointing to `GITHUB_USER.github.io.`.
- Add a `TXT` DNS record at `_mta-sts.YOURDOMAIN` indicating the use of MTA-STS, and update the `id` value on policy change.
- Create a new repository from this template repository.
- Replace `YOURDOMAIN` with your custom domain in `CNAME`.
- Update `.well-known/mta-sts.txt` to set `mx` directives to match the MX DNS records of your domain.
- Turn on GitHub Pages (Settings > Pages) for the repository, using the root (`/`) of the main branch as source.
- Turn on Enforce HTTPS setting for GitHub Pages.
