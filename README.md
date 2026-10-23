# zotero-bibs
Bibliography synchronization from Zotero to Github to Overleaf for LaTeX projects.

This repository stores BibTeX bibliography files for LaTeX projects. References are managed in Zotero, automatically exported using Better BibTeX, and synchronized with Overleaf through GitHub. The repository is for all bib files, not just one project.

### Configure Zotero
1. Make sure [Better BibTeX](https://retorque.re/zotero-better-bibtex/) is installed in Zotero.
2. Create a Zotero collection for each paper or project.
3. Right-click a collection and select **Export Collection**.
4. Select **Better BibTeX** as the export format.
5. Check **Keep updated**.
6. Save the file in the local GitHub repository (e.g., `references.bib`).
7. Repeat for additional collections.

### Upload Bibliographies to GitHub
1. Open GitHub Desktop.
2. Select the `zotero-bibs` repository.
3. Review the new `.bib` files under **Changes**.
4. Click **Commit to main**.
5. Click **Push origin**.

### Connect to Overleaf
1. Open the repository on GitHub.
2. Select the desired `.bib` file and click **Raw**.
3. Copy the URL of the new window.
4. Open the corresponding Overleaf project.
5. Import the bibliography using **File → Upload → From External URL**.
6. Add the bibliography to the LaTeX document:

```latex
\bibliography{references}
```

7. Compile the document.

## 2. Adding New References (Regular Workflow)

### In Zotero
1. Add the reference to the appropriate Zotero collection.
2. Better BibTeX automatically updates the corresponding `.bib` file.

### In GitHub Desktop
3. Open GitHub Desktop.
4. Review the updated `.bib` file under **Changes**.
5. Enter a commit message (e.g., `Update references`).
6. Click **Commit to main**.
7. Click **Push origin**.

### In Overleaf
8. Open the Overleaf project.
9. Refresh the imported `.bib` file to retrieve the latest references.
10. Cite the reference using its Better BibTeX citation key:

```latex
\citet{merchant2001}
\citep{merchant2001}
```

11. Recompile the document.

## Important Notes

- Always add and edit references in Zotero, not in the exported `.bib` files.
- **Automatic local updates:** Better BibTeX updates exported files when their Zotero collections change.
- **Manual GitHub synchronization:** GitHub Desktop requires committing and pushing changes.
  -- Will try to make this automatic soon.  
- **Overleaf updates:** Refresh the imported bibliography after pushing changes to GitHub.
- **Privacy:** Bibliography metadata in a public GitHub repository is publicly accessible.

## 5. Workflow Summary

**Zotero → Better BibTeX → GitHub Desktop → GitHub → Overleaf**

1. Add reference to Zotero.
2. Better BibTeX updates `.bib` automatically.
3. Commit and push in GitHub Desktop.
4. Refresh the bibliography in Overleaf.
5. Cite and compile.

