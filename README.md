# 💰 Xərc Tracker — Flutter App

Android üçün tam xərc və büdcə izləmə tətbiqi.

## Xüsusiyyətlər
- ✅ Xərc əlavə et / sil (sürüşdürərək)
- ✅ 7 kateqoriya (Qida, Nəqliyyat, Əyləncə, Sağlamlıq, Geyim, Kommunal, Digər)
- ✅ Aylıq büdcə təyin et
- ✅ Progress bar ilə büdcə izlə
- ✅ Pie chart statistika
- ✅ Qaranlıq/açıq tema dəstəyi
- ✅ Məlumatlar telefonda saxlanılır (offline)

## Quraşdırma

### 1. Flutter yüklə
https://flutter.dev/docs/get-started/install

### 2. Layihəni aç
```bash
cd xerc_tracker
flutter pub get
```

### 3. Android emulyatorda işlət
```bash
flutter run
```

### 4. APK hazırla (telefona quraşdırmaq üçün)
```bash
flutter build apk --release
```
APK faylı: `build/app/outputs/flutter-apk/app-release.apk`

## Layihə strukturu
```
lib/
  main.dart              # App başlanğıcı
  models/
    expense.dart         # Xərc modeli + kateqoriyalar
  services/
    storage_service.dart # Məlumat saxlama
  screens/
    home_screen.dart     # Alt naviqasiya
    expenses_screen.dart # Əsas ekran
    budget_screen.dart   # Büdcə ekranı
    stats_screen.dart    # Statistika ekranı
  widgets/
    summary_cards.dart   # Yuxarı kartlar
    add_expense_sheet.dart # Xərc əlavə etmə
```

## Yeni kateqoriya əlavə etmək
`lib/models/expense.dart` faylında `kCategories` siyahısına əlavə edin:
```dart
{'name': 'Kitab', 'icon': '📚', 'color': 0xFF1D9E75},
```
