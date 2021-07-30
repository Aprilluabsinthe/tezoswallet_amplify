## Build up project
```shell script
npx create-next-app tezoswallet
cd tezoswallet
npm run dev

```

create tsconfig.json
```shell script
npm install --save-dev @types/react @types/node
npm run dev
```

tsconfig.json will be automatically changed

## Amplify

```shell script
amplify init
```

settings:
```text
? Initialize the project with the above configuration? No
? Enter a name for the environment dev
? Choose your default editor: IntelliJ IDEA
? Choose the type of app that you're building javascript
Please tell us about your project
? What javascript framework are you using react
? Source Directory Path:  src
? Distribution Directory Path: build
? Build Command:  npm run build
? Start Command: npm run start
Using default provider  awscloudformation

? Select the authentication method you want to use: AWS profile
```

Wait for initiating.


```shell script
amplify add api
```

settings:
```text
? Please select from one of the below mentioned services: GraphQL
? Provide API name: tezoswallet
? Choose the default authorization type for the API API key
? Enter a description for the API key: apikey
? After how many days from now the API key should expire (1-365): 60
? Do you want to configure advanced settings for the GraphQL API Yes, I want to make some additional changes.
? Configure additional auth types? Yes
? Choose the additional authorization types you want to configure for the API Amazon Cognito User Pool
Cognito UserPool configuration
Using service: Cognito, provided by: awscloudformation
 
 The current configured provider is Amazon Cognito. 
 
 Do you want to use the default authentication and security configuration? Default configuration
 Warning: you will not be able to edit these selections. 
 How do you want users to be able to sign in? Email
 Do you want to configure advanced settings? No, I am done.
Successfully added auth resource tezoswalletc101f0e9 locally

```

modify schema.graphql

```shell script
amplify push
```

```text
? Do you want to generate code for your newly created GraphQL API Yes
? Choose the code generation language target typescript
? Enter the file name pattern of graphql queries, mutations and subscriptions src/graphql/**/*.ts
? Do you want to generate/update all possible GraphQL operations - queries, mutations and subscriptions Yes
? Enter maximum statement depth [increase from default if your schema is deeply nested] 2
? Enter the file name for the generated code src/API.ts

```