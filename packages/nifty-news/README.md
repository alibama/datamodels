# NiFTy News DataModel

DataModel implementation of the **NiFTy News** schema and definition specified here and inspired by https://schema.org/Event .

## Installation

```sh
npm install -D @datamodels/nifty-news
```

## Rationale

The **NiFTy News** contains a News or Blogs's basic information designed around sustainability, confidentiality, and simplicity of asserting accuracy through the ability to attach IPFS data for use in NFT creation. Leveraging the schema.org/Events space simplifies the process, however we use it aware of the limitations in its current design, as well as the opportunities to simplify this process using Ceramic's off-the-shelf features.

https://www.brightID.org is planned for integration in safely anonymizing the content with proving some anti-sybil security
https://www.foam.space/ is planned for integration in geospatially organizing this content

by building the product with BrightID compatibility we'll have a process for connecting content without risk of associating names or other biometric data that might compromise the safety of the news person

Ceramic also obviates some of the products in the schema.org profile. For instance the translator field - an integral asset tag for multi-language products - may be stored in the ceramic tile as the NiFTy News object is updated

**More provably first-hand accounts helps raise the bar in journalistic integrity.**: Obtaining accurate news from areas of conflict is difficult for many reasons. NiFTy News attempts to provide more equitable compensation, improved personal security, and more tamper-proof tools for people in many fields who may be familiar with these challenges.  





## Schema
* description | description field
* image | a thumbnail image field
* location | wgs84 - pull from foam.space later, use peermaps.org for pinning? 
* startDate | iso 8601
* endDate | iso 8601
* BrightID | weighted DID reference
* inLanguage |  IETF BCP 47 standard (EN-US vs EN-GB parsible)
* media | IPFS 
* additionalType | an optional linked data space


### [NiFTy News](./schemas/nifty-news.json)

The NiFTy News schema defines the format of a document that contains the properties listed below. Properties not defined in the schema _cannot_ be included in the Basic Profile, however the schema can always be updated via a new CIP.

| Property           | Description                    | Value                                                                                  | Max Size | Required | Example                      |
| ------------------ | ------------------------------ | -------------------------------------------------------------------------------------- | -------- | -------- | ---------------------------- |
| `description`             | what's going on                         | string                                                                                 | 420 char | optional | There's something strange, in the neighborhood                   |
| `image`            | an image for the thumbnail                      | Image a tuhmbnail image                                                                          |          | optional |                              |
| `location`            | WGS 84 ideally pulled from https://www.foam.space/                   | unicode                                                                                | 2 char   | optional | 
| `startDate`        | a date and time of things starting                | [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601)                                     | 19 char  | optional | 2007-04-05T14:30                  |
| `endDate`        | a date and time of things ending                | [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601)                                     | 19 char  | optional | 2007-04-05T14:30                  |string                                                                                 | 240 char | optional | http://ceramic.network       |
| `inLanguage`           | language being used - conform to IETF BCP 47 standard and reduce to two char hyphen two char format                       | string                                                                                 | 5 char  | optional | en-en                       |
| `BrightID`     | a reference to the BrightID identifier           | string                                                                                 | 140 char | optional                        |
| `media` | associated media        |  ipfs file    | 100MB?   | optional | big file                           |
| `additionalType` | optional extension tool        |  CID Schema reference    | ???   | optional | additional reference file to simplify upgrades


## [Discussion](https://github.com/ceramicstudio/datamodels/discussions/25)

## [Apologies]

The NiFTy News schema attempts to provide a reduced approach to the schema.org standard that, while inclusive and expansive, should probably be accorded a broader meta-data standard to then include mediawiki or other standard development products specific to the niche ecosystem.  and the whole damn thing should be done with silly little widgets.  

## License

Dual licensed under MIT and Apache 2
