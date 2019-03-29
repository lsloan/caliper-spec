# IMS Global Learning Consortium, Inc.

*Warning*: This is just a test branch to discuss potentially combining some repositories.


# Caliper Analytics&reg; Specification
The [Caliper Analytics® Specification](https://www.imsglobal.org/caliper/v1p1/caliper-spec-v1p1) 
provides a structured approach to describing, collecting and exchanging learning activity data at 
scale. Caliper also defines an application programming interface (the Sensor API™) for marshalling 
and transmitting event data from instrumented applications to target endpoints for storage, 
analysis and use.

### Core Documents

|Name|Public Version|Description|
|--- |--- |--- |
|`caliper-spec.md`| |The main spec document.|
|`implementation-guid.md`| |The implementation guide document.|
|`certification-guide.md`| |Instructions on certification.|
|`/ontology`| |The ontology files provide machine-readable documents that define the concepts, relationships and constraints that together comprise the Caliper information model. The ontology is available in three flavors: JSON-LD, RDF/XML and Turtle.|
|`/json-ld-context`|[Yes](https://github.com/IMSGlobal/caliper-contexts-public)|Caliper JSON-LD context documents for mapping Caliper terms to IRIs.|

### Test fixtures and JSON schema

|Name|Public Version|Description|
|--- |--- |--- |
|`/fixtures`| |A set of unit test fixtures for reference implementations to test against. Great for finding examples of Caliper Event JSON.|
|`/json-schema`| |A set of JSON schemas that can be used to validate Caliper JSON-based documents.|

### Related Specs

|Name|Public Version|Description|
|--- |--- |--- |
|[LTI-spec-Caliper](https://github.com/IMSGlobal/LTI-spec-Caliper)| |An LTI spec explaining how to use Caliper with LTI tools.|

### Example Apps

|Name|Public Version|Description|
|--- |--- |--- |
|[caliper-java-example-public](https://github.com/IMSGlobal/caliper-java-example-public)|Yes||
|[caliper-js-example](https://github.com/IMSGlobal/caliper-js-example)|||
|[caliper-eventstore-public](https://github.com/IMSGlobal/caliper-eventstore-public)|Yes||

### Reference Implementations

|Name|Public Version|Description|
|--- |--- |--- |
|[caliper-java](https://github.com/IMSGlobal/caliper-java)|[Yes](https://github.com/IMSGlobal/caliper-java-public)|Java library|
|[caliper-js](https://github.com/IMSGlobal/caliper-js)|[Yes](https://github.com/IMSGlobal/caliper-js-public)|Javascript library|
|[caliper-python](https://github.com/IMSGlobal/caliper-python)|[Yes](https://github.com/IMSGlobal/caliper-python-public)|Python library|
|[caliper-net](https://github.com/IMSGlobal/caliper-net)|[Yes](https://github.com/IMSGlobal/caliper-net-public)|.NET library|
|[caliper-ruby](https://github.com/IMSGlobal/caliper-ruby)|[Yes](https://github.com/IMSGlobal/caliper-ruby-public)|Ruby library|
|[caliper-php](https://github.com/IMSGlobal/caliper-php)|[Yes](https://github.com/IMSGlobal/caliper-php-public)|PHP library|

# Magic Documentation Tools

The magical IMS documentation tools can be used to generate and publish all the documents for Caliper. Here are the commands that totally exist:

## Publishable Document Generation


```bash
$ imsmagic generate primary_document caliper-spec.md
  #> files created: caliper-spec-v1p1.html
```

Generate the HTML for the primary document. Processes a markdown file into a respec file and generates everything needed for the publishable document.


```bash
$ imsmagic generate impl_guide
  #> files created: ims-caliper-analytics-implementation-guide.html
```

Generate the HTML for the implementation guide. The file is assumed to be named `implementation-guide.md`. You can pass an argument to specify a file with a different name.


```bash
$ imsmagic generate cert_guid --candidate-final
  #> files created: IMSCaliperv1RCDRAFT-ConformanceandCertificationGuide.html
```

Generate the HTML for the certification guide. You can pass flags to specify the version of this document.

## Document Publishing

```bash
$ imsmagic publish primary_document caliper-spec-v1p1.html
 #> Uploading to Drupal because that's totally what we'd want
 #> Just kidding, but maybe there is something that would make sense for this
```



# Contributing
We welcome the posting of issues by non IMS Global Learning Consortium members (e.g., feature 
requests, bug reports, questions, etc.) but we *do not* accept contributions in the form of pull 
requests from non-members. See [CONTRIBUTING.md](./CONTRIBUTING.md) for more 
information.

## Branches
* __master__: stable, deployable branch that stores the official release history. Updates to support documents will continue to be merged into `master` as appropriate.  
* __develop__: unstable development branch.  Current work that targets a future release is 
merged to this branch.

## Tags
Following the 1.1.0 release *caliper-spec* releases will be tagged as follows:

#### Tags on master 
* `1.2-final`: denotes the release of version 1.2 in Final state

* `1.1-errata.01`: denotes the first errata release for version 1.1 

* `1.1-errata.02`: denotes the second errata release for version 1.1

* `1.2-impl-guide.mm-dd-yyyy`: denotes a commit that a _published_ implementation guide came from

* `1.2-cert-guide.mm-dd-yyyy`: denotes a commit that a _published_ certification guide came from

#### Tags on develop (pre-release)
* `1.2-base.01`: denotes the first release of version 1.2 in Base Document state

* `1.2-candidate.01`: denotes the first release of version 1.2 in Candidate Final state

* `1.2-candidate.02`: denotes the second release of version 1.2 in Candidate Final state

_Note: the third `.nn` segment is incremented whenever the same type of release may occur 
multiple times for a given version of a document._


## License
This project is licensed under the terms of the IMS Global Learning Consortium Specification Document 
License. See the [LICENSE](./LICENSE.md) file for details.

©2018 IMS Global Learning Consortium, Inc. All Rights Reserved.
Trademark Information - http://www.imsglobal.org/copyright.html
