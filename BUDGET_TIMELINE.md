# Budget & Timeline Report
**Project**: Migrasi Frontend HTML → Next.js + Integrasi Backend Python  
**Report Date**: 8 Mei 2026  
**Currency Exchange Rate**: 1 USD = Rp 16.000

---

## Executive Summary

Proyek ini membutuhkan integrasi dengan 3 layanan eksternal untuk mengoptimalkan fungsionalitas aplikasi stock market. Total biaya operasional adalah **Rp 1.604.000 per bulan** atau **Rp 19.248.000 per tahun**.

---

## External Services & Budget Breakdown

### 1️⃣ OpenAI API
**Fungsi Utama**: AI-Powered Analytics & Insights

| Item | Detail |
|------|--------|
| **Monthly Cost** | $20 USD |
| **Conversion** | 1 USD = Rp 16.000 |
| **IDR Equivalent** | Rp 320.000/bulan |
| **Annual Cost** | Rp 3.840.000/tahun |

**Fitur yang Digunakan**:
- ✅ Broker Summary - Ringkasan analisis broker otomatis
- ✅ Buy/Sell Recommendations - Rekomendasi trading berbasis AI
- ✅ Fundamental Summary - Analisis data keuangan mendalam
- ✅ News Sentiment Analysis - Sentiment dari berita pasar
- ✅ Screener Insights - Penjelasan hasil screener
- ✅ Data Scraping Insights - Analisis data yang di-scrape

**Model**: GPT-4o mini (optimized for cost)

---

### 2️⃣ Sectors.app API
**Fungsi Utama**: Fundamental Data & Indonesian Stock Database

| Item | Detail |
|------|--------|
| **Monthly Cost** | $49 USD |
| **Conversion** | 1 USD = Rp 16.000 |
| **IDR Equivalent** | Rp 784.000/bulan |
| **Annual Cost** | Rp 9.408.000/tahun |

**Fitur yang Digunakan**:
- ✅ Data Emitan Indonesia - Database saham IDX lengkap
- ✅ Financial Data - Laporan keuangan & financial statements
- ✅ Shareholder Information - Struktur kepemilikan & pemegang saham
- ✅ Corporate Actions - Dividend, stock split, rights offering
- ✅ Valuation Data - Market cap, P/E ratio, dividend yield
- ✅ Historical Data - Price & fundamental history untuk backtesting

**Use Case**: Primary data source untuk fundamental analysis dan fitur screener aplikasi

---

### 3️⃣ goapi
**Fungsi Utama**: Real-time & Historical Market Data

| Item | Detail |
|------|--------|
| **Monthly Cost** | Rp 500.000 IDR |
| **Currency** | Indonesian Rupiah |
| **IDR Equivalent** | Rp 500.000/bulan |
| **Annual Cost** | Rp 6.000.000/tahun |

**Fitur yang Digunakan**:
- ✅ Real-time Stock Data - Harga bid/ask, volume live IDX
- ✅ Historical Price Data - Candlestick OHLC (1m, 5m, 15m, 1h, daily, weekly, monthly)
- ✅ Index Data - IDX Composite, LQ45, IDX30, IDX80
- ✅ Corporate Actions Events - Stock split, dividend, rights offering
- ✅ Trading Volume & Liquidity - Analisis likuiditas saham
- ✅ Market Statistics - Data untuk sentiment & technical analysis

**Use Case**: Real-time dan historical data untuk technical analysis, charting, dan price tracking

---

## 💰 Total Budget Summary

### Monthly Breakdown
```
OpenAI API        : Rp    320.000
Sectors.app       : Rp    784.000
goapi             : Rp    500.000
                    ─────────────
TOTAL PER BULAN   : Rp  1.604.000
```

### Annual Breakdown
```
OpenAI API        : Rp  3.840.000
Sectors.app       : Rp  9.408.000
goapi             : Rp  6.000.000
                    ─────────────
TOTAL PER TAHUN   : Rp 19.248.000
```

### Quarterly & Semester Breakdown
| Period | Cost |
|--------|------|
| **Per Minggu** | Rp 368.920 |
| **Per Bulan** | Rp 1.604.000 |
| **Per Kuartal** | Rp 4.812.000 |
| **Per Semester** | Rp 9.624.000 |
| **Per Tahun** | Rp 19.248.000 |

