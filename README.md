Theorem Proving in Lean
-----------------------

Built using Sphinx and restructured text.

# How to build

Make sure you have Lean installed. Use
```
leanproject get git@github.com:leanprover/theorem_proving_in_lean.git
```
to clone the repository and install the `mathlib` library. 

The build requires python 3, xelatex, latexmk and some OTF fonts.

On Ubuntu, you may install these dependencies by running

```bash
sudo apt install python3-venv texlive-xetex latexmk fonts-freefont-otf
```

```bash
make install-deps
make html
make latexpdf
PAPER_SIZE=a5paper make latexpdf  # for e-readers
```

The call to `make install-deps` is only required the first time, and only if you want to use the bundled version of Sphinx and Pygments with improved syntax highlighting for Lean.

# How to test the Lean code snippets

```
make leantest
```

# How to deploy

```
./deploy.sh leanprover theorem_proving_in_lean
```

# How to contribute

Pull requests with corrections are welcome. Please follow our `commit conventions <https://github.com/leanprover/lean/blob/master/doc/commit_convention.md>`. If you have questions about whether a change will be considered helpful, please contact Jeremy Avigad, ``avigad@cmu.edu``.
