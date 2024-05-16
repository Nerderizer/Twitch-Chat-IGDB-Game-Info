# Get Current Game Info Extension

## Author
UserID10T

## Version
1.0

## Description
This Streamer.bot extension retrieves the current game information for a Twitch broadcaster using the IGDB (Internet Game Database) API. The information includes the game name, developer name, release date, summary, genres, and websites. The extension uses global variables to determine which pieces of information to include in the output. These global variables are set in the Streamer.bot interface before the extension is executed.

## How to Use
1. Update the Set argument Sub-actions under the CUSTOMIZE GAME DETAILS group in the Streamer.bot interface. The arguments are 'addGameName', 'addDeveloperName', 'addReleaseDate', 'addSummary', 'addGenres', and 'addWebsites'. Set them to '1' to include the corresponding game detail in the output, or '0' to exclude it.
2. Configure preferred trigger(s) under the 'Get Current Game Info' action.
3.  Triggering the action will retrieve the current game information and send the preferred game details to the Twitch chat.

## Methods
- `Execute`: This is the main method that is called when the action is executed. It retrieves the broadcaster information, game name, and calls the IGDB API to get the game details. It then calls the `SendGameDetails` method to send the game details to the Twitch chat.
- `UnixTimeStampToDateTime`: This method converts a Unix timestamp to a date string.
- `SendGameDetails`: This method prepares the game details for output and sends them to the Twitch chat. It checks each global variable and appends the corresponding game detail to the output if the global variable is '1'.
- `AppendDetail`: This method appends a game detail to the output string. If the output string becomes too long, it sends the current output string to the Twitch chat and starts a new output string.

## Dependencies
This extension is designed to be used with Streamer.bot and requires the Streamer.bot libraries to run.

## Support
For support, please reach out to UserID10T.
