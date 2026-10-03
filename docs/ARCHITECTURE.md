# Ecommerce OS Architecture

Ecommerce OS is a portfolio-grade commerce operations command center.

## Current architecture

Browser → static application → local demo data.

- HTML: semantic application shell
- CSS: responsive design system
- JavaScript: navigation, filtering, demo state and export
- SVG: lightweight analytics visualization

## Production target

```
Browser
  ↓
Web App
  ↓
API Gateway
  ├── Inventory Service
  ├── Order Service
  ├── Procurement Service
  ├── Supplier Service
  └── Analytics Service
        ↓
     PostgreSQL
```

Core entities: Product, InventorySnapshot, Supplier, PurchaseOrder, CustomerOrder, OrderLine, Quote, Warehouse and AuditEvent.

The static prototype deliberately separates operational domains so it can evolve into a full-stack system without redesigning the information architecture.