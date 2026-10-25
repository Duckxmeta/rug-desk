# RUG DESK

Solana memecoin desk — paper first.

**Code kills. Grok reads X. You sign.**

This is a direct implementation of the setup from @0xboan.

## Quick start (paper mode)

1. Put your xAI API key in `.env`:
   ```
   XAI_API_KEY=your_key_here
   ```
2. `pip install requests`
3. Check a token:
   ```
   python check.py <CONTRACT_ADDRESS>
   ```
4. Watch open paper positions:
   ```
   python watch.py
   ```
5. Evening report:
   ```
   python report.py
   ```

`PAPER = True` in `config.py` means fake fills at real prices. Flip only after you read the logs.

## Files

- `config.py` — every number lives here
- `book.py` — positions, trades, limits
- `rugcheck.py` — 9 hard contract kills
- `market.py` — pool depth / age / sells
- `grok.py` + `prompts.py` — the only paid step (X search)
- `check.py` — one CA in, one verdict out
- `watch.py` — exits every 10 min
- `scan.py` — optional DexScreener fresh token feed
- `report.py` — daily summary

Never edit `config.py` without writing why in the same day.
