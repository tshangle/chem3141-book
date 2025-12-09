# Markdown Files

Whether you write your book's content in Jupyter Notebooks (`.ipynb`) or
in regular markdown files (`.md`), you'll write in the same flavor of markdown
called **MyST Markdown**.
This is a simple file to help you get started and show off some syntax.

## What is MyST?

MyST stands for "Markedly Structured Text". It
is a slight variation on a flavor of markdown called "CommonMark" markdown,
with small syntax extensions to allow you to write **roles** and **directives**
in the Sphinx ecosystem.

For more about MyST, see [the MyST Markdown Overview](https://jupyterbook.org/content/myst.html).

## Sample Roles and Directives

Roles and directives are two of the most powerful tools in Jupyter Book. They
are like functions, but written in a markup language. They both
serve a similar purpose, but **roles are written in one line**, whereas
**directives span many lines**. They both accept different kinds of inputs,
and what they do with those inputs depends on the specific role or directive
that is being called.

Here is a "note" directive:

```{note}
Here is a note
```

It will be rendered in a special box when you build your book.

Here is an inline directive to refer to a document: {doc}`markdown-notebooks`.


## Citations

You can also cite references that are stored in a `bibtex` file. For example,
the following syntax: `` {cite}`holdgraf_evidence_2014` `` will render like
this: {cite}`holdgraf_evidence_2014`.

Moreover, you can insert a bibliography into your page with this syntax:
The `{bibliography}` directive must be used for all the `{cite}` roles to
render properly.
For example, if the references for your book are stored in `references.bib`,
then the bibliography is inserted with:

```{bibliography}
```

## Learn more

This is just a simple starter to get you started.
You can learn a lot more at [jupyterbook.org](https://jupyterbook.org).

## Workflow for Pull Requests

## 1. Prepare Your Notebook
1. Finish writing your Jupyter notebook (`.ipynb`).
2. Give it a descriptive filename  
   *Example: `computational_set_05.ipynb`*.

## 2. Place the Notebook in the Correct Folder
On your computer, locate your local clone of your **fork** of the repository.  
For a computational notebook, move it into the folder `chem3141-book/conent/computational_sets/


Ensure the notebook is inside this directory.

---

## 3. Open GitHub Desktop
1. Launch **GitHub Desktop**.
2. Confirm that the **Current Repository** is your fork of `chem3141-book`.

---

## 4. Review Changes
GitHub Desktop will show the new notebook under **Changes**.

- Make sure your notebook file is checked in the list.

---

## 5. Write a Commit Message
In the bottom-left panel:

- **Summary:**  
  `Add new computational set notebook`

- **Description (optional):**  
  Brief explanation of what the notebook contains.

---

## 6. Commit the Changes
Click:

**Commit to main**  
(or whichever branch you are working on)

---

## 7. Push Changes to Your Fork on GitHub
Click:

**Push origin**

This uploads your changes to your GitHub fork.

---

## 8. Open a Pull Request
GitHub Desktop may show a banner with **Create Pull Request** — click it.

If not:

1. Go to your fork on GitHub.com  
2. Click **Compare & pull request**

---

## 9. Fill Out the Pull Request Form
- **Title:**  
  `Add new notebook to computational_sets folder`

- **Description:**  
  Briefly describe the notebook and why you're adding it.

Check that:
- **base repository:** the main `chem3141-book`  
- **base branch:** `main`  
- **compare branch:** your fork’s branch (usually `main`)

---

## 10. Submit the Pull Request
Click:

**Create pull request**

Your submission is now ready for review by the course maintainers!

---

## 🎉 You’re Done!
Once the pull request is reviewed and merged, your notebook will become part of the official course materials.



## Workflow for making edits

1.  Make edits within the main branch
2.  build jupyter book with `jupyter-book build .` from within the top-level directory of the main branch
3.  Commit changes to main branch from github desktop
4.  Push the `_build` folder to gh-pages branch using `ghp-import -n -p -f _build/html`
5. Check the build remotely by going to the gh-pages branch, push on the "Actions" button, and follow the link after the deploy action finalizes.  The page should render at https://foleylab.github.io/chem3141-book/intro.html
