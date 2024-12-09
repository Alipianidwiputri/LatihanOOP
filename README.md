# Bahasa pemrograman

# LatihanOOP

# Pyhton

    import tkinter as tk
    from view.input_form import InputForm
    from view.mahasiswa import MahasiswaView
    from data.mahasiswa import DataMahasiswa

    class MainApp:
    def __init__(self, master):
        self.master = master
        self.master.title("Aplikasi Data Mahasiswa")

        # Inisialisasi DataMahasiswa
        self.data_mahasiswa = DataMahasiswa()

        # Membuat tombol-tombol pada jendela utama
        self._create_widgets()

    def _create_widgets(self):
        """Membuat tombol utama aplikasi."""
        self.button_input = tk.Button(self.master, text="Input Mahasiswa", command=self.open_input_form)
        self.button_input.pack(pady=10)

        self.button_view = tk.Button(self.master, text="Lihat Daftar Mahasiswa", command=self.open_mahasiswa_view)
        self.button_view.pack(pady=10)

    def open_input_form(self):
        """Membuka form input di jendela baru."""
        self._open_new_window(InputForm)

    def open_mahasiswa_view(self):
        """Membuka daftar mahasiswa di jendela baru."""
        self._open_new_window(MahasiswaView)

    def _open_new_window(self, view_class):
        """Membantu membuka jendela baru dengan kelas tampilan tertentu."""
        new_window = tk.Toplevel(self.master)
        view_class(new_window, self.data_mahasiswa)

    if __name__ == "__main__":
        root = tk.Tk()
        app = MainApp(root)
         root.mainloop()

# hasil Pyhton

1. Input Data Mahasiswa 

![Screenshot 2024-12-09 223338](https://github.com/user-attachments/assets/401a2792-c095-4291-b95d-5f5f1decffc0)

2. hapus data

![Screenshot 2024-12-09 223612](https://github.com/user-attachments/assets/4489b61c-66e8-4ac6-99da-a2adc06d76b1)

3. ubah data
![Screenshot 2024-12-09 223716](https://github.com/user-attachments/assets/2dfd8ed8-71d2-45da-bb1f-d30b6565ee67)

