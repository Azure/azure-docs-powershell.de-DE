---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azdatalakegen2itemaclobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemACLObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemACLObject.md
ms.openlocfilehash: d16a476bea988afb53ddff7b34a83658e0f274e1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995929"
---
# Set-AzDataLakeGen2ItemAclObject

## Synopsis
Erstellt/aktualisiert ein datalake-Gen2-Element-ACL-Objekt, das in Update-AzDataLakeGen2Item-Cmdlet verwendet werden kann.

## Syntax

```
Set-AzDataLakeGen2ItemAclObject [-EntityId <String>] [-DefaultScope] -Permission <String>
 [-InputObject <PSPathAccessControlEntry[]>] -AccessControlType <AccessControlType> [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Satz-AzDataLakeGen2ItemAclObject** " erstellt/aktualisiert ein datalake Gen2-Element-ACL-Objekt, das in Update-AzDataLakeGen2Item-Cmdlet verwendet werden kann.
Wenn der neue ACL-Eintrag mit dem gleichen AccessControlType/Entity-DefaultScope nicht in der Eingabe-ACL vorhanden ist, wird ein neuer ACL-Eintrag erstellt, ansonsten Update-Berechtigung für vorhandenen ACL-Eintrag.

## Beispiele

### Beispiel 1: Erstellen eines ACL-Objekts mit 3 ACL-Eintrag und Update-ACL für ein Verzeichnis
```
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -Permission rwx -DefaultScope
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType group -Permission rw- -InputObject $acl 
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType other -Permission "rw-" -InputObject $acl
PS C:\>Update-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/dir3" -ACL $acl

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir3            True                         2020-03-23 09:34:31Z rwxrw-rw-+   $superuser           $superuser
```

Dieser Befehl erstellt ein ACL-Objekt mit 3 ACL-Einträgen (Use-Inputobject-Parameter zum Hinzufügen von ACL-Einträgen zu einem vorhandenen ACL-Objekt) und aktualisiert die ACL für ein Verzeichnis.

### Beispiel 2: Erstellen eines ACL-Objekts mit 4 ACL-Einträgen und Aktualisieren der Berechtigung eines vorhandenen ACL-Eintrags
```
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -Permission rwx -DefaultScope
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType group -Permission rw- -InputObject $acl 
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType other -Permission "rw-" -InputObject $acl
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -EntityId $id -Permission rwx -InputObject $acl 
PS C:\>$acl

DefaultScope AccessControlType EntityId                             Permissions
------------ ----------------- --------                             -----------
True         User                                                   rwx        
False        Group                                                  rw-        
False        Other                                                  rw-        
False        User              ********-****-****-****-************ rwx        

PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -EntityId $id -Permission r-x -InputObject $acl 
PS C:\>$acl  

DefaultScope AccessControlType EntityId                             Permissions
------------ ----------------- --------                             -----------
True         User                                                   rwx        
False        Group                                                  rw-        
False        Other                                                  rw-        
False        User              ********-****-****-****-************ r-x
```

Dieser Befehl erstellt zunächst ein ACL-Objekt mit 4 ACL-Einträgen und führt dann das Cmdlet erneut mit unterschiedlicher Berechtigung, aber demselben AccessControlType/Entitäts-DefaultScope eines vorhandenen ACL-Eintrags aus.
Dann wird die Berechtigung des ACL-Eintrags aktualisiert, aber es wird kein neuer ACL-Eintrag hinzugefügt.

## Parameter

### -AccessControlType
Es gibt vier Arten: "Benutzer" gewährt dem Besitzer oder einem benannten Benutzerrechte, "Gruppe" gewährt Rechte für die besitzende Gruppe oder eine benannte Gruppe, "Maske" schränkt die Rechte ein, die für benannte Benutzer und die Mitglieder von Gruppen gewährt werden, und "Other" gewährt Rechte an alle Benutzer, die in keinem der anderen Einträge gefunden wurden.

```yaml
Type: Azure.Storage.Files.DataLake.Models.AccessControlType
Parameter Sets: (All)
Aliases:
Accepted values: User, Group, Mask, Other

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultScope
Legen Sie diesen Parameter fest, um anzugeben, dass der ACE zur Standard-ACL für ein Verzeichnis gehört; Andernfalls ist Scope implizit und der ACE gehört zur Access-ACL.

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

### -Entitäts-Nr
Der Bezeichner des Benutzers oder der Gruppe.
Sie wird bei Einträgen von AccessControlType "Maske" und "Other" ausgelassen.
Der Benutzer-oder Gruppenbezeichner wird auch für den Besitzer und die besitzende Gruppe ausgelassen.

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

### -Inputobject
Wenn das PSPathAccessControlEntry \[ \] -Objekt eingegeben wird, wird die neue ACL als neues Element des Eingabe PSPathAccessControlEntry-Objekts hinzugefügt \[ \] .

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSPathAccessControlEntry[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Berechtigung
Das Feld "Berechtigung" ist eine 3-Zeichen-Sequenz, in der das erste Zeichen "r" ist, um Lesezugriff zu gewähren, das zweite Zeichen "w", um Schreibzugriff zu gewähren, und das dritte Zeichen "x", um die EXECUTE-Berechtigung zu erteilen.
Wenn Access nicht gewährt wird, wird das Zeichen "-" verwendet, um zu kennzeichnen, dass die Berechtigung verweigert wurde.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine

## Ausgaben

### Microsoft. WindowsAzure. Commands. Storage. Model. ResourceModel. PSPathAccessControlEntry

## Notizen

## Verwandte Links
