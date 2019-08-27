# Links

* Demos: [Joe](http://joe.discretezoo.xyz), [Jane](http://jane.discretezoo.xyz), [Mathilde](http://mathilde.discretezoo.xyz)
* [Generator code](https://github.com/UniFormal/MMT/tree/devel/src/mmt-lf/src/info/kwarc/mmt/sql)
* [Schema independent code](https://github.com/DiscreteZOO/Web-MBGen-Generated)

# Setup a schema declaration and run MBGen

1. Setup [MMT](https://uniformal.github.io/doc/setup/),
2. Initialize a new archive with a dependency on `MDDL`,
3. Write the schema theory or theories (described [here](https://kwarc.info/people/mkohlhase/submit/cicm19-MDH.pdf)),
4. Make sure your main schema theory has the `schemaGroup` metatag: `meta ?MDDL?schemaGroup "MySchemaGroupName"`
5. Prepare the template directory, for the example, call it `MBGen`.
    - Make a subfolder `frontend` and clone the [frontend repo](https://github.com/MathHubInfo/mdh-frontend) into it and
    - Make a subfolder `backend` and clone the [backend repo](https://github.com/MathHubInfo/mdh-backend) into it.
6. Create a file `settings.txt` in the folder `MBGen` with the following contents:
```
path/to/archive
MySchemaGroupName
jdbc:postgresql://localhost:5432/mydatabase
username
password
prefix
```
7. run MBGen

Notes on the settings file, line by line:
1. use the archive path you used to initialize it,
2. the name of the schema group should be the same as in your theory,
3. the jdbc url (you might need to create the database first),
4. database user,
5. password for the user,
6. a prefix you want to use for the tables (`MBGEN` is default).

Parts of this pipeline are still under heavy development

# Notes

1. New filters should probably wait until after the move to Django.

# Development

1. Project level issues in the [project board](https://github.com/orgs/MathHubInfo/projects/1)