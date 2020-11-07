---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubJob.md
ms.openlocfilehash: b0ea6f3cae3fe978a3d24b055eb47693ea466272
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663932"
---
# Get-AzureRmIotHubJob

## Synopsis
Ruft die Informationen zu einem IotHub-Auftrag ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Get-AzureRmIotHubJob [-ResourceGroupName] <String> [-Name] <String> [[-JobId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Ruft die Informationen zu einem IotHub-Auftrag ab.
Ein IotHub-Auftrag wird erstellt, wenn ein Import-oder Exportvorgang mithilfe der Befehle New-AzureRmIotHubExportDevices oder New-AzureRmIotHubImportDevices initialted wird.
Sie können entweder alle Aufträge auflisten oder die Aufträge nach der Auftrags-ID filtern.

## Beispiele

### Beispiel 1 Auflisten aller Aufträge
```
PS C:\> Get-AzureRmIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

Ruft alle Aufträge für das IotHub mit dem Namen "myiothub" ab.

### Beispiel 2 Abrufen eines bestimmten Auftrags
```
PS C:\> Get-AzureRmIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub" -JobId 3630fc31-4caa-43e8-a232-ea0577221cb2
```

Ruft Informationen über den Auftrag mit dem Bezeichner "3630fc31-4caa-43E8-a232-ea0577221cb2" für die IotHub mit dem Namen "myiothub" ab.

## Parameter

### -JobId
Die Auftrags-ID. 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Der Name des viel-Hubs. 

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

### -ResourceGroupName
Ressourcengruppen Name

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

### System. String

## Ausgaben

### Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubJobResponse
System. Collections. Generic. List \` 1 \[ \[ Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubJobResponse, Microsoft. Azure. Commands. IotHub, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null\]\]

## Notizen

## Verwandte Links

