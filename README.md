Account Creation Library
=======

This library contains a CreateRequest wrapper that facilitates the management of account creation request tokens.

## Installation

The `@greymass/account-creation` package is distributed as a module on [npm](https://www.npmjs.com/package/@greymass/account-creation).

```
yarn add @greymass/account-creation
# or
npm install --save @greymass/account-creation
```

## Usage


```
import { CreateRequest } from '@greymass/account-creation'

// Initialize the CreateRequest object with a creation token:
const createRequest = new CreateRequest("CREATION_TOKEN")

// or with a list of params:
const createRequest = new CreateRequest({
    code: string
    login_url?: string
    login_scope?: NameType
    return_path?: string
})

// Get the create request login scope
const loginScope = createRequest.login_scope

// Get the create request login esr
const esrLoginRequest = createRequest.loginRequest

// Get the token string
const createRequestToken = createRequest.toString()
```

## Developing

You need [Make](https://www.gnu.org/software/make/), [node.js](https://nodejs.org/en/) and [yarn](https://classic.yarnpkg.com/en/docs/install) installed.

Clone the repository and run `make` to checkout all dependencies and build the project. See the [Makefile](./Makefile) for other useful targets. Before submitting a pull request make sure to run `make lint`.

---

Made with ☕️ & ❤️ by [Greymass](https://greymass.com), if you find this useful please consider [supporting us](https://greymass.com/support-us).
