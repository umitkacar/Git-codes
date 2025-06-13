# Git Komut Kitapçığı

Bu döküman Git ile çalışırken en sık kullanılan komutların kısa bir özetini sunar. 
Git deposu oluşturma, değişiklikleri takip etme, dallar (branch) yönetimi ve uzaktaki (remote) depolarla çalışma gibi temel işlemleri içerir.

## 1. Kurulum ve Konfigürasyon
```bash
# Kullanıcı bilgilerini tanımla
git config --global user.name "Ad Soyad"
git config --global user.email "email@example.com"

# Mevcut ayarları görüntüle
git config --list
```

## 2. Depo Oluşturma ve Klonlama
```bash
# Yeni bir depo başlat
git init

# Varolan bir depoyu klonla
git clone <repo-adresi>
```

## 3. Değişiklik Takibi
```bash
# Çalışma dizinindeki durumu kontrol et
git status

# Dosyaları sahneye ekle
git add <dosya>
# veya tüm değişiklikleri eklemek için
git add .

# Değişiklikleri kaydet (commit)
git commit -m "Açıklama"
```

## 4. Dal (Branch) İşlemleri
```bash
# Yeni dal oluştur
git branch <yeni_dal>

# Dal değiştirme
git checkout <dal>

# Dal oluşturup aynı anda geçiş yapma
git checkout -b <yeni_dal>

# Değişiklikleri başka dala birleştirme
git merge <dal>

# Dal silme
git branch -d <dal>
# Zorla silmek için
git branch -D <dal>
```

## 5. Uzak Depo (Remote) İşlemleri
```bash
# Uzak depo ekleme
git remote add origin <url>

# Uzak depodaki değişiklikleri çekme
git pull origin <dal>

# Değişiklikleri göndermek
git push origin <dal>

# Uzak depoları listeleme
git remote -v
```

## 6. Değişiklikleri İnceleme
```bash
# Commit geçmişini göster
git log
# Tek satırlık özet
git log --oneline
# İki dal arasındaki farkları gör
git diff <dal1>..<dal2>
# Belirli bir commit'i detaylı göster
git show <commit>
```

## 7. Geri Alma ve Temizleme
```bash
# Çalışma dizinindeki değişiklikleri geri al
git checkout .

# Belirli bir commit'e dön
git reset --hard <commit>

# Stash ile geçici olarak sakla
git stash
# Saklanan değişiklikleri geri getir
git stash pop
```

## 8. Faydalı Diğer Komutlar
```bash
# Takipten çıkar
git rm --cached <dosya>

# Tag ekleme
git tag <etiket>

# Daha okunabilir log çıktısı
git log --graph --oneline --decorate
```

## 9. Kaynaklar
- [Git resmi dokümantasyonu](https://git-scm.com/docs/gittutorial)
- [Learn Git Branching](https://learngitbranching.js.org/)
- [Oh My Zsh](https://ohmyz.sh/)
