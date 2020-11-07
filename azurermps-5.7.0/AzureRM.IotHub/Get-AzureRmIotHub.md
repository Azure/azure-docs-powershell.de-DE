---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHub.md
ms.openlocfilehash: 80b629fe3d5ff5e028b73b22af95243849ecede7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662848"
---
# Get-AzureRmIotHub

## Synopsis
Ruft Informationen zu den IotHubs in einem Abonnement ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### ListIotHubsByResourceGroup (Standard)
```
Get-AzureRmIotHub [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetIotHubByName
```
Get-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Beschreibung
Ruft Informationen zu den IotHubs in einem Abonnement ab.
Sie können alle IotHub-Instanzen in einem Abonnement anzeigen oder Ihre Ergebnisse nach einer Ressourcengruppe oder einem bestimmten IotHub-Namen filtern.

## Beispiele

### Beispiel 1
```
PS C:\> Get-AzureRmIotHub
```

Ruft alle IotHubs des Abonnements ab.

### Beispiel 2
```
PS C:\> Get-AzureRmIotHub -ResourceGroupName "myresourcegroup"
```

Ruft alle IotHubs in dem Abonnement ab, die der ResourceGroup mit dem Namen "myresourcegroup" angehören.

### Beispiel 3
```
PS C:\> Get-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

Ruft Informationen über die IotHub mit dem Namen "myiothub" ab.

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Name des IotHub

```yaml
Type: String
Parameter Sets: GetIotHubByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Name der ResourceGroup

```yaml
Type: String
Parameter Sets: ListIotHubsByResourceGroup
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetIotHubByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

## Ausgaben

### Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub
System. Collections. Generic. List \` 1 \[ \[ Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub, Microsoft. Azure. Commands. IotHub, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null\]\]

## Notizen

## Verwandte Links

