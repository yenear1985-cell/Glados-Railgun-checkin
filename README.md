# g-sign-daily

Daily sign-in automation with auto exchange, deployed on GitHub Actions.

## Features

- Automated daily sign-in via GitHub Actions (Beijing 03:26, UTC 19:26)
- Two-domain rotation: glados.cloud → glados.one
- Points query and auto-exchange (plan100 / plan200 / plan500)
- All logs displayed in Beijing time
- Failure notification via GitHub Issue + email

## Usage

1. Fork this repository
2. Add GLADOS_COOKIES to **Settings → Secrets and variables → Actions**
3. (Optional) Add GLADOS_EXCHANGE_PLAN (default: plan500)
4. (Optional) Set GLADOS_VERBOSE to 	rue for detailed logs
5. Go to **Actions** tab and trigger manually, or wait for the scheduled run

## Notification

- At least one domain succeeds → no notification
- Both domains fail → GitHub creates an Issue automatically and sends an email to your account's email address

## Credits

Based on [Devilstore/Glados-Railgun-checkin](https://github.com/Devilstore/Glados-Railgun-checkin).