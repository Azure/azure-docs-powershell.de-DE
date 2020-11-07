---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BF5526C1-11B9-47A8-A5A6-CB275B470A9E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: c079b65dc0a37ea07815e2e3b47799b9a194f4e2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843044"
---
# Get-AzStorageTableStoredAccessPolicy

## Synopsis
Ruft die gespeicherte Zugriffsrichtlinie oder Richtlinien für eine Azure-Speichertabelle ab.

## Syntax

```
Get-AzStorageTableStoredAccessPolicy [-Table] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzStorageTableStoredAccessPolicy** " listet die gespeicherte Zugriffsrichtlinie oder Richtlinien für eine Azure-Speichertabelle auf.

## Beispiele

### Beispiel 1: Abrufen einer gespeicherten Zugriffsrichtlinie in einer Speichertabelle
```
PS C:\>Get-AzStorageTableStoredAccessPolicy -Table "Table02" -Policy "Policy50"
```

Dieser Befehl ruft die Access-Richtlinie mit dem Namen Policy50 in der Speichertabelle mit dem Namen Table02 ab.

### Beispiel 2: Abrufen aller gespeicherten Zugriffsrichtlinien in einer Speichertabelle
```
PS C:\>Get-AzStorageTableStoredAccessPolicy -Table "Table02"
```

Dieser Befehl ruft alle Zugriffsrichtlinien in der Tabelle mit dem Namen Table02 ab.

## Parameter

### -Context
Gibt den Azure-Speicherkontext an.
Verwenden Sie das New-AzStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.

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
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### – Richtlinien
Gibt eine Richtlinie für den gespeicherten Zugriff an, die die Berechtigungen für dieses SAS-Token (Shared Access Signature) enthält.

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

### -Tabelle
Gibt den Namen der Azure-Speichertabelle an.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

### Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext

## Ausgaben

### Microsoft. WindowsAz. Storage. Table. SharedAccessTablePolicy

## Notizen

## Verwandte Links

[Neu – AzStorageTableStoredAccessPolicy](./New-AzStorageTableStoredAccessPolicy.md)

[Remove-AzStorageTableStoredAccessPolicy](./Remove-AzStorageTableStoredAccessPolicy.md)

[Satz-AzStorageTableStoredAccessPolicy](./Set-AzStorageTableStoredAccessPolicy.md)

[Neu – AzStorageContext](./New-AzStorageContext.md)


