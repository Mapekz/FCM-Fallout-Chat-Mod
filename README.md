# Minerva layout screenshots

Code candidate: `6a812b58e120ea7c880967c1ea026641c23d30b1`.
Base: `d523f0f67e0f0f8188aadaf45c0a10616c0216f0`.

- `before.png`: original user-provided screenshot showing the reported layout.
- `after.png`: actual updated shared ChatOverlay on the /chat route in headless Chromium 153, 1000px viewport, 14px text, en-US / America/New_York.
- `after-narrow.png`: same candidate and fixture at a 320px viewport. Screenshot height expanded after layout assertions to show the full card.

After captures use local synthetic API/WebSocket responses and the original item examples, plus a long-name item and an item with an unknown price to exercise wrapping and fallback behavior. They are rendered UI captures, not mockups. The before image shows the game backdrop; the after captures use the dashboard backdrop.

The browser journey submits /minerva, checks complete descending-price inventory, alignment and overflow, and verifies keyboard source/share actions and share cooldown. Other captured states tested locally include 520px, 22px text at 320px, active Super Sale, and unavailable inventory.

Validation: 487 dashboard tests pass; both workspace typechecks and renderer builds pass; 1282 overlay tests pass and one unchanged portable-release case fails because pwsh is unavailable, reproduced on the base. Fresh independent code review has no open findings. Hosted CI is label-gated and is not claimed here.

## Screenshot SHA-256

- `before.png`: `18b9f822c15a7f28aa0d75c131c89c03e7e83df6d596f8feaf01e431e2610fb3`
- `after.png`: `901a670cadbe311cf1d192c44291aa70c5eeae4cc0d2e11f58f5253b0b801059`
- `after-narrow.png`: `33c8886dc6c1385d4dc244d9bd7102c2264af67f3c2c4523911abdc4535b68d1`
