# monte-carlo-stoiip
# Estimasi STOIIP dengan Simulasi Monte Carlo
Sumur Volve 15/9-19 (lanjutan dari interpretasi well log)

## Tujuan
Menghitung STOIIP satu zona pay (4316 sampai 4338 m) beserta
ketidakpastiannya (P90, P50, P10) dengan simulasi Monte Carlo.

## Scope
- Satu zona pay, satu fluida (minyak).
- Ini skenario hipotetis: fluida pada zona ini belum terkonfirmasi
  oleh uji sumur atau sampel fluida.
- Porositas, saturasi air, dan ketebalan net pay berasal dari hasil
  interpretasi well log saya (Python, data terbuka Volve).
- Luas reservoir (A) dan Bo adalah asumsi, bukan data lapangan.

## Rumus
STOIIP (STB) = 7758 × A × h × φ × (1 − Sw) / Bo

## Asumsi
1. Reservoir homogen (satu nilai rata-rata per parameter, dengan sebaran).
2. Satu kontak fluida, satu zona.
3. Sumur vertikal: ketebalan dari log (MD) dianggap sama dengan
   ketebalan vertikal.
4. h net sudah memuat efek NTG, jadi NTG tidak dikalikan lagi.
5. Parameter Archie (a, m, n), Rw, dan densitas matriks pada interpretasi
   log adalah asumsi.
