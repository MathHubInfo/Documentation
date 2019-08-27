# MathHub Administration

Here we document the workflows of [MathHub](http:/mathhub.info)
administrators, i.e. users who have [rights to Mathhub admin](http://mathhub.info/admin).
We assume that the admins are familiar with the [MMT system](https://uniformal.github.io/doc/) our main knowledge management system and basic [GIT](https://git-scm.com/) workflows. We will concentrate on MathHub-specific workflows here. 

### 1\. Adding a new [[MathHub Library|libraries]] or [[Data Collection|datacollections]]

Make sure that you have a well-configured MathHub Library, i.e. a group on
<http://gl.mathhub.info>
1. [make a new group](https://gl.mathhub.info/groups/new) (public, with good descriptions)
2. [make a `meta-inf` repository](https://gl.kwarc.info/projects/new) in this group with a valid `GROUP_MANIFEST.MF` file which has `title`, `teaser`, `description`, and `responsible` fields.
3.  There must be at least one valid [[math archive|math-archives]] in the group (see below)

### 2\. Adding a [[Math Archive|math-archives]] to MathHub

[make a repository](https://gl.kwarc.info/projects/new) to make it a [[valid math archive|math-archives]] you need to 
1. create a file `META-INF/MANIFEST.MF` file which has `title`, `teaser`,`description`, and `responsible` fields.
2. add a short description as a HTML paragraph (`<p>` as the top element) in `META-INF/desc.html`
3. create a `source` subdirectory. All files you will write (e.g. in MMT surface syntax or sTeX) should be here. 
4. build the archive, either via one of [our MMT IDEs](https://uniformal.github.io/doc/applications/ides.html) or from the [MMT shell](https://uniformal.github.io/doc/applications/ides.html) via `build <archive> <source>-omdoc`, where `<archive>` is the full archive name (e.g. `HelloWorld/MMT`) and `<source>` is the source format (e.g. `mmt` for MMT surface syntax or `stex` for sTeX).  MMT will generate various sister directories to `source` with generated data.
5. add, commit, and push the `content`, `relational`, and `narration` directories to the archive.
   From a shell: 
   ```
   git add content relational narration
   git commit -am're-generated'
   git push
   ```
6. Wait for MathHub to notice the push (you need to talk to a MathHub admin for that). 

### 3. [posting news](news)
