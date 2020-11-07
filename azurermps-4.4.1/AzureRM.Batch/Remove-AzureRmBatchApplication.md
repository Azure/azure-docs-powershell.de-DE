---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 2CED21D6-4BEF-423B-A04A-5B812CEB975D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchApplication.md
ms.openlocfilehash: 357759b4e3107aaa48b363da18de74229979851a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663988"
---
# Remove-AzureRmBatchApplication

## Synopsis
Löscht eine Anwendung aus einem Stapelverarbeitungs Konto.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Remove-AzureRmBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Remove-AzureRmBatchApplication** löscht eine Anwendung aus einem Azure-Batch Konto.

## Beispiele

### Beispiel 1: Löschen einer Anwendung aus einem Stapelverarbeitungs Konto
```
PS C:\>Remove-AzureRmBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware"
```

Dieser Befehl löscht die Litware-Anwendung aus dem ContosoBatch-Konto.
Der Befehl schlägt fehl, wenn die Anwendung Pakete enthält.

## Parameter

### -Kontoname
Gibt den Namen des Batch Kontos an, aus dem dieses Cmdlet eine Anwendung entfernt.

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

### -ApplicationId
Gibt die ID der Anwendung an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, die das Stapelverarbeitungs Konto enthält.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
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

## Ausgaben

## Notizen

## Verwandte Links

[Get-AzureRmBatchApplication](./Get-AzureRmBatchApplication.md)

[Get-AzureRmBatchApplicationPackage](./Get-AzureRmBatchApplicationPackage.md)

[Neu – AzureRmBatchApplication](./New-AzureRmBatchApplication.md)

[Neu – AzureRmBatchApplicationPackage](./New-AzureRmBatchApplicationPackage.md)

[Remove-AzureRmBatchApplicationPackage](./Remove-AzureRmBatchApplicationPackage.md)

[Satz-AzureRmBatchApplication](./Set-AzureRmBatchApplication.md)


