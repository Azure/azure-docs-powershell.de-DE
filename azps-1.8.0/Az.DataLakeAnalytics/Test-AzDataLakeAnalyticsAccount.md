---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0B52890D-102F-4C3C-9EF9-017F6ECA3E26
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/test-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: 77247853fe6412b0d01fb01c71e592efca12063d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93820231"
---
# Test-AzDataLakeAnalyticsAccount

## Synopsis
Überprüft, ob ein Data Lake Analytics-Konto vorhanden ist.

## Syntax

```
Test-AzDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Test-AzDataLakeAnalyticsAccount** überprüft, ob ein Data Lake Analytics-Konto vorhanden ist.

## Beispiele

### Beispiel 1: testen, ob ein Konto vorhanden ist
```
PS C:\>Test-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

Dieser Befehl testet, ob das Konto mit dem Namen ContosoAdlAccount vorhanden ist.

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

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

### -Name
Gibt den Namen des Daten Lake Analytics-Kontos an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Ressourcengruppennamen des Data Lake Analytics-Kontos an.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

## Ausgaben

### System. Boolean

## Notizen

## Verwandte Links

[Get-AzDataLakeAnalyticsAccount](./Get-AzDataLakeAnalyticsAccount.md)

[Neu – AzDataLakeAnalyticsAccount](./New-AzDataLakeAnalyticsAccount.md)

[Satz-AzDataLakeAnalyticsAccount](./Set-AzDataLakeAnalyticsAccount.md)


