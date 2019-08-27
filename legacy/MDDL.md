# MDDL: The Math Data Description Language and MathHub data hosting. 

The MDDL allows mathematical data set creators to describe the meaning of mathematical objects in a data set and their database encoding declaratively and then generate data tables, user interfaces, and update facilities from them. MDDL uses 
- **object theories** that specify the mathematical types of objects
- **data base theories** that specify database types, 
- **codecs** (encoders/decode pairs) that mediate between them, and finally
- **schema theories** that bind all of them together, and provide metadata-based hints for infrastruture generation. 

All of these are regular flexiformal theories, that can make use of the existing MathHub libraries. Consequently, a [[mathematical data colletions|datacollections]] are regular [[MathHub Library|libraries]] with MDDL schema theories. 
- **MDDL archives** for the schema theories. The main one is usually just called `mddl`.
- **VT archives** for the virtual theories generated from the `mddl` archive, the main one is usually called `vt`   
 
An example of a MDDL-based schema collection can be seen in MathHub ([MDDL](https://gl.mathhub.info/symmetric-objects/mddl), [VT](https://gl.mathhub.info/symmetric-objects/vt), and the [generated data collection _Symmetric Objects_](https://mathhub.info/library/group?id=symmetric-objects))