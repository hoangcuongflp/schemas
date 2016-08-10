## MAEC JSON Notes

* Currently no notion of namespaces
* The points at which MAEC schemas reference cybox (or other external) schemas are marked with (broken) json references. Essentially in places where there is a reference to an external, undefined schemas I have the following tag "{"$ref":"REFERENCE PLACEHOLDER FOR <name of external schema>"}"
* The groupings of MAEC schema types into the observed files does not follow a formal grouping scheme
(i.e. the types were grouped by what seems to be closely related). It is also assumed that all these json files will eventually be merged to one. This is the reason why all json schema references are defined under the "definitions" object within each file.
* Currently, some of the MAEC core schema reference MAEC vocab types. These vocab types were changed to json enum types within their parent objects(for now) instead of an auxiliary vocab.

### Changes from XML

* All property names are lowercased
    * E.g., "engine_version" instead of "Engine_Version"
* List types are not carried over, since they can be expressed as a property of type list with a restriction on its contents
    * E.g., no need for BehaviorListType