# Endpoint-security(Home Lab)

Created My own malware to understand windows OS, How it react to the malware?(Created only for educational purpose)

## Objective

Gained knowledge on windows OS, Antivirus, Windows registry.

### Skills Learned

- Analyzed Strength of the Windows antivirus
- Windows registry modifications
- Understand how malware makes network connections
- Malware behaviour

### Tools Used

- Virtual machine - Builted a Ubuntu VM
- Metaspoilt framework - Used this framework and created a malware
- Windows VM - Dowloaded the malware in windows to understand malware

## Steps
Dowloaded metaspolt framework for creation of malware( I didn't captured all screenshots ). I created malware in metaspolt with multi handler and exploited it with correct configurations.
<img width="1920" height="1080" alt="VirtualBox_SOClab-Ubuntu_17_12_2025_16_33_34" src="https://github.com/user-attachments/assets/f26c4304-c973-4d08-9d9e-1b1f6b8686f3" />


It is the actual malware payload executable that I created with msf venom
<img width="1920" height="1080" alt="VirtualBox_SOClab-Ubuntu_17_12_2025_16_31_24" src="https://github.com/user-attachments/assets/258216f9-e779-4bd9-98ce-53fbe1076789" />


Hosted malware in Python website to download it from windows 
<img width="1920" height="1080" alt="VirtualBox_SOClab-Ubuntu_17_12_2025_16_36_55" src="https://github.com/user-attachments/assets/0fd98f70-f116-4f02-9684-e76ee3f81e64" />


I have forgoted to take screenshots when dowloading malware in windows. I tried to dowload the malware in my windows VM. 
<img width="1920" height="1080" alt="VirtualBox_SOClab-Ubuntu_17_12_2025_17_11_41" src="https://github.com/user-attachments/assets/3308345a-1150-4271-8890-98804ac8c020" />


when dowloading malware in windows but It doesn't dowloaded yet at all because of antivirus. I manually disabled the antivirus from Real-time monitering but when dowloading the malware hosted on python website, It did not allowed the malware executable file to my system. May be it detected by Behaviour of the file or From malware signatures. 
Sometimes I forcedly dowloaded malware but even dowloaded file also been removed automatically by antivirus.
But in my Ubuntu machine mentioned as Malware died or crashed.
<img width="1920" height="1080" alt="VirtualBox_SOClab-Ubuntu_17_12_2025_17_13_07" src="https://github.com/user-attachments/assets/2a890c11-ccf4-40de-a774-7ccbfba320a1" />

1. I know if malware executed on my windows machine, that it will create a network connection to hacker, Un authorized access to external IP.
2. After that by gaining access the attacker can use LOLBINs like Powershell or Command prompt for their objectives.
3. We know that the malware creates a procees trees like Parent and Child processes > explorer.exe to malware.exe or explorer.exe to malware.exe and many sub child processes like powershell, commandprompt, vbscripts, w script.
4. With these connections the hacker can also change windows registry keys like H KEY LOCAL MACHINE(HKLM), H KEY CURRENT USER(HKCU)
5. if he changed registry keys, the malware execute again and again when system boots. 
