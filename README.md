##  Dokumentasi API

**Base URL:** `http://localhost:8080`  
**Content-Type:** `application/json`

### 1. Tambah Data User Baru (Create)
Menambahkan data user baru. ID akan *digenerate* secara otomatis dalam bentuk UUID.

* **URL:** `/api/users`
* **Method:** `POST`
* **Request Body:**
    ```json
    {
        "name": "Brody",
        "age": 20
    }
    ```
* **Success Response (201 Created):**
    ```json
    {
        "status": "success",
        "data": {
            "id": "2d7d8cd2-89bb-461d-a2bd-22b885b5046c",
            "name": "Brody",
            "age": 20
        }
    }
    ```

### 2. Ambil Semua Data User (Read All)
Menampilkan daftar seluruh user yang ada di dalam *database*.

* **URL:** `/api/users`
* **Method:** `GET`
* **Success Response (200 OK):**
    ```json
    {
        "status": "success",
        "data": [
            {
                "id": "2d7d8cd2-89bb-461d-a2bd-22b885b5046c",
                "name": "Brody",
                "age": 20
            }
        ]
    }
    ```

### 3. Ambil Detail User Spesifik (Read Detail)
Mencari dan menampilkan detail satu user berdasarkan ID.

* **URL:** `/api/users/{id}`
* **Method:** `GET`
* **URL Params:** `id=[String]`
* **Success Response (200 OK):**
    ```json
    {
        "status": "success",
        "data": {
            "id": "2d7d8cd2-89bb-461d-a2bd-22b885b5046c",
            "name": "Brody",
            "age": 20
        }
    }
    ```

### 4. Ubah Data User (Update)
Memperbarui data nama dan/atau umur dari user yang sudah ada.

* **URL:** `/api/users/{id}`
* **Method:** `PUT`
* **URL Params:** `id=[String]`
* **Request Body:**
    ```json
    {
        "name": "Brody Black Mamba",
        "age": 22
    }
    ```
* **Success Response (200 OK):**
    ```json
    {
        "status": "success",
        "data": {
            "id": "2d7d8cd2-89bb-461d-a2bd-22b885b5046c",
            "name": "Brody Black Mamba",
            "age": 22
        }
    }
    ```

### 5. Hapus Data User (Delete)
Menghapus data user secara permanen dari *database*.

* **URL:** `/api/users/{id}`
* **Method:** `DELETE`
* **URL Params:** `id=[String]`
* **Success Response (200 OK):**
    ```json
    {
        "status": "success delete user with id 2d7d8cd2-89bb-461d-a2bd-22b885b5046c"
    }
    ```

### Screenshot Tampilan Web
<img width="1919" height="1070" alt="image" src="https://github.com/user-attachments/assets/a0f448f6-03d6-43a2-afb4-b73349c4967b" />
