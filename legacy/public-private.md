# Public/Restricted Content and Interfaces in MathHub

MathHub encourages the development of a public domain of flexiformal mathematics, but acknowledges the need for private development practices. Therefore it supports both at every level.

## Public/Restricted Content
As MathHub delegates all user/permission management to the underlying [GitLab](https://gl.mathhub.info), we adopt its three visibility levels `public`, `internal` (visible to all authenticated users) and `private` (visible to restricted set of users); we call the latter two categories **restricted content**. [MathHub.info](https://mathhub.info) only sees public content, where as a [local MathHub working copy](lmhwc) can contain restricted content (to which the user has access). 

## Public/Private Portal 
As the MathHub system uses a [container-based architecture](architecture), it is very easy to [configure and deploy](https://github.com/MathHubInfo/MathHub) (e.g. on `localhost:8080` or an intranet) using a [local MathHub working copy](lmhwc) as the basis. We call this a **private MathHub**. The documentation on this wiki is mostly about the public portal [MathHub.info](https://mathhub.info), but applies equally to private MathHubs. The main use case for a private MathHub is full support content development with restricted content. This setup usually links the [local MathHub working copy](lmhwc) into the MMT container to avoid duplication of content and ensure direct compatibility with [local editing workflows](lmh-workflows). 

## MathHub Light (to be completed) 
An alternative to a private MathHub is a MathHub setup that only uses the frontend component - in particular it re-uses the system MMT process and the [local MathHub working copy](lmhwc). This is the most lightweight and flexible setup for MathHub -- we call this **MathHub Light**. It allows co-developing MMT, exporters, and services with the content. 

## Public/Restricted Services
I am not sure what we can/need-to say here. 