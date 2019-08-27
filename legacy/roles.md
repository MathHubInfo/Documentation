# User Roles in MathHub

MathHub does not provide user management itself, but delegates it to the underlying [GitLab system](https://gl.mathhub.info). Therefore we concentrate on the roles users can take in the interaction with the MathHub system and discuss the necessary permissions. 

## MathHub Readers
Anyone who uses the [MathHub Portal](https://mathhub.info) is a **MathHub reader**, as the content is public, no login is necessary and permissions are needed. 

## MathHub Contributors and Curators
Anyone who contributes to a [[MathHub archive|math-archives]] **MathHub contributor**, anyone who [[pushes generated content|build-system]] (usually those who are mentioned in the "responsible" field of an archive) is a **MathHub curator**. Curators must have GIT push rights to their respective archives. Contributors usually have push rights to their archives, but can also contribute via GIT pull requests (to be merged by a curator).  
 
## MathHub Administrators
**MathHub admins** have full control over the MathHub system. In particular they have adminpermissions on the underlying [GitLab](https://gl.mathhub.info) and are authenticated to the [MathHub admin interface](http://mathhub.info/admin). MathHub admins can create new libraries, give permissions, and re-start the system and individual containers.  
