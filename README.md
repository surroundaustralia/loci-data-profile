# Loc-I Data Profile
This is a _profile_, that is a multi-part _standard_ that constrains the use of other _standards_. 

_Formally, by 'profile', what is meant here is "A specification that constrains, extends, combines, or provides guidance or explanation about the usage of other specifications." (from [PROF](https://www.w3.org/TR/dx-prof/#definitions)) and, here the 'other specifications' are DCAT2, VoID etc. or, more correctly, intermediate profiles of them._

This profile presents a specification of constraints on the use of classes from the [DCAT2](https://www.w3.org/TR/vocab-dcat/), [GeoSPARQL](https://opengeospatial.github.io/ogc-geosparql/geosparql11/spec.html), [PROV-O](https://www.w3.org/TR/prov-o/), [VoID](http://rdfs.org/ns/void#) and [RDF](http://www.w3.org/TR/rdf-schema/) ontologies, namely `dcat:Dataset`, `geo:FeatureCollection`, `geo:Feature`, `prov:Bundle`, `void:Linkset` & `rdf:Statement`. These constraints are designed to ensure that use of these classes results in data that allows for [Location Index (Loc-I)](https://www.ga.gov.au/locationindex)-style use of that data. In short: the classes ust have certain properties associating them with one another and providing elements needed by APIs. 

Alonsgide the specification, this profile provides a series of validator resources ([Shapes Constraint Language (SHACL)](https://www.w3.org/TR/shacl/) files) which can be used to validate that instances data is valid according to the specification.


### Profile Formalism
This profile is formulated according to the [Profiles Vocabulary (PROF)](https://www.w3.org/TR/dx-prof/) and the persistent URI for this profile, see next, provides access to the PROF formal definition in both HTML & RDF.

This profile's persistent URI:

* <https://linked.data.gov.au/def/loci-dp>


## Profile Resources

### Specification
This profile's normative rules are presented in a _Specification document_ that identifies and states the various constraints that this profile places on a classes such as DCAT's Dataset. This _Specification document_ is an HTML web page that can be read here:

* [Specification document](https://linked.data.gov.au/def/loci-dp/spec)

### Validators
RDF data can be validated against this profile's rules, as identified and defined in _Specification document_, by use of a series of [SHACL](https://www.w3.org/TR/shacl/) validators, which are files within this repository's [validators/](validators/) folder.

These validators have their own URIs too: see their listing in the profile declaration at <https://linked.data.gov.au/def/loci-dp>.

Tools such as [pySHACL](https://github.com/RDFLib/pySHACL) and the online [SHACL Playground](https://shacl.org/playground/) can be used with these validators to apply them to data.

### Examples
Examples of valid and invalid data for each DCAT, VoID etc. class as needed by Loc-I systems are also presented as formal parts of this profile. See the [examples/](examples/) folder in this repository.


## Profile Use
There are several ways to use the resources in this profile. 

1. **Read the _specification_ to understand the requirements of data**
    * the Specification document in this profile is online at <https://linked.data.gov.au/def/loci-dp/spec> (and also the file in this repository [specification.html](https://raw.githack.com/surroundaustralia/loci-data-profile/master/specification.html))
    * it states the normative requirements of Loc-I data, per class, in English
2. **Validate data**
    * the 6 validators for this profile - one per Loc-I Ontology main class - are presented as SHACL files in this repository. Use a tool like [pySHACL](https://github.com/RDFLib/pySHACL) to apply a validator to instance data and check its validity

## License  
The contents of this repository are licensed using the [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) licence. See the [LICENSE file](LICENSE) for the deed. 

Note [Citation](#citation) below for attribution.


## Citation
This profile is implemented by [SURROUND Australia](https://surroundaustralia.com) to allow for data validation within the [Loc-I Project](https://www.ga.gov.au/locationindex) which is managed by [CSIRO](https://www.csiro.au) and [Geoscience Australia](https://www.ga.gov.au) .

To cite this profile, please use the following (formulated in [BibTex](http://www.bibtex.org/)):

```
@software{loci-dataset-profile,
  author = {{SURROUND Australia Pty Ltd}},
  publisher = {{Geoscience Australia}},
  title = {{Loc-I Data Profile}},
  version = {1.0},
  date = {2021},
  publisher = {{SURROUND Australia Pty Ltd}},
  url = {https://linked.data.gov.au/def/loci-dp}
}
``` 


## Contact
*publisher:*  
![](style/SURROUND-logo-100.png)  
**SURROUND Australia Pty. Ltd.**  
<https://surroundaustralia.com>  

*creator:*  
**Dr Nicholas J. Car**  
*Data Systems Architect*  
SURROUND Australia Pty. Ltd.  
<nicholas.car@surroudaustralia.com>  
<https://orcid.org/0000-0002-8742-7730>
