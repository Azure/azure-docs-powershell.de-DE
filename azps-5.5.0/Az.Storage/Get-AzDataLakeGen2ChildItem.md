---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azdatalakegen2childitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ChildItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ChildItem.md
ms.openlocfilehash: 9160eabf2492969ad7fa3916791854abd4ef6c44
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100155068"
---
# Get-AzDataLakeGen2ChildItem

## SYNOPSIS
Listet Unterverzeichnisse und Dateien aus einem Verzeichnis- oder Dateisystemstamm auf.

## SYNTAX

```
Get-AzDataLakeGen2ChildItem [-FileSystem] <String> [[-Path] <String>] [-FetchProperty] [-Recurse]
 [-MaxCount <Int32>] [-ContinuationToken <String>] [-AsJob] [-OutputUserPrincipalName]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Get-AzDataLakeGen2ChildItem"** listet Unterverzeichnisse und Dateien in einem Verzeichnis oder Filesystem in einem Azure-Speicherkonto auf.
Dieses Cmdlet funktioniert nur, wenn der hierarchische Namespace für das Konto "Storage" aktiviert ist. Diese Art von Konto kann durch Ausführen des Cmdlets "New-AzStorageAccount" mit "-EnableHierarchicalNamespace $true" erstellt werden.

## BEISPIELE

### Beispiel 1: Auflisten der direkten untergeordneten Elemente aus einem Filesystem
```
PS C:\>Get-AzDataLakeGen2ChildItem -FileSystem "filesystem1" 

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1                 True                         2020-03-13 13:07:34Z rwxr-x---    $superuser           $superuser          
dir2                 True                         2020-03-23 09:28:36Z rwxr-x---    $superuser           $superuser
```

Dieser Befehl listet die direkten untergeordneten Elemente aus einem Filesystem auf.

### Beispiel 2: Rekursiv aus einem Verzeichnis auflisten und Eigenschaften/ACL abrufen
```
PS C:\>Get-AzDataLakeGen2ChildItem -FileSystem "filesystem1" -Path "dir1/" -Recurse -FetchProperty

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir3            True                         2020-03-23 09:34:31Z rwx---rwx    $superuser           $superuser          
dir1/file1           False        1024            2020-03-23 09:29:18Z rwx---rwx    $superuser           $superuser           
dir1/testfile_1K_0   False        1024            2020-03-23 09:29:21Z rw-r-----    $superuser           $superuser
```

Dieser Befehl listet die direkten untergeordneten Elemente aus einem Filesystem auf.

### Beispiel 3: Rekursives Auflisten von Elementen aus einem Filesystem in mehreren Batches
```
PS C:\> $MaxReturn = 10000
PS C:\> $FileSystemName = "filesystem1"
PS C:\> $Total = 0
PS C:\> $Token = $Null
PS C:\> do
 {
     $items = Get-AzDataLakeGen2ChildItem -FileSystem $FileSystemName -Recurse -MaxCount $MaxReturn  -ContinuationToken $Token
     $Total += $items.Count
     if($items.Length -le 0) { Break;}
     $Token = $items[$items.Count -1].ContinuationToken;
 }
 While ($Token -ne $Null)
PS C:\> Echo "Total $Total items in Filesystem $FileSystemName"
```

In diesem Beispiel werden die *Parameter "MaxCount"* und *"ContinuationToken"* verwendet, um Elemente rekursiv aus einem Dateisystem in mehreren Batches auflisten.
Die ersten vier Befehle weisen Variablen Werte zu, die im Beispiel verwendet werden sollen.
Der fünfte Befehl gibt eine **Do-While-Anweisung** an, die das **Cmdlet "Get-AzDataLakeGen2ChildItem"** zum Auflisten von Elementen verwendet.
Die Anweisung enthält das fortsetzungstoken, das in der Variablen $Token ist.
$Token ändert den Wert, während die Schleife ausgeführt wird.
Im letzten Befehl wird der Befehl **"Echo"** zum Anzeigen der Summe verwendet.

## PARAMETERS

### -AsJob
Ausführen des Cmdlets im Hintergrund

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Context
Azure Storage Context Object

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ContinuationToken
Fortsetzungstoken.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FetchProperty
Rufen Sie die "datalake"-Elementeigenschaften und den ACL ab.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: FetchPermission

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FileSystem
FileSystem name

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -MaxCount
Die maximale Anzahl der BLOB-BloBs, die zurückgeben können.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OutputUserPrincipalName
Wenn Sie diesen Parameter vereinheitlichen, werden die in den Besitzer- und Gruppenfeldern jedes Listeneintrags zurückgegebenen Benutzeridentitätswerte aus Azure Active Directory-Objekt-IDs in Benutzerprinzipalnamen transformiert. Wenn dieser Parameter nicht angegeben wird, werden die Werte als Azure Active Directory-Objekt-IDs zurückgegeben. Beachten Sie, dass Gruppen- und Anwendungsobjekt-IDs nicht übersetzt werden, da sie keine eindeutigen Anzeigenamen haben.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: UserPrincipalName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
Der Pfad im angegebenen Dateisystem, der abgerufen werden soll.
Sollte ein Verzeichnis im Format 'directory1/directory2/' sein.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Recurse
Gibt an, ob das untergeordnete Element rekursiv erhalten wird.
Der Standardwert ist "false".

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### System.String

### Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext

## AUSGABEN

### Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN
