# Version History

## v4.0.1 - 2025-11-20

### Added

- Added to `OBInternalStatementFeeType1Code`:
  - `UK.OBIE.InstalmentPlan`
  - `UK.OBIE.ReturnedPayment`
- Added to `OBInternalStatementInterestType1Code`:
  - `UK.OBIE.InstalmentPlan`
  - `UK.OBIE.MoneyTransfer`
- Added `CRYP` to `ExternalPurpose1Code`
- Introduced `OBIntermediaryAgentStatus1Code` in `OB_Internal_Codeset`. This is used for
  `OBIntermediaryAgent/ProcessingStatus` and has the following codes:
  - `PDNG`
  - `RCVD`
  - `ACSP`
  - `ACSC`
  - `RJCT`
  - `UNKN`
  - `CANC`
- Description of code value `U037` updated to "Authorisation failed by one (or more) of the authenticators."

### Changed

- Separated `OBInternalConsentStatus1Code` into 3 codesets for certain contexts (#17):
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
- Updated description of `U037` in `OBExternalStatusReason1Code` (#7)
- Separated `ExternalPaymentTransactionStatus1Code` into 5 codesets for specific contexts (#16). New Codes look like:
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

- Removed duplicate `ExternalMandateStatus1Code` codes (#12)
- Removed deprecated `OBExternalStatus3Code` (#13)

### Fixed

- codesets are now contiguous and organized alphabetically
- several descriptions have been moved out of the codeset name column and into the description column
- Corrected `OBExternalStatusReason1Code` `1180` description (#21)
- Moved the `BusinessCurrentAccount` code from `OBInternalCardSchemeType1Code` to `OBInternalProductType1Code` (#13)
- Corrected `OBExternalAuthorisation1Code` to `OBInternalAuthorisation1Code` (#14)
- Fix typo in `ExternalPaymentGroupStatus1Code` `INFA` description (#15)

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
