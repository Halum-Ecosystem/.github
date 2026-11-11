# Contributing to Halum

Thank you for your interest in Halum. Contributions from every background are
welcome: medicine, engineering, design, writing, or simple curiosity.

Please read our [Code of Conduct](https://github.com/Halum-Ecosystem/.github/blob/main/CODE_OF_CONDUCT.md)
and [Safety rules](https://github.com/Halum-Ecosystem/halum-ecosystem/blob/main/Safety.md)
before contributing.

## Ways to contribute

You don't need to write code to help:

- **Share ideas and feedback** on projects in progress.
- **Bring a clinical perspective.** Tell us what a device needs to do in real
  life, and what would make it useful to patients and clinicians.
- **Build and test.** Follow a build guide and report what worked and what
  didn't.
- **Improve documentation:** fix unclear instructions, add diagrams, correct
  mistakes.
- **Write code or firmware,** or improve hardware designs.
- **Show your own work** in Discussions, even if it isn't a Halum project.

## Where things go

| You want to... | Go to |
|---|---|
| Ask a question, share an idea, show your work | [Discussions](https://github.com/Halum-Ecosystem/halum-ecosystem/discussions) in the hub |
| Report a bug or suggest a specific change to a project | Issues in that project's repository |
| Raise something about Halum as a whole | [Issues](https://github.com/Halum-Ecosystem/halum-ecosystem/issues) in the hub |
| Report a safety problem privately | The contact in [Safety.md](https://github.com/Halum-Ecosystem/halum-ecosystem/blob/main/Safety.md) |

## How to submit a change

Halum uses the standard GitHub workflow: you make changes in your own copy
of a repository (a *fork*), then ask for them to be added to Halum through a
*pull request*. You never need write access to Halum's repositories.

Work in the repository of the project you want to change, for example
`halum-prosthetic-hand`, not in the `halum-ecosystem` hub, unless your change
is about Halum as a whole.

### Before you start

For anything bigger than a typo, open an issue first, or comment on an
existing one, saying what you plan to do. This avoids two people doing the
same work, and lets us agree on the approach before you spend time on it.

### Small changes: edit on GitHub

For a typo or a small documentation fix, open the file on GitHub and click
the pencil icon. GitHub creates your fork and the pull request for you.

### Everything else: work on your computer

1. **Fork the repository.** Click **Fork** at the top right of the project's
   GitHub page. This creates your own copy under your account.

2. **Download your fork:**
   ```
   git clone https://github.com/<your-username>/<repo>.git
   cd <repo>
   ```

3. **Link it to the original Halum repository**, so you can keep up to date:
   ```
   git remote add upstream https://github.com/Halum-Ecosystem/<repo>.git
   ```
   `origin` is now your fork, and `upstream` is Halum's repository.

4. **Start a branch from the latest version.** Use one branch per change:
   ```
   git switch main
   git pull upstream main
   git switch -c fix/short-description
   ```

5. **Make your changes and commit them:**
   ```
   git add <files you changed>
5. **Make your changes and commit them:**
   ```
   git add <files you changed>
   git commit -m "Short description of what changed"
   ```

6. **Upload the branch to your fork:**
   ```
   git push -u origin fix/short-description
   ```

7. **Open a pull request.** On your fork's GitHub page, click **Compare &
   pull request**. Check that it targets `Halum-Ecosystem/<repo>` and the
   `main` branch, then fill in the template that appears.

8. **Respond to review.** A maintainer may ask for changes. Make them on the
   same branch and push again. The pull request updates automatically, so
   there is no need to open a new one.

### After your pull request is merged

Bring your fork up to date before starting your next change:
```
git switch main
git pull upstream main
git push origin main
git branch -d fix/short-description
```
You can also click **Sync fork** on your fork's GitHub page.

## What makes a good pull request

- **One change per pull request.** Small pull requests are reviewed faster.
- **A clear title**, such as "Add low-pass filter to EMG envelope", not
  "Update files".
- **An explanation** of what changed, why, and how you tested it.
- **A link to the related issue**, by writing `Closes #12` in the description.
- **Updated documentation** if your change affects how something is built or
  used.

We try to give a first response at least within a week or two. If you haven't heard back,
feel free to leave a comment on the pull request.

## Safety-related changes

Pull requests that change hardware, wiring, electronics, firmware or motor
control must explain:

- what could go wrong if the change has a fault,
- what happens if the signal or software fails, and
- how the change was tested, and on what.

These pull requests get a more careful review and may take longer. Never test
changes on a person in a way that breaks the
[Safety rules](https://github.com/Halum-Ecosystem/halum-ecosystem/blob/main/Safety.md).

## Licensing your contribution

By submitting a pull request, you agree that your contribution is shared
under the licence of the repository, or the part of it, that you are
changing. Each project's README says which licence applies where.

Only submit work you have the right to share. Do not copy designs, code or
files from other projects unless their licence allows it, and say where they
came from in your pull request.

## Getting help

Stuck, or not sure where to start? Ask in
[Discussions](https://github.com/Halum-Ecosystem/halum-ecosystem/discussions).
No question is too basic.

pull_request_template.md

The text inside <!-- --> is hidden on GitHub, so contributors see the guidance while editing, but it doesn't show in the finished pull request.

## What does this change?
<!-- A short summary of what you changed. -->

## Why?
<!-- The problem this solves, or the improvement it makes. -->

Closes #<!-- issue number, if there is one -->

## How was it tested?
<!-- What you did to check it works, and on what (simulator, hardware,
operating system). -->

## Type of change
- [ ] Documentation
- [ ] Software or code
- [ ] Firmware
- [ ] Hardware design (CAD, wiring, electronics)

## Safety impact
<!-- Required if you changed hardware, wiring, electronics, firmware or motor
control. What could go wrong if this change has a fault? What happens if the
signal or software fails? Otherwise write "None". -->

## Checklist
- [ ] I have read the contributing guide.
- [ ] This pull request makes one focused change.
- [ ] I have the right to share this work, and it can be shared under this
      repository's licence.
- [ ] It contains no patient data or personal information.
- [ ] I have updated documentation where needed.

Two lines to decide on:
- "We try to give a first response within a week." Make sure it's a promise you can keep, and change the timeframe if not. Being reliable matters more than being fast.
- The licensing section stops anyone from contributing something like the InMoov files under your licence. It's not legal advice, but it's the standard approach for small projects.
