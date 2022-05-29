# uri.semic.eu-thema

The branch `example` exists just for demonstration purpose. 
The content in this branch is realistic, i.e. it contains a copy of real data, but cannot be considered to be in any sense an official publication of the data specifications.


In SEMIC a Core Vocabulary is a mixture between what the OSLO toolchain determines as a vocabulary and and an application profile.
In the OSLO toolchain setting a vocabulary consists of an html document and RDF representation capturing the terms under consideration.
A graphical representation, SHACL template or JSON-LD context file are considered part of the notion of an application profile.
A SEMIC Core Vocabulary has the same intend as the OSLO vocabulary, but also wants to share (permissive) representations associated with an application profile.

Instead of a introducing a new documenttype 'Core Vocabulary' and adapting the toolchain processing to handle this type, it has been decided to (for now) exploit the existing notions as is.
That means for a Core Vocabulary the same data specification UML file will be used to create an application profile configuration aswell an vocabulary configuration. 
This decision can be revised in the future.



