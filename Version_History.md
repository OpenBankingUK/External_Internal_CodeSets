# Version History

For v4.0.1 the following approach has been adopted for identifying changes:

- [Known Issues](https://openbanking.atlassian.net/wiki/spaces/DZ/pages/47546479/Known+Specification+Issues) - these are a tagged with the KI identifier, e.g. [v40_KI45]
- [Change Requests](https://openbanking.atlassian.net/wiki/spaces/WOR/pages/3872948225/2025-09-11+EAG+for+v4.x.x+Standards+release+Workshop+4#Discussion-material) - these are tagged the CR number used in the consultations, e.g. [CR4a]
- EAG/Consultation items - Items included in the consultations are tagged with an identifier representing the consultation period they were introduced, e.g. [v4.0.1 RC 1]
- Feedback remediation - Technical errata and other minor corrections identified by participants or OBL during the Advanced Information period for Release Candidates 1 and 2 with an appropriate identifier for internal OBL traceability e.g. [CDRW-5006]

**Consultations:**

- [v4.x.x Consultation 1](https://openbanking.atlassian.net/wiki/spaces/WOR/pages/3880550401/Feedback+-+V4.x.x+Consultation+1)
- [v4.0.1 Draft 1](https://openbanking.atlassian.net/wiki/spaces/WOR/pages/4096950276/Feedback+-+v4.0.1+Draft+1)
- [v4.0.1 Release Candidate 1](https://openbanking.atlassian.net/wiki/spaces/WOR/pages/4203282434/Feedback+-+v4.0.1+Release+Candidate+1)
- [v4.0.1 Release Candidate 2](https://openbanking.atlassian.net/wiki/spaces/WOR/pages/4309942273/Feedback+-+v4.0.1+Release+Candidate+2)

## v4.0.1 - Unreleased

### Fixed

- [CDRW-5006] Fixed typo in `OBExternalStatusReason1Code` `U003` description
- [CDRW-5047] Fixed the following typographical issues:
  - Corrected capitalisation of `ProForma` in `OBInternalAccountStatus1Code`
  - Removed unneccesary `n` from the end of `ANNI` description
  - Fixed spelling of 'related' in `DEPT`
  - Removed additional whitespace from end of `OBExternalCommunicationMethod2Code`
  - Removed additional whitespace from end of `Enabled`
  - Removed additional whitespace from the end of `Annual`
  - Removed duplicate `BusinessCurrentAccount` entry.


## v4.0.1 Release Candidate 2 - 2026-02-04

### Added

- [v40_KI45] Added `LWMH`, `LXMH`, and `TWYR` to `OBFrequency6Code` in OBInternal
- [v40_KI46] Added `SLCT` to `OBFrequency2Code` in OBInternal

### Updated

- [CDRW-5007] Updated ISO 20022 External Codeset files to Q3 2025 release.
- [CR4a] Updated description for CRYP code to "Transaction is related to the purchase or sale of cryptocurrency."
- [CDRW-5002] Enhanced the descriptions of current `OBInternalPaymentContext1Code` codes `BillingGoodsAndServicesInAdvance`, `BillingGoodsAndServicesInArrears`, `EcommerceMerchantInitiatedPayment`, `FaceToFacePointOfSale`, `TransferToSelf`, `TransferToThirdParty`

## v4.0.1 Release Candidate 1 - 2026-01-05

### Added

- [CR1] Added to `OBInternalStatementFeeType1Code`:
  - `UK.OBIE.InstalmentPlan`
  - `UK.OBIE.ReturnedPayment`
- [CR1] Added to `OBInternalStatementInterestType1Code`:
  - `UK.OBIE.InstalmentPlan`
  - `UK.OBIE.MoneyTransfer`
- [CR4a] Added `CRYP` to `ExternalPurpose1Code`
- [CR2] Introduced `OBIntermediaryAgentStatus1Code` in `OB_Internal_Codeset`. This is used for
  `OBIntermediaryAgent/ProcessingStatus` and has the following codes:
  - `PDNG`
  - `RCVD`
  - `ACSP`
  - `ACSC`
  - `RJCT`
  - `UNKN`
  - `CANC`
- [v40_KI46] Added `NONE` to `OBFrequency2Code`

### Changed

- [v4.0.1 RC 1] Separated `OBInternalConsentStatus1Code` into 3 codesets for certain contexts (#17):
  - Removed `COND` & `AWUP` from `OBInternalConsentStatus2Code`
  - Added `OBInternalConsentStatus2Code` to `OB_Internal_Codeset.csv` with the following values:
    - `AWAU`
    - `RJCT`
    - `AUTH`
    - `COND`
  - Added `OBInternalConsentStatus3Code` to `OB_Internal_Codeset.csv` with the following values:
    - `AWAU`
    - `RJCT`
    - `AUTH`
    - `COND`
    - `AWUP`
- [v40_KI39] Updated description of `U037` in `OBExternalStatusReason1Code` to "Authorisation failed by one (or more) of the authenticators." (#7)
- [v4.0.1 RC 1] Separated `ExternalPaymentTransactionStatus1Code` into 5 codesets for specific contexts (#16). New Codes look like:
  - `ExternalPaymentTransactionStatus1Code` (16 codes) for Domestic Standing Orders & International Standing Orders:
    - `CANC`
    - `RCVD`
    - `ACTC`
    - `PATC`
    - `PDNG`
    - `RJCT`
    - `INFA`
    - `INCO`
    - `ACCP`
    - `ACFC`
    - `ACSP`
    - `ACWC`
    - `ACSC`
    - `BLCK`
    - `ACCC`
    - `ACWP`
  - `ExternalPaymentTransactionStatus2Code` (14 codes) for Domestic Scheduled Payments and International Scheduled Payments:
    - `CANC`
    - `RCVD`
    - `PDNG`
    - `ACTC`
    - `PATC`
    - `ACCP`
    - `ACFC`
    - `ACSP`
    - `ACWC`
    - `ACSC`
    - `BLCK`
    - `ACCC`
    - `ACWP`
    - `RJCT`
  - `ExternalPaymentTransactionStatus3Code` (13 codes) for Domestic Payments and International Payments:
    - `RCVD`
    - `PDNG`
    - `ACTC`
    - `PATC`
    - `ACCP`
    - `ACFC`
    - `ACSP`
    - `ACWC`
    - `ACSC`
    - `BLCK`
    - `ACCC`
    - `ACWP`
    - `RJCT`
  - `ExternalPaymentTransactionStatus4Code` (3 codes) for File Payments:
    - `PDNG`
    - `INFA`
    - `INCO`
  - `ExternalPaymentTransactionStatus5Code` (12 codes) for Domestic VRPs:
    - `RCVD`
    - `PDNG`
    - `ACTC`
    - `ACCP`
    - `ACFC`
    - `ACSP`
    - `ACWC`
    - `ACSC`
    - `BLCK`
    - `ACCC`
    - `ACWP`
    - `RJCT`

### Removed

- [CDRW-4860] Removed duplicate `ExternalMandateStatus1Code` codes (#12)
- [v40_KI43] Removed deprecated `OBExternalStatus3Code` (#13)

### Fixed

- [CDRW-4775] Codesets are now contiguous and organized alphabetically
- [CDRW-4775] Several descriptions have been moved out of the codeset name column and into the description column
- [CDRW-4906] Corrected `OBExternalStatusReason1Code` `1180` description (#21)
- [v40_KI43] Moved the `BusinessCurrentAccount` code from `OBInternalCardSchemeType1Code` to `OBInternalProductType1Code` (#13)
- [v40_KI44] Corrected `OBExternalAuthorisation1Code` to `OBInternalAuthorisation1Code` (#14)
- [CDRW-4855] Fix typo in `ExternalPaymentGroupStatus1Code` `INFA` description (#15)

## Older Versions

> **Note**: Information that has been removed is marked as ~~struck out~~ and that has changed or added is marked as 
> <ins>underlined</ins>.
> 
> Refer to [KI Page](https://openbanking.atlassian.net/wiki/spaces/DZ/pages/47546479/Known+Specification+Issues) for 
> all the known issues.

| Version No 	 | Created by         	 | Creation Date 	 | Version Notes                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            	                                                                                                                                                                        |
|--------------|----------------------|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| v0.1       	 | OBL Standards Team   | 01-Jul-2024   	 | 1) ~~OBExternalDirectDebitFrequency1Code~~ codeset and codevalues are also removed and replaced with <ins>OBFrequency6Code</ins><br><br>2) Removed incorrect values from <ins>OBInternalCardSchemeType1Codes</ins><br><br>3) Removed duplicate entries of <ins>ExternalBalanceType1Code, ExternalBalanceSubType1Code</ins><br><br>4) ~~OBExternalStatus1Code~~ codeset and codevalues are also removed and replaced with <ins>ExternalPaymentTransactionStatus1Code</ins><br><br>5) Moved all <ins>ExternalPaymentTransactionStatus1Code</ins> from ISO_External_Codeset to OB_Internal_Codeset<br><br>6) Added BusinessCurrentAccount which was missing as a Code Value in <ins>OBInternalProductType1Code</ins><br><br>7) Replaced few ~~OBInternalProductType1Code~~ with <ins>OBExternalOfferType1Code</ins> as they were incorrectly under that codeset<br><br>8) Removed ~~ACIS~~ from ISO_External_Codeset because it is not applicable<br><br>9) Renamed ~~OBExternalPaymentTransactionStatus1Code~~ to <ins>ExternalPaymentTransactionStatus1Code</ins> for two code values (INFA and INCO) in OB_Internal_Codeset<br><br>10) Moved <ins>ExternalPaymentGroupStatus1Code</ins> from ISO_External_Codeset to OB_Internal_Codeset <br><br>11) Added two code sets INFA and INCO under <ins>ExternalPaymentGroupStatus1Code</ins><br><br>12) Rename ~~OBExternalClassification1Code~~ with <ins>OBExternalMandateClassification1Code</ins><br><br>13) Updated CodeValue and CodeDefinition of all <ins>OBExternalMandateClassification1Code</ins><br><br> 	 |
| v0.2         | OBL Standards Team   | 16-Jan-2025   	 | 1) (v40_KI26) Added 9 codesets <ins>1100, 1161, 1162, 1163, 1165, 1166, 1177, 1178, 1180</ins> under OBExternalStatusReason1Code<br><br>2) (v40_KI27) Added <ins>RJCT</ins> codeset under ExternalEntryStatus1Code in ISO_External_Codeset<br><br>3) (v40_KI28)(TDA-270 and 271) Added new OBL Proprietary code values <ins>WODL,FOWK, TWMH, FOMH, FIMH, ALMH, NONE</ins> under OBFrequency6<br><br>4) (v40_KI31) Removed duplicate entries of ExternalDocumentFormat1code from ISO_External_Codeset and OB_Internal_Codeset<br><br>5) Added code definitions for below code values and updated code name in OBInternalPaymentContext1Code in OB_Internal_Codeset:<br>- BillingGoodsAndServicesInAdvance<br>- BillingGoodsAndServicesInArrears<br>- EcommerceMerchantInitiatedPayment<br>- FaceToFacePointOfSale<br>- TransferToSelf<br>- TransferToThirdParty<br><br>6)  Removed 'OTHER' from OBInternalPaymentContext1Code as it is a deprecated value<br>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
