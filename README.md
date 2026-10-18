<div align="center">

# ⚒️ ForgeCAD

### פרמטרי, קוד פתוח, לא מקוון — CAD חופשי לכולם

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![OCCT: LGPL 2.1](https://img.shields.io/badge/OCCT-LGPL%202.1-green.svg)](https://www.opencascade.com/)
[![Platform: Windows x64](https://img.shields.io/badge/Platform-Windows%20x64-lightgrey.svg)]()
[![.NET 8](https://img.shields.io/badge/.NET-8-purple.svg)]()
[![Status: Pre-Alpha](https://img.shields.io/badge/Status-Pre--Alpha-orange.svg)]()

**תוכנת CAD פרמטרית חופשית, קלת משקל ומקוונת לחלוטין — אלטרנטיבה פתוחה ל-SOLIDWORKS.**

[תכונות](#-תכונות-עיקריות) • [התקנה](#-התקנה) • [בנייה](#-בנייה-ממקור) • [רודמאפ](#-רודמאפ) • [תרומה](#-תרומה)

</div>

---

## 📖 אודות הפרויקט

**ForgeCAD** היא תוכנת CAD (Computer-Aided Design) פרמטרית בקוד פתוח, המיועדת לסביבת Windows x64. היא מספקת חוויית מידול תלת-ממדית מקצועית בדומה ל-SOLIDWORKS — אך ללא עלות, ללא רישום, ללא טלמטריה, וללא כל תלות בחיבור לאינטרנט.

הפרויקט נבנה מאפס על גבי ליבת הגיאומטריה **Open CASCADE Technology (OCCT)** — הסטנדרט דה-פקטו לתעשיית ה-CAD בקוד פתוח — תוך שימוש בממשק משתמש מודרני מבוסס **WPF** ו-**MaterialDesignInXAML**.

> **החזון:** לספק לכל מהנדס, סטודנט, או חובב יצירה — כלי CAD מקצועי, חופשי, פרטי ומקומי — בלי מנויים, בלי ענן, ובלי הגבלות.

---

## ✨ תכונות עיקריות

### 🧩 מידול מוצק פרמטרי
- **Sketcher** מלא עם אילוצים גיאומטריים ומידות
- **Extrude, Revolve, Sweep, Loft, Boundary** — פעולות בסיס ומתקדמות
- **Fillet, Chamfer, Shell, Hole, Draft, Rib** — עריכות מוצק
- **Boolean** (Union/Subtract/Intersect), **Pattern** (Linear/Circular), **Mirror**
- **היסטוריית פיצ'רים פרמטרית מלאה** עם Rollback ו-Reorder

### 🏗️ הרכבות (Assembly)
- הוספת רכיבים, Mates (Coincident, Concentric, Parallel, Distance, Angle, Gear, Cam)
- **Interference Detection** — בדיקת התנגשויות
- **Exploded View** ו-**BOM** אוטומטי
- תמיכה בהרכבות גדולות עם ביצועים משופרים

### 📐 שרטוטים דו-ממדיים (Drawings)
- יצירת מבטים סטנדרטיים אוטומטית ממודל תלת-ממדי
- **Section, Detail, Auxiliary, Broken-out** views
- מידות אוטומטיות, GD&T, סמלי ריתוך, הערות
- ייצוא ל-**PDF, DXF, DWG, SVG**

### 🛠️ גיליונות מתכת (Sheet Metal)
- Base Flange, Edge Flange, Miter Flange, Hem
- Sketched Bend, Jog, Tab, Corner Relief
- **Unfold / Fold / Flatten** עם טבלאות כיפוף

### 🌊 משטחים מתקדמים (Surfacing)
- Swept, Lofted, Boundary, Fill, Knit, Trim, Thicken
- Ruled Surface, Offset Surface, Untrim

### 🧪 סימולציה (FEA)
- ניתוח סטטי, תדרים, buckling, תרמי
- שילוב מנוע **CalculiX** (GPL)
- תוצאות: Stress, Displacement, Strain, Factor of Safety

### 🔩 מודולים נוספים
- **Weldments** — מבני מסגרות, גאסים, חישוב אורך
- **Mold Design** — Core/Cavity, Parting Surfaces
- **Mesh & Reverse Engineering** — ייבוא STL, המרה ל-BRep
- **BIM** — קירות, עמודים, קורות, ייצוא IFC
- **CAM** — כרסום, קידוח, G-Code (בתכנון)

### 🎨 ממשק משתמש
- **Dark Mode** כברירת מחדל עם ערכת נושא מודרנית
- **Ribbon** בסגנון Office/SOLIDWORKS
- **Feature Tree** אינטראקטיבי עם סטטוס פיצ'רים
- **Property Manager** תלוי-הקשר
- קיצורי מקלדת מלאים (`S`, `E`, `R`, `F`, `Ctrl+Z/Y`)

---

## 📂 תמיכת פורמטים

### ✅ קריאה + כתיבה (קוד פתוח מלא)

| פורמט | סיומת | ספרייה |
|---|---|---|
| STEP | `.step`, `.stp`, `.stepz` | OCCT |
| IGES | `.igs`, `.iges` | OCCT |
| BREP | `.brep`, `.shape` | OCCT |
| XCAF | `.xbf` | OCCT |
| STL | `.stl` | OCCT |
| OBJ | `.obj` | OCCT |
| glTF / GLB | `.gltf`, `.glb` | OCCT |
| VRML | `.wrl`, `.vrml` | OCCT |
| PLY | `.ply` | Assimp + OCCT |
| DXF / DWG | `.dxf`, `.dwg` | ACadSharp (MIT) |
| SVG | `.svg` | SVG.NET |

### 📥 קריאה בלבד (קוד פתוח)

| פורמט | סיומת | ספרייה |
|---|---|---|
| 3MF | `.3mf` | Assimp |
| AMF | `.amf` | Assimp |
| Collada | `.dae` | Assimp |
| IFC (BIM) | `.ifc` | IfcOpenShell |

### ⚠️ פורמטים קנייניים — לא נתמכים ללא רישיון מסחרי

| פורמט | סיומת | סטטוס |
|---|---|---|
| Parasolid | `.x_t`, `.x_b` | ❌ דורש רישיון Siemens |
| JT | `.jt` | ❌ מסחרי |
| ACIS | `.sat`, `.sab` | ❌ מסחרי |
| FBX | `.fbx` | ❌ Autodesk |
| USD | `.usd`, `.usdz` | ❌ מסחרי |

> **הערה:** פורמטים קנייניים לא ימומשו ללא רישיון מפורש. STEP משמש כנתיב החלפת הנתונים המעשי.

---

## 💻 התקנה

### דרישות מערכת
- **מערכת הפעלה:** Windows 10/11 x64
- **RAM:** 4GB מינימום, 8GB מומלץ
- **דיסק:** 500MB פנויים
- **אין צורך ב-.NET מותקן** (self-contained)
- **אין צורך בחיבור לאינטרנט**

### הורדה
הורד את הגרסה האחרונה מעמוד ה-[Releases](../../releases):

1. חלץ את `ForgeCAD-vX.X.X-win-x64.zip` לתיקייה לבחירתך.
2. הפעל את `ForgeCAD.exe`.
3. זהו. אין התקנה, אין רישום, אין הגדרות ראשוניות.

> 🔒 **פרטיות מוחלטת:** האפליקציה לא שולחת שום נתון לרשת. אין טלמטריה, אין אנליטיקה, אין בדיקות עדכון.

---

## 🔨 בנייה ממקור

### דרישות בנייה
- [.NET 8 SDK](https://dotnet.microsoft.com/download/dotnet/8.0)
- [Visual Studio 2022](https://visualstudio.microsoft.com/) (אופציונלי, מומלץ)
- [Git](https://git-scm.com/)

### שלבי בנייה

```bash
# שכפול המאגר
git clone https://github.com/your-org/ForgeCAD.git
cd ForgeCAD

# שחזור חבילות
dotnet restore

# בנייה
dotnet build -c Release

# הרצת בדיקות
dotnet test

# פרסום כ-EXE מקומי
dotnet publish src/ForgeCAD.App -c Release -r win-x64 \
    --self-contained true \
    /p:PublishSingleFile=true \
    -o ./publish
```

התוצר: `./publish/ForgeCAD.exe` — קובץ הרצה עצמאי ללא תלות ב-.NET חיצוני.

### מבנה הפרויקט

```
ForgeCAD/
├── src/
│   ├── ForgeCAD.App/            # WPF Application
│   ├── ForgeCAD.Core/           # Domain models, Feature Tree
│   ├── ForgeCAD.Geometry/       # IGeometryKernel + NetOcc
│   ├── ForgeCAD.Sketching/      # Sketcher engine
│   ├── ForgeCAD.Features/       # Extrude, Revolve, Fillet...
│   ├── ForgeCAD.Assembly/       # Mates, Components
│   ├── ForgeCAD.Drawing/        # 2D Drawings
│   ├── ForgeCAD.IO/             # Import/Export
│   ├── ForgeCAD.UI/             # WPF Controls, Themes
│   └── ForgeCAD.Tests/          # Unit + Integration Tests
├── native/
│   └── occt/                    # OCCT DLLs (x64)
├── docs/
│   ├── architecture.md
│   ├── formats.md
│   └── roadmap.md
├── CLAUDE.md
├── THIRD_PARTY_NOTICES.md
├── LICENSE
└── README.md
```

---

## 🚀 שימוש מהיר

### יצירת חלק חדש
1. `File → New Part` (או `Ctrl+N`)
2. בחר מישור סקיצה (Front / Top / Right)
3. שרטט סקיצה עם כלי ה-Sketcher
4. הוסף אילוצים ומידות
5. `Feature → Extrude` (`E`)
6. שמור כ-`.fcad` (`Ctrl+S`)

### ייבוא קובץ STEP
1. `File → Import → STEP`
2. בחר קובץ `.step` / `.stp`
3. המודל ייטען ל-Viewport
4. ניתן לערוך, למדוד, ולייצא מחדש

### קיצורי מקלדת נפוצים

| קיצור | פעולה |
|---|---|
| `S` | סקיצה חדשה |
| `E` | Extrude |
| `R` | Revolve |
| `F` | Fillet |
| `Ctrl+Z` | Undo |
| `Ctrl+Y` | Redo |
| `Ctrl+S` | שמירה |
| `F` | Fit All (ב-Viewport) |
| `MMB` | סיבוב מודל |
| `Shift+MMB` | פאן |
| `גלגלת` | זום |

---

## 🗺️ רודמאפ

| שלב | תוכן | סטטוס |
|---|---|---|
| **MVP-1** | Document Management, 3D Viewer, STEP I/O | 🚧 בפיתוח |
| **MVP-2** | Sketcher, Extrude/Revolve, Boolean | 📋 מתוכנן |
| **MVP-3** | Fillet/Chamfer/Shell/Hole, Pattern/Mirror | 📋 מתוכנן |
| **MVP-4** | Assembly (Mates, Interference Detection) | 📋 מתוכנן |
| **MVP-5** | Drawings (Views, Dimensions, BOM, PDF/DXF) | 📋 מתוכנן |
| **MVP-6** | Sheet Metal (Flange, Bend, Unfold) | 📋 מתוכנן |
| **MVP-7** | Sweep/Loft/Surface Basics | 📋 מתוכנן |
| **MVP-8** | Simulation (Static FEA via CalculiX) | 📋 מתוכנן |
| **עתידי** | CAM, BIM, Mold, Weldments, Mesh/Reverse | 💭 רעיונות |

רודמאפ מפורט זמין ב-[docs/roadmap.md](docs/roadmap.md).

---

## 🤝 תרומה

נתחיל בכך שנשמח לתרומות! בין אם מדובר בתיקון באג, שיפור תיעוד, או פיצ'ר חדש — כל תרומה מבורכת.

### איך לתרום
1. **Fork** את המאגר
2. צור ענף חדש: `git checkout -b feature/my-feature`
3. כתוב בדיקות (xUnit) עבור השינוי שלך
4. ודא שהכל עובר: `dotnet test`
5. Commit בשיטה ברורה: `git commit -m "feat: add revolve feature"`
6. Push: `git push origin feature/my-feature`
7. פתח **Pull Request** עם תיאור מפורט

### סגנון קוד
- **C# 12 / .NET 8**, Nullable enabled
- **SOLID** principles, **MVVM** ל-WPF
- כל פעולה גיאומטרית דרך `IGeometryKernel` בלבד
- כל פיצ'ר חייב להיות **טרנזקציונלי** (Undo/Redo)
- אין קוד רשת, אין טלמטרה, אין שילוב קוד מ-CAD קנייני

### דיווח באגים
פתח [Issue](../../issues) חדש עם:
- תיאור הבעיה
- שלבי שחזור
- גרסת ForgeCAD ו-Windows
- קובץ לוג מ-`%LOCALAPPDATA%\ForgeCAD\logs`

### תרומת קוד — כללים משפטיים
- כל ספריית צד שלישי חייבת להיות ברישיון **LGPL / MIT / Apache 2.0**
- יש להוסיף רשומה ל-`THIRD_PARTY_NOTICES.md`
- אין להעתיק קוד מ-SOLIDWORKS, FreeCAD, או כל CAD קנייני אחר

---

## 📜 רישוי

### הקוד של ForgeCAD
כל קוד האפליקציה מופץ תחת **[GNU General Public License v3.0](LICENSE)** — חופשי לשימוש, שינוי והפצה, כל עוד נשמרים החירויות של המשתמשים הקצה.

### OCCT (Open CASCADE Technology)
ליבת הגיאומטריה מופצת תחת **LGPL 2.1**. ForgeCAD מקשר ל-OCCT **באופן דינמי** (DLL), מה שמאפשר את השימוש ברישיון GPLv3 לאפליקציה. הודעת הרישיון המלאה נמצאת ב-[`LICENSE-OCCT.txt`](LICENSE-OCCT.txt).

### ספריות צד שלישי
כל הספריות בהן נעשה שימוש מפורטות ב-[`THIRD_PARTY_NOTICES.md`](THIRD_PARTY_NOTICES.md), כולל גרסאות ורישיונות.

### מה **לא** ניתן לעשות
- ❌ להעתיק קוד מ-SOLIDWORKS, NX, CATIA, או כל CAD קנייני
- ❌ לממש פורמטים קנייניים (Parasolid, JT, ACIS) ללא רישיון מסחרי
- ❌ לשלב את ה-Wrapper המסחרי של OCCT ל-.NET ללא רישיון
- ❌ לשלוח נתוני משתמש לשרת חיצוני

---

## 🙏 תודות

- **[Open CASCADE Technology](https://www.opencascade.com/)** — ליבת הגיאומטריה
- **[NetOcc](https://github.com/Open-Cascade-SAS/OCCT)** — עטיפת C# ל-OCCT 8.x
- **[ACadSharp](https://github.com/DomCR/ACadSharp)** — תמיכת DXF/DWG
- **[Assimp](https://github.com/assimp/assimp)** — ייבוא פורמטים גרפיים
- **[IfcOpenShell](https://ifcopenshell.org/)** — תמיכת IFC/BIM
- **[CalculiX](http://www.calculix.de/)** — מנוע FEA
- **[MaterialDesignInXAML](https://github.com/MaterialDesignInXAML/MaterialDesignInXamlToolkit)** — ערכת עיצוב WPF
- **[Helix Toolkit](https://github.com/helix-toolkit/helix-toolkit)** — תצוגה תלת-ממדית חלופית
- **קהילת הקוד הפתוח** — על הכלים, ההשראה והתמיכה

---

<div align="center">

**⚒️ ForgeCAD — בנה. עצב. שחרר.**

*נבנה באהבה על ידי קהילת הקוד הפתוח.*

[⬆ חזרה למעלה](#️-forgecad)

</div>
