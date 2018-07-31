# @extensionjs/extensionjs-angular

## Installation

To install this library, run:

```bash
$ npm install @extensionjs/extensionjs-angular --save
```

## Consuming your library

Once you have published your library to npm, you can import your library in any Angular application by running:

```bash
$ npm install @extensionjs/extensionjs-angular
```

and then from your Angular `AppModule`:

```typescript
import { BrowserModule } from '@angular/platform-browser';
import { NgModule } from '@angular/core';

import { AppComponent } from './app.component';

// Import your library
import { SampleModule } from '@extensionjs/extensionjs-angular';

@NgModule({
  declarations: [
    AppComponent
  ],
  imports: [
    BrowserModule,

    // Specify your library as an import
    LibraryModule
  ],
  providers: [],
  bootstrap: [AppComponent]
})
export class AppModule { }
```

Once your library is imported, you can use its components, directives and pipes in your Angular application:

```xml
<!-- You can now use your library component in app.component.html -->
<h1>
  {{title}}
</h1>
<sampleComponent></sampleComponent>
```

## Development

To generate all `*.js`, `*.d.ts` and `*.metadata.json` files:

```bash
$ yarn build
```

To lint all `*.ts` files:

```bash
$ yarn lint
```

To run the test suite:

```bash
yarn test
```

To buildb the library api documentation:

```bash
# build, compile & bundle with ztatic assets
$ yarn docs:build
# serve the documentation
$ yarn docs:serve
```

The generated documentation is can be found in the `docs/` folder.

During development - to hot-reload on changes:

```bash
$ yarn docs:watch
```

To publish a new version to the npm registry:

```bash
# Note:library needs to be build firsst
$ yarn publish dist
```

## License

MIT © [Patrick Jung](mailto:patrick.pddstudio@gmail.com)
