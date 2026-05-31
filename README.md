# API to Power BI (Power Query M)

## Overview
This repository contains Power Query M scripts for:
- retrieving an API access token (`Get_AccessToken`)
- loading and transforming API scan data (`Dataflow`)

## Files
- `Get_AccessToken`: token retrieval query (POST request).
- `Dataflow`: date-based data extraction and transformation query.

## Setup in Power BI
1. Open **Power BI Desktop**.
2. Create two blank queries and paste script content:
   - one query named `Token` (from `Get_AccessToken`)
   - one query for data loading (from `Dataflow`)
3. Replace placeholders:
   - `YOUR_WEBPAGE`
   - `YOUR_BASE64_ENCODED_CREDENTIALS`
   - `your_username` / `your_password`
   - `https://api.example.com`
   - `your_partner_id`
   - shop mappings in `Dataflow`
4. Configure incremental refresh parameters (`RangeStart`, `RangeEnd`) if required.

## Security Notes
- Do not commit real credentials or tokens.
- Use Power BI parameterization and secure credential storage.
- Keep this repo free from exported datasets containing sensitive data.