---

## Project Timeline

| Phase | Duration | Start | End | Focus |
|-------|----------|-------|-----|-------|
| Phase 1 | 1 week | Week 1 | Week 1 | Planning & Preparation |
| Phase 2 | 2 weeks | Week 2 | Week 3 | Frontend Migration |
| Phase 3 | 1 week | Week 4 | Week 4 | Backend Enhancement |
| Phase 4 | 2 weeks | Week 5 | Week 6 | Frontend-Backend Integration |
| Phase 5 | 2 weeks | Week 7 | Week 8 | Testing & QA |
| **TOTAL** | **~8 weeks** | - | - | Complete Project |

---

## ROI & Cost Justification

### Why These Services?

**OpenAI API ($20/mo)**
- ✅ Minimal cost untuk AI capabilities yang powerful
- ✅ GPT-4o mini optimized untuk cost-efficiency
- ✅ Dapat di-cache untuk menghemat usage
- ✅ Essential untuk value-add features seperti recommendations

**Sectors.app ($49/mo)**
- ✅ Primary data source yang reliable & structured
- ✅ Menggantikan scraping manual yang tidak scalable
- ✅ Comprehensive financial data coverage untuk IDX
- ✅ Shareholder data tidak tersedia di public sources lain

**goapi (Rp 500k/mo)**
- ✅ Real-time market data dengan latency rendah
- ✅ More reliable dari direct website scraping
- ✅ Comprehensive historical data untuk technical analysis
- ✅ Supporting charting & price tracking features

### Combined Value
**Total Monthly Investment: Rp 1.604.000** (~$100 USD)
- 3 data sources yang comprehensive
- AI-powered insights & recommendations
- Real-time + historical market data
- Fundamental + technical analysis capabilities
- ~2-3 developer months saved dari development effort

---

## Implementation Roadmap

### Week 1-2 (Phase 1-2)
- Setup Next.js project
- Configure environment variables untuk API keys
- Setup API integration layer di backend

### Week 3-4 (Phase 2-3)
- Integrate OpenAI API untuk basic features
- Integrate Sectors.app untuk fundamental data
- Setup data caching layer

### Week 5-6 (Phase 4)
- Integrate goapi untuk real-time data
- Complete frontend-backend integration
- Test API rate limits & caching

### Week 7-8 (Phase 5)
- Full testing & optimization
- Monitor API usage & costs
- Production deployment

---

## Cost Control Measures

1. **API Usage Monitoring**
   - Implement request logging untuk tracking usage
   - Alert ketika approaching quota limits
   - Analyze usage patterns untuk optimization

2. **Caching Strategy**
   - Cache fundamental data 1-2 hari (jarang berubah)
   - Cache real-time data 1-5 menit (update regular)
   - Cache AI results 3-7 hari (same query results)

3. **Error Handling & Fallback**
   - Fallback ke cached data jika API down
   - Client-side rate limiting untuk prevent overuse
   - Graceful degradation untuk non-critical features

4. **Regular Reviews**
   - Review API usage monthly
   - Optimize queries untuk efficiency
   - Evaluate alternative providers periodically

---

## Risk & Contingency

| Risk | Impact | Contingency |
|------|--------|-------------|
| API Price Increase | Medium | Budget +10% buffer, evaluate alternatives |
| API Rate Limits | Medium | Implement aggressive caching, queuing system |
| Service Downtime | High | Multi-source fallback, backup data sources |
| Integration Issues | Medium | Early testing phase, vendor support |

---

## Approval Checklist

- [ ] Budget approved: Rp 1.604.000/bulan
- [ ] Timeline approved: ~8 minggu development
- [ ] API vendors approved: OpenAI, Sectors.app, goapi
- [ ] Team resources allocated
- [ ] Development environment ready
- [ ] Ready to start Phase 1

---

## Contact & Support

**For API Integration Issues**:
- OpenAI Support: https://help.openai.com
- Sectors.app Support: https://sectors.app/support
- goapi Support: https://goapi.id/support

**For Project Questions**:
- Project Owner: @fauzannurhikmah
- Repository: https://github.com/fauzannurhikmah/frontend-stock

---

*Report Generated: 8 Mei 2026*  
*Exchange Rate: 1 USD = Rp 16.000*  
*Next Review: Monthly*
