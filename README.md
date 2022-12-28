# Log

## Setup

Make sure a contract is deployed to desired network. We deployed our nft marketplace contract to Goerli

`npm install -g @graphprotocol/graph-cli`

`graph init --studio nft-marketplace` -> follow prompts and provide the mainnet or test next contract address

`mv nft-marketplace/* ./` to move everything under root directory instead of having it nested

Create a subgraph at https://thegraph.com/studio/subgraph

## Populate schema

Structure of data to be captured by the events emitted
in [./schema.graphql](./schema.graphql)

Update the generated types with `graph codegen`. Run this whenever making changes to the schema to update the generated files

## Create Handler Logic

in [./src/nft-marketplace.ts](./src/nft-marketplace.ts)

## Authenticate within the CLI, build and deploy your subgraph to the Studio.

`graph auth --studio undefined`
`graph codegen && graph build`
`graph deploy --studio nft-marketplace`

## Use Development Query URL in front-end app

eg. https://api.studio.thegraph.com/query/38206/nft-marketplace/v0.0.2
