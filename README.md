# PSTU MS Thesis LaTeX Template

This is a LaTeX template designed specifically for Master of Science (MS) thesis reports at the **Department of Computer Science and Information Technology (CSIT)**, **Patuakhali Science and Technology University (PSTU)**. It automatically formats the title page, approval page, declaration, and other front matter according to the university's official postgraduate guidelines (please see the attached [rulebook.pdf](rulebook.pdf) for detailed rules).

## Features

* **Automated Front Matter:** Generates Title, Approval, Declaration, and Acknowledgement pages with correct formatting.
* **Separation of Concerns:** Author, supervisor, and thesis details are stored in modular `.txt` files inside the `parameters/` directory. No need to modify the complex `.sty` file!
* **APA Reference Style:** Pre-configured with APA style referencing using `biblatex` and `biber`.
* **Bangla Support:** Easy integration for writing in Bangla (via the `usebangla` package) if required.
* **Toggleable Lists:** Easily suppress the List of Figures, List of Tables, or List of Algorithms by commenting/uncommenting a single line in `main.tex`.

## Directory Structure

* `main.tex`: The main LaTeX document. This is where you include your chapters.
* `pstucsepgthesis.sty`: The core style file defining the layout and commands. (You generally do not need to edit this).
* `pstucsepgthesis.bib`: The bibliography file for your references.
* `parameters/`: Contains text files to easily update thesis metadata:
    * `thesistitle.txt`: Your thesis title.
    * `thesisdate.txt`: The date of submission (e.g., Month Year).
    * `students.txt`: Student name, Roll/ID, and Registration Number.
    * `supervisor.txt`: Supervisor's Name and Designation.
    * `cosupervisor.txt`: Co-Supervisor's Name and Designation.
    * `chairman.txt`: Chairman's Name and Designation.
* `inputs/`: Contains text files for standard front matter text:
    * `abstract.tex`: Your thesis abstract.
    * `acknowledgement.tex`: Your acknowledgements.
* `figures/`: Directory to store your images and diagrams (includes the official PSTU logo).
* `chapterX.tex`: Individual files for your thesis chapters.

## How to Use

1. **Clone or Download** this repository.
2. **Update Metadata:** Open the files in the `parameters/` folder and replace the placeholder text with your actual details (Name, Roll, Supervisor names, etc.). Make sure to follow the existing comma-separated format if applicable (as used by the `datatool` package for names and designations).
3. **Write Front Matter:** Edit `inputs/abstract.tex` and `inputs/acknowledgement.tex` with your content.
4. **Write Chapters:** Add your thesis content into `chapter1.tex`, `chapter2.tex`, etc.
5. **Manage References:** Add your citations to `pstucsepgthesis.bib`. 
6. **Compile:** Compile `main.tex` using your preferred LaTeX editor (e.g., TeXstudio, Overleaf, or VS Code with LaTeX Workshop). Ensure you compile with **biber** for the bibliography to work correctly.
    * Recommended build sequence: `pdflatex` -> `biber` -> `pdflatex` -> `pdflatex`

## Customization

* **Bangla Text:** To write in Bangla, uncomment `\usepackage{usebangla}` in `main.tex` (requires XeLaTeX or LuaLaTeX depending on your font setup).
* **Lists:** To remove the List of Figures or List of Tables, locate the `\suppresslistoffigures` or `\suppresslistoftables` commands in `main.tex` and uncomment them.

## Requirements

* A standard TeX distribution (TeX Live, MiKTeX, MacTeX).
* `datatool` package (used for reading the parameter files).
* `biblatex` and `biber` (for APA referencing).

## License

This template is open-source and free to use for any PSTU CSIT postgraduate student.
