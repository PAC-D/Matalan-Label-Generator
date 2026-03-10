# Version History
## v3.2 (Documentation Enhancements)
**Release Date:** March 11, 2026

### 📚 Documentation
- **Instruction Manual Expanded:**
  - Added new details about the *Carton Dimensions* (MM requirement) and *Gross Weight* in the Application Inputs section.
  - Increased the manual from **4 pages to 5 pages** to provide a cleaner layout for instructions.
  - Moved **Printing Specs** and **Troubleshooting** to the new Page 5.
  - Enlarged the print settings guide screenshot on Page 4 for better visibility and explicitly recommended opening the exported PDF in Microsoft Edge to apply those layout settings perfectly.
- **Troubleshooting Additions:**
  - Added visual fixes for: "Values not showing properly" (reselect size and re-enter values).
  - Added alignment guidance for mobile users (use a computer for perfectly consistent results).

---

## v3.1 (Favicon & Typo Fixes)
**Release Date:** March 10, 2026

### 🚀 New Features
- **Favicon Integration:**
  - Added a custom pacd favicon (`favicon.png`) to the main generator app and the instruction manual for better brand identity in browser tabs.

### 🐛 Bug Fixes
- **Label Text Consistency:**
  - Renamed "Dimensions" to "Label Size" in the configuration sidebar.
  - Renamed "Carton Dimensions" to "Carton Dimension" in the configuration sidebar for consistency.
  - Fixed a typo where it was misspelled as "CARTON DIMENTION" on the actual generated label.

---

## v3.0 (Major Layout & Fields Update)
**Release Date:** March 09, 2026

### 🚀 New Features
- **New Input Fields:**
  - Added *Carton Dimensions* (Length, Width, Height) inputs.
  - Added *Gross Weight (KG)* input.
- **Enhanced Label Layout:**
  - **A5 & Custom Modes:** Display PO Number / Style Ref on one line.
  - Display Pack ID / Box Quantity symmetrically on the same line to save vertical space.
  - New carton dimensions and gross weight neatly nested below.
  - Optimized corner box ("H") positioning to prevent overlaps.
- **Auto-Shrink Text (Single-Line Clamp):**
  - PO Number, Style Ref, Line Code, and Pack ID now automatically scale down their font sizes to guarantee they stay perfectly formatted on one line.
- **A5 Layout Optimization:** 
  - Reduced side paddings & vertical margins for maximized text space.
  - Distributed single-line items evenly across the label container vertically using flexbox (`justify-content: space-between`).

---

## v2.4 (Default Size Update)
**Release Date:** February 11, 2026

### 🚀 New Features
- **Updated Default Size Layout:**
  - Redefined the default values for the 12 size slots to include smaller and larger sizes.
  - **New Order:** XXXS, XXS, XS, S, M, L, XL, XXL, 3XL, 4XL, 5XL, 6XL.
  - Ensures immediate support for a wider range of sizes without manual entry.

---

## v2.3 (Size Layout Expansion)
**Release Date:** February 10, 2026

### 🚀 New Features
- **Expanded Size Inputs (12 Slots):**
  - Increased from 7 to **12 size input slots** in the configuration sidebar.
  - First 7 slots pre-filled with standard sizes (XS, S, M, L, XL, XXL, 3XL); remaining 5 are blank for custom sizes.
  - Sidebar inputs arranged in a **2 rows of 6** grid layout.

- **A5 Two-Row Size Table:**
  - When **A5** dimension is selected, the label's size table displays sizes in **2 rows of 6 columns** with a clear border separator between rows.
  - Provides a cleaner, more compact layout for labels with many sizes.

- **Total Column Removed:**
  - The "Total" column has been **removed** from both A5 and Custom label outputs for a cleaner appearance.

### 🐛 Bug Fixes
- **Blank Preview Fix:** Resolved a critical issue where the label preview was blank due to a **duplicate HTML ID collision** between size header inputs (`label1`–`label12`) and label container elements (`label1`, `label2`). Renamed inputs to `sizeLabel1`–`sizeLabel12`.
- **Duplicate `</main>` Tag:** Removed a stray duplicate closing `</main>` tag in `index.html`.

### 📚 Documentation
- Updated instruction manual to document the new 12-slot layout and A5 two-row display.
- Bumped manual version to **3.0 | March 2026**.

---

## v2.2 (Documentation & Branding Update)
**Release Date:** February 10, 2026

### 🎨 Branding Update
- **Name Change:** Updated application title to **"Matalan Shipping Label Generator"** across the interface and manual.
- **Enhanced Header:** Increased manual header logo size (60px) and added a white background for improved brand visibility on dark themes.

### 📚 Documentation (Instruction Manual)
- **Comprehensive Refactor:**
  - Expanded and restructured the manual into a clear **4-page** format to resolve overflow issues while maintaining a compact footprint.
- **New Page Structure:**
  - **Page 1:** Label Size Selection & Carton Type Options.
  - **Page 2:** Mapping Source Data (Part 1).
  - **Page 3:** Application Inputs (Part 2) with optimized image sizing (45%).
  - **Page 4:** Consolidated reference section including Special Classifications (Homeware), Final Steps, Printing Specs, and Troubleshooting.
- **Visual & Functional Updates:**
  - Updated guide images for clarity.
  - Refined layout to ensure all critical information fits perfectly on standard A4 paper.
  - **Export Logic:** Updated the PDF generation engine to robustly support the new multi-page structure.

---

## v2.1 (Previous Release)
**Release Date:** February 07, 2026

### 🚀 New Features
- **Dynamic Size Columns:** 
  - The "Size Breakdown" table now automatically adjusts the number of columns based on user input.
  - Columns for unused sizes are automatically hidden, ensuring a clean and professional label layout.
  - Table columns now auto-size proportionally instead of having fixed widths.

- **Editable Size Headers:**
  - Users can now rename standard size labels (XS, S, M, etc.) to any custom value (e.g., "Size 8", "3-4 Years") directly from the sidebar.
  - The preview table headers update immediately to reflect these custom names.

- **Carton Type Selection:**
  - Added a "Carton Type" selector with two modes:
    - **Ratio:** For cartons containing mixed sizes (Standard table view).
    - **Single:** For cartons containing only one specific size (Simplified view).

### 🛠 Improvements
- **Smart PDF Export:** 
  - Implemented a "Clone Strategy" for PDF generation to prevent screen-scaling issues.
  - Added logic to ensure exact A4/Custom dimensions regardless of the user's screen resolution or zoom level.
  - Automatic blank page removal.

- **Homeware Logic:**
  - The large Corner Box indicator ("H") now only appears specifically when the "H - Homeware" division is selected.

- **UI/UX Updates:**
  - Re-designed the "Size Breakdown" input section in the sidebar for better usability.
  - Added new grouping for size label and quantity inputs.
  - Integrated a comprehensive, multi-page **Instruction Manual** directly into the application.

---

## v1.0 (Initial Release)
- **Core Label Generation:** Basic functionality to generate standard Matalan/PacD labels.
- **Preview Engine:** Live HTML-based preview of the label.
- **Basic Export:** Simple PDF export functionality.
- **Standard Fields:** Fixed fields for PO, Style, Factory, etc.
