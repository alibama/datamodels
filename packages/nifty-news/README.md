# NiFTy News DataModel

DataModel implementation of the **NiFTy News** schema and definition specified here).

## Installation

```sh
npm install -D @datamodels/nifty-news
```

## Rationale

The **NiFTy News** contains a News or Blogs's basic information designed around sustainability, confidentiality, and simplicity of asserting accuracy through the ability to attach IPFS data for use in NFT creation. Leveraging the schema.org/Events space simplifies the process, however we use it aware of the limitations in its current design.

https://www.foam.space/ is planned for integration in geospatially organizing this product

by building the product with BrightID compatibility we'll have a process for connecting content without risk of associating names or other biometric data that might compromise the safety of the news person

**Where and when things happen is the foundation stone of news**: The NiFTy News schema attempts to provide a reduced approach to the schema.org standard that, while inclusive and expansive, should probably be accorded a broader meta-data standard to then include mediawiki or other standard development products specific to the niche ecosystem.  and the whole damn thing should be done with silly little widgets  



## Schemas
about | description field
location | wgs84 - pull from foam.space later, use peermaps.org for pinning?
location name | str
BrightID | uids
inLanguage | 
startDate | iso 8601
endDate | iso 8601
media | for NFT process


### [BasicProfile](./schemas/BasicProfile.json)

The Basic Profile schema defines the format of a document that contains the properties listed below. Properties not defined in the schema _cannot_ be included in the Basic Profile, however the schema can always be updated via a new CIP.

| Property           | Description                    | Value                                                                                  | Max Size | Required | Example                      |
| ------------------ | ------------------------------ | -------------------------------------------------------------------------------------- | -------- | -------- | ---------------------------- |
| `name`             | a name                         | string                                                                                 | 150 char | optional | Mary Smith                   |
| `image`            | an image                       | Image sources                                                                          |          | optional |                              |
| `description`      | a short description            | string                                                                                 | 420 char | optional | This is my cool description. |
| `emoji`            | an emoji                       | unicode                                                                                | 2 char   | optional | 🔢                           |
| `background`       | a background image (3:1 ratio) | Image sources                                                                          |          | optional |                              |
| `birthDate`        | a date of birth                | [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601)                                     | 10 char  | optional | 1990-04-24                   |
| `url`              | a url                          | string                                                                                 | 240 char | optional | http://ceramic.network       |
| `gender`           | a gender                       | string                                                                                 | 42 char  | optional | female                       |
| `homeLocation`     | a place of residence           | string                                                                                 | 140 char | optional | Berlin                       |
| `residenceCountry` | a country of residence         | [ISO 3166-1 alpha-2](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2)                 | 2 char   | optional | DE                           |
| `nationalities`    | nationalities                  | array of [ISO 3166-1 alpha-2](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2) values | 2 char   | optional | CN                           |
| `affiliations`     | affiliations                   | array of strings                                                                       | 240 char | optional | Ceramic Ecosystem Alliance   |

## [Discussion](https://github.com/ceramicstudio/datamodels/discussions/10)

## License

Dual licensed under MIT and Apache 2
