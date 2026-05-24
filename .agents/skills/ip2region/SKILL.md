```markdown
# ip2region Development Patterns

> Auto-generated skill from repository analysis

## Overview

This skill provides guidance for contributing to the `ip2region` project, a high-performance IP address to region database library. The repository is primarily Java-based but supports multiple language bindings (e.g., C#, Golang, Python, Node.js, PHP). It covers coding conventions, file organization, and common workflows such as adding new language bindings, updating the IP database, fixing or improving bindings, updating documentation, and merging external contributions.

## Coding Conventions

- **File Naming:**  
  Use PascalCase for class and main implementation files.  
  _Example:_  
  ```
  Ip2Region.java
  TestSearcher.java
  ```

- **Import Style:**  
  Use relative imports within language bindings.  
  _Example (Java):_  
  ```java
  import ip2region.Ip2Region;
  ```

- **Export Style:**  
  Use named exports (as appropriate for the language).  
  _Example (Java):_  
  ```java
  public class Ip2Region { ... }
  ```

- **Directory Structure:**  
  - Language bindings are placed under `binding/<language>/`
  - Core data files are in the `data/` directory
  - Documentation is in `README.md` files at both the root and per-binding level

## Workflows

### Add New Language Binding
**Trigger:** When adding support for a new programming language (e.g., C#, Golang, Python3)  
**Command:** `/add-language-binding`

1. Create a new directory under `binding/<language>/`
2. Add core implementation files (e.g., `ip2Region.*`)
3. Add test/example files (e.g., `testSearcher.*`, `main.*`, `Program.cs`)
4. Add or update `README.md` for the new binding
5. Update the top-level `README.md` to mention the new binding

_Example:_
```
binding/csharp/ip2Region.cs
binding/csharp/Program.cs
binding/csharp/README.md
```

### Update IP Database
**Trigger:** When updating the IP region data to the latest version  
**Command:** `/update-ip-database`

1. Replace `data/ip.merge.txt` with the new version
2. Replace `data/ip2region.db` with the new version
3. Commit with a message referencing the new data version

_Example commit message:_
```
Update ip2region.db to 2024-06 release
```

### Fix or Improve Language Binding
**Trigger:** When fixing bugs, improving, or refactoring an existing language binding  
**Command:** `/fix-binding`

1. Edit implementation file(s) for the binding (e.g., `ip2region.js`, `ip2Region.py`, `Ip2Region.class.php`, `ip2Region.go`)
2. Edit or add test/example files (e.g., `testSearcher.*`, `ip2region.spec.js`, `ip2Region_test.go`)
3. Update `README.md` for the binding if needed

_Example:_
```
binding/python/ip2Region.py
binding/python/testSearcher.py
binding/python/README.md
```

### Update or Fix README
**Trigger:** When fixing typos, adding instructions, or clarifying documentation  
**Command:** `/update-readme`

1. Edit `README.md` in the root or `binding/<language>/README.md`
2. Commit with a message referencing documentation or README

_Example commit message:_
```
Fix typo in Python binding README
```

### Merge External Contribution
**Trigger:** When integrating changes from a fork or external contributor  
**Command:** `/merge-contribution`

1. Merge the branch or pull request
2. Update relevant files (implementation, tests, docs)
3. Commit with a merge message referencing the contributor

_Example commit message:_
```
Merge PR #42 from @contributor: Add Rust binding
```

## Testing Patterns

- **Framework:** Not explicitly detected; varies by language binding.
- **File Pattern:** Test files typically follow the pattern `*Test.cs` (for C#), or similar for other languages (e.g., `testSearcher.py`, `ip2region.spec.js`).
- **Location:** Test files are placed alongside or within the language binding directory.

_Example (C#):_
```
binding/csharp/Ip2RegionTest.cs
```

_Example (Python):_
```
binding/python/testSearcher.py
```

## Commands

| Command                | Purpose                                                      |
|------------------------|--------------------------------------------------------------|
| /add-language-binding  | Add support for a new language binding                       |
| /update-ip-database    | Update the IP region database files                          |
| /fix-binding           | Fix or improve an existing language binding                  |
| /update-readme         | Update or correct documentation in README files              |
| /merge-contribution    | Merge a pull request or branch from an external contributor  |
```