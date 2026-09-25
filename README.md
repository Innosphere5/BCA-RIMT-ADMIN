# RIMT Academic Trust — T&P Web Admin Portal & Expo 57 System

An enterprise-grade **Training & Placement (T&P) Web Admin Portal** built with **Next.js (JSX)** and compatible with **Expo 57** (`react-native` / `FRONTEND-RIMT`).

Designed in 1:1 accordance with:
- **`stitch_custom_design_implementation`** (Glossy KPI Cards, Specular Highlights, Light Sweeps, Dark Hero `#15151F` Cards)
- **`DESIGN.md`** (Design system tokens, typography scales, color palettes)
- **`RESPONSIVE-DESIGN.md`** (3-State layout shell: Mobile drawer, Tablet icon rail, Desktop full sidebar)
- **`ADMIN-PORTAL.md`** (All 7 T&P core modules)

---

## 🎨 Design System Deep-Dive

### 1. Color Palette Tokens
| Token | Hex | Usage |
|---|---|---|
| **Primary Brand Maroon** | `#8B1D2C` | Active navigation, primary CTA buttons, logo badge, CGPA star chip |
| **Primary Hover / Dark** | `#6E1521` | Button pressed / hover states |
| **Dark Hero Surface** | `#15151F` | Hero greeting cards, profile identity card background |
| **Gold Highlight / Accent**| `#E7B94A` / `#FFDF9B` | Flagship drive badges, Super Dream tags, rating accents |
| **Success Green** | `#1E9E5A` | "Verified" pills, verified checks, attendance % |
| **Info Blue** | `#3E6FD9` | Neutral info badges, secondary icon tiles, technical tags |
| **Background Canvas** | `#F8F9FD` | Ultra-clean institutional background |
| **Surface Card** | `#FFFFFF` | Glassmorphic cards with backdrop blur & specular top line |
| **Tint Red / Maroon** | `#FBEAEA` | Stat card background tint (Degrees, Scholars) |
| **Tint Blue** | `#EAF0FC` | Stat card background tint (Courses, Tech) |
| **Tint Green** | `#EAF8EF` | Stat card background tint (Profile verification) |

### 2. Typography Hierarchy (Inter Sans)
- **`display-stat`**: 32px (Desktop) / 26px (Mobile), font-extrabold (`font-weight: 800`), letter-spacing `-0.02em`
- **`headline-page`**: 24px (Desktop) / 20px (Mobile), font-bold (`font-weight: 700`)
- **`headline-section`**: 18px, font-semibold (`font-weight: 600`)
- **`body-default`**: 14px, regular
- **`label-eyebrow`**: 11px, bold, uppercase tracking-wider
- **`label-badge`**: 12px, bold

### 3. Glossy Specular Aesthetics
- **1.5px Specular Inset Highlight**: `h-[1.5px] bg-gradient-to-r from-transparent via-white/80 to-transparent`
- **Dynamic Light Beam Sweeps**: `animate-sweep-maroon`, `animate-sweep-emerald`, `animate-sweep-blue`, `animate-sweep-amber`
- **Ambient Glow Auras**: `w-44 h-44 rounded-full bg-rose-500/15 blur-2xl`

---

## 📱 Responsive 3-State Layout Shell (`RESPONSIVE-DESIGN.md`)

1. **Mobile (0–767px)**:
   - Sidebar is off-canvas (`-translate-x-full`)
   - Hamburger icon button (`md:hidden`) opens overlay drawer with dark backdrop (`bg-black/50`)
   - Header is full width (`left-0`), main padding is `pl-0`
   - Search expands to clean overlay on demand
   - Full-width CTA buttons (min 44px tap target)
2. **Tablet (`md:` 768–1023px)**:
   - Persistent **collapsed icon rail** (`w-20`) with 36px icon chips
   - Header offset is `md:left-20`, main padding is `md:pl-20`
   - Labels hidden for maximum data table width
