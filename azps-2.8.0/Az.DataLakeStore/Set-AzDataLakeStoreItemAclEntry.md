---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 0671D833-8B3A-4480-A576-92F1A9E8CE92
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 2c82c2c3f47a1dc0f0220faa8654a7281081c73b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651506"
---
# Set-AzDataLakeStoreItemAclEntry

## Synopsis
Ändert einen Eintrag in der ACL einer Datei oder eines Ordners im Data Lake Store.

## Syntax

### SetByACLObject (Standard)
```
Set-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetSpecificACE
```
Set-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance> [-AceType] <AceType>
 [[-Id] <Guid>] [-Permissions] <Permission> [-Default] [-PassThru] [-Recurse] [-Concurrency <Int32>]
 [-ShowProgress] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **festlegen-AzDataLakeStoreItemAclEntry** " ändert einen Eintrag (ACE) in der Zugriffssteuerungsliste (ACL) einer Datei oder eines Ordners im Data Lake Store.

## Beispiele

### Beispiel 1: Ändern von Berechtigungen für einen ACE
```
PS C:\>Set-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId -Permissions All
```

Mit diesem Befehl wird das Ass für Patti Fuller so geändert, dass alle Berechtigungen vorhanden sind.

### Beispiel 2: rekursives Ändern der Berechtigungen für ein Ass
```
PS C:\>Set-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId -Permissions All -Recurse -Concurrency 128
```

### Beispiel 3: Ändern der Berechtigungen für ein Ass rekursiv mithilfe des ACL-Objekts
```
PS C:\>$fullAcl="user:userid1:--x,default:user:userid1:--x"
PS C:\>$newFullAcl = $fullAcl.Split("{,}")
PS C:\>Set-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -Acl $newFullAcl -Recurse -Concurrency 128
```

Mit diesem Befehl wird der ACE für Patti Fuller rekursiv so geändert, dass alle Berechtigungen für root und alle zugehörigen Unterverzeichnisse und Dateien vorhanden sind.

## Parameter

### -Konto
Gibt den Namen des Data Lake Store-Kontos an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AceType
Gibt den Typ des zu ändernden ACE an.
Die zulässigen Werte für diesen Parameter lauten wie folgt:
- Benutzer 
- Gruppe 
- Format 
- Anderen

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType
Parameter Sets: SetSpecificACE
Aliases:
Accepted values: User, Group, Mask, Other

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ACL
Gibt das ACL-Objekt an, das die zu ändernden Einträge enthält.

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]
Parameter Sets: SetByACLObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Parallelität
Die Anzahl von Dateien/Verzeichnissen, die parallel verarbeitet werden. Optional: ein angemessener Standardwert wird ausgewählt.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### – Standard
Gibt an, dass dieser Vorgang den Standard-ACE aus der angegebenen ACL ändert.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetSpecificACE
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ID
Gibt die Objekt-ID des AzureActive-Verzeichnis Benutzers, der Gruppe oder des Dienst Prinzipals an, für den ein ACE geändert werden soll.

```yaml
Type: System.Guid
Parameter Sets: SetSpecificACE
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Gibt an, dass die resultierende ACL zurückgegeben werden soll.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Path
Gibt den Daten See-Speicherpfad des Elements an, für das ein ACE geändert werden soll, beginnend mit dem Stammverzeichnis (/).

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Berechtigungen
Gibt die Berechtigungen für das ACE an.
Die zulässigen Werte für diesen Parameter lauten wie folgt:
- Keine
- Ausführen
- Schreiben
- WriteExecute
- Lesen
- ReadExecute
- ReadWrite
- Alle

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Permission
Parameter Sets: SetSpecificACE
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Rekursiv
Gibt an, dass die ACL rekursiv auf die untergeordneten Unterverzeichnisse und Dateien geändert werden soll.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Progress
Wenn übergeben, wird der Status Status angezeigt. Gilt nur, wenn die rekursive ACL-Änderung durchgeführt wird.

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

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

### Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance

### Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreItemAce []

### Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreEnums + AceType

### System. GUID

### Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreEnums +-Berechtigung

### System. Management. Automation. Switchparameter

### System. Int32

## Ausgaben

### Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreItemAce

## Notizen

## Verwandte Links

[Remove-AzDataLakeStoreItemAclEntry](./Remove-AzDataLakeStoreItemAclEntry.md)


