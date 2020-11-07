---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 91D58F60-F22A-454A-B04C-E5AEF33E9D06
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmFirewall.md
ms.openlocfilehash: cdaa9689919d2e307434d888b435dad9d29e105e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664825"
---
# Get-AzureRmFirewall

## Synopsis
Ruft eine Azure-Firewall ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Get-AzureRmFirewall [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmFirewall** " ruft mindestens eine Firewall in einer Ressourcengruppe ab.

## Beispiele

### 1: Abrufen aller Firewalls in einer Ressourcengruppe
```
Get-AzureRmFirewall -ResourceGroupName rgName
```

In diesem Beispiel werden alle Firewalls in der Ressourcengruppe "rgName" abgerufen.

### 2: Abrufen einer Firewall nach Namen
```
Get-AzureRmFirewall -ResourceGroupName rgName -Name azFw
```

In diesem Beispiel wird die Firewall mit dem Namen "azFw" in der Ressourcengruppe "rgName" abgerufen.

### 3: Abrufen einer Firewall und anschließendes Hinzufügen einer Anwendungsregel Sammlung zur Firewall
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$appRule = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$appRuleCollection = New-AzureRmFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $appRule -ActionType "Allow"
$azFw.AddApplicationRuleCollection($appRuleCollection)
```

In diesem Beispiel wird eine Firewall abgerufen und dann der Firewall eine Anwendungsregel Sammlung hinzugefügt, indem die AddApplicationRuleCollection-Methode aufgerufen wird.

### 4: Abrufen einer Firewall und anschließendes Hinzufügen einer Netzwerkregel Sammlung zur Firewall
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$netRule = New-AzureRmFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol "Udp" -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$netRuleCollection = New-AzureRmFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $netRule -ActionType "Allow"
$azFw.AddNetworkRuleCollection($netRuleCollection)
```

In diesem Beispiel wird eine Firewall abgerufen und dann der Firewall eine Netzwerkregel Sammlung hinzugefügt, indem die AddNetworkRuleCollection-Methode aufgerufen wird.

### 5: Abrufen einer Firewall und anschließendes Abrufen einer APP-Regelsammlung nach Namen aus der Firewall
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$getAppRc=$azFw.GetApplicationRuleCollectionByName("MyAppRuleCollection")
```

In diesem Beispiel wird eine Firewall abgerufen, und dann wird eine Regelsammlung nach Name aufgerufen, die für das GetApplicationRuleCollectionByName-Objekt aufgerufen wird. Der Name der Regelsammlung für Methoden-GetApplicationRuleCollectionByName ist keine Unterscheidung nach Groß-/Kleinschreibung.

### 6: Abrufen einer Firewall und Abrufen einer Netzwerkregel Sammlung nach Namen aus der Firewall
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$getNetRc=$azFw.GetNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

In diesem Beispiel wird eine Firewall abgerufen, und dann wird eine Regelsammlung nach Name aufgerufen, die für das GetNetworkRuleCollectionByName-Objekt aufgerufen wird. Der Name der Regelsammlung für Methoden-GetNetworkRuleCollectionByName ist keine Unterscheidung nach Groß-/Kleinschreibung.

### 7: Rufen Sie eine Firewall ab, und entfernen Sie dann eine Anwendung Regelsammlung nach Namen aus der Firewall.
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveApplicationRuleCollectionByName("MyAppRuleCollection")
```

In diesem Beispiel wird eine Firewall abgerufen, und anschließend wird eine Regelsammlung nach Name aufgerufen, wobei die RemoveApplicationRuleCollectionByName-Methode für das Firewall-Objekt aufgerufen wird. Der Name der Regelsammlung für Methoden-RemoveApplicationRuleCollectionByName ist keine Unterscheidung nach Groß-/Kleinschreibung.

### 8: Abrufen einer Firewall und Entfernen einer Netzwerkregel Sammlung nach Namen aus der Firewall
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

In diesem Beispiel wird eine Firewall abgerufen, und anschließend wird eine Regelsammlung nach Name aufgerufen, wobei die RemoveNetworkRuleCollectionByName-Methode für das Firewall-Objekt aufgerufen wird. Der Name der Regelsammlung für Methoden-RemoveNetworkRuleCollectionByName ist keine Unterscheidung nach Groß-/Kleinschreibung.

### 9: Abrufen einer Firewall und Zuweisen der Firewall
```
$vnet=Get-AzureRmVirtualNetwork -Name "vnet" -ResourceGroupName "rgName"
$publicIp=Get-AzureRmPublicIpAddress -Name "firewallpip" -ResourceGroupName "rgName"
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.Allocate($vnet, $publicIp)
```

In diesem Beispiel wird eine Firewall abgerufen und die Zuweisung für die Firewall aufgerufen, um den Firewalldienst mithilfe der Konfiguration (Anwendung und Netzwerkregel Sammlungen) zu starten, die der Firewall zugeordnet ist.

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
Gibt den Namen der Firewall an, die dieses Cmdlet erhält.

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
Gibt den Namen der Ressourcengruppe an, zu der die Firewall gehört.

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

### Keine
Dieses Cmdlet akzeptiert keine Eingaben.

## Ausgaben

### Microsoft. Azure. Commands. Network. Models. PSAzureFirewall

## Notizen

## Verwandte Links

[Neu – AzureRmFirewall](./New-AzureRmFirewall.md)

[Remove-AzureRmFirewall](./Remove-AzureRmFirewall.md)

[Satz-AzureRmFirewall](./Set-AzureRmFirewall.md)
