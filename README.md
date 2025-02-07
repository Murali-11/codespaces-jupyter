# Harvested Wood Products (HWP) Carbon Accounting Tool

## Overview
This tool calculates carbon stock changes and CO2 removals from Harvested Wood Products (HWP) following IPCC Guidelines. It implements the production approach for HWP accounting, with options for customizing calculation parameters.

Please change the input and output names as not naming them will overwrite the file 

## Features
- Calculates carbon stocks and stock changes for different HWP categories:
  - Sawnwood
  - Wood-based panels
  - Paper and paperboard
- Separates calculations for domestic consumption and exports
- Provides CO2 removal estimates
- Multiple customization options:
  - Domestic fraction calculation inclusion
  - Initial carbon stock calculation method
  - Inflow timing selection (current/previous year)
  - Custom initial year selection
- Exports results in both CSV and markdown formats

## Prerequisites
- Python 3.x
- Required Python packages:
  - pandas
  - numpy

## Input Data Requirements
The tool expects a CSV file (e.g., 'Austria_FAO.csv') containing annual HWP data with the following columns:
- Production, import, and export quantities for:
  - Industrial roundwood
  - Sawnwood
  - Wood panels
  - Paper and paperboard
  - Wood pulp

## Usage
1. Prepare your input CSV file with the required data
2. Run the script and follow the prompts to:
   - Choose whether to include domestic fraction calculations
   - Select initial carbon stock calculation method
   - Choose inflow timing preference
   - Specify the initial year for calculations

## Output
The tool generates two output files:
1. A CSV file - example> ('Austria_HWP_carbon_estimates_results.csv') containing:
   - Annual carbon stock changes
   - CO2 removals
   - Detailed calculations for domestic and export products

## Calculation Parameters - Can be edited in file 
- Default half-lives:
  - Sawnwood: 35 years
  - Wood-based panels: 25 years
  - Paper: 2 years
- Carbon conversion factors:
  - Sawnwood: 0.229
  - Wood-based panels: 0.269
  - Paper: 0.386

## Methodological Basis
This tool implements the IPCC Guidelines for HWP carbon accounting, using:
- First-order decay (FOD) function for stock changes
- Production approach accounting
- Stock-change method for carbon calculations

## Limitations
- Requires consistent historical data series
- Pre-1961 data is estimated using exponential growth assumptions
- Limited to three main HWP categories

## References
- 2006 IPCC Guidelines for National Greenhouse Gas Inventories
- 2019 Refinement to the 2006 IPCC Guidelines
