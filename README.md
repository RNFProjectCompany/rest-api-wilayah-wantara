## ENDPOINTS

#### 1. Mengambil Daftar Provinsi

```
GET https://rnfprojectcompany.github.io/rest-api-wilayah-wantara/api/provinces.json
```

Contoh Response:

```
[
  {
    "id": "11",
    "name": "ACEH"
  },
  {
    "id": "12",
    "name": "SUMATERA UTARA"
  },
  ...
]
```

#### 2. Mengambil Daftar Kab/Kota pada Provinsi Tertentu

```
GET "https://rnfprojectcompany.github.io/rest-api-wilayah-wantara/api/regencies/".concat(listprovinsimap.get((int)listview1P).get("id").toString().concat(".json"))
```

Contoh untuk mengambil daftar kab/kota di provinsi Aceh (ID = 11):

```
GET https://rnfprojectcompany.github.io/rest-api-wilayah-wantara/api/regencies/11.json
```

Contoh Response:

```
[
  {
    "id": "1101",
    "province_id": "11",
    "name": "KABUPATEN SIMEULUE"
  },
  {
    "id": "1102",
    "province_id": "11",
    "name": "KABUPATEN ACEH SINGKIL"
  },
  ...
]
```

#### 3. Mengambil Daftar Kecamatan pada Kab/Kota Tertentu

```
GET "https://rnfprojectcompany.github.io/rest-api-wilayah-wantara/api/districts/".concat(listprovinsimap.get((int)listview1P).get("id").toString().concat(".json"))
```

Contoh untuk mengambil daftar kecamatan di Aceh Selatan (ID = 1103):

```
GET https://rnfprojectcompany.github.io/rest-api-wilayah-wantara/api/districts/1103.json
```

Contoh Response:

```
[
  {
    "id": "1103010",
    "regency_id": "1103",
    "name": "TRUMON"
  },
  {
    "id": "1103011",
    "regency_id": "1103",
    "name": "TRUMON TIMUR"
  },
  ...
]
```

#### 4. Mengambil Daftar Kelurahan pada Kecamatan Tertentu

```
GET "https://rnfprojectcompany.github.io/rest-api-wilayah-wantara/api/villages/".concat(listprovinsimap.get((int)listview1P).get("id").toString().concat(".json"))
```

Contoh untuk mengambil daftar kelurahan di Trumon (ID = 1103010):

```
GET https://rnfprojectcompany.github.io/rest-api-wilayah-wantara/api/villages/1103010.json
```

Contoh Response:

```
[
  {
    "id": "1103010001",
    "district_id": "1103010",
    "name": "KUTA PADANG"
  },
  {
    "id": "1103010002",
    "district_id": "1103010",
    "name": "RAKET"
  },
  ...
]
```
