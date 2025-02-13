# MTA-STS.ST-JOHNSSCHOOL.NET

HUGE THANKS TO JIMEH FOR THE TEMPLATE: [https://github.com/jimeh/mta-sts-on-github-pages/tree/main]
  - Please note that original "usage guidance" from jimeh had a dot at the end of "GITHUB_USER.github.io", which is not needed.
  - I have updated the usage below accordingly, thanks.

Template repository for hosting `mta-sts.YOURDOMAIN/.well-known/mta-sts.txt` on GitHub Pages.

This serves as alternative as a supplier option in step 3 described here: [https://www.security.gov.uk/policy-and-guidance/set-up-tls-rpt-and-mta-sts/]

## Usage

- Add a `CNAME` DNS record at `mta-sts.YOURDOMAIN` pointing to `GITHUB_USER.github.io`.
- Add a `TXT` DNS record at `_mta-sts.YOURDOMAIN` indicating the use of MTA-STS, and update the `id` value on policy change.
- Create a new repository from this template repository.
- Replace `YOURDOMAIN` with your custom domain in `CNAME`.
- Update `.well-known/mta-sts.txt` to set `mx` directives to match the MX DNS records of your domain.
- Turn on GitHub Pages (Settings > Pages) for the repository, using the root (`/`) of the main branch as source.
- Turn on Enforce HTTPS setting for GitHub Pages (You might need to wait for 24 hours before completing this step)
