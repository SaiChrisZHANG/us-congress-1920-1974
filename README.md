
# Codebook for U.S. Congressional Election Results 1920 - 1974

The file `1920-1974-house` documents constituency (district) election results for elections to the U.S. House of Representatives from 1920 to 1974. The file `1920-1974-senate` documents senate election results from 1920 to 1974. The data source is the document "[Election Statistics: 1920 to Present](https://history.house.gov/Institution/Election-Statistics/Election-Statistics/)", collected and published by the Clerk of the House. This data complements the congressional election results from 1976 to 2022 cleaned by [MIT Election Lab](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/IG0UN2), for the convenience of users, the data is structured similarly as the MIT Election Lab data.

The data are cleaned, organized, and structured by Sai Zhang. When using the data, please cite:.

If you have encountered any issues, please report to the Github page where the developer version is hosted.

## Variables

The variables are listed as they appear in the data file, all string variables are in upper case:

----------------

### year

- **Description**: year in which election was held

----------------

### state

- **Description**: state name

----------------

### office

- **Description**: US House/Senate

----------------

### district

- **Description**: district number
- ***note***: At-large districts are coded as 0 (zero); when there is only one senate seat up for election in a state, coded as 0, otherwise numbered as 1/2 for separation.

----------------

### stage

- **Description**: electoral stage: GEN (general elections)

----------------

### runoff

- **Description**: FALSE (constant)

----------------

### special

- **Description**: special election

| code | definition |
|:---|:---|
| "TRUE" | special elections |
| "FALSE" | regular elections |

----------------

### special_termend

- **Description**: the end year of the special election seats

----------------

### candidate
  
- **Description**: name of the candidate
- ***Note***: The name is as it appears in the House Clerk report, in uppercase.

----------------

### party

- **Description**: party of the candidate
- ***Note***: Parties are as they appear in the House Clerk report. For states where candidates are allowed to appear on multiple party lines, vote counts from each party are documented separately. See MIT Election Lab data page for more details.

----------------

### writein

- **Description**: vote totals associated with write-in candidates
- **Coding**:

| code | definition |
|:---|:---|
| "TRUE" | write-in candidates |
| "FALSE" | non-write-in candidates |

----------------

### mode

- **Description**: mode of voting, "total"

----------------

### candidatevotes

- **Description**: votes received by one candidate for a particular party
- ***Note***: no vote counts were published for some uncontested elections, coded as -1.

----------------

### fusion_ticket

- **Description**: an indicator for candidates vote records from multiple parties in one election.

----------------

### unofficial

- **Description**: all vote counts come from the official documents, FALSE

----------------

### state_po

- **Description**: U.S. postal code state abbreviation

----------------

### state_fips

- **Description**: State FIPS code

----------------

### state_cen

- **Description**: U.S. Census state code

----------------

### state_ic

- **Description**: ICPSR state code

----------------

### version

- **Description**: date when the current version was finalized, in `yyyymmdd` format.

## Version Control

- Published version: the published version contains two `.csv` format files (house and senate separately) and two `.dta` format files.

- Developer version: contains the raw data files in `.xslx` format. The files are the product of OCR extraction from the original documents publicly available in `.pdf` format and manually cleaned.
