# Key
package main

import (
	"crypto/rand"
	"encoding/base64"
	"fmt"
	"log"
)

func generateSecretKey() string {
	// Tạo 32 byte ngẫu nhiên
	bytes := make([]byte, 32)
	_, err := rand.Read(bytes)
	if err != nil {
		log.Fatal(err)
	}

	// Chuyển đổi thành chuỗi base64
	return base64.URLEncoding.EncodeToString(bytes)
}

func main() {
	// In ra SECRET_KEY
	fmt.Println("SECRET_KEY:", generateSecretKey())
}
# .env
/* DB_HOST=localhost
DB_PORT=3306
DB_USER=quangtnn
DB_PASSWORD=12332167
DB_NAME=bloapp
SECRET_KEY=RnXHGleyAcRfJaULJMJxK7vlYDE2VMUYiYSwM2UwoVg=
*/


![image](https://github.com/user-attachments/assets/9090a4c8-81bb-4015-a3ab-08156ff750ab)
