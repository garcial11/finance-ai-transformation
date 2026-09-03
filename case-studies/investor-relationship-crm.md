# Investor Relationship CRM

> Sanitized case study. No investor information, ownership records, commitments, documents, prompts, user mappings, API credentials, production code, or proprietary business logic is shared.

## Business problem

Investor conversations, ownership context, documents, and follow-up commitments often live across email, notes, spreadsheets, and task-management systems. This fragmentation makes it difficult to preserve relationship history and ensure that promises become accountable actions.

## Solution

A lightweight investor CRM built on Google Workspace centralizes relationship activity and connects each interaction to the relevant investor and investment vehicle. Users can log conversations, track relationship context, attach supporting files, retrieve filtered history, and convert commitments into monday.com tasks.

~~~mermaid
flowchart TD
    A[Investor interaction] --> B[AI-assisted draft]
    B --> C[Human review and edit]
    C --> D[Relationship history]
    C --> E[Follow-up commitment]
    E --> F[monday.com task]
    D --> G[Filtered history and report]
~~~

AI assists with drafting structured summaries from rough notes or email text. The proposed content remains editable, and an AI-service interruption never blocks the underlying record from being saved.

## Business impact

- Consolidated investor interactions and relationship history into one controlled workflow.
- Connected commitments made in conversations to assigned, dated follow-up tasks.
- Reduced the effort required to turn rough notes into structured summaries.
- Preserved human review over every AI-generated draft.
- Improved access to filtered history and supporting documents.
- Maintained historical continuity when investor roles or positions changed.

## Control design

- Human approval before saving AI-assisted content
- AI drafting separated from the system of record
- Graceful operation when the AI service is unavailable
- Controlled document storage and indexing
- Explicit relationship and position history
- One accountable task per commitment workflow
- Filtered reporting without exposing source records broadly

## Technology pattern

Google Apps Script web application, Google Sheets, Google Drive, monday.com API, large language model, structured drafting, local browser caching, incremental synchronization, and PDF reporting.

## Portfolio boundary

Investor identities, investment vehicles, ownership positions, interaction records, commitments, documents, prompts, field mappings, board configuration, access rules, internal identifiers, and production implementation remain private.
