---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D818C404-60E4-42DB-AADF-063305D9541B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerinboundnatruleconfig
schema: 2.0.0
ms.openlocfilehash: 2af05b60498fc83b74c00701794dba7f1b59e6a6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850635"
---
# Remove-AzureRmLoadBalancerInboundNatRuleConfig

## Synopsis
Entfernt eine eingehende NAT-Regelkonfiguration von einem Lastenausgleichsmodul.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Remove-AzureRmLoadBalancerInboundNatRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Remove-AzureRmLoadBalancerInboundNatRuleConfig** entfernt eine eingehende NAT-Regelkonfiguration (Network Address Translation) aus einem Azure Load Balancer.

## Beispiele

### 1: Löschen einer eingehenden NAT-Regel aus einem Azure Load Balancer
```
$loadbalancer = Get-AzureRmLoadBalancer -Name mylb -ResourceGroupName myrg

 Remove-AzureRmLoadBalancerInboundNatRuleConfig -Name "myinboundnatrule" -LoadBalancer $loadbalancer
```

Der erste Befehl lädt ein bereits vorhandenes Lastenausgleichsmodul mit dem Namen "mylb" und speichert es in der Variablen $Load Balancer. Der zweite Befehl entfernt die eingehende NAT-Regel, die diesem Lastenausgleichsmodul zugeordnet ist.

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

### -LoadBalancer
Gibt das **LoadBalancer** -Objekt an, das die von diesem Cmdlet entfernte eingehende NAT-Regelkonfiguration enthält.

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Gibt den Namen der eingehenden NAT-Regelkonfiguration an, die vom Cmdlet entfernt wird.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### PSLoadBalancer
Der Parameter "LoadBalancer" akzeptiert den Wert vom Typ "PSLoadBalancer" aus der Pipeline.

## Ausgaben

### Microsoft. Azure. Commands. Network. Models. PSLoadBalancer

## Notizen

## Verwandte Links

[Add-AzureRmLoadBalancerInboundNatRuleConfig](./Add-AzureRmLoadBalancerInboundNatRuleConfig.md)

[Get-AzureRmLoadBalancerInboundNatRuleConfig](./Get-AzureRmLoadBalancerInboundNatRuleConfig.md)

[Neu – AzureRmLoadBalancerInboundNatRuleConfig](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[Satz-AzureRmLoadBalancerInboundNatRuleConfig](./Set-AzureRmLoadBalancerInboundNatRuleConfig.md)


