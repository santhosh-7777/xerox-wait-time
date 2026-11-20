# Fieldwork Notes — Parimalnath Xerox & Binding Shop

## 1. Observation Visits & Timing Method
- **Location:** Parimalnath's Xerox and Binding Shop (campus area)
- **Visit 1 (Evening):** November 19, 2026, ~8:40 PM – 9:10 PM (recorded customer events between `20:43` and `20:52`)
- **Visit 2 (Morning):** November 20, 2026, `08:30` AM – `09:10` AM (recorded customer events between `08:32` and `09:10`)
- **How Orders Were Timed:**
  - I stood directly beside the xerox and spiral binding counter and wrote down each person's arrival time, leave time, visible job type, page count when known, and whether they left carrying their completed work.
  - `actual_wait_minutes` was calculated as `leave_time - arrival_time`.
  - Details that were not visible or spoken aloud (unseen page counts, color vs. B&W on some orders, and exact queue length at arrival) were recorded as `unknown` rather than estimated.

---

## 2. Photographic Evidence (`photos/`)
- **Timestamp:** November 19, 2026 at `9:02 PM` (2 photos saved in `photos/`).
- **What They Show:** Counter activity and student queue conditions during the evening rush window. *(Replace this line with your two exact image filenames from `photos/` before committing.)*

---

## 3. Shopkeeper Statements & Key Surprise
- **Verbal Wait Quotes Observed at the Counter:**
  - During the November 20 morning rush, Parimalnath told one student from a group of three girls to **"come after 30 minutes,"** and she left without waiting (`turned_away`, `quoted_wait_minutes = 30`).
  - At `08:50` AM, he told a student requesting spiral binding (`50` pages) to wait **40 minutes**, though the student received his completed binding in **20 minutes** (at `09:10` AM).
  - At `08:52` AM, he gave a shared **30-minute** quote to a pair arriving together for project report binding, and both finished in **10 minutes** (at `09:02` AM).
- **Key Surprise (4–5 Pre-Day Calls & Priority Queueing):**
  - Parimalnath stated that he typically receives **4 to 5 phone calls the day/night before**, and when those callers arrive at the shop, **he gives them higher priority** over walk-in students because they called ahead and have already been waiting.
  - **Impact on Walk-In Queue:** Walk-in students cannot judge their wait time just by looking at the physical line, because pre-called orders jump ahead in priority—explaining both sudden walk-in delays (up to 26 minutes) and why he over-quotes or turns walk-ins away with 30–40 minute estimates. *(Note: The 4–5 calls figure is Parimalnath's verbal estimate, not a direct count from the 20-row log.)*

---

## 4. Dataset Summary & Limitations (`data.csv`)
- **Total Recorded Rows:** 20 customer observations (2 from Nov 19 evening; 18 from Nov 20 morning).
- **Outcome Breakdown:**
  - `completed`: 17 orders (1 on Nov 19; 16 on Nov 20—all confirmed by seeing students leave the counter carrying their work)
  - `left_without_service`: 2 people (1 on Nov 19; 1 on Nov 20)
  - `turned_away`: 1 person (Nov 20, quoted 30 minutes)
- **Known Limitations:**
  - **Missing wait durations on 3 unserved rows:** Two rows from the Nov 20 three-girls group have `unknown` arrival and leave times, and the Nov 19 `20:43` row left after 2 minutes without service, so **17 of 20 rows** (all 17 completed orders) have a numeric `actual_wait_minutes` value (ranging from `3` to `26` minutes, average `8.94` min).
  - **Small quoted-wait sample:** Most customers did not ask for or receive a verbal time estimate. Only **3 completed rows** (`08:50` spiral binding and the `08:52` project-report pair, which shared a single verbal quote) have both a quoted wait and a recorded completion time (average over-quote of `20.0` minutes), alongside 1 turned-away row quoted at `30` minutes.
  - **Hidden priority arrivals:** Because phone callers were not tagged separately at the counter, the 20-row CSV does not distinguish which morning arrivals were part of the 4–5 priority callers.