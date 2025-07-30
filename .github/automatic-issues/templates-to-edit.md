
[Follow the instructions here in ottrproject.org](https://www.ottrproject.org/writing_content_courses.html) for details on how to start editing your OTTR course

The following files need to be edited to get this new course started!

### Files that need edited upon creating a new course.

- [ ] `README.md` - Fill in all the `{ }`.
- [ ] `index.Rmd` - `title:` should be updated.
- [ ] `index.Rmd` - `description:` should be updated (this is what is displayed when you share a link to the book/course)
- [ ] `01-intro.Rmd` - replace the information there with information pertinent to this new course.
- [ ] `02-chapter_of_course.Rmd` - This Rmd has examples of how to set things up, if you don't need it as a reference, it can be deleted.

### License:
Your new repository will be set up with a CC-BY 4.0 License.  If you wish to use a different license and/or to include material that is distributed under a different license, you should:

- [ ] Update `LICENSE.md`
- [ ] Update `footer.html`

### Files that need to be edited upon adding each new chapter (including upon creating a new course):

- [ ] `_bookdown.yml` - The list of Rmd files that need to be rendered needs to be updated. See [instructions](https://www.ottrproject.org/course_publishing.html#publishing-with-bookdown).
- [ ] `book.bib` - any citations need to be added. See [instructions](https://www.ottrproject.org/more_features.html#citing-sources).

### Files that need to be edited upon adding new packages that the book's code uses:

- `docker/Dockerfile` needs to have the new package added so it will be installed. See [instructions](https://www.ottrproject.org/customize-docker.html).
- The code chunk in `index.Rmd` should be edited to add the new package.
