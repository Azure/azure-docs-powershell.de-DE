---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azdatalakegen2itemaclobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemAclObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemAclObject.md
ms.openlocfilehash: 209cb5ded738faabfdafc113d3d9524f7c01e927
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100175041"
---
# Set-AzDataLakeGen2ItemAclObject

## SYNOPSIS
Erstellt/aktualisiert ein DataLake gen2-Element-ACL-Objekt, das in einem Update-AzDataLakeGen2Item verwendet werden kann.

## SYNTAX

```
Set-AzDataLakeGen2ItemAclObject [-EntityId <String>] [-DefaultScope] -Permission <String>
 [-InputObject <PSPathAccessControlEntry[]>] -AccessControlType <AccessControlType> [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Set-AzDataLakeGen2ItemAclObject"** erstellt/aktualisiert ein DataLake gen2-Element-ACL-Objekt, das in einem Update-AzDataLakeGen2Item verwendet werden kann.
Wenn der neue Eintrag "ACL" mit demselben AccessControlType/EntityId/DefaultScope nicht in der Eingabe-ACL vorhanden ist, wird ein neuer "ACL"-Eintrag erstellt. Andern falls die Berechtigung eines vorhandenen ACL-Eintrags aktualisiert wird.

## BEISPIELE

### Beispiel 1: Erstellen eines ACL-Objekts mit 3 ACL-Eintrag und Aktualisieren der ACL für ein Verzeichnis
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

Dieser Befehl erstellt ein ACL-Objekt mit drei ACL-Einträgen (verwenden Sie den Parameter "-InputObject" zum Hinzufügen eines acl-Eintrags zu einem vorhandenen acl-Objekt), und aktualisiert die ACL für ein Verzeichnis.

### Beispiel 2: Erstellen eines ACL-Objekts mit vier ACL-Einträgen und Aktualisieren der Berechtigung eines vorhandenen Eintrags für den Zugriffssteuerungseintrag (ACL)
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

Dieser Befehl erstellt zuerst ein ACL-Objekt mit vier ACL-Einträgen. Führen Sie dann das Cmdlet erneut mit einer anderen Berechtigung aus, aber mit demselben AccessControlType/EntityId/DefaultScope eines vorhandenen ACL-Eintrags.
Anschließend wird die Berechtigung für den Eintrag "ACL" aktualisiert, aber es wird kein neuer Eintrag für die Zugriffssteuerungsberechtigung hinzugefügt.

## PARAMETERS

### -AccessControlType
Es gibt vier Typen: "Benutzer" gewährt dem Besitzer oder einem benannten Benutzer Rechte, "Gruppe" gewährt Rechte für die besitzende Gruppe oder eine benannte Gruppe, "mask" schränkt rechte ein, die benannten Benutzern und Mitgliedern von Gruppen gewährt werden, und "andere" gewährt Rechte für alle Benutzer, die in keinem der anderen Einträge gefunden werden.

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
Legen Sie diesen Parameter so ein, dass der ACE zu der #A0 für ein Verzeichnis gehört. andernfalls ist der Bereich implizit, und der ACE gehört zur Zugriffs-ACL.

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

### -EntityId
Der Benutzer- oder Gruppenbezeichner.
Für Einträge von AccessControlType"mask" und "other" wird es weggelassen.
Der Benutzer- oder Gruppenbezeichner wird auch für den Besitzer und die besitzende Gruppe ausgelassen.

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

### -InputObject
Wenn Sie das "PSPathAccessControlEntry"-Objekt eingeben, wird die neue ACL als neues Element des Eingabeobjekts \[ \] "PSPathAccessControlEntry" \[ \] hinzugefügt.

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

### -Permission
Das Berechtigungsfeld ist eine aus drei Zeichen abfolge, bei der das erste Zeichen "r" ist, um Lesezugriff zu gewähren, das zweite Zeichen "w", um Schreibzugriff zu gewähren, und das dritte Zeichen "x" zum Erteilen der Ausführungsberechtigung.
Wenn der Zugriff nicht gewährt wird, wird mit dem "-"-Zeichen darauf hindementiert, dass die Berechtigung verweigert wird.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Keine

## AUSGABEN

### Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSPathAccessControlEntry

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN
