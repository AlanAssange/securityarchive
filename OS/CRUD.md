# CRUD

Cuando trabajmos con archivos en un sistema o aplicación, debemos entender como performar operacaiones CRUD (Create, Read, Update, Delete).

## Creación de archivos

Windows: podemos crear archivos utilizando la powershell con el comando New-Item seguido del file path. Ejemplo:

```bash
New-Item -Path "C:\Example\example.txt" -ItemType "file"
```

Linux: podemos crear archivos utilizando una terminal de cualquier distribución de linux utilizando el siguiente comando:

```bash
touch /example/example.txt
```

File Reading
Windows: You can read a file using standard file readers, such as Notepad, Wordpad, etc., or you can utilize PowerShell commands. The Get-Content command provides the file content.

Get-Content -Path "C:\Example\example.txt"
Linux: The cat command is the most common way to read the contents of a file in Linux.

cat /example/example.txt
File Updating
Windows: File updating can be accomplished using the previously mentioned text editors or PowerShell. The Set-Content or Add-Content commands are useful for updating a file.

Set-Content -Path "C:\Example\example.txt" -Value "Updated content"
Add-Content -Path "C:\Example\example.txt" -Value "Appended content"
Linux: Linux uses the built-in text editors, such as nano or vim, to update files. Alternatively, the echo command can append content to a file.

echo "Appended content" >> /example/example.txt
File Deletion
Windows: File deletion is performed by right-clicking the file and selecting ‘Delete’ or using PowerShell commands. The Remove-Item command followed by the file path can delete a file.

Remove-Item -Path "C:\Example\example.txt"
Linux: The rm command allows you to delete a file in Linux.

rm /example/example.txt
By mastering these CRUD operations, you can enhance your cyber security knowledge and implement effective incident response and file management strategies.