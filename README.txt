CPP10 PROJECT: EVENT REGISTRATION SYSTEM
Student name: Jiya Dasadia
Enrollment number: IU2541230420
GitHub URL: https://github.com/jiyadasadiya/Event-Registration-System

OVERVIEW
A modular, menu-driven C++ application to manage events, participants, organizers, and registrations. It demonstrates classes, encapsulation, STL vectors, exceptions, validation, modular compilation, and file persistence.

REQUIREMENTS
- C++11 or later compiler (g++ recommended)
- Terminal/command prompt
- Keep the Source and Data folders in the same project directory.

BUILD
From the project root:
g++ -std=c++11 Source/main.cpp Source/Event.cpp Source/Participant.cpp Source/Organizer.cpp Source/Registration.cpp Source/FileManager.cpp Source/EventSystem.cpp -o Executable/Project

RUN
Linux/macOS:
./Executable/Project
Windows (MinGW):
g++ -std=c++11 Source\main.cpp Source\Event.cpp Source\Participant.cpp Source\Organizer.cpp Source\Registration.cpp Source\FileManager.cpp Source\EventSystem.cpp -o Executable\Project.exe
Executable\Project.exe

IMPORTANT PATH NOTE
The default data path is ../Data because the application is expected to run from the Executable folder. To run from the project root, change EventSystem app("../Data") in Source/main.cpp to EventSystem app("Data"), or run the executable from Executable as shown above. Data files use pipe-delimited text. Avoid using | in field values.

MENU
1 List events
2 Add event
3 Add participant
4 List participants
5 Add organizer
6 List organizers
7 Register participant for event
8 List registrations
9 Cancel registration
0 Save and exit

MAIN TRANSACTION
Registration validates that the participant and event exist, rejects duplicate participant-event registrations, checks event capacity, creates a registration, increments the registered-seat count, and persists the updated data. Cancellation removes the registration and releases one seat.

DATA FILES
events.txt: id|name|date|venue|capacity|registered
participants.txt: id|name|email
organizers.txt: id|name|department
registrations.txt: registrationId|participantId|eventId|timestamp

UML
PlantUML source files are in Diagrams. Render them with a PlantUML-compatible renderer for diagram images. Do not claim screenshots or generated diagram images are included unless you add/render them.

SUBMISSION CHECKLIST
[ ] Enter name and enrollment number in README and report.
[ ] Compile and test on the college system.
[ ] Capture genuine screenshots of the running program and place them in Screenshots.
[ ] Render the four .puml files to PNG/SVG and include if required.
[ ] Add the real GitHub URL after pushing the project.
[ ] Confirm the college-specific final submission form requirements.

WINDOWS QUICK START
Double-click RUN_ON_WINDOWS.bat from the project root after installing g++ and adding it to PATH. The program's main() function is in Source/main.cpp. Do not try to run the Linux Executable/Project binary as a Windows .exe.
