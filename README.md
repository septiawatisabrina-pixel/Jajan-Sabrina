<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=yes, viewport-fit=cover">
  <title>Sabrina • Keuangan Jajan</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      background: linear-gradient(145deg, #f9efe2 0%, #fce4d4 100%);
      font-family: 'Segoe UI', 'Poppins', system-ui, -apple-system, sans-serif;
      min-height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      padding: 1.5rem;
      margin: 0;
    }

    .app-container {
      max-width: 500px;
      width: 100%;
      background: rgba(255, 248, 240, 0.85);
      backdrop-filter: blur(18px);
      -webkit-backdrop-filter: blur(18px);
      background: #fffbf5;
      border-radius: 3rem;
      box-shadow: 0 25px 45px rgba(120, 70, 40, 0.15), 0 10px 20px rgba(0,0,0,0.05);
      padding: 2rem 1.5rem 2.2rem;
      border: 1px solid rgba(255, 215, 180, 0.7);
    }

    /* Header Sabrina */
    .brand {
      display: flex;
      align-items: center;
      justify-content: space-between;
      margin-bottom: 1.8rem;
    }

    .logo-text {
      display: flex;
      align-items: baseline;
      gap: 0.2rem;
    }

    .app-name {
      font-size: 2.4rem;
      font-weight: 700;
      letter-spacing: -0.5px;
      background: linear-gradient(135deg, #b45f3a, #d98c5f);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      text-shadow: 2px 2px 10px rgba(180, 95, 58, 0.2);
    }

    .badge {
      background: #f5d5b8;
      color: #5e3a28;
      font-size: 0.8rem;
      font-weight: 700;
      padding: 0.2rem 0.9rem;
      border-radius: 30px;
      letter-spacing: 0.5px;
      background: #fae3cc;
      box-shadow: inset 0 1px 4px rgba(255,255,255,0.8);
    }

    .balance-card {
      background: #fae9dd;
      border-radius: 2rem;
      padding: 1.4rem 1.8rem;
      margin-bottom: 2rem;
      display: flex;
      justify-content: space-between;
      align-items: center;
      background: #f7e1ce;
      box-shadow: 0 8px 18px rgba(160, 100, 60, 0.18);
      border: 1px solid #efcdb0;
    }

    .balance-label {
      font-size: 0.9rem;
      font-weight: 600;
      color: #7b5a44;
      text-transform: uppercase;
      letter-spacing: 0.4px;
    }

    .balance-amount {
      font-size: 2.2rem;
      font-weight: 700;
      color: #3e2c1f;
      line-height: 1.1;
    }

    .balance-action {
      background: white;
      border: none;
      background: #ffffffd6;
      backdrop-filter: blur(5px);
      font-size: 1.6rem;
      width: 45px;
      height: 45px;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      cursor: pointer;
      box-shadow: 0 6px 12px rgba(140, 80, 30, 0.2);
      color: #a15832;
      transition: all 0.25s ease;
      border: 1px solid #f7cfb0;
      font-weight: bold;
    }

    .balance-action:hover {
      background: #fff2e6;
      transform: scale(1.05);
      color: #7a3b1e;
    }

    .menu-title {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 1.2rem;
      font-weight: 700;
      color: #5a3c2c;
      font-size: 1.1rem;
    }

    .menu-grid {
      display: flex;
      flex-direction: column;
      gap: 1rem;
      margin-bottom: 1.8rem;
    }

    .menu-item {
      background: #ffffff;
      border-radius: 1.8rem;
      padding: 1rem 1.4rem;
      display: flex;
      align-items: center;
      justify-content: space-between;
      box-shadow: 0 12px 20px -10px rgba(150, 90, 40, 0.12);
      border: 1px solid #ffede1;
      transition: all 0.2s ease;
      cursor: pointer;
      background: #fffbf7;
      backdrop-filter: blur(4px);
    }

    .menu-item:active {
      transform: scale(0.98);
      background: #fff3e9;
      border-color: #e7b690;
    }

    .menu-info {
      display: flex;
      align-items: center;
      gap: 1rem;
    }

    .menu-emoji {
      font-size: 2.6rem;
      background: #fbe9dd;
      width: 55px;
      height: 55px;
      display: flex;
      align-items: center;
      justify-content: center;
      border-radius: 18px;
      background: #fae3d3;
      box-shadow: 0 5px 10px rgba(200, 130, 70, 0.1);
    }

    .menu-details h3 {
      font-size: 1.2rem;
      font-weight: 700;
      color: #4a3322;
      margin-bottom: 0.15rem;
    }

    .price {
      font-weight: 700;
      color: #b4693c;
      font-size: 1rem;
      background: #fff1e5;
      padding: 0.2rem 0.8rem;
      border-radius: 20px;
      display: inline-block;
    }

    .click-hint {
      font-size: 0.8rem;
      color: #b18162;
      display: flex;
      align-items: center;
      gap: 0.2rem;
    }

    .click-icon {
      font-size: 1.2rem;
      opacity: 0.8;
    }

    .history-section {
      background: #fbeede;
      border-radius: 1.8rem;
      padding: 1.2rem 1.3rem;
      margin-top: 0.8rem;
      border: 1px solid #f3d7bc;
      box-shadow: inset 0 1px 8px rgba(255,250,245,0.9);
    }

    .history-header {
      display: flex;
      justify-content: space-between;
      font-weight: 700;
      color: #634832;
      margin-bottom: 0.8rem;
      font-size: 0.95rem;
    }

    .history-list {
      max-height: 150px;
      overflow-y: auto;
      font-size: 0.9rem;
      display: flex;
      flex-direction: column;
      gap: 0.5rem;
      padding-right: 4px;
    }

    .history-item {
      display: flex;
      justify-content: space-between;
      background: #fff9f3;
      padding: 0.5rem 0.9rem;
      border-radius: 1.2rem;
      color: #4e3824;
      font-weight: 500;
      border: 1px solid #f7ddcc;
    }

    .empty-history {
      color: #b29278;
      font-style: italic;
      font-size: 0.85rem;
      text-align: center;
      padding: 0.8rem;
    }

    .reset-area {
      display: flex;
      justify-content: flex-end;
      margin-top: 0.7rem;
    }

    .reset-btn {
      background: none;
      border: 1px solid #e0bba0;
      background: #fff4ea;
      padding: 0.4rem 1.2rem;
      border-radius: 2rem;
      font-weight: 600;
      color: #7c5439;
      font-size: 0.8rem;
      cursor: pointer;
      transition: 0.2s;
      display: flex;
      align-items: center;
      gap: 0.2rem;
    }

    .reset-btn:hover {
      background: #f9dcc8;
      border-color: #c28b64;
    }

    hr {
      border: 0.5px solid #edd6c2;
      margin: 0.8rem 0 0.5rem;
    }
  </style>
</head>
<body>
  <div class="app-container">
    <!-- Nama aplikasi Sabrina -->
    <div class="brand">
      <div class="logo-text">
        <span class="app-name">Sabrina</span>
      </div>
      <span class="badge">jajan hemat</span>
    </div>

    <!-- Saldo -->
    <div class="balance-card">
      <div>
        <div class="balance-label">Saldo Sabrina</div>
        <div class="balance-amount" id="saldoDisplay">Rp50.000</div>
      </div>
      <button class="balance-action" id="topupBtn" title="Isi saldo">+</button>
    </div>

    <!-- Menu jajan -->
    <div class="menu-title">
      <span>🍽️ Menu Hari Ini</span>
      <span style="font-size:0.8rem;">klik untuk beli</span>
    </div>

    <div class="menu-grid" id="menuContainer">
      <!-- Menu item akan dirender lewat JavaScript agar dinamis dan bisa diklik -->
    </div>

    <!-- Riwayat transaksi -->
    <div class="history-section">
      <div class="history-header">
        <span>📋 Riwayat Jajan</span>
        <span id="historyCount">0</span>
      </div>
      <div class="history-list" id="historyList">
        <div class="empty-history">Belum ada transaksi</div>
      </div>
      <div class="reset-area">
        <button class="reset-btn" id="resetBtn">
          <span>↺</span> Reset
        </button>
      </div>
    </div>
    <hr>
    <div style="text-align: center; font-size: 0.75rem; color: #b48b6e; margin-top: 0.3rem;">
      ketuk menu untuk jajan • Sabrina
    </div>
  </div>

  <script>
    (function() {
      // Data menu sesuai permintaan: seblak, dimsum keju, butterscotch latte, mie ayam
      const menuItems = [
        { id: 1, name: "Seblak", emoji: "🍲", price: 12000 },
        { id: 2, name: "Dimsum Keju", emoji: "🧀🥟", price: 10000 },
        { id: 3, name: "Butterscotch Latte", emoji: "🍮☕", price: 15000 },
        { id: 4, name: "Mie Ayam", emoji: "🍜", price: 13000 }
      ];

      // State awal
      let saldo = 50000;
      let transactions = []; // array of { id, name, price, timestamp }

      // DOM elements
      const saldoDisplay = document.getElementById('saldoDisplay');
      const menuContainer = document.getElementById('menuContainer');
      const historyList = document.getElementById('historyList');
      const historyCount = document.getElementById('historyCount');
      const topupBtn = document.getElementById('topupBtn');
      const resetBtn = document.getElementById('resetBtn');

      // Format rupiah
      function formatRupiah(angka) {
        return 'Rp' + angka.toLocaleString('id-ID');
      }

      // Update tampilan saldo
      function updateSaldoDisplay() {
        saldoDisplay.textContent = formatRupiah(saldo);
      }

      // Render history list
      function renderHistory() {
        historyList.innerHTML = '';
        if (transactions.length === 0) {
          historyList.innerHTML = '<div class="empty-history">Belum ada transaksi</div>';
        } else {
          // tampilkan dari terbaru (paling atas transaksi terakhir)
          const reversed = [...transactions].reverse();
          reversed.forEach(trx => {
            const historyItem = document.createElement('div');
            historyItem.className = 'history-item';
            const timeStr = new Date(trx.timestamp).toLocaleTimeString('id-ID', { hour: '2-digit', minute: '2-digit' });
            historyItem.innerHTML = `<span>${trx.emoji || '🍴'} ${trx.name}</span><span style="font-weight:700;color:#b45f3a;">-${formatRupiah(trx.price)}</span><span style="font-size:0.7rem;color:#aa8b78;">${timeStr}</span>`;
            historyList.appendChild(historyItem);
          });
        }
        historyCount.textContent = transactions.length;
      }

      // Fungsi beli (dipanggil saat klik menu)
      function beliMenu(menu) {
        if (saldo < menu.price) {
          alert(`💸 Saldo tidak cukup untuk membeli ${menu.name}.\nButuh ${formatRupiah(menu.price)}, saldo kamu ${formatRupiah(saldo)}.`);
          return;
        }

        // Kurangi saldo
        saldo -= menu.price;
        // Catat transaksi
        const newTransaction = {
          id: Date.now(),
          name: menu.name,
          emoji: menu.emoji,
          price: menu.price,
          timestamp: new Date().toISOString()
        };
        transactions.push(newTransaction);

        // Update UI
        updateSaldoDisplay();
        renderHistory();

        // Notifikasi kecil (opsional)
        // Bisa juga tambahkan animasi halus, tapi alert cukup informatif.
        // Gunakan feedback visual tanpa alert yang mengganggu? Kita beri toast sederhana.
        showTemporaryMessage(`✅ Berhasil beli ${menu.name} -${formatRupiah(menu.price)}`);
      }

      // Fungsi pesan sementara (toast tipis)
      function showTemporaryMessage(text) {
        // Buat elemen kecil
        const toast = document.createElement('div');
        toast.textContent = text;
        toast.style.position = 'fixed';
        toast.style.bottom = '30px';
        toast.style.left = '50%';
        toast.style.transform = 'translateX(-50%)';
        toast.style.backgroundColor = '#4e3422';
        toast.style.color = '#fff9f0';
        toast.style.padding = '0.7rem 1.5rem';
        toast.style.borderRadius = '40px';
        toast.style.fontWeight = '600';
        toast.style.fontSize = '0.9rem';
        toast.style.boxShadow = '0 8px 20px rgba(0,0,0,0.2)';
        toast.style.zIndex = '999';
        toast.style.backdropFilter = 'blur(10px)';
        toast.style.background = '#5e3e2bdd';
        document.body.appendChild(toast);

        setTimeout(() => {
          toast.style.transition = 'opacity 0.4s';
          toast.style.opacity = '0';
          setTimeout(() => {
            if (toast.parentNode) toast.parentNode.removeChild(toast);
          }, 400);
        }, 1500);
      }

      // Render menu (bisa diklik)
      function renderMenu() {
        menuContainer.innerHTML = '';
        menuItems.forEach(menu => {
          const menuCard = document.createElement('div');
          menuCard.className = 'menu-item';
          menuCard.setAttribute('data-id', menu.id);
          menuCard.innerHTML = `
            <div class="menu-info">
              <div class="menu-emoji">${menu.emoji}</div>
              <div class="menu-details">
                <h3>${menu.name}</h3>
                <span class="price">${formatRupiah(menu.price)}</span>
              </div>
            </div>
            <div class="click-hint">
              <span>beli</span>
              <span class="click-icon">🛒</span>
            </div>
          `;
          
          // Event klik untuk membeli
          menuCard.addEventListener('click', (e) => {
            // Cegah event bubbling yang tidak diinginkan
            e.stopPropagation();
            beliMenu(menu);
          });

          menuContainer.appendChild(menuCard);
        });
      }

      // Top up saldo (isi ulang)
      function handleTopUp() {
        let jumlah = prompt('💰 Masukkan jumlah top up saldo Sabrina:', '20000');
        if (jumlah === null) return;
        
        const amount = parseInt(jumlah.replace(/\D/g, ''));
        if (isNaN(amount) || amount <= 0) {
          alert('Masukkan angka yang valid untuk top up.');
          return;
        }
        
        saldo += amount;
        updateSaldoDisplay();
        showTemporaryMessage(`✨ Top up berhasil +${formatRupiah(amount)}`);
      }

      // Reset semua data
      function handleReset() {
        if (transactions.length === 0 && saldo === 50000) {
          // opsional: tetap bisa reset saldo ke 50000
        }
        const konfirmasi = confirm('🔄 Reset semua data? Saldo kembali ke Rp50.000 dan riwayat dihapus.');
        if (!konfirmasi) return;
        
        saldo = 50000;
        transactions = [];
        updateSaldoDisplay();
        renderHistory();
        showTemporaryMessage('↺ Data direset. Sabrina siap jajan lagi!');
      }

      // Event listener untuk tombol
      topupBtn.addEventListener('click', handleTopUp);
      resetBtn.addEventListener('click', handleReset);

      // Inisialisasi tampilan
      renderMenu();
      updateSaldoDisplay();
      renderHistory();

      // Optional: klik pada saldo card juga bisa topup (user-friendly)
      const balanceCard = document.querySelector('.balance-card');
      balanceCard.addEventListener('click', (e) => {
        // hanya jika bukan klik tombol + (agar tidak dobel)
        if (e.target.id === 'topupBtn' || e.target.closest('#topupBtn')) return;
        // klik area saldo juga bisa topup
        handleTopUp();
      });

    })();
  </script>
</body>
</html>
