# Purchase Plan URL Configuration

This document outlines the URL structure for the purchase plan pages, designed to be used by external sites for checkout flow.

**Base URL:** `https://panel.floxy.io`

Append all urls with `autoCheckout=true` at the end for automatic navigation to checkout. See full examples below.

---

## Mobile Proxies

-   **Path:** `/purchase-plan/mobile`
-   **Search Params:**
    -   `bandwidth` (or `gb`): The amount of bandwidth in GB. (e.g., `2`)
    -   `coupon`: A discount code. (e.g., `TEST`)
-   **Auto Checkout Param:** `autoCheckout=true`
-   **Full Example with Auto Checkout:**
    ```
    https://panel.floxy.io/purchase-plan/mobile?bandwidth=2&coupon=TEST&autoCheckout=true
    ```

---

## Residential Proxies

### Residential Bandwidth (Price per GB)

-   **Path:** `/purchase-plan/residential`
-   **Search Params:**
    -   `planType`: Must be `price-per-gb`.
    -   `bandwidth` (or `gb`): The amount of bandwidth in GB. (e.g., `5`)
    -   `coupon`: A discount code. (e.g., `SAVE10`)
-   **Auto Checkout Param:** `autoCheckout=true`
-   **Full Example with Auto Checkout:**
    ```
    https://panel.floxy.io/purchase-plan/residential?planType=price-per-gb&bandwidth=5&coupon=SAVE10&autoCheckout=true
    ```

### Residential Unlimited

-   **Path:** `/purchase-plan/residential`
-   **Search Params:**
    -   `planType`: Must be `unlimited`.
    -   `planId`: The ID of the unlimited plan.
        -   1 Month: `res_unlim_1m`
        -   1 Week: `res_unlim_1w`
        -   1 Day: `res_unlim_1d`
    -   `coupon`: A discount code. (e.g., `UNLIMITED20`)
-   **Auto Checkout Param:** `autoCheckout=true`
-   **Full Example with Auto Checkout:**
    ```
    https://panel.floxy.io/purchase-plan/residential?planType=unlimited&planId=res_unlim_1m&coupon=UNLIMITED20&autoCheckout=true
    ```

---

## ISP Proxies

-   **Path:** `/purchase-plan/isp`
-   **Search Params:**
    -   `ip` (or `ipQuantity`): The number of IPs. (e.g., `50`)
    -   `region`: The region code. (e.g., `dtag` for Germany)
    -   `planId`: The ID of the ISP plan.
        -   1 Month: `isp_ip_1m`
        -   1 Quarter: `isp_ip_1q`
        -   1 Year: `isp_ip_1y`
    -   `coupon`: A discount code. (e.g., `ISPDEAL`)
-   **Auto Checkout Param:** `autoCheckout=true`
-   **Full Example with Auto Checkout:**
    ```
    https://panel.floxy.io/purchase-plan/isp?ip=50&region=dtag&planId=isp_ip_1m&coupon=ISPDEAL&autoCheckout=true
    ```

---

## Datacenter Proxies

### Datacenter Shared (Unlimited)

-   **Path:** `/purchase-plan/datacenter`
-   **Search Params:**
    -   `planType`: Must be `shared`.
    -   `planId`: The ID of the shared datacenter plan.
        -   1 Day: `dc_unlim_1d`
        -   1 Week: `dc_unlim_1w`
        -   1 Month: `dc_unlim_1m`
    -   `coupon`: A discount code. (e.g., `SHARED15`)
-   **Auto Checkout Param:** `autoCheckout=true`
-   **Full Example with Auto Checkout:**
    ```
    https://panel.floxy.io/purchase-plan/datacenter?planType=shared&planId=dc_unlim_1m&coupon=SHARED15&autoCheckout=true
    ```

### Datacenter Dedicated (Price Per IP/GB)

-   **Path:** `/purchase-plan/datacenter`
-   **Search Params:**
    -   `planType`: Must be `dedicated`.
    -   `gb` (or `bandwidth`): The amount of bandwidth in GB. (e.g., `250`)
    -   `ip` (or `ipCount`): The number of IPs. (e.g., `100`)
    -   `countries`: A dot-separated list of country codes and IP counts. (e.g., `US50.CA50`)
    -   `coupon`: A discount code. (e.g., `DEDICATED30`)
-   **Auto Checkout Param:** `autoCheckout=true`
-   **Full Example with Auto Checkout:**
    ```
    https://panel.floxy.io/purchase-plan/datacenter?planType=dedicated&gb=250&ip=100&countries=US50.CA50&coupon=DEDICATED30&autoCheckout=true
    ```

---

## IPv6 Proxies

### IPv6 Bandwidth (Price per GB)

-   **Path:** `/purchase-plan/ipv6`
-   **Search Params:**
    -   `planType`: Must be `price-per-gb`.
    -   `bandwidth` (or `gb`): The amount of bandwidth in GB. (e.g., `100`)
    -   `coupon`: A discount code. (e.g., `IPV6SALE`)
-   **Auto Checkout Param:** `autoCheckout=true`
-   **Full Example with Auto Checkout:**
    ```
    https://panel.floxy.io/purchase-plan/ipv6?planType=price-per-gb&bandwidth=100&coupon=IPV6SALE&autoCheckout=true
    ```

### IPv6 Unlimited

-   **Path:** `/purchase-plan/ipv6`
-   **Search Params:**
    -   `planType`: Must be `unlimited`.
    -   `durationKind`: The duration type (`DAY`, `WEEK`, `MONTH`). (e.g., `DAY`)
    -   `durationAmount`: The amount for the duration, which is always `1`. (e.g., `1`)
    -   `speed`: The speed in Mbps. (e.g., `30`)
    -   `coupon`: A discount code. (e.g., `IPV6UNLIMITED`)
-   **Auto Checkout Param:** `autoCheckout=true`
-   **Full Example with Auto Checkout:**
    ```
    https://panel.floxy.io/purchase-plan/ipv6?planType=unlimited&durationKind=DAY&durationAmount=1&speed=30&coupon=IPV6UNLIMITED&autoCheckout=true
    ``` 
