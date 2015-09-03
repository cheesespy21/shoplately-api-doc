# Category

## Get All Categories

```shell
curl "http://shoplately.com/api/v1/categories" \
  -H "X-SHOPLATELY-API-KEY: meowmeowmeow"
```

> The above command returns JSON structured like this:

```json
[
  {
    "depth": 1,
    "id": 18,
    "name": "Accessories",
    "numProduct": 32357,
    "urlRoute": "accessories",
    "subCategory": [
      {
        "depth": 1,
        "id": 20,
        "name": "Bags",
        "numProduct": 1628,
        "urlRoute": "bags",
        "subCategory": [
          {
            "depth": 1,
            "id": 41,
            "name": "Backpacks",
            "numProduct": 54,
            "urlRoute": "bags-backpacks",
            "subCategory": []
          },
          {
            "depth": 1,
            "id": 56,
            "name": "Handbag Hangers",
            "numProduct": 12,
            "urlRoute": "bags-handbag-hangers",
            "subCategory": []
          },
          {
            "depth": 1,
            "id": 39,
            "name": "Handbags",
            "numProduct": 636,
            "urlRoute": "bags-handbags",
            "subCategory": []
          },
          {
            "depth": 1,
            "id": 46,
            "name": "Luggage",
            "numProduct": 8,
            "urlRoute": "bags-luggage",
            "subCategory": []
          },
          {
            "depth": 1,
            "id": 45,
            "name": "Make Up Bags",
            "numProduct": 21,
            "urlRoute": "bags-make-up-bags",
            "subCategory": []
          },
          {
            "depth": 1,
            "id": 42,
            "name": "Small Bags & Clutches",
            "numProduct": 631,
            "urlRoute": "bags-small-bags-and-clutches",
            "subCategory": []
          },
          {
            "depth": 1,
            "id": 40,
            "name": "Totes",
            "numProduct": 105,
            "urlRoute": "bags-totes",
            "subCategory": []
          },
          {
            "depth": 1,
            "id": 44,
            "name": "Wallets",
            "numProduct": 130,
            "urlRoute": "bags-wallets",
            "subCategory": []
          }
        ]
      },
      {
        "depth": 1,
        "id": 26,
        "name": "Beauty",
        "numProduct": 538,
        "urlRoute": "beauty",
        "subCategory": []
      },
      {
        "depth": 1,
        "id": 25,
        "name": "Belts",
        "numProduct": 276,
        "urlRoute": "belts",
        "subCategory": []
      },
      {
        "depth": 1,
        "id": 54,
        "name": "Cold Weather",
        "numProduct": 23,
        "urlRoute": "cold-weather",
        "subCategory": []
      },
      {
        "depth": 1,
        "id": 23,
        "name": "Gloves",
        "numProduct": 49,
        "urlRoute": "gloves",
        "subCategory": []
      },
      {
        "depth": 1,
        "id": 27,
        "name": "Hair Accessories",
        "numProduct": 837,
        "urlRoute": "hair-accessories",
        "subCategory": []
      },
      {
        "depth": 1,
        "id": 21,
        "name": "Hats",
        "numProduct": 128,
        "urlRoute": "hats",
        "subCategory": []
      },
      {
        "depth": 1,
        "id": 19,
        "name": "Jewelry",
        "numProduct": 26638,
        "urlRoute": "jewelry",
        "subCategory": [
          {
            "depth": 1,
            "id": 60,
            "name": "Anklets",
            "numProduct": 20,
            "urlRoute": "jewelry-anklets",
            "subCategory": []
          },
          {
            "depth": 1,
            "id": 63,
            "name": "Body Jewelry",
            "numProduct": 269,
            "urlRoute": "jewelry-body-jewelry",
            "subCategory": []
          },
          {
            "depth": 1,
            "id": 48,
            "name": "Bracelets",
            "numProduct": 6065,
            "urlRoute": "jewelry-bracelets",
            "subCategory": []
          },
          {
            "depth": 1,
            "id": 53,
            "name": "Earrings",
            "numProduct": 5932,
            "urlRoute": "jewelry-earrings",
            "subCategory": []
          },
          {
            "depth": 1,
            "id": 52,
            "name": "Jewelry Storage",
            "numProduct": 25,
            "urlRoute": "jewelry-jewelry-storage",
            "subCategory": []
          },
          {
            "depth": 1,
            "id": 47,
            "name": "Necklaces",
            "numProduct": 8604,
            "urlRoute": "jewelry-necklaces",
            "subCategory": []
          },
          {
            "depth": 1,
            "id": 51,
            "name": "Pins",
            "numProduct": 26,
            "urlRoute": "jewelry-pins",
            "subCategory": []
          },
          {
            "depth": 1,
            "id": 49,
            "name": "Rings",
            "numProduct": 3211,
            "urlRoute": "jewelry-rings",
            "subCategory": []
          },
          {
            "depth": 1,
            "id": 50,
            "name": "Watches",
            "numProduct": 2451,
            "urlRoute": "jewelry-watches",
            "subCategory": []
          }
        ]
      },
      {
        "depth": 1,
        "id": 55,
        "name": "Key Chains",
        "numProduct": 55,
        "urlRoute": "key-chains",
        "subCategory": []
      },
      {
        "depth": 1,
        "id": 58,
        "name": "Neckwear",
        "numProduct": 45,
        "urlRoute": "neckwear",
        "subCategory": []
      },
      {
        "depth": 1,
        "id": 22,
        "name": "Scarves",
        "numProduct": 1026,
        "urlRoute": "scarves",
        "subCategory": []
      },
      {
        "depth": 1,
        "id": 62,
        "name": "Shoe Accessories",
        "numProduct": 30,
        "urlRoute": "shoe-accessories",
        "subCategory": []
      },
      {
        "depth": 1,
        "id": 59,
        "name": "Style Solutions",
        "numProduct": 51,
        "urlRoute": "style-solutions",
        "subCategory": []
      },
      {
        "depth": 1,
        "id": 28,
        "name": "Sunglasses",
        "numProduct": 279,
        "urlRoute": "sunglasses",
        "subCategory": []
      },
      {
        "depth": 1,
        "id": 57,
        "name": "Tech Accessories",
        "numProduct": 690,
        "urlRoute": "tech-accessories",
        "subCategory": []
      },
      {
        "depth": 1,
        "id": 24,
        "name": "Tights & Socks",
        "numProduct": 59,
        "urlRoute": "tights-and-socks",
        "subCategory": []
      },
      {
        "depth": 1,
        "id": 29,
        "name": "Umbrellas",
        "numProduct": 0,
        "urlRoute": "umbrellas",
        "subCategory": []
      }
    ]
  },
  {
    "depth": 1,
    "id": 248,
    "name": "Clothing",
    "numProduct": 2019,
    "urlRoute": "clothing",
    "subCategory": [
      {
        "depth": 1,
        "id": 254,
        "name": "Denim",
        "numProduct": 16,
        "urlRoute": "denim",
        "subCategory": [
          {
            "depth": 1,
            "id": 281,
            "name": "Flare",
            "numProduct": 1,
            "urlRoute": "denim-flare",
            "subCategory": []
          },
          {
            "depth": 1,
            "id": 284,
            "name": "High-Waisted",
            "numProduct": 1,
            "urlRoute": "denim-high-waisted",
            "subCategory": []
          },
          {
            "depth": 1,
            "id": 287,
            "name": "Skinny",
            "numProduct": 10,
            "urlRoute": "denim-skinny",
            "subCategory": []
          },
          {
            "depth": 1,
            "id": 290,
            "name": "Straight Leg",
            "numProduct": 1,
            "urlRoute": "denim-straight-leg",
            "subCategory": []
          }
        ]
      },
      {
        "depth": 1,
        "id": 251,
        "name": "Dresses",
        "numProduct": 718,
        "urlRoute": "dresses",
        "subCategory": [
          {
            "depth": 1,
            "id": 293,
            "name": "Casual",
            "numProduct": 420,
            "urlRoute": "dresses-casual",
            "subCategory": []
          },
          {
            "depth": 1,
            "id": 296,
            "name": "Cocktail",
            "numProduct": 166,
            "urlRoute": "dresses-cocktail",
            "subCategory": []
          },
          {
            "depth": 1,
            "id": 299,
            "name": "High-Low",
            "numProduct": 29,
            "urlRoute": "dresses-high-low",
            "subCategory": []
          },
          {
            "depth": 1,
            "id": 302,
            "name": "Maxi",
            "numProduct": 61,
            "urlRoute": "dresses-maxi",
            "subCategory": []
          }
        ]
      },
      {
        "depth": 1,
        "id": 257,
        "name": "Jackets & Coats",
        "numProduct": 137,
        "urlRoute": "jackets-and-coats",
        "subCategory": [
          {
            "depth": 1,
            "id": 305,
            "name": "Blazer",
            "numProduct": 42,
            "urlRoute": "jackets-and-coats-blazer",
            "subCategory": []
          },
          {
            "depth": 1,
            "id": 308,
            "name": "Denim",
            "numProduct": 8,
            "urlRoute": "jackets-and-coats-denim",
            "subCategory": []
          },
          {
            "depth": 1,
            "id": 311,
            "name": "Leather",
            "numProduct": 15,
            "urlRoute": "jackets-and-coats-leather",
            "subCategory": []
          },
          {
            "depth": 1,
            "id": 314,
            "name": "Trench",
            "numProduct": 31,
            "urlRoute": "jackets-and-coats-trench",
            "subCategory": []
          },
          {
            "depth": 1,
            "id": 317,
            "name": "Vest",
            "numProduct": 11,
            "urlRoute": "jackets-and-coats-vest",
            "subCategory": []
          }
        ]
      },
      {
        "depth": 1,
        "id": 263,
        "name": "Leggings",
        "numProduct": 80,
        "urlRoute": "leggings",
        "subCategory": []
      },
      {
        "depth": 1,
        "id": 260,
        "name": "Pants",
        "numProduct": 84,
        "urlRoute": "pants",
        "subCategory": [
          {
            "depth": 1,
            "id": 320,
            "name": "Casual",
            "numProduct": 72,
            "urlRoute": "pants-casual",
            "subCategory": []
          },
          {
            "depth": 1,
            "id": 323,
            "name": "Trouser",
            "numProduct": 8,
            "urlRoute": "pants-trouser",
            "subCategory": []
          }
        ]
      },
      {
        "depth": 1,
        "id": 266,
        "name": "Rompers & Jumpsuits",
        "numProduct": 38,
        "urlRoute": "rompers-and-jumpsuits",
        "subCategory": []
      },
      {
        "depth": 1,
        "id": 269,
        "name": "Shorts",
        "numProduct": 47,
        "urlRoute": "shorts",
        "subCategory": [
          {
            "depth": 1,
            "id": 326,
            "name": "Denim",
            "numProduct": 10,
            "urlRoute": "shorts-denim",
            "subCategory": []
          },
          {
            "depth": 1,
            "id": 329,
            "name": "High-Waisted",
            "numProduct": 12,
            "urlRoute": "shorts-high-waisted",
            "subCategory": []
          },
          {
            "depth": 1,
            "id": 332,
            "name": "Trouser",
            "numProduct": 9,
            "urlRoute": "shorts-trouser",
            "subCategory": []
          }
        ]
      },
      {
        "depth": 1,
        "id": 272,
        "name": "Skirts",
        "numProduct": 118,
        "urlRoute": "skirts",
        "subCategory": [
          {
            "depth": 1,
            "id": 335,
            "name": "High-Low",
            "numProduct": 29,
            "urlRoute": "skirts-high-low",
            "subCategory": []
          },
          {
            "depth": 1,
            "id": 341,
            "name": "Maxi",
            "numProduct": 18,
            "urlRoute": "skirts-maxi",
            "subCategory": []
          },
          {
            "depth": 1,
            "id": 338,
            "name": "Mini",
            "numProduct": 39,
            "urlRoute": "skirts-mini",
            "subCategory": []
          },
          {
            "depth": 1,
            "id": 344,
            "name": "Pencil",
            "numProduct": 14,
            "urlRoute": "skirts-pencil",
            "subCategory": []
          }
        ]
      },
      {
        "depth": 1,
        "id": 275,
        "name": "Sweaters & Knits",
        "numProduct": 229,
        "urlRoute": "sweaters-and-knits",
        "subCategory": [
          {
            "depth": 1,
            "id": 347,
            "name": "Cardigan",
            "numProduct": 60,
            "urlRoute": "sweaters-and-knits-cardigan",
            "subCategory": []
          },
          {
            "depth": 1,
            "id": 350,
            "name": "Kimono",
            "numProduct": 0,
            "urlRoute": "sweaters-and-knits-kimono",
            "subCategory": []
          },
          {
            "depth": 1,
            "id": 353,
            "name": "Sweater & Tunic",
            "numProduct": 138,
            "urlRoute": "sweaters-and-knits-sweater-and-tunic",
            "subCategory": []
          },
          {
            "depth": 1,
            "id": 356,
            "name": "Sweatshirts & Hoodies",
            "numProduct": 13,
            "urlRoute": "sweaters-and-knits-sweatshirts-and-hoodies",
            "subCategory": []
          }
        ]
      },
      {
        "depth": 1,
        "id": 278,
        "name": "Tops",
        "numProduct": 550,
        "urlRoute": "tops",
        "subCategory": [
          {
            "depth": 1,
            "id": 359,
            "name": "Blouse",
            "numProduct": 154,
            "urlRoute": "tops-blouse",
            "subCategory": []
          },
          {
            "depth": 1,
            "id": 362,
            "name": "Cami",
            "numProduct": 6,
            "urlRoute": "tops-cami",
            "subCategory": []
          },
          {
            "depth": 1,
            "id": 365,
            "name": "Casual",
            "numProduct": 71,
            "urlRoute": "tops-casual",
            "subCategory": []
          },
          {
            "depth": 1,
            "id": 368,
            "name": "Crop Top",
            "numProduct": 74,
            "urlRoute": "tops-crop-top",
            "subCategory": []
          },
          {
            "depth": 1,
            "id": 371,
            "name": "Dressy",
            "numProduct": 39,
            "urlRoute": "tops-dressy",
            "subCategory": []
          },
          {
            "depth": 1,
            "id": 374,
            "name": "Tank Top",
            "numProduct": 47,
            "urlRoute": "tops-tank-top",
            "subCategory": []
          },
          {
            "depth": 1,
            "id": 377,
            "name": "Tees",
            "numProduct": 63,
            "urlRoute": "tops-tees",
            "subCategory": []
          },
          {
            "depth": 1,
            "id": 380,
            "name": "Tunic",
            "numProduct": 27,
            "urlRoute": "tops-tunic",
            "subCategory": []
          }
        ]
      }
    ]
  },
  {
    "depth": 1,
    "id": 68,
    "name": "Shoes",
    "numProduct": 677,
    "urlRoute": "shoes",
    "subCategory": [
      {
        "depth": 1,
        "id": 92,
        "name": "Booties",
        "numProduct": 58,
        "urlRoute": "booties",
        "subCategory": []
      },
      {
        "depth": 1,
        "id": 71,
        "name": "Boots",
        "numProduct": 88,
        "urlRoute": "boots",
        "subCategory": []
      },
      {
        "depth": 1,
        "id": 101,
        "name": "Flats",
        "numProduct": 160,
        "urlRoute": "flats",
        "subCategory": []
      },
      {
        "depth": 1,
        "id": 104,
        "name": "Heels",
        "numProduct": 286,
        "urlRoute": "heels",
        "subCategory": []
      },
      {
        "depth": 1,
        "id": 98,
        "name": "Sandals",
        "numProduct": 34,
        "urlRoute": "sandals",
        "subCategory": []
      },
      {
        "depth": 1,
        "id": 95,
        "name": "Sneakers",
        "numProduct": 19,
        "urlRoute": "sneakers",
        "subCategory": []
      },
      {
        "depth": 1,
        "id": 107,
        "name": "Wedges",
        "numProduct": 21,
        "urlRoute": "wedges",
        "subCategory": []
      }
    ]
  }
]
```

This endpoint retrieves a full category tree

### HTTP Request

`GET /api/v1/getegories`

### Query Parameters
