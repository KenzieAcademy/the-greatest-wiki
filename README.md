# The Greatest Wiki

The goal of this is to compile a basic site where we can point students when they run into semi-common errors that we already know the answer to -- the things that we end up repeating quarter after quarter. This shouldn't be an all-knowing compendium; we just want to have answers to basic problems (or guides to set up software) that students will encounter throughout the curriculum.

The root page is accessible at https://kenzieacademy.github.io/the-greatest-wiki/.

## Editing

Because this is a cheap and easy site that just uses github pages, there's not a whole lot of functionality (which also means there's less to worry about). Extending the site involves cloning this repo and modifying whatever you need, then pushing to master. Here's an example:

```shell script
cp docs/page.md.template docs/lang/javascript/assessment_3_common_issues.md
# Edit the file in your favorite editor
# link to the file in other pages if you want
git add .
git commit -sm "update wiki and add js info"
git push origin master
```

> Note: any time you are creating a link in the markdown, make sure that you link to the file _minus the extension_. For example: `/the-greatest-wiki/docs/lang/javascript/index`. If you include the `.md`, GitHub will show the raw markdown underneath it instead of the nice rendered page.

To edit the landing page, you'll just need to modify index.html directly.
