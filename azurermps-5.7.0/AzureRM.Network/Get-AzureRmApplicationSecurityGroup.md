---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationSecurityGroup.md
ms.openlocfilehash: 5a1c519bd545ecb750f3842dac490eb31703e4d3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663225"
---
# Get-AzureRmApplicationSecurityGroup

## Synopsis
Ruft eine Anwendungs Sicherheitsgruppe ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Get-AzureRmApplicationSecurityGroup [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmApplicationSecurityGroup** " Ruft eine Anwendungs Sicherheitsgruppe ab.

## Beispiele

### Beispiel 1: Abrufen aller Anwendungs Sicherheitsgruppen
```
PS C:\> Get-AzureRmApplicationSecurityGroup
```

Der obige Befehl gibt alle Anwendungs Sicherheitsgruppen im Abonnement zurück.

### Beispiel 2: Abrufen von Anwendungs Sicherheitsgruppen in einer Ressourcengruppe.
```
PS C:\> Get-AzureRmApplicationSecurityGroup -ResourceGroupName MyResourceGroup
```

Der obige Befehl gibt alle Anwendungs Sicherheitsgruppen zurück, die zur Ressourcengruppe myresourcegroup gehören.

### Beispiel 3: Abrufen einer bestimmten Anwendungs Sicherheitsgruppe
```
PS C:\> Get-AzureRmApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name MyApplicationSecurityGroup
```

Der obige Befehl gibt die Anwendungs Sicherheitsgruppe MyApplicationSecurityGroup unter der Ressourcengruppe myresourcegroup zurück.

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

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
Der Ressourcenname.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Der Name der Ressourcengruppe.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

## Ausgaben

### Microsoft. Azure. Commands. Network. Models. PSApplicationSecurityGroup

## Notizen

## Verwandte Links

[Neu – AzureRmApplicationSecurityGroup](./New-AzureRmApplicationSecurityGroup.md)

[Remove-AzureRmApplicationSecurityGroup](./Remove-AzureRmApplicationSecurityGroup.md)

[Get-AzureRmNetworkSecurityRuleConfig](./Get-AzureRmNetworkSecurityRuleConfig.md)

[Get-AzureRmNetworkInterfaceIpConfig](./Get-AzureRmNetworkInterfaceIpConfig.md)
