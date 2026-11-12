# MockMirror for Fiber

A mock Fiber Network node you can run in one command, so you can build and test payment UIs on Fiber without running two real nodes and opening channels first.

Status: proposal stage. This repo is for my Spark Program application on Nervos Talk. Nothing is built yet, code lands here week by week if it gets funded.

## Plan

- JSON-RPC server that answers the Fiber methods a payment app calls: new_invoice, parse_invoice, get_invoice, send_payment, get_payment, list_channels, open_channel, node_info
- Small state store so invoices get paid and channel balances change
- Scenarios: success, no route, channel balance too low, payment stuck pending, node unreachable
- Recorder that captures real Fiber testnet node responses, plus a test that compares mock and real output
- npm package (`npx mockmirror-fiber`), hosted mock endpoint, GitHub Action for CI, example checkout app

Built on MockMirror, my instant API mocking tool: https://mockmirror.vercel.app

## Author

Abdulahad Irfan Dayatar - https://github.com/abdulahaddayater - https://abdulahaddayatar.com

## License

MIT
