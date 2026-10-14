<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sistem Keuangan Masjid</title>
    <!-- Tailwind CSS untuk tampilan yang rapi dan modern -->
    <script src="https://cdn.tailwindcss.com"></script>
</head>
<body class="bg-slate-50 font-sans">

    <!-- Navbar -->
    <nav class="bg-emerald-700 text-white shadow-md">
        <div class="max-w-7xl mx-auto px-4 py-4 flex justify-between items-center">
            <h1 class="text-xl font-bold">Masjid Al-Ikhlas - Keuangan</h1>
            <span class="text-sm bg-emerald-800 px-3 py-1 rounded-full">Dashboard Digital</span>
        </div>
    </nav>

    <!-- Konten Utama -->
    <main class="max-w-7xl mx-auto px-4 py-8">
        
        <!-- Dashboard Kartu Ringkasan -->
        <div class="grid grid-cols-1 md:grid-cols-4 gap-6 mb-8">
            <div class="bg-white p-6 rounded-xl shadow-sm border border-slate-100">
                <p class="text-sm text-slate-500 font-medium">Total Saldo Kas</p>
                <h3 id="totalSaldo" class="text-2xl font-bold text-slate-800 mt-2">Rp 0</h3>
            </div>
            <div class="bg-white p-6 rounded-xl shadow-sm border border-slate-100">
                <p class="text-sm text-slate-500 font-medium">Total Pemasukan</p>
                <h3 id="totalMasuk" class="text-2xl font-bold text-emerald-600 mt-2">Rp 0</h3>
            </div>
            <div class="bg-white p-6 rounded-xl shadow-sm border border-slate-100">
                <p class="text-sm text-slate-500 font-medium">Total Pengeluaran</p>
                <h3 id="totalKeluar" class="text-2xl font-bold text-rose-600 mt-2">Rp 0</h3>
            </div>
            <div class="bg-white p-6 rounded-xl shadow-sm border border-slate-100">
                <p class="text-sm text-slate-500 font-medium">Saldo Iuran Pengajian</p>
                <h3 id="saldoPengajian" class="text-2xl font-bold text-indigo-600 mt-2">Rp 0</h3>
            </div>
        </div>

        <!-- Grid: Form Input & Tabel Riwayat -->
        <div class="grid grid-cols-1 lg:grid-cols-3 gap-8">
            
            <!-- Form Tambah Transaksi -->
            <div class="bg-white p-6 rounded-xl shadow-sm border border-slate-100 h-fit">
                <h2 class="text-lg font-bold text-slate-800 mb-4">Catat Transaksi Baru</h2>
                <form id="formTransaksi" class="space-y-4">
                    <div>
                        <label class="block text-sm font-medium text-slate-600 mb-1">Tanggal</label>
                        <input type="date" id="tanggal" required class="w-full border border-slate-300 rounded-lg px-3 py-2 focus:outline-none focus:ring-2 focus:ring-emerald-500">
                    </div>
                    <div>
                        <label class="block text-sm font-medium text-slate-600 mb-1">Keterangan</label>
                        <input type="text" id="keterangan" placeholder="Contoh: Infaq Jumat / Beli Alat Kebersihan" required class="w-full border border-slate-300 rounded-lg px-3 py-2 focus:outline-none focus:ring-2 focus:ring-emerald-500">
                    </div>
                    <div>
                        <label class="block text-sm font-medium text-slate-600 mb-1">Jenis Transaksi</label>
                        <select id="jenis" class="w-full border border-slate-300 rounded-lg px-3 py-2 focus:outline-none focus:ring-2 focus:ring-emerald-500">
                            <option value="Masuk">Pemasukan</option>
                            <option value="Keluar">Pengeluaran</option>
                        </select>
                    </div>
                    <div>
                        <label class="block text-sm font-medium text-slate-600 mb-1">Kategori Keuangan</label>
                        <select id="kategori" class="w-full border border-slate-300 rounded-lg px-3 py-2 focus:outline-none focus:ring-2 focus:ring-emerald-500">
                            <option value="Iuran Utama">Iuran Utama (Kas Umum/Jumat)</option>
                            <option value="Iuran Pengajian">Iuran Pengajian</option>
                            <option value="Lain-lain">Kebutuhan Lain-lain</option>
                        </select>
                    </div>
                    <div>
                        <label class="block text-sm font-medium text-slate-600 mb-1">Nominal (Rp)</label>
                        <input type="number" id="nominal" placeholder="Contoh: 500000" required class="w-full border border-slate-300 rounded-lg px-3 py-2 focus:outline-none focus:ring-2 focus:ring-emerald-500">
                    </div>
                    <button type="submit" class="w-full bg-emerald-600 text-white font-medium py-2 rounded-lg hover:bg-emerald-700 transition">Simpan Transaksi</button>
                </form>
            </div>

            <!-- Tabel Riwayat Alur Kas -->
            <div class="lg:col-span-2 bg-white p-6 rounded-xl shadow-sm border border-slate-100">
                <div class="flex justify-between items-center mb-4">
                    <h2 class="text-lg font-bold text-slate-800">Riwayat Alur Kas</h2>
                    <button onclick="resetData()" class="text-xs text-rose-500 hover:underline">Reset Semua Data</button>
                </div>
                <div class="overflow-x-auto">
                    <table class="w-full text-left border-collapse">
                        <thead>
                            <tr class="border-b border-slate-200 text-slate-500 text-sm">
                                <th class="py-3 px-2">Tanggal</th>
                                <th class="py-3 px-2">Keterangan</th>
                                <th class="py-3 px-2">Kategori</th>
                                <th class="py-3 px-2">Jenis</th>
                                <th class="py-3 px-2 text-right">Nominal</th>
                                <th class="py-3 px-2 text-center">Aksi</th>
                            </tr>
                        </thead>
                        <tbody id="tabelTransaksi" class="text-sm divide-y divide-slate-100">
                            <!-- Data akan dimasukkan lewat JavaScript -->
                        </tbody>
                    </table>
                </div>
            </div>

        </div>
    </main>

    <!-- Skrip JavaScript untuk Logika Aplikasi & Penyimpanan Lokal -->
    <script>
        // Ambil data dari localStorage atau buat array kosong jika belum ada
        let transaksiList = JSON.parse(localStorage.getItem('transaksi_masjid')) || [];

        const form = document.getElementById('formTransaksi');
        const tabelTransaksi = document.getElementById('tabelTransaksi');
        const totalSaldoEl = document.getElementById('totalSaldo');
        const totalMasukEl = document.getElementById('totalMasuk');
        const totalKeluarEl = document.getElementById('totalKeluar');
        const saldoPengajianEl = document.getElementById('saldoPengajian');

        // Format angka ke Rupiah
        function formatRupiah(angka) {
            return 'Rp ' + Number(angka).toLocaleString('id-ID');
        }

        // Render data ke Dashboard dan Tabel
        function renderApp() {
            tabelTransaksi.innerHTML = '';
            let totalMasuk = 0;
            let totalKeluar = 0;
            let saldoPengajian = 0;

            if (transaksiList.length === 0) {
                tabelTransaksi.innerHTML = `<tr><td colspan="6" class="text-center py-4 text-slate-400">Belum ada data transaksi.</td></tr>`;
            }

            transaksiList.forEach((item, index) => {
                const nominalNum = Number(item.nominal);
                
                // Hitung total masuk/keluar
                if (item.jenis === 'Masuk') {
                    totalMasuk += nominalNum;
                    if (item.kategori === 'Iuran Pengajian') {
                        saldoPengajian += nominalNum;
                    }
                } else {
                    totalKeluar += nominalNum;
                    if (item.kategori === 'Iuran Pengajian') {
                        saldoPengajian -= nominalNum;
                    }
                }

                // Tambahkan baris ke tabel
                const tr = document.createElement('tr');
                tr.innerHTML = `
                    <td class="py-3 px-2 text-slate-600">${item.tanggal}</td>
                    <td class="py-3 px-2 font-medium text-slate-800">${item.keterangan}</td>
                    <td class="py-3 px-2"><span class="bg-slate-100 text-slate-700 px-2 py-1 rounded text-xs">${item.kategori}</span></td>
                    <td class="py-3 px-2"><span class="${item.jenis === 'Masuk' ? 'text-emerald-600 font-semibold' : 'text-rose-600 font-semibold'}">${item.jenis}</span></td>
                    <td class="py-3 px-2 text-right font-medium ${item.jenis === 'Masuk' ? 'text-emerald-600' : 'text-rose-600'}">${item.jenis === 'Masuk' ? '+' : '-'} ${formatRupiah(item.nominal)}</td>
                    <td class="py-3 px-2 text-center"><button onclick="hapusTransaksi(${index})" class="text-rose-500 hover:text-rose-700 text-xs font-semibold">Hapus</button></td>
                `;
                tabelTransaksi.appendChild(tr);
            });

            let totalSaldo = totalMasuk - totalKeluar;

            // Update Tampilan Dashboard
            totalSaldoEl.innerText = formatRupiah(totalSaldo);
            totalMasukEl.innerText = formatRupiah(totalMasuk);
            totalKeluarEl.innerText = formatRupiah(totalKeluar);
            saldoPengajianEl.innerText = formatRupiah(saldoPengajian);

            // Simpan ke LocalStorage supaya tidak hilang saat di-refresh
            localStorage.setItem('transaksi_masjid', JSON.stringify(transaksiList));
        }

        // Tambah Transaksi
        form.addEventListener('submit', function(e) {
            e.preventDefault();
            const tanggal = document.getElementById('tanggal').value;
            const keterangan = document.getElementById('keterangan').value;
            const jenis = document.getElementById('jenis').value;
            const kategori = document.getElementById('kategori').value;
            const nominal = document.getElementById('nominal').value;

            transaksiList.push({ tanggal, keterangan, jenis, kategori, nominal });
            form.reset();
            renderApp();
        });

        // Hapus Transaksi Satuan
        function hapusTransaksi(index) {
            if (confirm("Apakah Anda yakin ingin menghapus data ini?")) {
                transaksiList.splice(index, 1);
                renderApp();
            }
        }

        // Reset Semua Data
        function resetData() {
            if (confirm("Yakin ingin menghapus seluruh data pencatatan?")) {
                transaksiList = [];
                localStorage.removeItem('transaksi_masjid');
                renderApp();
            }
        }

        // Jalankan render saat pertama kali dibuka
        renderApp();
    </script>
</body>
</html>
