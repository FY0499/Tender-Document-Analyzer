# Tender Document Analyzer

I built this n8n workflow to analyze uploaded tender documents, extract important submission requirements and deadlines, and use AI to prepare a Go, No-Go, or Review recommendation.

<img width="442" height="166" alt="Tender Document Analyzer workflow demo" src="https://github.com/user-attachments/assets/23ac67c3-9048-45d3-b916-dd7ba8bd66c3" />

## How it works

1. A user uploads a tender PDF through a form and provides the email address of the person responsible for the submission.
2. The workflow extracts the text from the PDF document.
3. Google Gemini reviews the tender and identifies the main requirements, important deadlines, required submission documents, and special conditions.
4. The AI prepares a recommendation (Go, No-Go, or Review) with its reasoning.
5. JavaScript structures the analysis, then the result is saved to Google Sheets and sent to the responsible person by email.

## Main features

- Tender PDF upload and text extraction.
- Key requirement identification.
- Deadline and required document extraction.
- Special conditions review.
- Go / No-Go / Review recommendation.
- Google Sheets record keeping and email reporting.

## Technologies

n8n, Google Gemini, PDF extraction, AI Agent, Google Sheets, Gmail, JavaScript, and n8n Forms.

## Setup

Import [workflow.json](./workflow.json) into n8n, configure your Gemini, Google Sheets, and Gmail credentials, then connect your tender analysis sheet and set the email address for the person responsible for the submission. Test with a sample tender document first.
