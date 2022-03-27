package com.company;

//Mahasiswa
class Mahasiswa{
    //Data
    String nama;
    double waktuPeminjaman;
    Buku book;

    //Method
    void lakukanPeminjaman(Buku book){
        this.book = book;
    }

    //Constructor
    Mahasiswa(String nama, int waktuPeminjaman){
        this.nama = nama;
        this.waktuPeminjaman = waktuPeminjaman;
    }

    void detailPeminjaman(){
        System.out.println("Nama Mahasiswa : " + nama);
        System.out.println("Waktu Peminjaman (Hari) : " + waktuPeminjaman);
        book.detailBuku();
    }
}

//Judul buku
class Buku{
    String judulBuku;

    //Constructor
    Buku(String judulBuku){
        this.judulBuku = judulBuku;
    }

    //Method
    void detailBuku(){
        System.out.println("Judul Buku : " + judulBuku);
    }
}

public class Main {

    public static void main(String[] args) {
        Mahasiswa Budi = new Mahasiswa("Budi", 7);

        Buku HarryPotter = new Buku("Harry Potter");

        Budi.lakukanPeminjaman(HarryPotter);

        Budi.detailPeminjaman();
    }
}
