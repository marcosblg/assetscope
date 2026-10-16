*[Español](README.md) · **English***

# AssetScope

**What each device is and how long it will last you.** Inventory, warranties and end of support in a single HTML file. No server, no installation, and no data ever leaves your computer.

[RackScope](https://github.com/marcosblg/rackscope) tells you *where* each device is. [SubnetScope](https://github.com/marcosblg/subnetscope) tells you *which IP* it has. AssetScope tells you *what it is and when it expires*.

It was built to replace the usual inventory spreadsheet: the one with twenty columns that nobody reads, which tells you the server's warranty had expired once the server is already broken. Here, the first thing you see is a traffic light with what has already expired and what expires soon.

### 👉 [Try it now in your browser](https://marcosblg.github.io/assetscope/)

🌐 **In English and Spanish**: it opens in your browser's language and the **EN / ES** button switches it.

Nothing to install or download: the link opens the tool with a sample inventory. Press **▶ Ver demo** for the guided tour.

![AssetScope demo](docs/demo.gif)

🎬 **[Watch the demo video (30 s)](docs/demo.mp4)** · or press **▶ Watch demo** inside the app to walk through it yourself.

## What it does

**The expiry traffic light**
- You don't open onto a table, you see what matters: 🔴 **expired**, 🟠 **expires within 90 days** and 🟢 **covered**, sorted by date.
- Three dates per device: **end of warranty**, **end of manufacturer support** and **end of maintenance contract**.
- Devices with no dates at all are listed separately, so you know what is still missing.
- The warning window is set in ⚙ (90 days by default). Retired devices don't count.

**Device record**
- **Identity**: name, type (server, switch, router, firewall, storage, UPS, AP, PC, laptop, printer…), make, model and **serial number**.
- **Status**: in production, in storage, on loan, in RMA or retired. Every status change is logged in the history.
- **Location**: room, rack and U if racked, or free text ("Office 3").
- **Assigned to** a person or a department.
- **Purchase**: supplier, date, invoice number, price and cost centre.
- **History** of faults and dated notes.
- **Attachments** by path or link (the invoice at `\\server\invoices\…`), never the file itself inside the data.
- Warns if you repeat a serial or inventory number.

**Inventory**
- A table with every device, filters by type, status and location, and sorting by any column.
- Search by name, serial number, person, room, supplier or invoice (Ctrl+F).

**Fleet report**
- How many devices of each type, total purchase value and how many are 5 years old or more.
- **What expires in the next 12 months and what renewing it would cost**, using each record's renewal cost or, failing that, its purchase price.
- Breakdown by type, age, status and location.
- Exports to a ready-to-present **PDF**, with the full inventory at the end.

**QR labels**
- A4 sheet of 3 × 8 labels (70 × 37 mm) with inventory number, name, model, serial number and a QR code.
- The QR holds the device data and can be read offline by any phone. Or, if you prefer, a link that opens its record in AssetScope.
- The QR generator is built into the HTML itself: no external service is called.

**Import without retyping**
- **From Excel (CSV)**: recognises the usual columns in Spanish or English (*Nº de serie*, *Serial Number*, *Fin de garantía*, *Warranty end*…), dates in any format and prices with decimal commas. If the device already exists (same serial number), it only fills in what's missing.
- **From RackScope**: brings in the devices from your racks with their room, rack and U. Patch panels and gaps are skipped.

**The usual**
- Export to **CSV for Excel**, **PDF** and **JSON** (backup).
- **Save to a file of your own**: link it once and it is rewritten automatically on every change. It can live in a network folder.
- Undo and redo with **Ctrl+Z / Ctrl+Y**, light and dark theme, and a guided demo.

## What it doesn't do (on purpose)

No network-scanning agents, no tickets, no software licences, no server. GLPI and friends already do that. AssetScope answers one question and answers it well: what you have and when it expires.

## How to use it

1. Download `index.html` (or open the [demo link](https://marcosblg.github.io/assetscope/)).
2. Double-click it to open it in Chrome, Edge or Firefox.
3. Press **Reiniciar › Empezar en blanco** and add your devices, or bring in your spreadsheet with **Importar › Desde Excel**.
4. Press **💾 Archivo** so it saves itself to a file of your own.

File linking works in Chrome and Edge. In Firefox data is kept in the browser and you can export the JSON whenever you like.

## Privacy

Everything runs inside your browser. The HTML blocks any Internet connection (`connect-src 'none'` security policy): no analytics, no external fonts, no third-party libraries.

## License

AGPL-3.0. Use it and modify it freely, including inside your company. If you distribute a modified version or offer it as a service, you must publish the source under this same license.

The **AssetScope** name and visual identity are not covered by the code license: if you publish a derivative, give it a different name.

**Using it at work?** If you need a license that does not require publishing your code, or support, get in touch on LinkedIn: https://es.linkedin.com/in/marcos-belmonte-gomez-9b5a71205
