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

## Budget & External Tools

### 1. OpenAI API - $20/bulan

**Tujuan Penggunaan:**
- **Broker Summary**: Generate ringkasan otomatis dari analisis broker untuk setiap saham, ekstrak insight penting dari laporan analis
- **Buy/Sell Recommendation**: Menganalisis tren historis, fundamental data, dan sentiment market untuk memberikan rekomendasi buy/sell/hold
- **Fundamental Summary**: Membuat ringkasan komprehensif dari data fundamental (PE ratio, ROE, debt-to-equity, dll) dengan analisis mendalam
- **News Sentiment Analysis**: Menganalisis sentiment dari berita pasar dan press release untuk prediksi price movement
- **Screener Insights**: Interpretasi hasil screener saham dengan insights tentang mengapa saham memenuhi kriteria
- **Data Scraping Insights**: Menganalisis data yang di-scrape dan mengekstrak informasi meaningful dari raw data

**Model yang Digunakan**: GPT-4o mini (cost-effective untuk batch processing)

**API Keys Required**: `OPENAI_API_KEY` di backend

---

### 2. Sectors.app API - $49/bulan

**Tujuan Penggunaan:**
- **Data Emitan Indonesia**: Akses database lengkap saham-saham yang terdaftar di IDX (Indonesia Stock Exchange) dengan informasi perusahaan, sektor, dan sub-sektor
- **Financial Data**: Dapatkan financial statements (laporan keuangan), quarterly/annual reports, balance sheet, income statement
- **Shareholder Information**: Data lengkap pemegang saham utama, struktur kepemilikan, perubahan kepemilikan institusional
- **Corporate Actions**: Informasi tentang dividend, stock split, corporate restructuring, rights offering, dll
- **Valuation Data**: Market cap, trading volume, P/E ratio, dividend yield, dan metrics valuasi lainnya
- **Historical Data**: Price history, fundamental metrics history untuk analysis dan backtesting

**Use Case**: Primary data source untuk fundamental analysis dan screener fitur aplikasi. Menggantikan scraping manual dengan API yang lebih reliable dan structured.

**API Keys Required**: `SECTORS_API_KEY` di backend

**Documentation**: Lihat di https://sectors.app/docs untuk endpoint lengkap

---

### 3. goapi - Rp 500.000/bulan

**Tujuan Penggunaan:**
- **Real-time Stock Market Data**: Akses data pasar saham IDX secara real-time (harga bid/ask, volume, dll)
- **Historical Price Data**: Candlestick data (OHLC - Open, High, Low, Close) untuk berbagai timeframe (1m, 5m, 15m, 1h, daily, weekly, monthly)
- **Index Data**: Tracking IDX indices (IDX Composite, LQ45, IDX30, IDX80, dll) dengan real-time updates
- **Corporate Actions Events**: Stock split, dividend distribution, rights offering, bonus shares
- **Trading Volume & Liquidity Data**: Analisis volume trading dan likuiditas untuk setiap saham
- **Market Statistics**: Aggregate market data untuk sentiment dan technical analysis

**Use Case**: Real-time dan historical data untuk technical analysis, charting, dan price tracking. API yang lebih cepat dan reliable dibanding direct scraping untuk data yang sering berubah.

**API Keys Required**: `GOAPI_KEY` di backend

**Documentation**: Lihat di https://goapi.id/docs untuk endpoint lengkap dan rate limits

---

## Integration Architecture

```
Frontend (Next.js)
    ↓
Backend (Flask)
    ├─→ OpenAI API (untuk AI analysis)
    ├─→ Sectors.app (untuk fundamental data & shareholder info)
    └─→ goapi (untuk real-time market data & history)
```

**Caching Strategy**:
- **Fundamental Data** (Sectors.app): Cache 1-2 hari (berubah jarang)
- **Real-time Data** (goapi): Cache 1-5 menit (update regular)
- **AI Analysis Results** (OpenAI): Cache 3-7 hari (untuk same stock query)

**Error Handling**:
- Implement fallback ke cached data jika API down
- Rate limiting client-side untuk menghindari API quota exceeded
- Monitoring & alerts untuk API health

---

## Next Steps
1. Approve timeline & tech stack
2. Setup development environment
3. Create detailed task board (GitHub Issues/Projects)
4. Register API keys untuk ketiga external services
5. Start Phase 1 activities
