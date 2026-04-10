# Job Hunt Agent - OpenAI Secure Defaults

This version follows the transcript flow:
1. LinkedIn search URL input
2. Apify LinkedIn jobs scrape
3. Batch loop over jobs
4. Read base resume from Google Docs
5. Relevance check with OpenAI
6. Tailor resume
7. Convert HTML to markdown
8. Create a private Google Doc
9. Append job + resume URL to tracker sheet

## Defaults used
- AI provider: OpenAI
- Model: gpt-4.1-mini
- Search URL: AI Engineer in the United States, remote-friendly query
- Security posture: private Google Drive folder only
- Tracker schema: same columns as the transcript/video

## Replace these values in `Workflow Config`
- `REPLACE_WITH_GOOGLE_DOC_ID`
- `REPLACE_WITH_GOOGLE_SHEET_ID`
- `REPLACE_WITH_PRIVATE_DRIVE_FOLDER_ID`
- `REPLACE_WITH_APIFY_LINKEDIN_JOBS_ACTOR`
- `REPLACE_WITH_YOUR_NAME`

## Credentials to reconnect
- Apify
- Google Docs
- Google Sheets / Drive
- OpenAI

## Important note
The Google Docs formatting step can still need light adjustment depending on your n8n version. If the markdown update node does not render nicely, switch that step to a Google Docs `batchUpdate` HTTP Request approach.