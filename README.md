curalink/
├── backend/               ← Node.js + Express
│   ├── server.js
│   ├── models/Session.js          (MongoDB schema)
│   ├── routes/chat.js             (main POST /api/chat)
│   ├── routes/sessions.js
│   ├── routes/research.js
│   └── services/
│       ├── pubmedService.js       (PubMed esearch + efetch)
│       ├── openAlexService.js     (OpenAlex 100 results)
│       ├── clinicalTrialsService.js (ClinicalTrials.gov v2)
│       ├── rankingService.js      (multi-factor scoring)
│       ├── llmService.js          (Ollama/Mistral + fallback)
│       └── researchOrchestrator.js (ties it all together)
├── frontend/              ← React 18
│   └── src/
│       ├── ChatWindow.js          (chat UI + suggestions)
│       ├── Sidebar.js             (session history)
│       ├── ResearchPanel.js       (publications + trial cards)
│       └── ContextModal.js        (patient name/disease/location)
├── docker-compose.yml
└── README.md              (architecture, pipeline, deployment guide)
