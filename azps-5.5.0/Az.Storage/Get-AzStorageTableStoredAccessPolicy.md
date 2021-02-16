---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BF5526C1-11B9-47A8-A5A6-CB275B470A9E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: b17a294392ca4336d4a96e5d136ad4e321eb45a7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158116"
---
# Get-AzStorageTableStoredAccessPolicy

## SYNOPSIS
Ruft die Richtlinie oder Richtlinien für den gespeicherten Zugriff für eine Azure -Speichertabelle ab.

## SYNTAX

```
Get-AzStorageTableStoredAccessPolicy [-Table] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Get-AzStorageTableStoredAccessPolicy"** listet die gespeicherten Zugriffsrichtlinien für eine Azure -Speichertabelle auf.

## BEISPIELE

### Beispiel 1: Erhalten einer gespeicherten Zugriffsrichtlinie in einer Speichertabelle
```
PS C:\>Get-AzStorageTableStoredAccessPolicy -Table "Table02" -Policy "Policy50"
```

Dieser Befehl ruft die Zugriffsrichtlinie mit dem Namen "Policy50" in der Speichertabelle namens "Table02" ab.

### Beispiel 2: Alle Richtlinien für den gespeicherten Zugriff in einer Speichertabelle erhalten
```
PS C:\>Get-AzStorageTableStoredAccessPolicy -Table "Table02"
```

Dieser Befehl ruft alle Zugriffsrichtlinien in der Tabelle mit dem Namen "Table02" ab.

## PARAMETERS

### -Context
Gibt den Azure -Speicherkontext an.
Verwenden Sie zum Abrufen eines Speicherkontexts das New-AzStorageContext Cmdlet.

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

### -Policy
Gibt eine Gespeicherte Zugriffsrichtlinie an, die die Berechtigungen für dieses Token für die Gemeinsam genutzte Zugriffssignatur (Shared Access Signature, SAS) enthält.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Table
Gibt den Namen der Azure -Speichertabelle an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### System.String

### Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext

## AUSGABEN

### Microsoft.WindowsAzure.Storage.Table.SharedAccessTablePolicy

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[New-AzStorageTableStoredAccessPolicy](./New-AzStorageTableStoredAccessPolicy.md)

[Remove-AzStorageTableStoredAccessPolicy](./Remove-AzStorageTableStoredAccessPolicy.md)

[Set-AzStorageTableStoredAccessPolicy](./Set-AzStorageTableStoredAccessPolicy.md)

[New-AzStorageContext](./New-AzStorageContext.md)


