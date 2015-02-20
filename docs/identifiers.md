# Identifiers
All objects in the Kubernetes REST API are identified by a Name and a UID.

## Names
Names are user-provided.  Only one object of a given kind can have a given name at a time.  But if you delete an object, you can make a new object with the same name.  Names are the used to refer to an object in a resource URL, such as `/api/v1beta3/pods/some.name`.   Names may be up to maximum length of 253 characters and consist of lower case alphanumeric characters, `-`, and `.`.  See the [identifiers design doc](design/identifiers.md) for the precise syntax rules for names.

## UIDs
UID are generated by Kubernetes.  Every object created over the whole lifetime of a Kubernetes cluster has a distinct UID.