# Next-Level-Education

Next-Level-Education is a Facebook Messenger bot that matches people for peer-to-peer life coaching. A visitor chats with the bot, builds a short profile, shares how they want to be contacted, and is paired with another person who is looking for the same kind of support.

The bot keeps the conversation in Messenger, stores profiles and pairs, and can remind a pair about a weekly meeting and collect feedback afterward.

## Contact

**Next-Level-Education**

- Email: [hello@nextleveleducation.com](mailto:hello@nextleveleducation.com)
- Phone: [+1 (415) 555-0148](tel:+14155550148)
- Address: 120 Learning Street, Suite 300, San Francisco, CA 94105
- Hours: Monday to Saturday, 8:00 AM – 7:00 PM

**Alternative contact**

- Admissions desk: [+1 (415) 555-0192](tel:+14155550192)
- Email: [admissions@nextleveleducation.com](mailto:admissions@nextleveleducation.com)

The same details are shown in the bot when someone asks for help (`info`) and in the note that points people to coaching guidance. The admissions address is the alternative contact when the main desk is unavailable.

## What people can do in the bot

- Start a conversation and introduce themselves with a name and a short bio
- Add a phone number or a Skype name, and add or remove those contact details later
- Browse people who are available as peers and send or cancel a request
- Accept a request and see the other person’s contact details
- Set a weekly meeting day and time, turn reminders on or off, and send feedback after a meeting
- Stop searching, end a coaching pair, or reset the profile and start again

## Run it locally

Install Node.js, then from this folder:

```
npm install
npm run bot-client
```

Use a different session id to act as another person:

```
npm run bot-client -- --session=<ID>
```

You can also walk through saved conversations:

```
npm run visualize
```

See [doc/flow/README.md](doc/flow/README.md) for how those conversations are generated. The scripts in this repository were written for Node.js 6.1.0.

Copy `.env.example` to `.env` before a real Messenger deploy and fill in the Facebook tokens. Deployment steps are in [doc/deploy-instructions.md](doc/deploy-instructions.md).

## Documentation

- [Architecture](doc/architecture.md)
- [Deploy instructions](doc/deploy-instructions.md)
- [Testing instructions](doc/testing-instructions.md)
- [Chatbot framework API](doc/apidoc/README.md)
- [Definition of Done](doc/dod.md)

## Project layout

| Path | What it holds |
| --- | --- |
| `src/coaching-chatbot` | Dialog, actions, and the Finnish and English message text |
| `src/chatbot` | Session and chatbot service |
| `src/facebook-messenger` | Messenger webhook handler |
| `src/util` | Session, pair, and feedback storage |
| `test/ut` | Unit tests |
| `test/ft` | Feature tests that walk through conversations |
| `doc` | Architecture, deploy, testing, and API notes |

## Checks

```
npm test
npm run ft
npm run lint
```
