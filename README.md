# Getting started with the DatoLens early-access beta

Thank you for testing DatoLens. This guide takes about ten minutes to read, and gets you from download to a validated, exported production.

## What DatoLens is

DatoLens is a Windows desktop app that loads, checks, fixes and exports e-discovery load files. **Everything stays on your computer:** your data is never uploaded anywhere. The only network traffic is the check for new builds (see Updates).

## Install

1. Open **Releases** on this page and download `DatoLens-Setup-<version>.exe` from the newest release.
2. Run it. It installs for your Windows user only, so **no administrator rights are needed**.
3. Windows will show **"Windows protected your PC"**. That's because early-access builds aren't code-signed yet. Click **More info**, then **Run anyway**. You'll see this once, at first install.

You need Windows 10 or 11.

## Your invite code

The first time you open DatoLens, it asks for the **invite code** from your invitation email.

- Type it and click **Continue**. Capital letters and spaces don't matter.
- You enter it once per Windows user. DatoLens remembers it, including across updates.
- If you're told the code isn't right, check the email and try again.

Each beta build works for **90 days after it was built**. Automatic updates keep you on a current build, so normally you'll never notice.

If you ever see **"This beta build has expired"**, a newer build may already be downloading: close DatoLens, wait a few minutes, and open it again. If it's still expired, email bam011.dev@gmail.com for a new installer. Your projects are safe on your computer either way.

## Updates

- Each time DatoLens starts, it checks for a new build and downloads it in the background. When it's ready, a message tells you.
- The new build installs the next time you close DatoLens. Your projects aren't touched.
- To turn this off, use **Help → Check for updates automatically**.

## Your first project, step by step

1. **New Project.** On the Welcome page, click **New Project**, give it a name and choose where to save it. A project is a single `.dlens` file.
2. **Load Data.** Click **Browse files** and pick a load file:
   - DAT, in the Concordance/Relativity standard layout (þ quotes, DC4 between fields);
   - CSV, TSV, or a file with any other delimiter.

   UTF-8 and ANSI (Windows-1252) files are detected automatically. Check the preview, then click **Load into project**. You can append more files to the same project later.
3. **Dashboard.** See your data's quality at a glance: a quality score, a production-readiness checklist and field warnings.
4. **Validate.** Pick the checks you want and click **Run validation**:
   - **Bates Number Gaps:** missing numbers in a Bates range.
   - **Bates Number Duplicates:** the same Bates number on more than one record.
   - **Date Consistency:** dates in mixed formats, or that don't parse.
   - **Empty Required Fields:** blanks in fields that must be filled.
   - **MD5 Hash Deduplication:** documents with the same hash.
   - **File Path Verification:** native or text paths that don't point to a real file.
   - **Standard DAT QC:** structural problems in a DAT file.
   - **Relativity Load File Check:** problems that would stop a Relativity import.

   You can also build your own custom rules.
5. **Records.** Browse every record in a grid. Search, tag records, and change fields in bulk. Bulk changes can be previewed first and undone.
6. **Export.** Export a DAT or CSV, including productions with Bates ranges. The privilege safeguard stops privileged records leaving by mistake. Click **Export**, then **Confirm export**.
7. **Reports.** Generate a Validation Summary, Audit Trail, Gap / Duplicate, Comparison or Email Analysis report, as PDF, HTML, CSV or JSON. Pick a report and click **Generate**.

## Tips

- **Work on a copy** of real case data while you're testing.
- **Ctrl+S** saves the project.
- Every change to your data is recorded in the audit trail: see **Reports → Audit Trail**.
- DatoLens is designed for projects of up to about 500,000 records.

## Sending feedback

Your feedback is the point of this beta. Please send anything that's broken, confusing or missing.

- **Help → Send feedback…** opens an email to bam011.dev@gmail.com with your DatoLens version filled in. Say what happened, what you expected, and the steps that led to it.
- **To include the log:** use **Help → Open logs folder** and attach `datolens.log`. The log records what the app did, not your documents' contents. If you're unsure, glance through it before sending.
- **Don't send case data.** If a particular file causes the problem, describe its shape instead: the format, the number of records and the number of fields.

## Known limitations in this build

- Windows only.
- The installer isn't code-signed yet, hence the SmartScreen step under Install.
- There's no Settings page yet.
- Every feature is switched on. There are no paid plans or license keys in the beta.
- The Email Analysis report is a file, not an interactive view.
- In the Records grid, paging very deep (past about page 4,000 in a 500,000-record project) gets slow.
