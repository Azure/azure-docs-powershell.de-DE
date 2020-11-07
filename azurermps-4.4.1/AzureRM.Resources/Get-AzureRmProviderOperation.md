---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderOperation.md
ms.openlocfilehash: d4e58e1fc2da68d9293afa27072a4cf32023f661
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663540"
---
# Get-AzureRmProviderOperation

## Synopsis
Ruft die Vorgänge für einen Azure-Ressourcenanbieter ab, die mithilfe von Azure RBAC Sicherungs fähig sind.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Get-AzureRmProviderOperation [-OperationSearchString] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Beschreibung
Die Get-AzureRmProviderOperation ruft die von Azure-Ressourcen Anbietern verfügbar gemachten Vorgänge ab.
Vorgänge können zum Erstellen benutzerdefinierter Rollen in Azure RBAC zusammengestellt werden.
Der Befehl nimmt als Eingabe eine Vorgangs Suchzeichenfolge (mit möglichen Platzhalterzeichen (*)) an, die die anzuzeigenden Vorgangsdetails bestimmt.

Verwenden Sie Get-AzureRmProviderOperation *, um alle Vorgänge für alle Azure-Ressourcenanbieter abzurufen.

Verwenden Sie Get-AzureRmProviderOperation Microsoft. COMPUTE/*, um alle Vorgänge des Microsoft. Compute-Ressourcenanbieters zu erhalten.

## Beispiele

### --------------------------Alle Aktionen für alle Anbieter abrufen--------------------------
```
PS C:\> Get-AzureRmProviderOperation *
```

### --------------------------Abrufen von Aktionen für einen bestimmten Ressourcenanbieter--------------------------
```
PS C:\> Get-AzureRmProviderOperation Microsoft.Insights/*
```

### --------------------------Alle Aktionen abrufen, die auf virtuellen Computern ausgeführt werden können--------------------------
```
PS C:\> Get-AzureRmProviderOperation */virtualMachines/*
```

## Parameter

### -OperationSearchString
Die Suchzeichenfolge des Vorgangs (mit möglichen Platzhalterzeichen (*))

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Zeichenfolge
Der Parameter "OperationSearchString" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.

## Ausgaben

### Microsoft. Azure. Commands. resources. Models. PSResourceProviderOperation

## Notizen
Schlüsselwörter: Azure, azurerm, arm, Ressource, Verwaltung, Manager, Ressource, Gruppe, Vorlage, Bereitstellung

## Verwandte Links

