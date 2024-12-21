# Investec Card Code Template

This is a template for Investec card code. This is schaffolding sets up  a project with the tools to upload code to the Investec card.

Copy over the `.env.example` file to `.env` and fill in the required fields.
```sh
cp .env.example .env
```
To install the dependencies, run the following command:
```sh
npm install
```
## Usage
To run the code locally, run the following command:
```sh
npx investec-card-cli run main.js --environment "env.json" --amount 60000 --currency ZAR --mcc 0000 --merchant "Test Merchant" --city "Test City" --country ZA
```

To upload code you will need a card key this can be retireved by calling the following command:
```sh
npx investec-card-cli fetch-cards
```

To upload code to the card, run the following command by setting the card key and the file to upload:
```sh
npx investec-card-cli upload 700615 main.js
```
To upload your environment variables to the card, run the following command:
```sh
npx investec-card-cli upload-env 700615 env.json
```
## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details
