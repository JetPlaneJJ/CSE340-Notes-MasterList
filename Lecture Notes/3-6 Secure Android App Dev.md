CSE340 Winter 2020
3/6/2020 Friday (Online) Zoom Lecture
Lecturer: Franziska Roesner, Associate CSE Professor --> CSE 484 Computer Security

# Lecture Topic: Secure Android Application Development

1. What can go wrong?
	- "Threat Model" --> explicitly malicious applications
	- Mobile Platform Security Features
		- Goal: limit harm devs of malicious apps can do!
		- Key Feature: Application isolation, modern memory protections, secure hardware, full disk encrypt, app store reviews
2. How are mobile platforms designed for security?
	- Applications are isolated from each other --> run in separate processes with separate UIDs
		- isolated from system --> no shared file system, no default access to devices
	- Prompted permissions --> access your location?
		- Android 6.0 prompts --> apps now have to prepare that user says NO to permissions
		- ask for as little permissions as possible
3. Best mobile app dev practices
	- Only ask for permissions you need, dont be "over-privileged"
	- use "internal storage" for sensitive data, not accessible to other apps
		- android has internal (ex: EncryptedFile) and external storage (ex: SD cards)
	- validate input from external sources, web, other apps (including users)
		- Length? Format?
		- SQL injections?
		- Be careful with WebViews
	- encrypt network comm.
		- use HTTPS protocol (user data won't be readable over network)
		- NOT HTTP!!!
	- don't hard code secrets in your data
		- ex: don't do this --> private static String SECRET_KEY = "passwordkey";
		- apk tools can DECOMPILE applications, go to human readable source code
		- instead, use Android Keystore
	- use existing cryptography libraries (carefully), unless you are pro cryptographer
	- b careful w/ inter-process communications
		- Android intents are sent between application components, need to think about validating legit input
		- should explicitly specify component name --> com.example.testApp.MainActivity
		- buggy apps might accidentally expose component->component messages publickly (eavesdropping)	
			- may act on unauthorized messages they receive
			- app w/out permission gains additional privileges through another app
	- careful about libraries you include (with old security flaws)
	