3. **Desktop (`lg:` 1024px+)**:
   - Full **expanded sidebar** (`w-72`) with brand shield, labels, and system status
   - Header offset is `lg:left-72`, main padding is `lg:pl-72`
   - Max width container (`max-w-[1600px] mx-auto`) prevents stretching on ultrawide monitors

---

## 🖥️ 7 Complete Admin Screens (All `.jsx`)

| # | Screen | Key Features |
|---|---|---|
| **01** | [StudentManagement.jsx](file:///c:/Users/r3dha/OneDrive/Desktop/ADMIN-PANEL-RIMT/src/views/StudentManagement.jsx) | Scholar roster, 4 glossy KPIs, batch/section filters, live verification status, interactive slide-out Dossier Drawer, + Add Scholar modal, Bulk Import CSV |
| **02** | [CompanyManagement.jsx](file:///c:/Users/r3dha/OneDrive/Desktop/ADMIN-PANEL-RIMT/src/views/CompanyManagement.jsx) | Corporate directory, Tier-1 MNC tags, active MoUs, Card Grid vs Table toggle, Campus SPOC modal, + Add Company modal |
| **03** | [DriveManagement.jsx](file:///c:/Users/r3dha/OneDrive/Desktop/ADMIN-PANEL-RIMT/src/views/DriveManagement.jsx) | Flagship TCS hiring hero card, 4 glossy KPIs, assessment round tracking, eligibility criteria, Schedule Drive modal |
| **04** | [PlacementStatistics.jsx](file:///c:/Users/r3dha/OneDrive/Desktop/ADMIN-PANEL-RIMT/src/views/PlacementStatistics.jsx) | Institutional intelligence, 82.4% placement rate, CTC brackets breakdown progress bars, sector donut breakdown, department-wise conversion bars |
| **05** | [TrainingManagement.jsx](file:///c:/Users/r3dha/OneDrive/Desktop/ADMIN-PANEL-RIMT/src/views/TrainingManagement.jsx) | Pre-placement skill sprints, trainer assignments, session progress bars, RFID attendance %, course materials drawer, + Add Training modal |
| **06** | [InternshipMonitoring.jsx](file:///c:/Users/r3dha/OneDrive/Desktop/ADMIN-PANEL-RIMT/src/views/InternshipMonitoring.jsx) | 6-month semester credit track, corporate stipends (avg ₹32,500), student-to-mentor mapping, completion progress bar, certificate issuance |
| **07** | [ReportGeneration.jsx](file:///c:/Users/r3dha/OneDrive/Desktop/ADMIN-PANEL-RIMT/src/views/ReportGeneration.jsx) | NAAC Criteria 5.2 compliance export engine, PDF & Excel generation, automated scheduled queues, instant preview & download modal |

---

## 🚀 Running the Next.js Web App

```bash
# In c:\Users\r3dha\OneDrive\Desktop\ADMIN-PANEL-RIMT:
npm run dev
```
Open [http://localhost:3000](http://localhost:3000) in your browser.

---

## 📱 Expo 57 Compatibility (`src/expo/`)

The repository includes a complete Expo 57 compatible screen suite:
- `src/expo/colors.js` — React Native design tokens
- `src/expo/screens/StudentManagementScreen.jsx`
- `src/expo/screens/CompanyManagementScreen.jsx`
- `src/expo/screens/DriveManagementScreen.jsx`
- `src/expo/screens/PlacementStatisticsScreen.jsx`
- `src/expo/screens/TrainingManagementScreen.jsx`
- `src/expo/screens/InternshipMonitoringScreen.jsx`
- `src/expo/screens/ReportGenerationScreen.jsx`
- `src/expo/AdminPortalNavigator.jsx` — Multi-tab screen navigator container

### Using in your Expo 57 project (`FRONTEND-RIMT`):
1. Copy `src/expo/` and `src/constants/data.js` into your `c:\Users\r3dha\OneDrive\Desktop\FRONTEND-RIMT` project.
2. Import `<AdminPortalNavigator />` anywhere into your Expo 57 app!
