# Bench Drift Checker

A browser-based controller tester for repair benches. Plug in a gamepad, press any button, and run four tests on each stick to document drift before and after a repair.

**Live page:** `https://<your-username>.github.io/bench-drift-checker/`

## Tests

| Test | What it checks | Good | Watch | Problem |
|---|---|---|---|---|
| 1 · Rest drift | Stick offset with hands off for 3 seconds | ≤ 0.05 | ≤ 0.10 | > 0.10 |
| 2 · Reach | How far the stick travels up, down, left, right | ≥ 95% | ≥ 85% | < 85% |
| 3 · Circle accuracy | Roundness of the outer edge when rolled | ≤ 10% error | ≤ 15% | > 15% |
| 4 · Return to center | Time to settle after letting go from the edge | ≤ 150 ms | ≤ 400 ms | > 400 ms or never |

It also shows live trigger travel and button presses.

## Repair workflow

1. Connect the controller to the bench PC and press any button.
2. Fill in customer, ticket #, and controller model.
3. Run all four tests, then click **Save as "Before repair."**
4. Do the repair and run the tests again.
5. Screenshot the **Customer results card** to send to the customer.
6. Click **Copy notes** and paste the before/after results into the ticket.

## Requirements

- Chrome or Edge on desktop (uses the [Gamepad API](https://developer.mozilla.org/en-US/docs/Web/API/Gamepad_API)).
- Works with Xbox, PlayStation, Switch Pro, and most XInput/DirectInput controllers over USB or Bluetooth.
- Until a real controller is detected, the page shows a demo controller with upward drift on the left stick.
- Everything runs locally in the browser. No data is uploaded or stored.

## Deploying to GitHub Pages

1. Create a new public repo named `bench-drift-checker`.
2. Upload `index.html`, `README.md`, `.nojekyll`, and `LICENSE` to the repo root.
3. Go to **Settings → Pages**, set **Source** to *Deploy from a branch*, choose `main` and `/ (root)`, and save.
4. The page goes live at `https://<your-username>.github.io/bench-drift-checker/` within a minute or two.

## License

MIT. See [LICENSE](LICENSE).

---

Built by TSTSI Endeavors.
