# oichin-web

Tài liệu kỹ thuật, cấu trúc Schema.org và scripts tối ưu hóa cho website [oichin.net](https://oichin.net).

---

## 📁 Cấu Trúc Repository

```
oichin-web/
├── schema/          # Schema.org JSON-LD structures
│   ├── organization.json
│   ├── local-business.json
│   ├── product.json
│   └── breadcrumb.json
├── scripts/         # Web optimization scripts
│   ├── seo/
│   └── performance/
└── docs/            # Deployment documentation
    ├── setup.md
    └── deployment.md
```

---

## 🏗️ Schema.org Implementation

Website oichin.net sử dụng các Schema.org types sau:

| Schema Type | Mục đích | URL áp dụng |
|---|---|---|
| `Organization` | Thông tin tổ chức Oichin | Toàn site |
| `LocalBusiness` | NAP + địa chỉ cửa hàng | Homepage |
| `Product` | Thông tin sản phẩm | Product pages |
| `BreadcrumbList` | Điều hướng phân cấp | Tất cả pages |
| `FAQPage` | Câu hỏi thường gặp | Blog, landing pages |
| `WebSite` | Sitelinks search box | Homepage |

---

## 📍 NAP (Name · Address · Phone)

Thông tin NAP chuẩn dùng trong Schema.org và toàn bộ entity network:

```json
{
  "@type": "LocalBusiness",
  "name": "Oichin",
  "url": "https://oichin.net",
  "telephone": "+84836665511",
  "email": "Contact@oichin.net",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "27-29 Đường Kênh Tân Hóa",
    "addressLocality": "Phường Tân Thới Hoà, Quận Tân Phú",
    "addressRegion": "TP. Hồ Chí Minh",
    "postalCode": "700000",
    "addressCountry": "VN"
  },
  "geo": {
    "@type": "GeoCoordinates",
    "latitude": "10.7893",
    "longitude": "106.6296"
  }
}
```

---

## ⚙️ Tech Stack

| Layer | Technology |
|---|---|
| Backend |  PHP |
| Template | Blade |
| Database | MySQL |
| Cache | Redis |
| CDN | Cloudflare |
| Analytics | Google Analytics 4 |
| Search Console | Google Search Console |

---

## 🔗 Sitemap & Indexing

| Sitemap | Nội dung |
|---|---|
| [oichin.net/sitemap.xml](https://oichin.net/sitemap.xml) | Sitemap index — tổng hợp toàn bộ sitemaps |
| [oichin.net/productcate-sitemap.xml](https://oichin.net/productcate-sitemap.xml) | Danh mục sản phẩm |
| [oichin.net/product-sitemap.xml](https://oichin.net/product-sitemap.xml) | Trang sản phẩm chi tiết |
| [oichin.net/blogcate-sitemap.xml](https://oichin.net/blogcate-sitemap.xml) | Danh mục bài viết |
| [oichin.net/blog-sitemap.xml](https://oichin.net/blog-sitemap.xml) | Bài viết blog |

---

## 📊 Core Web Vitals Target

| Metric | Target | Hiện tại |
|---|---|---|
| LCP (Largest Contentful Paint) | < 2.5s | — |
| FID (First Input Delay) | < 100ms | — |
| CLS (Cumulative Layout Shift) | < 0.1 | — |
| TTFB (Time to First Byte) | < 800ms | — |

---

## 📝 Changelog

| Ngày | Thay đổi |
|---|---|
| 2026-01 | Initial commit — Schema.org structures |
| 2026-02 | Thêm LocalBusiness schema |
| 2026-04 | Cập nhật sitemap priority |

---

*Maintained by [oichinnet](https://github.com/oichinnet) · [oichin.net](https://oichin.net)*
