# Aplikasi Input data siswa


import os
import sys

class Mahasiswa;
        nim=''
        nama=''

pilih = 0
dataSiswa =[]

def menu ():
  os.system('cls')
  print ("Menu Aplikasi Data Siswa");
  print ("-------------------------")
  print ("1.Input dlData Siswa")
  print ("2.Tampilan Data Siswa")
  print ("3.Updet Data Siswa")
  print ("5.Author")
  print ("6.Keluar Dari Aplikasi")
  pilih = int(input("Masukan Pilihan Anda :"))
  if pilih == 1 :
    tampil1()
    input("Kembali Menu Utama")
    menu()
  elif pilih == 2:
    index_updet=-1
    tampil()
    id_edit = int(input("input Nim yang akan di update"))
    for a in range(0, len(dataSiswa)):
      if id_edit == dataSiswa[a].nim:
        index_update = a
        break
      if (index_update > -1):
        print ("INPUT DATA YANG DI UPDATE")
        siswa = Mahasiswa ()
        siswa.nim = (int(input("Masukan Nim Siswa :")))
        siswa.nama = (input("Masukan Nama Siswa :"))
        dataSiswa[index_update] = siswa
        print ("Berhasil Update data siswa")
      else : print("nim tidak di temukan")
      input("Kembali menu utama")
      menu()
    elif pilih ==4:
      os.system('cls')
      tampil()
      index_delet=-1
      id_hapus = int(input("Input Nim yang akan di hapus :"))
      for a in range(0, len(dataSiswa)):
        if id_edit == dataSiswa[a].nim:
                    index_update = a
                    break
      if(index_delet > -1):
        del dataSiswa[index_delete]
        print ("Data Telah di hapus")
      else : print ("Nim tidak ditemukan")
      input ("Kembali ke menu utama")
      menu()
    elif pilih == 5 :
      author ()
      input("\n\n Kembali menu utama")
      menu()
    elif pilih == 6 :
      sys.exit()
    
def tampil() :
  os.system('cls')
  print ("DATA MAHASISWA")
  for data in dataSiswa :
    print ("Nim : "+str(data.nim))
    print ("Nama : "+data.nama)
    print ("---------------------")
    
def author ():
  os.system('cls')
  print ("Pakde Edri")
  print ("UnHar")
  
def pilih1():
  ulang = 'y'
  while ulang in('y', 'y')
      os.system('cls')
      siswaBaru = Mahasiswa()
      print("INPUT DATA MAHASISWA")
      siswaBaru.nim = (int(input("Masukkan Nim :")))
      siswaBaru.nama = (input("Masukkan Nama siswa :"))
      dataSiswa.append(siswaBaru)
      ulang = input("Apakah Anda ingin mengulangnya (Y/T)?")
      
      
menu()
