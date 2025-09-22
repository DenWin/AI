# Apply/Use Policy

## 🎯 Purpose

Load and activate external policy sets from a Git repository.
Both `Apply Policy` and `Use Policy` commands are supported.
By default, only reload policies when the index shows a newer timestamp.
Optionally, reload all policies regardless of timestamps.

## ⌨️ Input

* **Command**:

  * `Apply Policy <name>` or `Use Policy <name>` → normal mode (reload only if updated).
  * `Apply Policy <name> reload all` or `Use Policy <name> reload all` → force reload all policies.
* **Repository root**: Fixed known base path to indices.
* **Index file**: `<base-path>/<name>-index.csv` with comma-separated entries.

## 📄 Index File Format

```
# date,url
YYYY-MM-DD,<policy-url>
```

## ⚙️ Behavior

1. Parse the command.
2. Locate the `<name>-index.csv`.
3. For each entry:

   * If mode = normal: reload only if date is newer than last loaded.
   * If mode = reload all: reload every listed policy, regardless of date.
4. Activate the loaded policies.
5. Keep them active until replaced or reset.

## 📤 Output

* Silent confirmation of load.
* Optionally list skipped items with `<!-- SKIPPED: unchanged YYYY-MM-DD -->` in normal mode.

## 🚫 Constraints

* Always go through the index.
* Never assume rules not listed.
* Policies remain active until another `Apply Policy` / `Use Policy` or `Reset Policies`.

## 💡 Example

**Command:**

```
Apply Policy SQL
Use Policy SQL
```

→ Only reload policies with newer dates.

**Command:**

```
Apply Policy SQL reload all
Use Policy SQL reload all
```

→ Reload every SQL policy in the index, even if dates are unchanged.
