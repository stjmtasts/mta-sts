# MTA-STS.st-johnsschool.net

HUGE THANKS TO JIMEH FOR THE TEMPLATE: [https://github.com/jimeh/mta-sts-on-github-pages/tree/main]
  - Please note:
    - That original "usage guidance" from jimeh had a dot at the end of "GITHUB_USER.github.io", which is not needed.
    - I have updated the usage below accordingly, thanks.

Template repository for hosting `mta-sts.YOURDOMAIN/.well-known/mta-sts.txt` on GitHub Pages.

This serves as alternative supplier option in step 3 described here: [https://www.security.gov.uk/policy-and-guidance/set-up-tls-rpt-and-mta-sts/]

## Usage

- Add a `CNAME` DNS record at `mta-sts.YOURDOMAIN` pointing to `GITHUB_USER.github.io`.
- Add a `TXT` DNS record at `_mta-sts.YOURDOMAIN` indicating the use of MTA-STS, and update the `id` value on policy change.
- Create a new repository from this template repository.
- Replace `YOURDOMAIN` with your custom domain in `CNAME`.
- Update `.well-known/mta-sts.txt` to set `mx` directives to match the MX DNS records of your domain.
- Turn on GitHub Pages (Settings > Pages) for the repository, using the root (`/`) of the main branch as source.
- Turn on Enforce HTTPS setting for GitHub Pages.
  - Please note that if GitHub tells you to get ssl for your custom domain, try removing your custom domain from the field and then re-adding.
  - After typing and saving it again, DNS should be succesful and you should be able to tick "enforce HTTPS".

