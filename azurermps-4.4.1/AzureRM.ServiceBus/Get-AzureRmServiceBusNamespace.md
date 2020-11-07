---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 2e6e044d888386b56d04ad48b7fbdaedadbd7497
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662400"
---
# Get-AzureRmServiceBusNamespace

## Synopsis
Ruft eine Beschreibung für den angegebenen ServiceBus-Namespace innerhalb der Ressourcengruppe ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Get-AzureRmServiceBusNamespace [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmServiceBusNamespace** " Ruft eine Beschreibung für den angegebenen ServiceBus-Namespace innerhalb der Ressourcengruppe ab.

## Beispiele

### Beispiel 1
```
PS C:\> Get-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

Gibt eine Beschreibung des angegebenen ServiceBus-Namespace zurück.

## Parameter

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

### -Name
Namespace Name.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Der Name der Ressourcengruppe

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### -ResourceGroup
System. String

### -Namespacename
 System. String

## Ausgaben

### System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. ServiceBus. Models. NamespaceAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.0.1.0, Culture = neutral, PublicKeyToken = null]]
Name: SB-Example1-ID:/Subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/default-ServiceBus-WestUS/Providers/Microsoft.ServiceBus/Namespaces/SB-example1 Ort: US-amerikanische SKU: Name: Standard, Kapazität: 1, Stufe: Standard ProvisioningState: erfolgreicher Status: Active CreatedAt: 1/20/2017 1:40:01 am UpdatedAt: 1/20/2017 1:40:24 am ServiceBusEndpoint: https://SB-Example1.servicebus.windows.net:443/ aktiviert: wahr

## Notizen
## Verwandte Links

## Verwandte Links

