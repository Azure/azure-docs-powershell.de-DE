---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azdatalakegen2itemaclobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemAclObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemAclObject.md
ms.openlocfilehash: 6396da138a0bafd54241f859c107601a1ce14b32
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935459"
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
Das **Cmdlet Set-AzDataLakeGen2ItemAclObject** erstellt/aktualisiert ein DataLake gen2-Element-ACL-Objekt, das in einem Update-AzDataLakeGen2Item verwendet werden kann.
Wenn der neue ACL-Eintrag mit demselben AccessControlType/EntityId/DefaultScope nicht in der Eingabe-ACL vorhanden ist, wird ein neuer ACL-Eintrag erstellt, sonst wird die Berechtigung des vorhandenen ACL-Eintrags aktualisiert.

## BEISPIELE

### Beispiel 1: Erstellen eines ACL-Objekts mit 3 ACL-Eintrag und Aktualisieren der ACL in einem Verzeichnis
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

Mit diesem Befehl wird ein ACL-Objekt mit drei ACL-Einträgen erstellt (verwenden Sie den Parameter -InputObject, um dem vorhandenen acl-Objekt einen acl-Eintrag hinzuzufügen), und aktualisiert die ACL in einem Verzeichnis.

### Beispiel 2: Erstellen eines ACL-Objekts mit vier ACL-Einträgen und Aktualisieren der Berechtigung eines vorhandenen ACL-Eintrags
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

Mit diesem Befehl wird zuerst ein ACL-Objekt mit vier ACL-Einträgen erstellt, und dann wird das Cmdlet erneut mit einer anderen Berechtigung, aber demselben AccessControlType/EntityId/DefaultScope eines vorhandenen ACL-Eintrags ausgeführt.
Anschließend wird die Berechtigung des ACL-Eintrags aktualisiert, aber kein neuer ACL-Eintrag hinzugefügt.

## PARAMETER

### -AccessControlType
Es gibt vier Typen: "Benutzer" gewährt dem Besitzer oder einem benannten Benutzer Rechte, "Gruppe" gewährt der besitzenden Gruppe oder einer benannten Gruppe Rechte, "mask" schränkt rechte ein, die benannten Benutzern und den Mitgliedern von Gruppen gewährt werden, und "andere" gewährt Allen Benutzern Rechte, die in keinem der anderen Einträge gefunden wurden.

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
Legen Sie diesen Parameter so ein, dass der #A0 zur Standard-ACL für ein Verzeichnis gehört. andernfalls ist der Bereich implizit, und der ACE gehört zur Zugriffs-ACL.

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
Es wird für Einträge von AccessControlType "mask" und "other" nicht angegeben.
Der Benutzer- oder Gruppenbezeichner wird auch für den Besitzer und die besitzende Gruppe nicht angegeben.

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
Wenn Sie das PSPathAccessControlEntry-Objekt eingeben, wird die neue ACL als neues Element des Eingabeobjekts \[ \] PSPathAccessControlEntry \[ \] hinzugefügt.

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
Das Berechtigungsfeld ist eine Drei-Zeichen-Sequenz, bei der das erste Zeichen "r" lautet, um Lesezugriff zu gewähren, das zweite Zeichen ist "w", um Schreibzugriff zu gewähren, und das dritte Zeichen ist "x", um die Ausführungsberechtigung zu erteilen.
Wenn der Zugriff nicht gewährt wird, wird das Zeichen "-" verwendet, um zu bezeichnen, dass die Berechtigung verweigert wird.

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
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Keine

## AUSGABEN

### Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSPathAccessControlEntry

## NOTIZEN

## VERWANDTE LINKS
