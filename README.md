## Richierich ECommerce Next

Richierich's ECommerce Next provides a way to quickly get up and running with a fully configurable ECommerce site using Next.js.

Out of the box, the site uses completely static data coming from a provider at `providers/inventoryProvider.js`. You can update this provider to fetch data from any real API by changing the call in the `getInventory` function.

### Live preview

Click [here](https://www.jamstackecommerce.dev/) to see a live preview.



### Getting started

1. Clone the project

```sh
$ git clone https://github.com/Ishwar-Zatke/totalitycorp-frontend-challenge.git
```

2. Install the dependencies:

```sh
$ yarn

# or

$ npm install
```

3. Run the project

```sh
$ npm run dev

# or to build

$ npm run build
```

## Deploy to Netlify

Use the [Netlify ](https://www.netlify.com/)


## Deploy to AWS

```sh
npx serverless
```

## About the project

### Tailwind

This project is styled using Tailwind. To learn more how this works, check out the Tailwind documentation [here](https://tailwindcss.com/docs).

### Components

The main files, components, and images you may want to change / modify are:

__Logo__ - public/logo.png   
__Button, ListItem, etc..__ - components   
__Form components__ - components/formComponents   
__Context (state)__ - context/mainContext.js   
__Pages (admin, cart, checkout, index)__ - pages   
__Templates (category view, single item view, inventory views)__ - templates   

### How it works

As it is set up, inventory is fetched from a local hard coded array of inventory items. This can easily be configured to instead be fetched from a remote source like Shopify or another CMS or data source by changing the inventory provider.

#### Configuring inventory provider

Update __utils/inventoryProvider.js__ with your own inventory provider.

#### Download images at build time

If you change the provider to fetch images from a remote source, you may choose to also download the images locally at build time to improve performance. Here is an example of some code that should work for this use case:


You can use this function to map over the inventory data after fetching and replace the image paths with a reference to the location of the downloaded images, probably would look something like this:



### Updating with Auth / Admin panel

1. Update __pages/admin.js__ with sign up, sign, in, sign out, and confirm sign in methods.

2. Update __components/ViewInventory.js__ with methods to interact with the actual inventory API.

3. Update __components/formComponents/AddInventory.js__ with methods to add item to actual inventory API.

### Roadmap

- Full product and category search
- Auto dropdown navigation for large number of categories
- Ability to add more / more configurable metadata to item details
- Themeing + dark mode
- Optional user account / profiles out of the box
- Make Admin Panel responsive
### Other considerations


Also, consider verifying totals by passing in an array of IDs into the function, calculating the total on the server, then comparing the totals to check and make sure they match.
