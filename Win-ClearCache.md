```Shell
del c:\Windows\Temp /S /Q
del "%UserProfile%\AppData\Local\Temp" /S /Q

del "%UserProfile%\AppData\Local\Microsoft\VisualStudio\12.0\Designer\ShadowCache" /S /Q
del "%UserProfile%\AppData\Local\Microsoft\VisualStudio\14.0\Designer\ShadowCache" /S /Q

del "%UserProfile%\AppData\Local\Google\Chrome\User Data\Default\Cache\" /S /Q
del c:\inetpub\logs\LogFiles\W3SVC1\ /S /Q

rmdir c:\MSOCache\ /s /q
rmdir c:\Users\svc_deploy\ /s /q


FOR /D %%p IN ("%UserProfile%\AppData\Local\Temp\*.*") DO rmdir "%%p" /s /q

FOR /D %%p IN ("c:\Portal\External\TestResults\*.*") DO rmdir "%%p" /s /q
FOR /D %%p IN ("c:\Portal\External\OS33.Windows\TestResults\*.*") DO rmdir "%%p" /s /q
FOR /D %%p IN ("c:\Portal\Staging\TestResults\*.*") DO rmdir "%%p" /s /q
FOR /D %%p IN ("c:\Portal\Staging\OS33.Windows\TestResults\*.*") DO rmdir "%%p" /s /q
FOR /D %%p IN ("c:\Portal\OS33.Api-Staging\TestResults\*.*") DO rmdir "%%p" /s /q
FOR /D %%p IN ("c:\Portal\OS33.Api-Production\TestResults\*.*") DO rmdir "%%p" /s /q
FOR /D %%p IN ("c:\Portal\OS33.Api\TestResults\*.*") DO rmdir "%%p" /s /q
rem pause

#! cleanup image!
dism.exe /online /cleanup-image  /StartComponentCleanup
```
