# Investec Card Code Template

This is a template for Investec card code. This is schaffolding sets up  a project with the tools to upload code to the Investec card.

## 🌟 Community-Powered Repository 🌟

This repository is crafted with ❤️ by our talented community members. It's a space for everyone to use, contribute to, and share. While it aligns with the spirit of our community, please note that this repo is not directly endorsed or supported by Investec. Always exercise caution and discretion when using or contributing to community-driven projects.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Copy over the `.env.example` file to `.env` and fill in the required fields.
```sh
cp .env.example .env
```

The .env file is for your local environment and the .env.prod file is for the production environment.
```sh
cp .env.example .env.prod
```

To install the dependencies, run the following command:
```sh
npm install
```
## Configuration
You can access your client id, client secret and api key from the Investec Developer Portal.
More information on how to access your keys can be found on the [Investec Developer Community Wiki](https://investec.gitbook.io/programmable-banking-community-wiki/get-started/api-quick-start-guide/how-to-get-your-api-keys).

To configure the CLI, run the following command:
```bash
npx ipb config --client-id <client-id> --client-secret <client-secret> --card-id <card-id>
```
The card id is optional and can be set when calling each command. If you specify a card when calling a command, it will override the card id set in the configuration.

## Usage
To run the code locally, run the following command:
```sh
npx ipb run -f main.js --env prod --amount 60000 --currency ZAR --mcc 0000 --merchant "Test Merchant" --city "Test City" --country ZA
```

To upload code you will need a card key this can be retireved by calling the following command:
```sh
npx ipb cards
```

To upload code to the card, run the following command by setting the card key, the file and the env to upload:
The env is optional and needs the file to be .env.prod if you specify prod

```sh
npx ipb deploy -c <cardkey> -f main.js --env prod
```

You can get your card execution logs with the following command
```sh
npx ipb logs -f <filename> -c <cardkey>
```

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details
