# Project Timeline: Migrasi Frontend HTML → Next.js + Integrasi Backend Python

## Overview
Migrasi aplikasi frontend dari HTML ke Next.js dan integrasi dengan backend Python (scrap-idx-fundamental).

---

## Phase 1: Planning & Preparation
**Durasi**: ~1 minggu

### Tasks
- [ ] Audit struktur HTML saat ini di `frontend-stock`
- [ ] Finalisasi tech stack (Next.js, TypeScript, React Query, dll)
- [ ] Setup repository structure untuk Next.js project
- [ ] Configure environment variables (.env.local template)
- [ ] Setup development environment (Node.js, npm/yarn)
- [ ] Dokumentasi API dari backend (scrap-idx-fundamental)

---

## Phase 2: Frontend Migration
**Durasi**: ~2 minggu

### Tasks
- [ ] Initialize Next.js project dengan TypeScript
- [ ] Setup folder structure:
  - `app/` - App Router components
  - `components/` - Reusable React components
  - `lib/` - Utilities & helpers
  - `hooks/` - Custom React hooks
  - `types/` - TypeScript interfaces
- [ ] Migrate HTML pages menjadi React components
- [ ] Setup global styles (Tailwind CSS / CSS Modules)
- [ ] Implement responsive design
- [ ] Configure routing

### Deliverables
- Next.js app berjalan dengan semua halaman terintegrasi
- Components reusable dan modular

---

## Phase 3: Backend Enhancement
**Durasi**: ~1 minggu

### Tasks
- [ ] Review struktur Flask di `scrap-idx-fundamental`
- [ ] Add CORS support untuk frontend integration
- [ ] Standardize API response format (success/error handling)
- [ ] Add request validation dengan Pydantic
- [ ] Enhance error messages & HTTP status codes
- [ ] Add rate limiting untuk API endpoints
- [ ] Implement logging system

### Deliverables
- Backend siap untuk menerima request dari frontend
- API dokumentasi clear (Swagger/OpenAPI)

---

## Phase 4: Frontend-Backend Integration
**Durasi**: ~2 minggu

### Tasks
- [ ] Setup API client di frontend (axios/fetch wrapper)
- [ ] Implement authentication/authorization flow
- [ ] Create custom hooks untuk API calls:
  - `useFundamental()` - fetch fundamental data
  - `useStockSearch()` - search saham
  - dll
- [ ] Integrate form submissions ke API
- [ ] Add loading states & error handling
- [ ] Implement caching strategy (React Query / SWR)
- [ ] Add success/error notifications (toast)

### Deliverables
- Frontend fully connected dengan backend
- All features functional

---

## Phase 5: Testing & Quality Assurance
**Durasi**: ~2 minggu

### Frontend Tests
- [ ] Unit tests (React components)
- [ ] Integration tests (API calls)
- [ ] E2E tests (user workflows)
- [ ] Performance testing & optimization

### Backend Tests
- [ ] Unit tests (scraper, API endpoints)
- [ ] Integration tests (database, external APIs)
- [ ] Load testing

### QA
- [ ] Manual testing semua features
- [ ] Cross-browser compatibility testing
- [ ] Security audit (XSS, CSRF, injection)
- [ ] Code review & cleanup
- [ ] Documentation finalization

### Deliverables
- Test coverage >= 80%
- Bug tracking & fix prioritization
- Performance baseline established

---

## Effort Estimation
- **Total**: ~8 minggu development
- **Team**: ~2 developer (1 frontend, 1 backend) atau 1 full-stack
- **Working Days**: ~40-50 hari
- **Contingency**: +20% (buffer untuk unexpected issues)

---

## Tech Stack

### Frontend
- **Framework**: Next.js 14+
- **Language**: TypeScript
- **UI Library**: React 18+
- **Styling**: Tailwind CSS
- **State Management**: React Query / SWR
- **HTTP Client**: Axios
- **Testing**: Jest + React Testing Library

### Backend
- **Framework**: Flask
- **Language**: Python 3.9+
- **Database**: (as needed)
- **API**: REST API
- **Scraping**: BeautifulSoup4
- **AI Integration**: OpenAI API

---

## Key Milestones
1. ✅ Phase 1 Complete → Tech stack approved
2. ✅ Phase 2 Complete → Frontend skeleton ready
3. ✅ Phase 3 Complete → Backend enhanced & documented
4. ✅ Phase 4 Complete → Integration complete & functional
5. ✅ Phase 5 Complete → Ready for production launch

---

## Risks & Mitigation

| Risk | Impact | Mitigation |
|------|--------|-----------|
| Data migration complexity | High | Early testing & documentation |
| API compatibility issues | Medium | Early integration testing |
| Performance issues at scale | Medium | Load testing & optimization early |
| Team member unavailability | Medium | Clear documentation & knowledge sharing |

---

## 💰 Budget & External Tools

**Currency Exchange Rate**: 1 USD = Rp 16.000

### 1️⃣ OpenAI API - $20/bulan

| Item | Detail |
|------|--------|
| **Cost** | $20 USD |
| **IDR Equivalent** | **Rp 320.000/bulan** |

**Digunakan untuk**:
- Broker Summary - Ringkasan analisis broker otomatis
- Buy/Sell Recommendations - Rekomendasi trading berbasis AI
- Fundamental Summary - Analisis data keuangan mendalam
- News Sentiment Analysis - Sentiment dari berita pasar
- Screener Insights - Penjelasan hasil screener

---

### 2️⃣ Sectors.app API - $49/bulan

| Item | Detail |
|------|--------|
| **Cost** | $49 USD |
| **IDR Equivalent** | **Rp 784.000/bulan** |

**Digunakan untuk**:
- Data Emitan Indonesia - Database saham IDX lengkap
- Financial Data - Laporan keuangan & financial statements
- Shareholder Information - Struktur kepemilikan & pemegang saham
- Corporate Actions - Dividend, stock split, rights offering
- Valuation Data - Market cap, P/E ratio, dividend yield

---

### 3️⃣ goapi - Rp 500.000/bulan

| Item | Detail |
|------|--------|
| **Cost** | Rp 500.000 |
| **IDR Equivalent** | **Rp 500.000/bulan** |

**Digunakan untuk**:
- Real-time Stock Data - Harga bid/ask, volume live IDX
- Historical Price Data - Candlestick OHLC untuk technical analysis
- Index Data - IDX Composite, LQ45, IDX30, IDX80
- Market Statistics - Data untuk sentiment analysis

---

## 💵 Total Budget Per Bulan

```
OpenAI API        : Rp    320.000
Sectors.app       : Rp    784.000
goapi             : Rp    500.000
                    ─────────────
TOTAL PER BULAN   : Rp  1.604.000 (~$100 USD)
```

---

## Next Steps
1. Approve timeline & tech stack
2. Setup development environment
3. Create detailed task board (GitHub Issues/Projects)
4. Register API keys untuk ketiga external services
5. Start Phase 1 activities
