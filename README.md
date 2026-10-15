# Decision Pac-Man

A student side project. It studies whether an oracle can post-train a small decision model like Jev. The oracle is a search that rolls the game engine 5 seconds forward for each option at a junction (`oracle-pellets-5s`). The oracle labels game states, and a small model is fine-tuned on those labels. The fine-tuned model then plays from the current state alone, with no lookahead.

## Run

Requirements: Node 20+, Ollama 0.35+.

```bash
npm install
npm run dev            # open http://localhost:5173/?model=<ollama model>
npm test
```

## Docs

- [docs/local-usage.md](docs/local-usage.md): play with hosted Jev, a local model, or the random players.
- [docs/plan_ceiling.md](docs/plan_ceiling.md): the research plan.
- [docs/guides/distill-oracle-gpu.md](docs/guides/distill-oracle-gpu.md): label, train, and evaluate on GPU servers.

## License

MIT. Pac-Man is a trademark of Bandai Namco. This project is not affiliated with it and uses no original art or audio.
