# xRef: A Reference Verification System

xRef is a lightweight, self-contained reference verification tool designed to help researchers, editors, and students check the accuracy of their bibliography metadata. By parsing EndNote text exports, xRef cross-references every field in your bibliography against multiple authoritative scholarly databases from a single HTML application.

Because xRef runs entirely within the browser, it requires no server installation or backend dependencies. It performs live lookups directly from your local machine while respecting the rate limits of external APIs.

## Key Features

The xRef application offers a comprehensive suite of verification capabilities designed to ensure the integrity of bibliographic data.

**Live Cross-Database Checking**
The tool simultaneously queries up to six major scholarly databases to verify your references. These include DOI.org for authoritative identifier resolution, PubMed and Europe PMC for biomedical literature, CrossRef for general journals and books, and OpenAlex and Semantic Scholar for broad, open-access scholarly search.

**Comprehensive Field Verification**
xRef does not just check if a reference exists; it compares nine distinct metadata fields. The system verifies Authors, Title, Journal, Year, Volume, Issue, Pages, DOI, and PMID. Any discrepancies between your input file and the database records are flagged for review.

**Adjustable Match Strictness**
Recognizing that different databases may format metadata slightly differently, xRef includes a configurable partial-match threshold. By default, this is set to 80%. Any field scoring at or above 95% is automatically considered a clean match, while scores below the user-defined threshold are highlighted as mismatches.

**Dual Operating Modes**
Users can choose to verify an entire bibliography in bulk by uploading a text file, or they can use the single reference lookup mode. The single lookup mode allows users to paste a DOI, title, or a loose citation to search the selected databases and merge matching records into candidates.

## Usage Instructions

Using xRef is straightforward, as the entire application is contained within the `index.html` file. You can either download the repository and open `index.html` in your preferred web browser, or access the live version hosted on GitHub Pages at [kazilab.github.io/xRef/](https://kazilab.github.io/xRef/).

### Preparing Your References

To verify a full bibliography, you must format your references correctly. **Of special note: users need to use the provided `xRef.ens` EndNote style file to ensure references contain the specific information required by the application.**

1. Download the `xRef.ens` file from this repository and install it in your EndNote styles folder.
2. In EndNote, select the "xRef" style for your bibliography.
3. Export your references as a plain text (`.txt`) file.
4. You can then upload this text file directly into the xRef application, or simply copy and paste the text content into the provided input area.

For a demonstration of the expected format, refer to the `Example_ref.txt` file included in the repository.

### Running the Verification

Once your references are loaded into the application, you can select which databases you wish to query and which specific fields you want to compare. Adjust the match strictness slider if necessary, and click "Verify references." The application will process each entry, displaying real data differences rather than parsing artifacts.

## Repository Contents

The repository contains all the necessary files to run and test the xRef application locally.

| File | Description |
|---|---|
| `index.html` | The core application; a self-contained HTML file that runs in any modern browser. |
| `xRef.ens` | The custom EndNote output style required to format references correctly for parsing. |
| `Example_ref.txt` | A sample text file containing correctly formatted references for testing purposes. |
| `README.md` | This documentation file. |
| `LICENSE` | The MIT License governing the use of this software. |

## License

This project is licensed under the MIT License. See the `LICENSE` file for full details.
