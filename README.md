# Proxy Pricing API Endpoints

**Base URL:** `https://clientserver-06j4.onrender.com/api/pricing`

## Endpoints

### 1. Get All Pricing
```http
GET https://clientserver-06j4.onrender.com/api/pricing/
```
**Returns:**
```json
{
  "datacenter": [DatacenterProxyPricing],
  "ipv6": [IPv6ProxyPricing],
  "mobile": [MobileProxyPricing],
  "residential": [ResidentialProxyPricing],
  "isp": [IspProxyPricing],
  "total_count": number
}
```

### 2. Get Datacenter Pricing
```http
GET https://clientserver-06j4.onrender.com/api/pricing/datacenter
```
**Returns:** Array of:
```json
{
  "id": "string",
  "pricing_type": "fixed" | "tiered",
  "unit_price": number,
  "plan_type": "shared" | "dedicated",
  "data_amount": number | null,
  "ip_amount": number | null,
  "subscription_period": "daily" | "weekly" | "monthly" | "quarterly",
  "is_unlimited": boolean,
  "tiers": [PricingTier] | undefined,
  "created_at": "string",
  "updated_at": "string"
}
```

### 3. Get IPv6 Pricing
```http
GET https://clientserver-06j4.onrender.com/api/pricing/ipv6
```
**Returns:** Array of:
```json
{
  "id": "string",
  "pricing_type": "fixed" | "tiered",
  "unit_price": number,
  "plan_type": "static" | "standard",
  "data_amount": number | null,
  "speed": number,
  "days": number,
  "subscription_period": "daily" | "weekly" | "monthly" | "quarterly",
  "is_unlimited": boolean,
  "tiers": [PricingTier] | undefined,
  "created_at": "string",
  "updated_at": "string"
}
```

### 4. Get ISP Pricing
```http
GET https://clientserver-06j4.onrender.com/api/pricing/isp
```
**Returns:** Single object:
```json
{
  "id": "string",
  "pricing_type": "fixed" | "tiered",
  "unit_price": number,
  "plan_type": "isp",
  "ip_amount": number | null,
  "subscription_period": "daily" | "weekly" | "monthly" | "quarterly",
  "is_unlimited": boolean,
  "tiers": [PricingTier],
  "created_at": "string",
  "updated_at": "string"
}
```

### 5. Get Mobile Pricing
```http
GET https://clientserver-06j4.onrender.com/api/pricing/mobile
```
**Returns:** Single object:
```json
{
  "id": "string",
  "pricing_type": "fixed" | "tiered",
  "unit_price": number,
  "plan_type": "standard",
  "data_amount": number | null,
  "country": string | null,
  "subscription_period": "daily" | "weekly" | "monthly" | "quarterly",
  "is_unlimited": boolean,
  "tiers": [PricingTier],
  "created_at": "string",
  "updated_at": "string"
}
```

### 6. Get Residential Pricing
```http
GET https://clientserver-06j4.onrender.com/api/pricing/residential
```
**Returns:** Array of:
```json
{
  "id": "string",
  "pricing_type": "fixed" | "tiered",
  "unit_price": number,
  "plan_type": "unlimited" | "gb",
  "data_amount": number | null,
  "country": string | null,
  "duration": "Day" | "Week" | "Month" | "Quarter" | "Year",
  "subscription_period": "daily" | "weekly" | "monthly" | "quarterly",
  "is_unlimited": boolean,
  "tiers": [PricingTier] | undefined,
  "created_at": "string",
  "updated_at": "string"
}
```

## PricingTier Structure
```json
{
  "id": "string",
  "min_quantity": number,
  "max_quantity": number | null,
  "unit_price": number,
  "created_at": "string",
  "updated_at": "string"
}
```

## Quick Reference
| Endpoint | Method | Returns |
|----------|--------|---------|
| `/api/pricing/` | GET | All pricing data |
| `/api/pricing/datacenter` | GET | Datacenter pricing array |
| `/api/pricing/ipv6` | GET | IPv6 pricing array |
| `/api/pricing/isp` | GET | Single ISP pricing |
| `/api/pricing/mobile` | GET | Single mobile pricing |
| `/api/pricing/residential` | GET | Residential pricing array | 
