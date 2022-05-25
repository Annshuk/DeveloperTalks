ESM Build
react-intl and its underlying libraries (@formatjs/icu-messageformat-parser, intl-messageformat, @formatjs/intl-relativetimeformat) export ESM artifacts. This means you should configure your build toolchain to transpile those libraries.

Jest
Add transformIgnorePatterns to always include those libraries, e.g:

{
  transformIgnorePatterns: [
    '/node_modules/(?!intl-messageformat|@formatjs/icu-messageformat-parser).+\\.js$',
  ],
}
webpack
If you're using babel-loader, or ts-loader, you can do 1 of the following:

Add those libraries in include:
{
  include: [
    path.join(__dirname, 'node_modules/react-intl'),
    path.join(__dirname, 'node_modules/intl-messageformat'),
    path.join(__dirname, 'node_modules/@formatjs/icu-messageformat-parser'),
  ]
}
OR

Add those libraries in exclude:
exclude: /node_modules\/(?!react-intl|intl-messageformat|@formatjs\/icu-messageformat-parser)/,
