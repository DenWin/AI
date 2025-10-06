# Apply/Use Policy – Human Readable

## 🎯 Executive Summary

This command loads policies from your repository.
Normally it reloads only updated ones, but you can also force a full reload.

## 📌 Purpose

Make sure the system always follows the latest version of your rules without reloading unchanged files.
Provide an option to reload everything if a full refresh is needed.

## ⚙️ How It Works

1. You issue: `Apply Policy <name>` or `Use Policy <name>`.

   * The system opens `<name>-index.csv`.
   * Each entry has a date and a URL.
   * Reload only if the date is newer than the last load.

2. You issue: `Apply Policy <name> reload all` or `Use Policy <name> reload all`.

   * The same index is read.
   * **Every policy** is reloaded, regardless of date.

3. All active policies remain until you change them or reset.

## 💡 Example

* Index line: `2025-09-15,https://github.com/.../sql-performance.yml`
* Normal load: If last load = `2025-09-15`, skip.
* Reload all: Always reload, even with same date.

## 📚 Usage Scenarios

* Normal mode to stay efficient and only pull updates.
* Reload all to ensure a clean reset of the active rules.
* Switch between SQL, Python, or documentation rules without duplication.

## 🚫 Notes

* Index controls everything—no policy is loaded outside it.
* `Reset Policies` clears all active sets.
* Reload all is the only way to ignore timestamps.
