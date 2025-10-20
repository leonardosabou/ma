1. Project Idea <br />
This project is a mobile application for managing basketball teams, players, transfers, and training sessions. Coaches and managers can easily organize their teams, track player details, record transfers, and schedule training sessions. The app is simple to use and supports both online and offline functionality — allowing users to make changes anytime. Once an internet connection is available, all local updates are synced automatically with the server to keep information consistent. <br />
<br />
2. Domain Details <br />
Entities <br />
Team <br />
•	TeamID – unique identifier for each team. <br />
•	Name – name of the basketball team (required). <br />
•	City – city where the team is based. <br /> 
•	CoachName – name of the team’s coach. <br />
•	Budget – total financial budget of the team. <br />
Player <br />
•	PlayerID – unique identifier for each player. <br />
•	Name – player’s full name (required). <br />
•	Age – player’s age. <br />
•	Height – player’s height. <br />
•	Weight – player’s weight. <br />
•	Salary – player’s salary. <br />
•	Position – player’s role (Guard, Forward, Center). <br />
•	TeamID – foreign key linking the player to their team. <br />
Transfer <br />
•	TransferID – unique identifier for each transfer. <br />
•	PlayerID – player being transferred. <br />
•	FromTeamID – current team of the player. <br />
•	ToTeamID – destination team. <br />
•	TransferDate – date of the transfer. <br />
•	Fee – transfer fee. <br />
Training <br />
•	TrainingID – unique identifier for each training session. <br />
•	TeamID – team associated with the session. <br />
•	Date – scheduled date and time. <br />
•	Type – training focus (e.g., Shooting, Defense, Conditioning). <br />
•	Duration – duration of the session. <br />

3. CRUD Operations <br />
•	Create – Add a new team, player, training, or transfer. <br />
•	Read – View all existing teams, players, ongoing transfers, and scheduled trainings. <br />
•	Update – Edit teams (e.g., players, budget), player information (e.g., height, weight, salary), transfer details (e.g., fee, date), or trainings (e.g., type, team, schedule). <br />
•	Delete – Delete a team, player, training, or transfer. <br />

4. Persistence Details <br />
Local Database (on device): <br />
•	Create – Store new teams, players, transfers, and trainings locally. <br />
•	Read – Display cached data even when offline. <br />
•	Update – Save offline edits and apply them once reconnected. <br />
•	Delete – Mark deleted items locally for removal when synced. <br />
Server (cloud database): <br />
•	Create – Upload new data to the cloud once online. <br />
•	Read – Fetch the latest version of all data from the server. <br />
•	Update – Sync all modified records with the cloud database. <br />
•	Delete – Permanently remove deleted data from the server. <br />

5. Offline Scenarios <br />
•	Create (offline): Add a new player, team, transfer, or training → saved locally → synced when connected. <br />
•	Read (offline): View all previously stored information about teams, players, and trainings. <br />
•	Update (offline): Edit details (e.g., player stats, training info) → stored locally → updated on the server later. <br />
•	Delete (offline): Deletion actions are recorded locally and applied to the server after reconnection. <br />

6. App Mockup (see Project Idea folder)
