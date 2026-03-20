# Programming 3 — Desktop labs & exam-style solutions (2024)

Teaching and practice materials for **Programming 3** (*Programiranje 3*): C# **Windows Forms** desktop apps built on a shared academic template (the **FIT.*** projects). This repository includes the **Template 2024** starter and several **exam-style workshop solutions** from 2024.

---

## Repository layout

| Path | Description |
|------|-------------|
| [`Template 2024/`](Template%202024/) | Baseline solution: layered projects, main form `frmPocetna`, RDLC reports, SQLite database wiring. |
| [`Workshops/`](Workshops/) | Self-contained solutions per session — full code for practice and comparison. |

### Workshop folders (exam sets)

- **ISPITNI FEB-1-2024**
- **ISPITNI FEB-22-2024**
- **ISPITNI JUL-04-2024**
- **ISPITNI DEC-23-2024**

Each folder contains its own `FIT.sln`. There is **no** single root solution for the entire repo.

---

## Tech stack

- **.NET 6** (`net6.0-windows` for WinForms)
- **Windows Forms**
- **Entity Framework Core 6** with **SQLite** (`DLWMS.db`)
- **ReportViewer** (RDLC) via **ReportViewerCore.WinForms**

### Typical solution structure

1. **FIT.Data** — entities and DTOs  
2. **FIT.Infrastructure** — EF Core `DbContext` and data access (`DLWMSDbContext`)  
3. **FIT.WinForms** — UI, forms, reports  

---

## Prerequisites

- **Windows** (required for WinForms + `net6.0-windows`)
- [.NET 6 SDK](https://dotnet.microsoft.com/download/dotnet/6.0)
- **Visual Studio 2022** with the *.NET desktop development* workload (recommended), or another IDE that handles SDK-style WinForms projects well

---

## How to run

1. Open the `FIT.sln` you need (e.g. `Template 2024/FIT.sln` or any `Workshops/.../FIT.sln`).
2. Check **FIT.WinForms/App.config**: the `DLWMSBaza` connection string must point to a valid **SQLite** file (the template often uses a relative path to `DLWMS.db`).
3. In Visual Studio: **Build → Rebuild Solution**, then run with **FIT.WinForms** as the startup project if it is not already.

> **Tip:** After a fresh clone or copy, **Rebuild** the whole solution before the first run — this avoids many issues with generated resources and project references.

---

## About suffixes like `IB180079` in code

Names such as **IB180079** on forms/classes are **student/index placeholders from exam briefs**, not part of the framework. Replace them with your own index when doing coursework, per your course rules.

---

## License & use

Intended for **educational** use (labs, tutoring, exam prep). Follow your faculty’s rules for graded work and attribution.

---

*PRIII desktop (C#) — academic year ~2024.*
