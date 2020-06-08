---


---

<p>Untuk mengakses database API AOL Dibagi Menjadi 2 Step :</p>
<h3 id="mendapatkan-daftarlist-database-accurate-online">1. Mendapatkan daftar/list database Accurate Online</h3>
<p>Untuk mendapatkan daftar database yang dapat dibuka oleh pengguna <a href="mailto:john@example.com">john@example.com</a>, gunakan API  <strong>Db List</strong>  seperti berikut:</p>

<table>
<thead>
<tr>
<th></th>
<th></th>
</tr>
</thead>
<tbody>
<tr>
<td>URL</td>
<td><a href="https://account.accurate.id/api/db-list.do">https://account.accurate.id/api/db-list.do</a></td>
</tr>
<tr>
<td>Method</td>
<td>GET</td>
</tr>
<tr>
<td><strong>Header</strong></td>
<td></td>
</tr>
<tr>
<td>Authorization</td>
<td>Bearer e8446369-bd56-4731-acea-c0a9e0cc46fa</td>
</tr>
</tbody>
</table><p><strong>Penjelasan :</strong></p>
<ul>
<li>Header Authorization diisi dengan token yang sudah didapatkan dari proses otentikasi dan autentikasi.</li>
</ul>
<p><strong>Response</strong> :</p>
<p>Hasil dari request tersebut adalah daftar database seperti berikut:</p>
<pre><code>{
  "d": [
    {
      "id": 1156,
      "alias": "PT Demo Example"
    },
    {
      "id": 1253,
      "alias": "PT Contoh"
    }
  ],
  "s": true
}

</code></pre>
<h3 id="mendapatkan-session-dan-host-dari-database">2. Mendapatkan session dan host dari Database</h3>
<p>Untuk dapat membaca dan menulis ke database diperlukan informasi <strong>session</strong> dan <strong>host</strong> untuk database tersebut. Misalkan Anda ingin menggunakan database <strong>PT Demo Example</strong> maka <strong>session</strong> dan <strong>host</strong> dapat didapatkan menggunakan API <strong>Open Db</strong> dengan mengirimkan <strong>id</strong> dari database tersebut sebagai parameter sbb:</p>

<table>
<thead>
<tr>
<th></th>
<th></th>
</tr>
</thead>
<tbody>
<tr>
<td>URL</td>
<td><a href="https://account.accurate.id/api/open-db.do">https://account.accurate.id/api/open-db.do</a></td>
</tr>
<tr>
<td>Method</td>
<td>GET</td>
</tr>
<tr>
<td><strong>Header</strong></td>
<td></td>
</tr>
<tr>
<td>Authorization</td>
<td>Bearer e8446369-bd56-4731-acea-c0a9e0cc46fa</td>
</tr>
<tr>
<td><strong>Parameter</strong></td>
<td></td>
</tr>
<tr>
<td>id</td>
<td>1132</td>
</tr>
</tbody>
</table><p><strong>Penjelasan :</strong></p>
<ul>
<li>Header Authorization diisi dengan token yang sudah didapatkan dari proses otentikasi dan autentikasi.</li>
<li>Parameter ID didapakan dari list db accurate.</li>
</ul>
<p><strong>Response :</strong><br>
Hasil dari request tersebut adalah sebagai berikut:</p>
<pre><code>{
  "d": [
    "Proses Berhasil Dilakukan"
  ],
  "host": "https://public.accurate.id",
  "session": "7ff842b6-53e2-4d7b-8038-09e3f8318f1b",
  "s": true
}

</code></pre>
<p>Dari hasil berikut didapatkan session <strong>7ff842b6-53e2-4d7b-8038- 09e3f8318f1b</strong> dan host <strong><a href="https://public.accurate.id">https://public.accurate.id</a></strong> yang dapat digunakan untuk mengakses data pada database terkait sesuai dengan scope yang diminta. Informasi host ini akan menentukan prefix URL untuk mengakses API Accurate.</p>

