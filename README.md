RecyclerView Sample App 📱

Aplikasi sampel Android berbasis Kotlin yang mendemonstrasikan implementasi RecyclerView untuk menampilkan daftar data bertipe dinamis/scrollable secara efisien.

📌 Fitur Utama

Penggunaan RecyclerView: Menampilkan daftar item (Item 1 sampai Item 20+) menggunakan arsitektur RecyclerView.

Custom Layout Item: Menggunakan desain tampilan kustom berbasis card_view_design.xml.

ViewModel Architecture: Memanfaatkan ItemsViewModel untuk mengelola data tampilan secara terpisah dari UI logic.

Custom Adapter: Implementasi CustomAdapter untuk mengikat (binding) data ke dalam item daftar.

🛠️ Struktur Proyek

Sesuai dengan struktur paket proyek lat.pam.recyclerviewsample:

lat.pam.recyclerviewsample/
 ├── CustomAdapter.kt      # Adapter untuk menghubungkan data dengan RecyclerView
 ├── ItemsViewModel.kt     # Model data yang merepresentasikan setiap item dalam daftar
 └── MainActivity.kt       # Activity utama yang menginisialisasi RecyclerView & LayoutManager


File Layout (res/layout/)

activity_main.xml — Layout utama yang berisi widget androidx.recyclerview.widget.RecyclerView.

card_view_design.xml — Layout XML khusus untuk mendesain tampilan masing-masing baris/card item.

💻 Contoh Kode (activity_main.xml)

<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout 
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <androidx.recyclerview.widget.RecyclerView
        android:id="@+id/recyclerview"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        tools:itemCount="5"
        tools:listitem="@layout/card_view_design" />

</androidx.constraintlayout.widget.ConstraintLayout>


🛠️ Teknologi & Prerequisites

Bahasa: Kotlin

IDE: Android Studio (Ladybug / modern release)

UI Architecture: ConstraintLayout, RecyclerView, CardView

Build System: Gradle Version Catalog (libs.versions.toml) & Kotlin DSL (build.gradle.kts)

🚀 Cara Menjalankan Project

Open folder project ini di Android Studio.

Lakukan Gradle Sync untuk mengunduh semua dependensi.

Jalankan aplikasi pada emulator (misal: Medium Phone API 36) atau perangkat Android fisik.
