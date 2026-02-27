# Event Modeling for Non-Technical People — Companion Repository

Examples, templates, and an LLM prompt for building Event Models, accompanying the book [Event Modeling for Non-Technical People](https://leanpub.com/eventmodeling-for-non-technical-people).

**Available on Leanpub starting at $0.**

## Examples

All examples use the hotel booking domain from the book and are written in the [Event Model format](https://github.com/sparkle-space/event-modeler/blob/main/docs/event-model-format-spec.md) with [emlang](https://github.com/emlang-project/spec) slice definitions.

| File | Description | Book Chapter |
|------|-------------|--------------|
| [complete-slice.md](examples/hotel-booking/complete-slice.md) | Complete booking slice with automation — all 4 swimlanes in one slice | Ch. 2 |
| [full-model.md](examples/hotel-booking/full-model.md) | Full hotel booking model — 4 slices spanning the entire system | Ch. 3 |
| [booking-slice.md](examples/hotel-booking/booking-slice.md) | Booking slice — guest books a room | Ch. 3 |
| [search-slice.md](examples/hotel-booking/search-slice.md) | Search slice — view-only read model | Ch. 3 |
| [cancellation-slice.md](examples/hotel-booking/cancellation-slice.md) | Cancellation slice — guest cancels a booking | Ch. 3 |
| [automation-slice.md](examples/hotel-booking/automation-slice.md) | Automation slice — confirmation email triggered by booking | Ch. 3 |

## Templates

| File | Description |
|------|-------------|
| [event-model-template.md](templates/event-model-template.md) | Blank Event Model template — starting point for your own models |

## LLM Prompt

| File | Description |
|------|-------------|
| [build-event-model.md](prompts/build-event-model.md) | Comprehensive prompt for building Event Models with an LLM |

Use the prompt with or without the book as context. It produces a complete Event Model document in the standard format.

## Related

- [Event Modeler](https://github.com/sparkle-space/event-modeler) — Visual, collaborative event modeling for system design
  - [Product Spec](https://github.com/sparkle-space/event-modeler/blob/main/docs/product-spec.md)
  - [Event Model Format Spec](https://github.com/sparkle-space/event-modeler/blob/main/docs/event-model-format-spec.md)
- [sparkle.space](https://sparkle.space)

## License

MIT — see [LICENSE](LICENSE).
