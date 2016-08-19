# EnumarateFilePaths

This small project calculates and stores all the file paths of a logical drive on a Windows machine. It does so within seconds. For instance, C: drive with approximately 200K files takes around 10-15 seconds(this is approximate).

It scans the Master File Table(MFT) to get all the file information. The C# API is attributed to Dave A Gordon, and can be found at [MSDN](https://code.msdn.microsoft.com/windowsapps/CCS-LABS-C-Accessing-the-d317805c).

The author there has suggested the GetFilePath method which uses some P-Invoke to find the path. I found that very slow.
This project does a reverse path calculation starting with a file and recursively finding the parent folder.

I have used a .NET Dictionary, with it's TryGetValue method. I haven't studied LINQ in detail yet, so someone may try using it instead, and quantify the results.


