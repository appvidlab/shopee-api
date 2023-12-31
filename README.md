# Shopee Indonesia API

Shopee is one of the largest online retailers in Southeast Asia and Latin America, connecting millions of buyers and sellers through its platform. If you want to access Shopee's data, such as products, shops, categories, and reviews, you can use the Shopee API from RapidAPI.

RapidAPI is a platform that provides access to thousands of APIs from various categories, such as ecommerce, travel, sports, entertainment, and more. You can use RapidAPI to find, test, and connect to any API with a single account and a standardized interface.

In this tutorial, we will show you how to use the Shopee API from RapidAPI with Python, PHP, Ruby, and JavaScript examples. You will learn how to:

- Sign up for a RapidAPI account and subscribe to the Shopee API
- Use the Shopee API endpoints to get data from Shopee
- Parse and display the data in your application

Let's get started!

## Prerequisites

To follow this tutorial, you will need:

- A RapidAPI account. You can sign up for free here: [https://rapidapi.com/signup](https://rapidapi.com/auth/sign-up)
- A subscription to the Shopee API. You can subscribe here: [Shopee API](https://rapidapi.com/ptwebsolution/api/shopee-indonesia)

## How to Use the Shopee API Endpoints

The Shopee API from RapidAPI has several endpoints that allow you to get different types of data from Shopee. You can find the full list of endpoints and their documentation here: [Shopee API](https://rapidapi.com/ptwebsolution/api/shopee-indonesia)

To use any of these endpoints, you will need to provide two parameters:

- **x-rapidapi-key**: This is your RapidAPI key that authenticates your requests. You can find it in your RapidAPI dashboard.
- **x-rapidapi-host**: This is the host name of the API. For the Shopee API, it is `shopee-indonesia.p.rapidapi.com`.

### Autocomplete
```
curl --request GET \
	--url 'https://shopee-indonesia.p.rapidapi.com/autocomplete?keyword=tas' \
	--header 'X-RapidAPI-Host: shopee-indonesia.p.rapidapi.com' \
	--header 'X-RapidAPI-Key: SIGN-UP-FOR-KEY'
```
```json
{
  "success": true,
  "message": "success",
  "results": [
    {
      "keyword": "tas selempang wanita",
      "rnum": 0,
      "cat_display_name": "",
      "catid": 0,
      "record_type": 0,
      "data": null,
      "trackingid": "",
      "keyword_source_type": 0,
      "position": 0,
      "search_info": "{\"queue\":\"keyword\",\"scene\":\"1\",\"rewrite\":\"tas\"}",
      "bff_info": "{}"
    },
    ...
  ]
}
```

### Flash Sale
```
curl --request GET \
	--url https://shopee-indonesia.p.rapidapi.com/flash-sale \
	--header 'X-RapidAPI-Host: shopee-indonesia.p.rapidapi.com' \
	--header 'X-RapidAPI-Key: SIGN-UP-FOR-KEY'
```
```json
{
  "success": true,
  "message": "success",
  "results": [
    {
      "itemid": 6890345496,
      "shopid": 409837563,
      "modelids": null,
      "promotionid": 192870873255937,
      "brand_sale_brand_custom_logo": null,
      "image": "id-11134207-7r98t-lot7r3qu26ijba",
      "raw_discount": 0,
      "price_before_discount": 7290000000,
      "flash_sale_type": 0,
      "promo_overlay_image": "sg-11134004-7qvf9-lhiw1s84d5fc9d",
      "promo_images": [
        "id-11134601-7qul0-ljqx01hf3osj48"
      ],
      "price": 7290000000,
      "start_time": 1703955600,
      "end_time": 1703998800,
      "discount": "-64%",
      "flash_catid": 39,
      "reference_item_id": "",
      "is_shop_official": false,
      "flash_sale_stock": 50,
      "name": "【COD】Jovitech Spaker Bluetooth 5.0 Alarm LED Display Ultra Bass S10",
      "item_type": 0,
      "is_shop_preferred": true,
      "promo_name": "【COD】Jovitech Spaker Bluetooth 5.0 Alarm LED Display Ultra Bass S10",
      "stock": 46,
      "hidden_price_display": null,
      "voucher": {
        "min_spend": null,
        "discount_percentage": null,
        "coin_percentage": null,
        "discount_value": null,
        "voucher_code": null,
        "reward_type": null,
        "promotionid": null
      },
      "cat_label": 0,
      "extra_discount_info": null,
      "reminder_count": null,
      "is_mart": false,
      "cats": [
        100535,
        100582,
        100625
      ],
      "is_shopee_food": null,
      "shopee_food_log_id": null,
      "shopee_food_trace": null,
      "shopee_food_discount_id": null,
      "item_rating": {
        "rating_star": 4.658093043532416,
        "rating_counts": [
          32121,
          489,
          323,
          1484,
          5101,
          24724
        ]
      },
      "shopee_food_discount_id_str": null,
      "historical_sold": 70174,
      "promo_overlay_image_desc": "GO Xtra + CashbackXtra",
      "item_tags": null
    },
    ...
  ]
}
```

### Get Shop Info
```
curl --request GET \
	--url https://shopee-indonesia.p.rapidapi.com/shop/yvettery.id \
	--header 'X-RapidAPI-Host: shopee-indonesia.p.rapidapi.com' \
	--header 'X-RapidAPI-Key: SIGN-UP-FOR-KEY'
```
```json
{
  "success": true,
  "message": "success",
  "results": {
    "shopid": 569137110,
    "userid": 569156695,
    "name": "Yvettery",
    "cover": "2053fdda60dec22a99e7487f3a15bcd5",
    "follower_count": 124035,
    "show_official_shop_label": false,
    "is_preferred_plus_seller": true,
    "is_shopee_verified": true,
    "chat_disabled": false,
    "rating_star": 4.562153,
    "has_decoration": true,
    "account": {
      "username": "yvettery.id",
      "following_count": 1,
      "portrait": "7992cedae75bea34319ee98f98e75389",
      "is_seller": true,
      "phone_verified": true,
      "email_verified": true,
      "fbid": "",
      "total_avg_star": 4.562153,
      "feed_account_info": {
        "can_post_feed": true
      },
      "status": 1
    },
    "last_active_time": 1703966789,
    "vacation": false,
    "followed": false,
    "real_url_if_matching_custom_url": "",
    "description": "Selamat Datang di Yverrery~\n🤗kami menjual aksesoris fashion yang paling disukai\n🤗Ayo kunjungi dan ikuti terus toko kami dan dapatkan informasi menarik seperti Giveaway, Voucher Diskon, Flash Sale dan Harga Spesial.\nMengapa Belanja di Yverrery：\n💕Mengutamakan Kualitas produk & Pelayanan\n💕 Harga termurah Semua Produk dijual dg Harga GROSIR\n💕Pengiriman dalam waktu 24 jam Gudang berada di Tangerang\n🌎Fast Response Senin - Minggu : 09.00 - 22.00",
    "item_count": 3846,
    "response_rate": 100,
    "show_video_entry": true,
    "video_entry_info": "10 Video",
    "campaign_hot_deal_discount_min": 30,
    "show_deco_entry": false,
    "shop_rating": {
      "rating_normal": 13751,
      "rating_bad": 6922,
      "rating_good": 177584
    },
    "seller_metrics": {
      "cancellation_visibility": 10,
      "cancellation_warning": 20
    },
    "response_time": 229,
    "ctime": 1634784320,
    "show_tab": {
      "new_arrival_tab": {
        "show_new_arrival_items": true,
        "new_arrival_items_start_ts": 1701446400,
        "latest_item_ctime": 1703917438
      },
      "show_live_tab": false,
      "membership_tab": {
        "show_membership_tab": false,
        "has_join_membership": false
      },
      "show_flash_sale_tab": true
    },
    "toggles": {
      "disable_chat_performance": false
    },
    "shop_tab_meta": {
      "shop_is_non_deco": false,
      "decoration_type": "general_deco",
      "is_high_end_brand_shop": false
    },
    "block_cb_user": false,
    "video_rn_jump_url": "rn/@shopee-rn/lucky-video/BGB_VIDEO_PAGE_SHOP_VIDEO?fromSource=shop_entry&shopId=569137110&userId=569156695",
    "background_color": "",
    "highlight_color": "",
    "brand_day_end_time": 0
  }
}
```

For list of endpoint and complete documentation, you can visit [Shopee API](https://rapidapi.com/ptwebsolution/api/shopee-indonesia)
