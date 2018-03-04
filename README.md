# DDH_HomelessServices

https://eastbay.homeless-connection.org/

A mobile-friendly web app for homeless folks to find shelters and services.

Concept document: https://xd.adobe.com/view/7bb0db8f-e55c-4827-9839-b9bf7be78244/

Service locations are hosted at Airtable: https://airtable.com/tblCsWJj89Fo3qzXF/viwBuB5lZ6j5Od1Bn


## Domain Name and CNAME File

The canonical URL is an alias for https://greeninfo-network.github.io/DDH_HomelessServices/

The *github.io* URL should work fine, though some internal links such as the / link may act strangely.

Do not delete the file **CNAME** This is an instruction to Github Pages for the custom hostname. It will not affect your local development, but is important to the domain setup working!



## Documentation and Client

Client: Pro-bono work for Dorothy Day House, Homeless Services

QuickBooks: GIN:Marketing:News Maps

Github: https://github.com/GreenInfo-Network/DDH_HomelessServices/

Drive Folder: https://drive.google.com/drive/folders/0B4DS3bml4a4xWEZHc3RnZ1hpSmM

P Folder: P_Projects/proj_e_h/greeninfo/NewsMaps/DorothyDayHouseHomelessServices


## Development and Testing

Babel, SASS/SCSS, Webpack.

Upon initial setup on your system, run `nvm use` and `yarn install` to set up build tools.

**index.html** **index.css** **index.js** are browser-side "deliverables" These are compiled by `npm run build` using webpack. Note that there **are** included in version control, so they may be hosted via Github Pages without us needing to work in additional tooling.

`npm run watch` will watch for changes and re-run `npm run build` upon detecting changes.

For development, you probably want `npm run serve` This will run a HTTP server with live reload when you change files. Don't forget to do a build though, if you intend to deploy your changes to the site.
