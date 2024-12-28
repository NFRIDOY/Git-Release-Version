# Git-Release-Version using CLI
Git Release Version and Naming Convention

## Releasing a version using CLI

1. Create a tag:
```bash
git tag -a v1.0.0 -m "Release version 1.0.0"
```
2. Push the tag to the remote GitLab repository:
```bash
git push origin v1.0.0
```
v MAJOR.MINOR.PATCH (e.g. v1.2.3)
e.g. 
v breaking_change.features.bugfix


## Version Naming Guide 

Version naming (also known as **versioning**) follows a systematic approach to manage and track changes to software over time. The most common version naming convention is **Semantic Versioning (SemVer)**, but other systems also exist. Here’s an overview:

## 1. Semantic Versioning (SemVer)
Semantic Versioning is a widely used convention and follows a format like:


### Components of SemVer:
1. **MAJOR**: Increased when there are breaking changes that are not backward-compatible (e.g., an API change that requires users to modify their code).
   - Example: `v2.0.0` → breaking change in how the software works.
   
2. **MINOR**: Increased when new features or functionality are added in a backward-compatible manner. It means users can upgrade without breaking existing functionality.
   - Example: `v1.2.0` → new features added, but backward-compatible.
   
3. **PATCH**: Increased when backward-compatible fixes or minor improvements (e.g., bug fixes) are made.
   - Example: `v1.0.1` → bug fixes or small tweaks.
   
### Pre-release and Build Metadata:
- **Pre-release version**: Indicated by appending a hyphen and an identifier (e.g., `v1.0.0-alpha`, `v2.0.0-beta`).
- **Build metadata**: Can be added using a plus sign (e.g., `v1.0.0+20130313144700` for a timestamp-based version).

---

## 2. Example SemVer Versions
- `v1.0.0`: Initial release, stable, no backward compatibility issues.
- `v2.0.0`: Major changes that break backward compatibility.
- `v1.1.0`: New features added, no breaking changes.
- `v1.0.1`: Patch fix, e.g., a bug or minor tweak.
- `v1.2.0-beta`: A beta version of the upcoming `v1.2.0` release.

---

## 3. Other Versioning Systems
Some projects use simpler or different systems, often based on dates or other custom schemes. Here are a few examples:

### 1. Date-based Versioning
- Uses the release date as the version (e.g., `2024.12.28`).
- Good for projects where the release cycle is closely tied to specific dates.

### 2. Sequential Versioning
- Uses an incremental number (e.g., `v1`, `v2`, `v3`, etc.) without breaking down into MAJOR, MINOR, or PATCH.
- Simple but less informative about the nature of changes between versions.

### 3. Incremental Versioning (Build Numbers)
- Versions are incremented with build numbers or release numbers (e.g., `v1.0.0-build125`).
- Often used in continuous integration/continuous deployment (CI/CD) environments.

---

## 4. Guidelines for Versioning
- **Start with `1.0.0`**: After an initial product is stable, use `v1.0.0` as the first release.
- **Incrementation**:
  - Increment the **MAJOR** version for incompatible changes.
  - Increment the **MINOR** version for adding features in a backward-compatible way.
  - Increment the **PATCH** version for bug fixes.
- **Pre-release versions**: If a version is not stable or ready for production, use pre-release identifiers like `alpha`, `beta`, or `rc` (release candidate).
  - Example: `v1.0.0-alpha`, `v1.0.0-beta`, `v1.0.0-rc1`.

---

## 5. Choosing a Versioning Scheme
When choosing a version naming system, consider the following:
- **Audience**: Do you need users to understand the nature of changes easily (SemVer)?
- **Release Cycle**: Does your release process follow a set schedule (date-based)?
- **Backward Compatibility**: Are breaking changes frequent or rare (SemVer is ideal here)?

By using a versioning system, you make it easier for users and developers to track the evolution of your software and understand what to expect with each release.
