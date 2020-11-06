---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: FB5E4ED2-8EF3-462F-A053-7EC82C767E8D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementVirtualNetwork.md
ms.openlocfilehash: 42213ddd4a7780b4d69b357c4b801df34aa9aca4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477445"
---
# New-AzureRmApiManagementVirtualNetwork

## Synopsis
Erstellt eine Instanz von PsApiManagementVirtualNetwork.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzureRmApiManagementVirtualNetwork** ist ein Hilfsbefehl zum Erstellen einer Instanz von **PsApiManagementVirtualNetwork**.
Dieser Befehl wird mit dem Cmdlet " **Satz-AzureRMApiManagementVirtualNetworks** " verwendet.

## Beispiele

### Beispiel 1: Erstellen eines virtuellen Netzwerks
```
PS C:\>$VirtualNetworks = @()
PS C:\> $VirtualNetworks += New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubtenName "ContosoNet" -VnetId "089D3F4D-B986-4DFD-9259-9112BA7A1F03"
PS C:\> Set-AzureRmApiManagementVirtualNetworks -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetworks $VirtualNetworks
```

In diesem Beispiel wird ein virtuelles Netzwerk erstellt und anschließend das Cmdlet " **setAzureRmApiManagementVirtualNetworks** " aufgerufen.

## Parameter

### -Standort
Gibt den Speicherort des virtuellen Netzwerks an, in dem dieses Cmdlet die Instanz erstellt.

Die zulässigen Werte für diesen Parameter lauten wie folgt:

- Nord-Zentral-USA
- Süd-Mittelamerika
- Zentral-US
- West Europa
- Nordeuropa
- West-US
- East US
- East US 2
- Japan (Ost)
- Japan West
- Brasilien Süd
- Südostasien
- Ostasien
- Australien (Ost)
- Australien südöstlich

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

### -SubnetResourceId
Gibt die Subnetz-Ressourcen-ID des virtuellen Netzwerks an.

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

### Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementVirtualNetwork

## Notizen

## Verwandte Links

