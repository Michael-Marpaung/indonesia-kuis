<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Ujian Bahasa Indonesia Kelas XII - Kurikulum Merdeka</title>
<style>
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }
  body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    min-height: 100vh;
    padding: 20px;
    color: #333;
  }
  .container {
    max-width: 1000px;
    margin: 0 auto;
    background: #fff;
    border-radius: 16px;
    box-shadow: 0 20px 60px rgba(0,0,0,0.3);
    overflow: hidden;
  }
  header {
    background: linear-gradient(135deg, #1e3c72 0%, #2a5298 100%);
    color: #fff;
    padding: 30px 40px;
    text-align: center;
  }
  header h1 {
    font-size: 1.8em;
    margin-bottom: 8px;
  }
  header p {
    font-size: 0.95em;
    opacity: 0.9;
  }
  .info-bar {
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
    gap: 10px;
    background: #f0f4f8;
    padding: 15px 40px;
    border-bottom: 2px solid #e0e6ed;
    font-size: 0.9em;
  }
  .info-bar span {
    background: #fff;
    padding: 6px 14px;
    border-radius: 20px;
    border: 1px solid #d0d7de;
    font-weight: 600;
    color: #2a5298;
  }
  .content {
    padding: 30px 40px;
  }
  .section-title {
    background: linear-gradient(90deg, #2a5298, #4a7bc8);
    color: #fff;
    padding: 12px 20px;
    border-radius: 8px;
    margin: 30px 0 20px;
    font-size: 1.15em;
    font-weight: 700;
  }
  .section-title:first-child { margin-top: 0; }
  .difficulty-badge {
    display: inline-block;
    padding: 4px 12px;
    border-radius: 20px;
    font-size: 0.75em;
    font-weight: 700;
    margin-bottom: 10px;
    text-transform: uppercase;
    letter-spacing: 0.5px;
  }
  .badge-sedang { background: #d4edda; color: #155724; }
  .badge-sulit { background: #fff3cd; color: #856404; }
  .badge-sangat { background: #f8d7da; color: #721c24; }
  .question {
    background: #fafbfc;
    border: 1px solid #e1e8ed;
    border-radius: 12px;
    padding: 22px;
    margin-bottom: 20px;
    transition: all 0.3s;
  }
  .question:hover {
    border-color: #2a5298;
    box-shadow: 0 4px 12px rgba(42,82,152,0.1);
  }
  .question-number {
    display: inline-block;
    background: #2a5298;
    color: #fff;
    width: 32px;
    height: 32px;
    line-height: 32px;
    text-align: center;
    border-radius: 50%;
    font-weight: 700;
    margin-right: 10px;
  }
  .question-text {
    font-size: 1em;
    line-height: 1.7;
    margin-bottom: 15px;
  }
  .passage {
    background: #fff;
    border-left: 4px solid #4a7bc8;
    padding: 15px 20px;
    margin: 12px 0;
    font-style: italic;
    border-radius: 0 8px 8px 0;
    line-height: 1.7;
    color: #444;
  }
  .passage p { margin-bottom: 8px; }
  .passage p:last-child { margin-bottom: 0; }
  .options {
    list-style: none;
    margin-top: 12px;
  }
  .options li {
    margin-bottom: 10px;
  }
  .options label {
    display: flex;
    align-items: flex-start;
    padding: 10px 14px;
    border: 1px solid #d0d7de;
    border-radius: 8px;
    cursor: pointer;
    transition: all 0.2s;
    line-height: 1.5;
  }
  .options label:hover {
    background: #eef3f9;
    border-color: #2a5298;
  }
  .options input[type="radio"],
  .options input[type="checkbox"] {
    margin-right: 12px;
    margin-top: 4px;
    flex-shrink: 0;
    width: 18px;
    height: 18px;
    accent-color: #2a5298;
    cursor: pointer;
  }
  .options label.selected {
    background: #e3f2fd;
    border-color: #2a5298;
  }
  .input-uraian {
    width: 100%;
    min-height: 150px;
    padding: 15px;
    border: 1px solid #d0d7de;
    border-radius: 8px;
    font-family: inherit;
    font-size: 1em;
    line-height: 1.6;
    resize: vertical;
    margin-top: 10px;
  }
  .input-uraian:focus {
    outline: none;
    border-color: #2a5298;
    box-shadow: 0 0 0 3px rgba(42,82,152,0.15);
  }
  .btn-group {
    display: flex;
    gap: 15px;
    justify-content: center;
    flex-wrap: wrap;
    margin: 40px 0 20px;
  }
  button {
    padding: 14px 32px;
    font-size: 1em;
    font-weight: 700;
    border: none;
    border-radius: 8px;
    cursor: pointer;
    transition: all 0.3s;
    font-family: inherit;
  }
  .btn-submit {
    background: linear-gradient(135deg, #11998e, #38ef7d);
    color: #fff;
  }
  .btn-submit:hover {
    transform: translateY(-2px);
    box-shadow: 0 8px 20px rgba(17,153,142,0.4);
  }
  .btn-reset {
    background: #f0f4f8;
    color: #2a5298;
    border: 2px solid #2a5298;
  }
  .btn-reset:hover {
    background: #2a5298;
    color: #fff;
  }
  .result {
    display: none;
    background: linear-gradient(135deg, #f0f9ff, #e0f2fe);
    border: 2px solid #2a5298;
    border-radius: 12px;
    padding: 30px;
    margin-top: 30px;
    text-align: center;
  }
  .result.show { display: block; animation: fadeIn 0.5s; }
  @keyframes fadeIn {
    from { opacity: 0; transform: translateY(10px); }
    to { opacity: 1; transform: translateY(0); }
  }
  .score-display {
    font-size: 3em;
    font-weight: 800;
    color: #2a5298;
    margin: 10px 0;
  }
  .score-label {
    font-size: 1.1em;
    color: #666;
    margin-bottom: 15px;
  }
  .score-detail {
    display: flex;
    justify-content: center;
    gap: 30px;
    flex-wrap: wrap;
    margin-top: 20px;
  }
  .score-item {
    background: #fff;
    padding: 15px 25px;
    border-radius: 10px;
    border: 1px solid #d0d7de;
    min-width: 150px;
  }
  .score-item .num {
    font-size: 1.5em;
    font-weight: 700;
    color: #2a5298;
  }
  .score-item .lbl {
    font-size: 0.85em;
    color: #666;
  }
  .feedback {
    margin-top: 15px;
    padding: 12px;
    border-radius: 8px;
    font-size: 0.95em;
    display: none;
    line-height: 1.6;
  }
  .feedback.show { display: block; }
  .feedback.correct {
    background: #d4edda;
    color: #155724;
    border-left: 4px solid #28a745;
  }
  .feedback.incorrect {
    background: #f8d7da;
    color: #721c24;
    border-left: 4px solid #dc3545;
  }
  .feedback .answer-key {
    font-weight: 700;
    margin-top: 6px;
  }
  .note {
    background: #fff8e1;
    border-left: 4px solid #ffc107;
    padding: 12px 18px;
    border-radius: 0 8px 8px 0;
    margin: 12px 0;
    font-size: 0.9em;
    color: #7a5a00;
  }
  .rubric-table {
    width: 100%;
    border-collapse: collapse;
    margin: 15px 0;
    font-size: 0.85em;
  }
  .rubric-table th,
  .rubric-table td {
    border: 1px solid #d0d7de;
    padding: 8px 10px;
    text-align: left;
  }
  .rubric-table th {
    background: #2a5298;
    color: #fff;
  }
  .rubric-table tr:nth-child(even) {
    background: #f6f8fa;
  }
  footer {
    background: #1e3c72;
    color: #fff;
    text-align: center;
    padding: 20px;
    font-size: 0.85em;
  }
  @media (max-width: 600px) {
    body { padding: 10px; }
    header, .content { padding: 20px; }
    .info-bar { padding: 12px 20px; }
    .score-display { font-size: 2em; }
  }
</style>
</head>
<body>
<div class="container">
  <header>
    <h1>📝 Ujian Bahasa Indonesia Kelas XII</h1>
    <p>Kurikulum Merdeka | Literasi &amp; Penalaran Kritis | HOTS (C4–C6)</p>
  </header>

  <div class="info-bar">
    <span>⏱️ Waktu: 120 Menit</span>
    <span>📊 Total Soal: 24</span>
    <span>🎯 PG: 20 | Uraian: 4</span>
    <span>📈 Level: C4 – C6</span>
  </div>

  <div class="content">
    <form id="examForm">

      <!-- ============ BAGIAN I: PILIHAN GANDA ============ -->
      <div class="section-title">BAGIAN I — PILIHAN GANDA (Soal 1–15)</div>

      <!-- Soal 1 -->
      <div class="question" data-type="pg" data-answer="B">
        <div><span class="difficulty-badge badge-sedang">Sedang • C4</span></div>
        <div class="question-text">
          <span class="question-number">1</span>
          <strong>Bacalah teks berikut untuk menjawab soal 1–3!</strong>
        </div>
        <div class="passage">
          <p>(1) Perubahan iklim bukan lagi sekadar prediksi para ilmuwan, melainkan kenyataan yang telah kita rasakan bersama. (2) Suhu bumi terus meningkat, pola musim bergeser, dan bencana hidrometeorologi semakin sering terjadi. (3) Namun, respons kebijakan Indonesia masih terkesan setengah hati. (4) Alih-alih mempercepat transisi energi terbarukan, pemerintah justru memperluas izin tambang batu bara. (5) Kebijakan ini tentu saja berseberangan dengan komitmen penurunan emisi yang telah dicanangkan dalam forum internasional. (6) Jika tidak segera dikoreksi, janji net zero emission 2060 hanya akan menjadi retorika politik tanpa makna.</p>
        </div>
        <div class="question-text">Ide pokok paragraf tersebut adalah …</div>
        <ul class="options">
          <li><label><input type="radio" name="q1" value="A"> A. Prediksi ilmuwan tentang perubahan iklim</label></li>
          <li><label><input type="radio" name="q1" value="B"> B. Ketidaksesuaian kebijakan Indonesia dengan realitas perubahan iklim</label></li>
          <li><label><input type="radio" name="q1" value="C"> C. Pentingnya forum internasional dalam penurunan emisi</label></li>
          <li><label><input type="radio" name="q1" value="D"> D. Dampak perluasan izin tambang batu bara</label></li>
          <li><label><input type="radio" name="q1" value="E"> E. Retorika politik pemerintah tentang net zero emission</label></li>
        </ul>
        <div class="feedback" id="fb-q1"></div>
      </div>

      <!-- Soal 2 -->
      <div class="question" data-type="pg" data-answer="E">
        <div><span class="difficulty-badge badge-sedang">Sedang • C4</span></div>
        <div class="question-text">
          <span class="question-number">2</span>
          Kalimat yang mengandung <strong>opini</strong> penulis ditandai nomor …
        </div>
        <ul class="options">
          <li><label><input type="radio" name="q2" value="A"> A. (1) dan (2)</label></li>
          <li><label><input type="radio" name="q2" value="B"> B. (2) dan (3)</label></li>
          <li><label><input type="radio" name="q2" value="C"> C. (3) dan (4)</label></li>
          <li><label><input type="radio" name="q2" value="D"> D. (1) dan (6)</label></li>
          <li><label><input type="radio" name="q2" value="E"> E. (3) dan (5)</label></li>
        </ul>
        <div class="feedback" id="fb-q2"></div>
      </div>

      <!-- Soal 3 -->
      <div class="question" data-type="pg" data-answer="C">
        <div><span class="difficulty-badge badge-sedang">Sedang • C4</span></div>
        <div class="question-text">
          <span class="question-number">3</span>
          Makna kata <strong>retorika</strong> dalam kalimat (6) adalah …
        </div>
        <ul class="options">
          <li><label><input type="radio" name="q3" value="A"> A. janji yang tertulis</label></li>
          <li><label><input type="radio" name="q3" value="B"> B. pidato yang bersemangat</label></li>
          <li><label><input type="radio" name="q3" value="C"> C. pernyataan yang bersifat simbolis tanpa realisasi</label></li>
          <li><label><input type="radio" name="q3" value="D"> D. strategi komunikasi politik yang efektif</label></li>
          <li><label><input type="radio" name="q3" value="E"> E. dokumen resmi pemerintah</label></li>
        </ul>
        <div class="feedback" id="fb-q3"></div>
      </div>

      <!-- Soal 4 -->
      <div class="question" data-type="pg" data-answer="B">
        <div><span class="difficulty-badge badge-sedang">Sedang • C4</span></div>
        <div class="question-text">
          <span class="question-number">4</span>
          Cermati kalimat berikut!<br><br>
          <em>"Meskipun banyak kritik yang dialamatkan kepada kebijakan tersebut, namun pemerintah tetap bersikeras menerapkannya."</em><br><br>
          Kalimat tersebut <strong>tidak efektif</strong> karena …
        </div>
        <ul class="options">
          <li><label><input type="radio" name="q4" value="A"> A. menggunakan kata "banyak" yang tidak perlu</label></li>
          <li><label><input type="radio" name="q4" value="B"> B. terdapat pemborosan kata berupa penggunaan "meskipun" dan "namun" secara bersamaan</label></li>
          <li><label><input type="radio" name="q4" value="C"> C. tidak memiliki subjek yang jelas</label></li>
          <li><label><input type="radio" name="q4" value="D"> D. menggunakan kata "bersikeras" yang tidak baku</label></li>
          <li><label><input type="radio" name="q4" value="E"> E. struktur kalimatnya terlalu panjang</label></li>
        </ul>
        <div class="feedback" id="fb-q4"></div>
      </div>

      <!-- Soal 5 -->
      <div class="question" data-type="pg" data-answer="B">
        <div><span class="difficulty-badge badge-sedang">Sedang • C4</span></div>
        <div class="question-text">
          <span class="question-number">5</span>
          Bacalah kutipan cerpen berikut!
        </div>
        <div class="passage">
          <p>"Ia menatap cermin. Wajah yang memantul di sana bukan wajah yang ia kenal. Matanya sayu, pipinya cekung. Di dadanya, ada sesuatu yang telah lama hilang—sebuah harapan."</p>
        </div>
        <div class="question-text">Majka yang paling tepat untuk menggambarkan suasana kutipan tersebut adalah …</div>
        <ul class="options">
          <li><label><input type="radio" name="q5" value="A"> A. kegembiraan yang meluap</label></li>
          <li><label><input type="radio" name="q5" value="B"> B. kekosongan dan kehilangan</label></li>
          <li><label><input type="radio" name="q5" value="C"> C. kemarahan yang terpendam</label></li>
          <li><label><input type="radio" name="q5" value="D"> D. ketenangan yang semu</label></li>
          <li><label><input type="radio" name="q5" value="E"> E. kebingungan yang lucu</label></li>
        </ul>
        <div class="feedback" id="fb-q5"></div>
      </div>

      <!-- Soal 6 -->
      <div class="question" data-type="pg" data-answer="B">
        <div><span class="difficulty-badge badge-sulit">Sulit • C4</span></div>
        <div class="question-text">
          <span class="question-number">6</span>
          Cermati dua kutipan teks berikut!
        </div>
        <div class="passage">
          <p><strong>Teks A:</strong> "Program makan siang gratis di sekolah perlu didukung karena terbukti meningkatkan konsentrasi belajar siswa di negara-negara yang telah menerapkannya."</p>
          <p><strong>Teks B:</strong> "Program makan siang gratis harus dipertimbangkan secara matang karena beban anggaran negara yang tidak kecil, sementara masih banyak kebutuhan dasar lain yang lebih mendesak."</p>
        </div>
        <div class="question-text">Perbedaan <strong>sudut pandang</strong> kedua teks tersebut adalah …</div>
        <ul class="options">
          <li><label><input type="radio" name="q6" value="A"> A. Teks A menekankan aspek anggaran; Teks B menekankan aspek gizi</label></li>
          <li><label><input type="radio" name="q6" value="B"> B. Teks A mendukung berdasarkan efektivitas; Teks B mengkritisi berdasarkan efisiensi anggaran</label></li>
          <li><label><input type="radio" name="q6" value="C"> C. Teks A bersifat subjektif; Teks B bersifat objektif</label></li>
          <li><label><input type="radio" name="q6" value="D"> D. Teks A menggunakan data kuantitatif; Teks B menggunakan data kualitatif</label></li>
          <li><label><input type="radio" name="q6" value="E"> E. Teks A menolak program; Teks B menerima program</label></li>
        </ul>
        <div class="feedback" id="fb-q6"></div>
      </div>

      <!-- Soal 7 -->
      <div class="question" data-type="pg" data-answer="C">
        <div><span class="difficulty-badge badge-sulit">Sulit • C5</span></div>
        <div class="question-text">
          <span class="question-number">7</span>
          Bacalah kutipan editorial berikut!
        </div>
        <div class="passage">
          <p>"Pemerintah seolah menutup mata terhadap penderitaan rakyat kecil. Kenaikan harga bahan pokok yang tidak terkendali membuat mereka kian sulit bertahan. Sementara itu, di sisi lain, kebijakan yang dikeluarkan justru berpihak pada pemilik modal besar."</p>
        </div>
        <div class="question-text">Tujuan penulis dalam kutipan editorial tersebut adalah …</div>
        <ul class="options">
          <li><label><input type="radio" name="q7" value="A"> A. menyampaikan informasi netral tentang harga bahan pokok</label></li>
          <li><label><input type="radio" name="q7" value="B"> B. mengajak pembaca untuk mendukung kebijakan pemerintah</label></li>
          <li><label><input type="radio" name="q7" value="C"> C. mengkritik kebijakan pemerintah yang dianggap tidak berpihak pada rakyat</label></li>
          <li><label><input type="radio" name="q7" value="D"> D. memaparkan data ekonomi secara objektif</label></li>
          <li><label><input type="radio" name="q7" value="E"> E. menghibur pembaca dengan sindiran ringan</label></li>
        </ul>
        <div class="feedback" id="fb-q7"></div>
      </div>

      <!-- Soal 8 -->
      <div class="question" data-type="pg" data-answer="C">
        <div><span class="difficulty-badge badge-sulit">Sulit • C4</span></div>
        <div class="question-text">
          <span class="question-number">8</span>
          Perhatikan kalimat berikut!<br><br>
          <em>"Laporan pertanggungjawaban yang disusun oleh panitia kegiatan tersebut telah kami terima dan akan segera kami pelajari sebelum diserahkan kepada pembina."</em><br><br>
          Kalimat tersebut menggunakan <strong>kalimat pasif</strong> yang ditandai oleh …
        </div>
        <ul class="options">
          <li><label><input type="radio" name="q8" value="A"> A. "laporan pertanggungjawaban" sebagai subjek</label></li>
          <li><label><input type="radio" name="q8" value="B"> B. kata "telah" sebagai penanda waktu</label></li>
          <li><label><input type="radio" name="q8" value="C"> C. predikat "kami terima" dengan kata ganti "kami" sebagai pelaku</label></li>
          <li><label><input type="radio" name="q8" value="D"> D. frasa "akan segera" sebagai keterangan</label></li>
          <li><label><input type="radio" name="q8" value="E"> E. "sebelum diserahkan" sebagai anak kalimat</label></li>
        </ul>
        <div class="feedback" id="fb-q8"></div>
      </div>

      <!-- Soal 9 -->
      <div class="question" data-type="pg" data-answer="A">
        <div><span class="difficulty-badge badge-sulit">Sulit • C4</span></div>
        <div class="question-text">
          <span class="question-number">9</span>
          Cermati kutipan puisi berikut!
        </div>
        <div class="passage">
          <p>Aku adalah rumah yang tak pernah kau tinggali<br>
          Aku adalah jalan yang tak pernah kau lalui<br>
          Aku adalah nama yang tak pernah kau sebut</p>
        </div>
        <div class="question-text">Majas yang dominan dalam kutipan tersebut adalah …</div>
        <ul class="options">
          <li><label><input type="radio" name="q9" value="A"> A. metafora</label></li>
          <li><label><input type="radio" name="q9" value="B"> B. personifikasi</label></li>
          <li><label><input type="radio" name="q9" value="C"> C. hiperbola</label></li>
          <li><label><input type="radio" name="q9" value="D"> D. eufemisme</label></li>
          <li><label><input type="radio" name="q9" value="E"> E. litotes</label></li>
        </ul>
        <div class="feedback" id="fb-q9"></div>
      </div>

      <!-- Soal 10 -->
      <div class="question" data-type="pg" data-answer="C">
        <div><span class="difficulty-badge badge-sulit">Sulit • C4</span></div>
        <div class="question-text">
          <span class="question-number">10</span>
          Bacalah kutipan teks negosiasi berikut!
        </div>
        <div class="passage">
          <p><strong>Pembeli:</strong> "Bu, boleh saya minta harga lebih murah? Saya mahasiswa, uang saya terbatas."</p>
          <p><strong>Penjual:</strong> "Hmm, ini sudah harga pas, Mas. Tapi kalau ambil tiga, saya kasih potongan lima ribu per item."</p>
          <p><strong>Pembeli:</strong> "Baiklah, Bu. Saya ambil tiga. Terima kasih."</p>
        </div>
        <div class="question-text">Tahap negosiasi yang ditunjukkan oleh dialog penjual adalah …</div>
        <ul class="options">
          <li><label><input type="radio" name="q10" value="A"> A. orientasi</label></li>
          <li><label><input type="radio" name="q10" value="B"> B. pengajuan</label></li>
          <li><label><input type="radio" name="q10" value="C"> C. penawaran</label></li>
          <li><label><input type="radio" name="q10" value="D"> D. persetujuan</label></li>
          <li><label><input type="radio" name="q10" value="E"> E. penutup</label></li>
        </ul>
        <div class="feedback" id="fb-q10"></div>
      </div>

      <!-- Soal 11 -->
      <div class="question" data-type="pg" data-answer="B">
        <div><span class="difficulty-badge badge-sulit">Sulit • C5</span></div>
        <div class="question-text">
          <span class="question-number">11</span>
          Perhatikan data berikut!
        </div>
        <table class="rubric-table">
          <tr><th>No.</th><th>Pernyataan</th></tr>
          <tr><td>1</td><td>Siswa yang membaca buku fiksi &gt; 5 judul/tahun memiliki skor literasi lebih tinggi</td></tr>
          <tr><td>2</td><td>Kebiasaan membaca berkorelasi positif dengan kemampuan menulis</td></tr>
          <tr><td>3</td><td>Minat baca siswa Indonesia tergolong rendah</td></tr>
          <tr><td>4</td><td>Perpustakaan sekolah kurang dimanfaatkan</td></tr>
        </table>
        <div class="question-text">
          Berdasarkan data tersebut, <strong>simpulan yang paling tepat</strong> untuk proposal penelitian berjudul <em>"Pengaruh Kebiasaan Membaca terhadap Kemampuan Menulis Siswa"</em> adalah …
        </div>
        <ul class="options">
          <li><label><input type="radio" name="q11" value="A"> A. Minat baca siswa rendah sehingga perlu program literasi</label></li>
          <li><label><input type="radio" name="q11" value="B"> B. Terdapat korelasi positif antara kebiasaan membaca dan kemampuan menulis</label></li>
          <li><label><input type="radio" name="q11" value="C"> C. Perpustakaan sekolah tidak berfungsi optimal</label></li>
          <li><label><input type="radio" name="q11" value="D"> D. Siswa lebih suka membaca buku fiksi daripada nonfiksi</label></li>
          <li><label><input type="radio" name="q11" value="E"> E. Kemampuan menulis siswa dipengaruhi oleh kurikulum</label></li>
        </ul>
        <div class="feedback" id="fb-q11"></div>
      </div>

      <!-- Soal 12 -->
      <div class="question" data-type="pg" data-answer="B">
        <div><span class="difficulty-badge badge-sangat">Sangat Sulit • C5</span></div>
        <div class="question-text">
          <span class="question-number">12</span>
          Cermati dua kritik sastra berikut!
        </div>
        <div class="passage">
          <p><strong>Kritik A:</strong> "Novel ini gagal membangun karakter tokoh utama. Perubahan sikapnya dari penakut menjadi pemberani terjadi secara tiba-tiba tanpa proses psikologis yang meyakinkan."</p>
          <p><strong>Kritik B:</strong> "Novel ini justru berhasil menampilkan tokoh utama yang kompleks. Perubahan sikapnya yang mendadak adalah cerminan realitas bahwa manusia dapat berubah dalam situasi ekstrem—sebuah pilihan artistik yang berani."</p>
        </div>
        <div class="question-text">Perbedaan <strong>pendekatan kritik</strong> yang digunakan kedua kritikus tersebut adalah …</div>
        <ul class="options">
          <li><label><input type="radio" name="q12" value="A"> A. Kritik A menggunakan pendekatan mimetik; Kritik B menggunakan pendekatan pragmatik</label></li>
          <li><label><input type="radio" name="q12" value="B"> B. Kritik A menggunakan pendekatan objektif (struktural); Kritik B menggunakan pendekatan reseptif/ekspresif</label></li>
          <li><label><input type="radio" name="q12" value="C"> C. Kritik A menggunakan pendekatan moral; Kritik B menggunakan pendekatan psikologis</label></li>
          <li><label><input type="radio" name="q12" value="D"> D. Kritik A menggunakan pendekatan sosiologis; Kritik B menggunakan pendekatan formalis</label></li>
          <li><label><input type="radio" name="q12" value="E"> E. Keduanya menggunakan pendekatan yang sama, hanya berbeda kesimpulan</label></li>
        </ul>
        <div class="feedback" id="fb-q12"></div>
      </div>

      <!-- Soal 13 -->
      <div class="question" data-type="pg" data-answer="A">
        <div><span class="difficulty-badge badge-sangat">Sangat Sulit • C5</span></div>
        <div class="question-text">
          <span class="question-number">13</span>
          Bacalah kutipan esai berikut!
        </div>
        <div class="passage">
          <p>"Ironisnya, di negeri yang katanya kaya akan budaya gotong royong ini, kita justru semakin individualistis. Media sosial yang seharusnya mendekatkan, malah menjauhkan. Kita sibuk mengomentari kehidupan orang lain, sementara tetangga sebelah rumah sakit sendirian."</p>
        </div>
        <div class="question-text">Gaya bahasa yang <strong>paling menonjol</strong> dalam kutipan esai tersebut adalah …</div>
        <ul class="options">
          <li><label><input type="radio" name="q13" value="A"> A. ironi dan paradoks</label></li>
          <li><label><input type="radio" name="q13" value="B"> B. simile dan metafora</label></li>
          <li><label><input type="radio" name="q13" value="C"> C. hiperbola dan litotes</label></li>
          <li><label><input type="radio" name="q13" value="D"> D. personifikasi dan alegori</label></li>
          <li><label><input type="radio" name="q13" value="E"> E. eufemisme dan sarkasme</label></li>
        </ul>
        <div class="feedback" id="fb-q13"></div>
      </div>

      <!-- Soal 14 -->
      <div class="question" data-type="pg" data-answer="B">
        <div><span class="difficulty-badge badge-sangat">Sangat Sulit • C5</span></div>
        <div class="question-text">
          <span class="question-number">14</span>
          Perhatikan kutipan karya ilmiah berikut!
        </div>
        <div class="passage">
          <p>"Berdasarkan hasil penelitian, dapat disimpulkan bahwa terdapat hubungan signifikan antara intensitas penggunaan media sosial dan tingkat kecemasan remaja (p &lt; 0,05). Namun, penelitian ini hanya melibatkan 30 responden dari satu sekolah, sehingga hasilnya belum dapat digeneralisasikan ke populasi yang lebih luas."</p>
        </div>
        <div class="question-text">Kelemahan metodologis yang diakui penulis dalam kutipan tersebut adalah …</div>
        <ul class="options">
          <li><label><input type="radio" name="q14" value="A"> A. tidak menggunakan analisis statistik</label></li>
          <li><label><input type="radio" name="q14" value="B"> B. sampel terlalu kecil dan tidak representatif</label></li>
          <li><label><input type="radio" name="q14" value="C"> C. tidak ada variabel kontrol</label></li>
          <li><label><input type="radio" name="q14" value="D"> D. instrumen penelitian tidak valid</label></li>
          <li><label><input type="radio" name="q14" value="E"> E. kesimpulan tidak sesuai dengan rumusan masalah</label></li>
        </ul>
        <div class="feedback" id="fb-q14"></div>
      </div>

      <!-- Soal 15 -->
      <div class="question" data-type="pg" data-answer="A">
        <div><span class="difficulty-badge badge-sangat">Sangat Sulit • C4</span></div>
        <div class="question-text">
          <span class="question-number">15</span>
          Cermati dua kalimat berikut!
        </div>
        <div class="passage">
          <p><strong>(1)</strong> "Para siswa-siswa yang hadir di acara sosialisasi tersebut diberikan penjelasan mengenai bahaya narkoba."</p>
          <p><strong>(2)</strong> "Kepada para peserta diharapkan hadir tepat waktu."</p>
        </div>
        <div class="question-text">Alasan kedua kalimat tersebut <strong>tidak baku</strong> adalah …</div>
        <ul class="options">
          <li><label><input type="radio" name="q15" value="A"> A. (1) pemborosan kata "para" + "siswa-siswa"; (2) pemborosan kata "kepada" + "para" dan subjek tidak jelas</label></li>
          <li><label><input type="radio" name="q15" value="B"> B. (1) tidak memiliki subjek; (2) tidak memiliki predikat</label></li>
          <li><label><input type="radio" name="q15" value="C"> C. (1) menggunakan kata tidak baku; (2) menggunakan kalimat pasif yang salah</label></li>
          <li><label><input type="radio" name="q15" value="D"> D. (1) salah ejaan; (2) salah tanda baca</label></li>
          <li><label><input type="radio" name="q15" value="E"> E. (1) dan (2) sama-sama tidak memiliki objek</label></li>
        </ul>
        <div class="feedback" id="fb-q15"></div>
      </div>

      <!-- ============ BAGIAN II: PG KOMPLEKS ============ -->
      <div class="section-title">BAGIAN II — PILIHAN GANDA KOMPLEKS (Soal 16–20)</div>
      <div class="note">📌 <strong>Petunjuk:</strong> Pilih lebih dari satu jawaban yang benar!</div>

      <!-- Soal 16 -->
      <div class="question" data-type="pgk" data-answer="A,C">
        <div><span class="difficulty-badge badge-sulit">Sulit • C5</span></div>
        <div class="question-text">
          <span class="question-number">16</span>
          Bacalah teks berikut!
        </div>
        <div class="passage">
          <p>"Pemerintah resmi menaikkan harga BBM bersubsidi mulai bulan depan. Kebijakan ini diambil untuk mengurangi beban subsidi yang membengkak. Namun, dampaknya terhadap daya beli masyarakat kecil perlu diwaspadai. Oleh karena itu, pemerintah menjanjikan bantuan langsung tunai sebagai kompensasi."</p>
        </div>
        <div class="question-text">Pernyataan yang <strong>sesuai</strong> dengan teks tersebut adalah … <em>(pilih 2 jawaban)</em></div>
        <ul class="options">
          <li><label><input type="checkbox" name="q16" value="A"> A. Kenaikan harga BBM dilakukan untuk mengurangi subsidi yang membengkak</label></li>
          <li><label><input type="checkbox" name="q16" value="B"> B. Pemerintah tidak memberikan kompensasi apa pun</label></li>
          <li><label><input type="checkbox" name="q16" value="C"> C. Daya beli masyarakat kecil berpotensi terdampak</label></li>
          <li><label><input type="checkbox" name="q16" value="D"> D. Kenaikan BBM berlaku bulan ini</label></li>
          <li><label><input type="checkbox" name="q16" value="E"> E. Bantuan langsung tunai diberikan kepada seluruh masyarakat</label></li>
        </ul>
        <div class="feedback" id="fb-q16"></div>
      </div>

      <!-- Soal 17 -->
      <div class="question" data-type="pgk" data-answer="B,C">
        <div><span class="difficulty-badge badge-sulit">Sulit • C4</span></div>
        <div class="question-text">
          <span class="question-number">17</span>
          Cermati kutipan drama berikut!
        </div>
        <div class="passage">
          <p><strong>Ayu:</strong> "Kau tidak pernah mengerti perasaanku, Mas."</p>
          <p><strong>Bima:</strong> "Aku sudah berusaha, Yu. Tapi kau juga harus mengerti posisiku."</p>
          <p><strong>Ayu:</strong> "Posisi? Selalu posisi! Kau lebih mementingkan pekerjaanmu daripada keluarga!"</p>
          <p><strong>Bima:</strong> <em>(terdiam, menunduk)</em></p>
        </div>
        <div class="question-text">Konflik yang tergambar dalam kutipan drama tersebut adalah … <em>(pilih 2 jawaban)</em></div>
        <ul class="options">
          <li><label><input type="checkbox" name="q17" value="A"> A. perebutan harta warisan</label></li>
          <li><label><input type="checkbox" name="q17" value="B"> B. ketidakseimbangan antara pekerjaan dan keluarga</label></li>
          <li><label><input type="checkbox" name="q17" value="C"> C. kesalahpahaman dalam komunikasi pasangan</label></li>
          <li><label><input type="checkbox" name="q17" value="D"> D. persaingan bisnis antar saudara</label></li>
          <li><label><input type="checkbox" name="q17" value="E"> E. konflik politik dalam keluarga</label></li>
        </ul>
        <div class="feedback" id="fb-q17"></div>
      </div>

      <!-- Soal 18 -->
      <div class="question" data-type="pgk" data-answer="A,C,E">
        <div><span class="difficulty-badge badge-sulit">Sulit • C5</span></div>
        <div class="question-text">
          <span class="question-number">18</span>
          Perhatikan pernyataan tentang <strong>karya ilmiah</strong> berikut! <em>(pilih 3 jawaban benar)</em>
        </div>
        <ul class="options">
          <li><label><input type="checkbox" name="q18" value="A"> A. Karya ilmiah harus menggunakan bahasa baku dan denotatif</label></li>
          <li><label><input type="checkbox" name="q18" value="B"> B. Karya ilmiah boleh menggunakan bahasa konotatif untuk memperindah</label></li>
          <li><label><input type="checkbox" name="q18" value="C"> C. Sumber rujukan harus dicantumkan secara jelas</label></li>
          <li><label><input type="checkbox" name="q18" value="D"> D. Opini penulis harus mendominasi seluruh isi</label></li>
          <li><label><input type="checkbox" name="q18" value="E"> E. Struktur karya ilmiah mencakup pendahuluan, metode, hasil, dan pembahasan</label></li>
        </ul>
        <div class="feedback" id="fb-q18"></div>
      </div>

      <!-- Soal 19 -->
      <div class="question" data-type="pgk" data-answer="A,B,C,E">
        <div><span class="difficulty-badge badge-sulit">Sulit • C4</span></div>
        <div class="question-text">
          <span class="question-number">19</span>
          Bacalah kutipan proposal berikut!
        </div>
        <div class="passage">
          <p>"Kegiatan ini bertujuan meningkatkan kesadaran siswa terhadap pentingnya pengelolaan sampah. Sasaran kegiatan adalah siswa kelas X–XII. Kegiatan akan dilaksanakan pada 15–17 November 2024 di aula sekolah. Anggaran yang dibutuhkan sebesar Rp7.500.000,00."</p>
        </div>
        <div class="question-text">Informasi yang <strong>lengkap</strong> tersedia dalam kutipan proposal tersebut adalah … <em>(pilih 4 jawaban)</em></div>
        <ul class="options">
          <li><label><input type="checkbox" name="q19" value="A"> A. tujuan kegiatan</label></li>
          <li><label><input type="checkbox" name="q19" value="B"> B. sasaran kegiatan</label></li>
          <li><label><input type="checkbox" name="q19" value="C"> C. waktu dan tempat pelaksanaan</label></li>
          <li><label><input type="checkbox" name="q19" value="D"> D. susunan panitia</label></li>
          <li><label><input type="checkbox" name="q19" value="E"> E. anggaran kegiatan</label></li>
        </ul>
        <div class="feedback" id="fb-q19"></div>
      </div>

      <!-- Soal 20 -->
      <div class="question" data-type="pgk" data-answer="A,C">
        <div><span class="difficulty-badge badge-sangat">Sangat Sulit • C5</span></div>
        <div class="question-text">
          <span class="question-number">20</span>
          Cermati kutipan teks debat berikut!
        </div>
        <div class="passage">
          <p><strong>Moderator:</strong> "Silakan tim kontra menyampaikan sanggahan."</p>
          <p><strong>Tim Kontra:</strong> "Kami menolak argumen tim pro bahwa penggunaan AI dalam pembelajaran meningkatkan kreativitas. Faktanya, AI justru cenderung menyeragamkan jawaban dan mengurangi proses berpikir kritis siswa."</p>
        </div>
        <div class="question-text">Kelemahan argumen tim kontra tersebut adalah … <em>(pilih 2 jawaban)</em></div>
        <ul class="options">
          <li><label><input type="checkbox" name="q20" value="A"> A. tidak menyebutkan data atau bukti empiris</label></li>
          <li><label><input type="checkbox" name="q20" value="B"> B. menggunakan bahasa yang tidak sopan</label></li>
          <li><label><input type="checkbox" name="q20" value="C"> C. mengabaikan bahwa AI juga dapat digunakan sebagai alat bantu berpikir</label></li>
          <li><label><input type="checkbox" name="q20" value="D"> D. tidak menyanggah argumen tim pro sama sekali</label></li>
          <li><label><input type="checkbox" name="q20" value="E"> E. keluar dari topik debat</label></li>
        </ul>
        <div class="feedback" id="fb-q20"></div>
      </div>

      <!-- ============ BAGIAN III: URAIAN ============ -->
      <div class="section-title">BAGIAN III — URAIAN (Soal 21–23)</div>

      <!-- Soal 21 -->
      <div class="question" data-type="uraian">
        <div><span class="difficulty-badge badge-sedang">Sedang–Sulit • C4</span></div>
        <div class="question-text">
          <span class="question-number">21</span>
          Bacalah dua kutipan berikut!
        </div>
        <div class="passage">
          <p><strong>Kutipan 1:</strong> "Oleh karena itu, diperlukan sinergi antara pemerintah, sekolah, dan orang tua dalam membangun budaya literasi."</p>
          <p><strong>Kutipan 2:</strong> "Jadi, mau tidak mau, suka tidak suka, kita harus mulai membaca dari sekarang."</p>
        </div>
        <div class="question-text">
          Bandingkan <strong>kekuatan argumentasi</strong> kedua kutipan tersebut! Manakah yang lebih efektif sebagai bagian dari teks argumentasi? Jelaskan alasanmu berdasarkan aspek <strong>diksi, kelogisan, dan kesantunan berbahasa</strong>!
        </div>
        <textarea class="input-uraian" name="q21" placeholder="Tulis jawabanmu di sini..."></textarea>
      </div>

      <!-- Soal 22 -->
      <div class="question" data-type="uraian">
        <div><span class="difficulty-badge badge-sulit">Sulit • C5</span></div>
        <div class="question-text">
          <span class="question-number">22</span>
          Perhatikan data berikut!
        </div>
        <table class="rubric-table">
          <tr><th>No.</th><th>Judul Buku</th><th>Jenis</th><th>Peminjam (2023)</th><th>Peminjam (2024)</th></tr>
          <tr><td>1</td><td><em>Bumi Manusia</em></td><td>Fiksi</td><td>45</td><td>38</td></tr>
          <tr><td>2</td><td><em>Laskar Pelangi</em></td><td>Fiksi</td><td>52</td><td>60</td></tr>
          <tr><td>3</td><td><em>Sapiens</em></td><td>Nonfiksi</td><td>20</td><td>15</td></tr>
          <tr><td>4</td><td><em>Filosofi Teras</em></td><td>Nonfiksi</td><td>30</td><td>42</td></tr>
          <tr><td>5</td><td><em>Atomic Habits</em></td><td>Nonfiksi</td><td>25</td><td>48</td></tr>
        </table>
        <div class="question-text">
          Berdasarkan data tersebut:<br>
          a. <strong>Evaluasilah</strong> tren peminjaman buku fiksi vs. nonfiksi!<br>
          b. <strong>Simpulkan</strong> jenis buku yang paling diminati pada 2024!<br>
          c. <strong>Berikan rekomendasi</strong> kepada pustakawan berdasarkan simpulan tersebut!
        </div>
        <textarea class="input-uraian" name="q22" placeholder="Tulis jawabanmu di sini..."></textarea>
      </div>

      <!-- Soal 23 -->
      <div class="question" data-type="uraian">
        <div><span class="difficulty-badge badge-sangat">Sangat Sulit • C5</span></div>
        <div class="question-text">
          <span class="question-number">23</span>
          Bacalah kutipan esai berikut!
        </div>
        <div class="passage">
          <p>"Kita bangga menjadi bangsa yang beragam, tetapi keragaman itu sering kali justru menjadi sumber perpecahan. Perbedaan agama, suku, dan pandangan politik kerap dijadikan alasan untuk saling menjatuhkan. Di media sosial, kita dengan mudahnya menghakimi orang lain hanya karena berbeda pendapat. Padahal, bukankah keragaman seharusnya menjadi kekuatan, bukan kelemahan?"</p>
        </div>
        <div class="question-text">
          <strong>Evaluasilah</strong> kutipan esai tersebut berdasarkan:<br>
          a. Kekuatan argumen (apakah didukung bukti/logika yang kuat?)<br>
          b. Kelemahan argumen (apakah ada generalisasi berlebihan?)<br>
          c. Saran perbaikan agar argumen lebih meyakinkan!
        </div>
        <textarea class="input-uraian" name="q23" placeholder="Tulis jawabanmu di sini..."></textarea>
      </div>

      <!-- ============ BAGIAN IV: MENCIpta ============ -->
      <div class="section-title">BAGIAN IV — SOAL MENCIpta (C6)</div>

      <!-- Soal 24 -->
      <div class="question" data-type="uraian">
        <div><span class="difficulty-badge badge-sangat">Sangat Sulit • C6</span></div>
        <div class="question-text">
          <span class="question-number">24</span>
          Bacalah teks berikut!
        </div>
        <div class="passage">
          <p>"Fenomena 'doomscrolling'—kebiasaan menghabiskan waktu berjam-jam menelusuri berita negatif di media sosial—semakin marak di kalangan remaja. Dampaknya, tingkat kecemasan dan stres remaja meningkat. Namun, banyak remaja yang tidak menyadari bahwa kebiasaan ini merugikan kesehatan mental mereka."</p>
        </div>
        <div class="question-text">
          <strong>Tugas:</strong><br>
          1. <strong>Ciptakan</strong> sebuah <strong>teks argumentasi</strong> (3–5 paragraf) yang bertujuan meyakinkan pembaca (remaja) untuk mengurangi kebiasaan <em>doomscrolling</em>!<br>
          2. Gunakan <strong>minimal 2 strategi argumentasi</strong> (data/fakta, contoh, analogi, atau otoritas ahli)!<br>
          3. Perhatikan <strong>struktur teks argumentasi</strong> (pendahuluan, argumen, simpulan) dan <strong>keefektifan kalimat</strong>!
        </div>
        <textarea class="input-uraian" name="q24" placeholder="Tulis teks argumentasimu di sini..." style="min-height: 250px;"></textarea>
      </div>

      <!-- Tombol -->
      <div class="btn-group">
        <button type="button" class="btn-submit" onclick="submitExam()">✅ Kumpulkan &amp; Lihat Nilai</button>
        <button type="button" class="btn-reset" onclick="resetExam()">🔄 Ulangi Ujian</button>
      </div>

      <!-- Hasil -->
      <div class="result" id="result">
        <h2>📊 Hasil Ujian</h2>
        <div class="score-display" id="scoreDisplay">0</div>
        <div class="score-label" id="scoreLabel">dari 100</div>
        <div class="score-detail" id="scoreDetail"></div>
        <div id="uraianNote" style="margin-top: 20px; font-size: 0.9em; color: #666;"></div>
      </div>

    </form>
  </div>

  <footer>
    <p>© 2024 Ujian Bahasa Indonesia Kelas XII — Kurikulum Merdeka | HOTS C4–C6</p>
    <p style="margin-top: 5px; opacity: 0.7;">Dikembangkan untuk asesmen literasi dan penalaran kritis</p>
  </footer>
</div>

<script>
  // Kunci jawaban PG & PG Kompleks
  const answerKeys = {
    q1: "B", q2: "E", q3: "C", q4: "B", q5: "B",
    q6: "B", q7: "C", q8: "C", q9: "A", q10: "C",
    q11: "B", q12: "B", q13: "A", q14: "B", q15: "A",
    q16: ["A", "C"],
    q17: ["B", "C"],
    q18: ["A", "C", "E"],
    q19: ["A", "B", "C", "E"],
    q20: ["A", "C"]
  };

  // Pembahasan singkat
  const explanations = {
    q1: "Ide pokok mencakup keseluruhan paragraf: ketidaksesuaian kebijakan Indonesia dengan realitas perubahan iklim.",
    q2: "Kalimat (3) 'masih terkesan setengah hati' dan (5) 'berseberangan dengan komitmen' merupakan opini penulis.",
    q3: "Konteks kalimat menunjukkan 'retorika politik tanpa makna' = pernyataan simbolis yang tidak diwujudkan.",
    q4: "Konjungsi 'meskipun' dan 'namun' tidak digunakan sekaligus karena bermakna sama (pleonasme).",
    q5: "Diksi 'sayu,' 'cekung,' 'telah lama hilang' menunjukkan kekosongan dan kehilangan.",
    q6: "Teks A = argumen pro berdasarkan efektivitas; Teks B = argumen kontra berdasarkan anggaran.",
    q7: "Diksi 'menutup mata,' 'berpihak pada pemilik modal' menunjukkan kritik terhadap pemerintah.",
    q8: "Kalimat pasif ditandai predikat dengan kata ganti pelaku 'kami' sebelum verba tanpa awalan.",
    q9: "'Aku adalah rumah/jalan/nama' merupakan metafora (perbandingan langsung tanpa kata pembanding).",
    q10: "Penjual mengajukan penawaran (potongan harga jika ambil tiga) sebagai respons permintaan pembeli.",
    q11: "Data (1) dan (2) secara langsung mendukung judul penelitian tentang pengaruh kebiasaan membaca.",
    q12: "Kritik A = pendekatan objektif/struktural; Kritik B = pendekatan reseptif/ekspresif.",
    q13: "Pertentangan 'gotong royong' vs 'individualistis,' 'mendekatkan' vs 'menjauhkan' = ironi dan paradoks.",
    q14: "Penulis menyebut keterbatasan: 30 responden dari satu sekolah → sampel kecil dan tidak representatif.",
    q15: "'Para siswa-siswa' = pleonasme; 'Kepada para peserta diharapkan hadir' = pemborosan + subjek tidak jelas.",
    q16: "Pernyataan A dan C sesuai teks. B, D, E bertentangan dengan isi teks.",
    q17: "Konflik: ketidakseimbangan pekerjaan-keluarga dan kesalahpahaman komunikasi pasangan.",
    q18: "Karya ilmiah: bahasa baku denotatif (A), sumber rujukan jelas (C), struktur lengkap (E).",
    q19: "Informasi lengkap: tujuan (A), sasaran (B), waktu/tempat (C), anggaran (E). Susunan panitia tidak ada.",
    q20: "Kelemahan: tidak ada data/bukti empiris (A) dan mengabaikan sisi positif AI (C)."
  };

  // Fungsi submit
  function submitExam() {
    let correct = 0;
    let totalPG = 15;
    let totalPGK = 5;
    let pgScore = 0, pgkScore = 0;

    // Cek PG
    for (let i = 1; i <= 15; i++) {
      const name = "q" + i;
      const selected = document.querySelector(`input[name="${name}"]:checked`);
      const fb = document.getElementById("fb-" + name);
      const correctAns = answerKeys[name];

      fb.classList.remove("show", "correct", "incorrect");

      if (selected) {
        if (selected.value === correctAns) {
          correct++;
          pgScore++;
          fb.className = "feedback show correct";
          fb.innerHTML = "✅ <strong>Benar!</strong><br>" + explanations[name];
        } else {
          fb.className = "feedback show incorrect";
          fb.innerHTML = "❌ <strong>Salah.</strong> Jawaban benar: <span class='answer-key'>" + correctAns + "</span><br>" + explanations[name];
        }
      } else {
        fb.className = "feedback show incorrect";
        fb.innerHTML = "⚠️ <strong>Tidak dijawab.</strong> Jawaban benar: <span class='answer-key'>" + correctAns + "</span><br>" + explanations[name];
      }
    }

    // Cek PG Kompleks (parsial: setiap jawaban benar +1, salah -0.5)
    for (let i = 16; i <= 20; i++) {
      const name = "q" + i;
      const checked = Array.from(document.querySelectorAll(`input[name="${name}"]:checked`)).map(c => c.value);
      const fb = document.getElementById("fb-" + name);
      const correctAns = answerKeys[name];

      fb.classList.remove("show", "correct", "incorrect");

      let score = 0;
      checked.forEach(val => {
        if (correctAns.includes(val)) score += 1;
        else score -= 0.5;
      });
      // Normalisasi: skor maksimal = jumlah jawaban benar
      let normalized = Math.max(0, score) / correctAns.length;
      pgkScore += normalized;

      if (normalized === 1) {
        fb.className = "feedback show correct";
        fb.innerHTML = "✅ <strong>Benar semua!</strong> Jawaban: " + correctAns.join(", ") + "<br>" + explanations[name];
      } else if (normalized > 0) {
        fb.className = "feedback show incorrect";
        fb.innerHTML = "⚠️ <strong>Sebagian benar.</strong> Jawaban benar: <span class='answer-key'>" + correctAns.join(", ") + "</span><br>" + explanations[name];
      } else {
        fb.className = "feedback show incorrect";
        fb.innerHTML = "❌ <strong>Salah.</strong> Jawaban benar: <span class='answer-key'>" + correctAns.join(", ") + "</span><br>" + explanations[name];
      }
    }

    // Hitung nilai
    const pgPercent = (pgScore / totalPG) * 60;   // bobot 60%
    const pgkPercent = (pgkScore / totalPGK) * 40; // bobot 40%
    const finalScore = Math.round(pgPercent + pgkPercent);

    // Tampilkan hasil
    const result = document.getElementById("result");
    result.classList.add("show");
    document.getElementById("scoreDisplay").textContent = finalScore;
    document.getElementById("scoreLabel").textContent = "dari 100 (PG & PG Kompleks)";

    let predikat = "";
    if (finalScore >= 85) predikat = "🌟 Sangat Baik (A)";
    else if (finalScore >= 70) predikat = "👍 Baik (B)";
    else if (finalScore >= 55) predikat = "📘 Cukup (C)";
    else predikat = "📕 Perlu Belajar Lagi (D)";

    document.getElementById("scoreDetail").innerHTML = `
      <div class="score-item">
        <div class="num">${pgScore}/${totalPG}</div>
        <div class="lbl">Pilihan Ganda</div>
      </div>
      <div class="score-item">
        <div class="num">${pgkScore.toFixed(1)}/${totalPGK}</div>
        <div class="lbl">PG Kompleks</div>
      </div>
      <div class="score-item">
        <div class="num">${predikat}</div>
        <div class="lbl">Predikat</div>
      </div>
    `;

    document.getElementById("uraianNote").innerHTML =
      "📝 <strong>Catatan:</strong> Soal uraian (21–24) dinilai manual oleh guru menggunakan rubrik yang tersedia. Nilai di atas hanya mencakup soal pilihan ganda.";

    result.scrollIntoView({ behavior: "smooth", block: "start" });
  }

  // Fungsi reset
  function resetExam() {
    if (!confirm("Yakin ingin mengulangi ujian? Semua jawaban akan dihapus.")) return;
    document.getElementById("examForm").reset();
    document.querySelectorAll(".feedback").forEach(fb => {
      fb.classList.remove("show", "correct", "incorrect");
      fb.innerHTML = "";
    });
    document.getElementById("result").classList.remove("show");
    window.scrollTo({ top: 0, behavior: "smooth" });
  }

  // Highlight pilihan
  document.querySelectorAll(".options input").forEach(input => {
    input.addEventListener("change", function() {
      const name = this.name;
      if (this.type === "radio") {
        document.querySelectorAll(`input[name="${name}"]`).forEach(inp => {
          inp.closest("label").classList.remove("selected");
        });
      }
      if (this.checked) {
        this.closest("label").classList.add("selected");
      } else {
        this.closest("label").classList.remove("selected");
      }
    });
  });
</script>
</body>
</html>
