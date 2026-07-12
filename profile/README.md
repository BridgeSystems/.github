# Bridge Systems BV

We make **Bridgemate** — table-top scoring devices and software for bridge clubs and tournaments
worldwide. This organization hosts the open resources for scoring program developers who want
their software to talk to **Bridgemate Control Software (BCS 5)** through the **Bridgemate Data
Connector**.

## Writing a scoring program client — start here

Your scoring program exchanges JSON messages with the local Data Connector service over http
(or named pipes on the same machine, .NET only): initialize an event, send players and results,
poll the queues for what the Bridgemates produce. Pick your language:

| Language | Repository | Package |
| --- | --- | --- |
| C# / .NET (reference) | [Bridgemate-Data-Connector-Scoring-Program-Client](https://github.com/BridgeSystems/Bridgemate-Data-Connector-Scoring-Program-Client) | NuGet [`BridgeSystems.Bridgemate.DataConnector.ScoringProgramClient`](https://www.nuget.org/packages/BridgeSystems.Bridgemate.DataConnector.ScoringProgramClient) |
| PHP | [Bridgemate-Data-Connector-Scoring-Program-Client-PHP](https://github.com/BridgeSystems/Bridgemate-Data-Connector-Scoring-Program-Client-PHP) | Composer [`bridgemate/dataconnector-client`](https://packagist.org/packages/bridgemate/dataconnector-client) |
| Java | [Bridgemate-Data-Connector-Scoring-Program-Client-Java](https://github.com/BridgeSystems/Bridgemate-Data-Connector-Scoring-Program-Client-Java) | Maven `nl.bridgemate:bridgemate-dataconnector-client` |
| Python | [Bridgemate-Data-Connector-Scoring-Program-Client-Python](https://github.com/BridgeSystems/Bridgemate-Data-Connector-Scoring-Program-Client-Python) | PyPI [`bridgemate-dataconnector-client`](https://pypi.org/project/bridgemate-dataconnector-client/) |

All four clients speak an identical wire format: the PHP, Java and Python layers are generated
from the C# source and verified against golden fixtures. Every repository ships a
**getting-started console sample** that runs the whole workflow against a live Data Connector and
prints each request and response — the fastest way to learn the protocol.

## Resources

- 📖 [Developer's guide](https://github.com/BridgeSystems/Bridgemate-Data-Connector-Scoring-Program-Client/blob/master/Documentation/MD/index.md) — the protocol, the procedures, all data types
- 📚 [API reference](https://bridgesystems.github.io/Bridgemate-Data-Connector-Scoring-Program-Client/html/b11ca58b-c149-48f8-af9a-cf6a2c7bfe53.htm) — context-sensitive help for the .NET client
- 🖥️ [Scoring Program Emulator](https://github.com/BridgeSystems/Bridgemate-Data-Connector-Scoring-Program-Client/releases) — ready-to-run WPF app to exercise the Data Connector (attached to every release)
- 💬 [Questions & answers](https://github.com/BridgeSystems/Bridgemate-Data-Connector-Scoring-Program-Client/discussions) — one Discussions board for all languages
- 🌐 [bridgemate.com](https://www.bridgemate.com) — the products themselves
