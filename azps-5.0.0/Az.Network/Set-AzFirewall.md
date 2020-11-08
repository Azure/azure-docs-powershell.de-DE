---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40E56EC1-3327-4DFF-8262-E2EEBB5E4447
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
ms.openlocfilehash: 9ef4d8f2638fdb853fa83b896bb51f95d1ef119e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179826"
---
# Set-AzFirewall

## Synopsis
Speichert eine geänderte Firewall.

## Syntax

```
Set-AzFirewall -AzureFirewall <PSAzureFirewall> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Satz-AzFirewall** " aktualisiert eine Azure-Firewall.

## Beispiele

### 1: Aktualisieren der Priorität einer Firewall-Anwendungsregel Sammlung
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetApplicationRuleCollectionByName("ruleCollectionName")
$ruleCollection.Priority = 101
Set-AzFirewall -AzureFirewall $azFw
```

In diesem Beispiel wird die Priorität einer vorhandenen Regelsammlung einer Azure-Firewall aktualisiert.
Wenn die Azure Firewall "AzureFirewall" in der Ressourcengruppe "RG" eine Anwendungsregel Sammlung mit dem Namen "ruleCollectionName" enthält, werden die oben aufgeführten Befehle die Priorität dieser Regelsammlung ändern und anschließend die Azure-Firewall aktualisieren. Ohne den Befehl Set-AzFirewall werden alle Vorgänge, die für das lokale $azFw Objekt ausgeführt werden, nicht auf dem Server widergespiegelt.

### 2: Erstellen einer Azure Firewall und späteres Einrichten einer Anwendungsregel Sammlung
```
$azFw = New-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg" -VirtualNetworkName "vnet-name" -PublicIpName "pip-name"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$RuleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
$azFw.ApplicationRuleCollections = $RuleCollection

$azFw | Set-AzFirewall
```

In diesem Beispiel wird zunächst eine Firewall ohne Anwendungsregel Sammlungen erstellt. Anschließend werden eine Anwendungsregel und eine Anwendungsregel Sammlung erstellt, und das firewallobjekt wird im Arbeitsspeicher geändert, ohne dass sich dies auf die reale Konfiguration in der Cloud auswirkt. Damit Änderungen in der Cloud wiedergegeben werden, müssen Set-AzFirewall aufgerufen werden.

### 3: Aktualisieren des Bedrohungs-Intel-Betriebsmodus der Azure Firewall
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ThreatIntelMode = "Deny"
Set-AzFirewall -Firewall $azFw
```

In diesem Beispiel wird der Bedrohungs-Intel-Betriebsmodus der Azure Firewall "AzureFirewall" in der Ressourcengruppe "RG" aktualisiert.
Ohne den Befehl Set-AzFirewall werden alle Vorgänge, die für das lokale $azFw Objekt ausgeführt werden, nicht auf dem Server widergespiegelt.

### 4: Freigeben und Zuweisen der Firewall
```
$firewall=Get-AzFirewall -ResourceGroupName rgName -Name azFw
$firewall.Deallocate()
$firewall | Set-AzFirewall

$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress - ResourceGroupName rgName -Name publicIpName
$firewall.Allocate($vnet, $pip)
$firewall | Set-AzFirewall
```
In diesem Beispiel wird eine Firewall abgerufen, die Firewall dereserviert und gespeichert. Mit dem Befehl "freigeben" wird der ausgeführte Dienst entfernt, die Konfiguration der Firewall bleibt jedoch erhalten. Damit Änderungen in der Cloud wiedergegeben werden, müssen Set-AzFirewall aufgerufen werden.
Wenn der Benutzer den Dienst erneut starten möchte, sollte die Allocate-Methode für die Firewall aufgerufen werden.
Das neue VNet und die öffentliche IP-Adresse müssen sich in derselben Ressourcengruppe wie die Firewall befinden. Damit Änderungen in der Cloud wiedergegeben werden, müssen Set-AzFirewall aufgerufen werden.

### 5: Zuweisen mit einer öffentlichen Verwaltungs-IP-Adresse für erzwungene Tunneling-Szenarien
```
$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress - ResourceGroupName rgName -Name publicIpName
$mgmtPip = Get-AzPublicIpAddress - ResourceGroupName rgName -Name MgmtPublicIpName
$firewall.Allocate($vnet, $pip, $mgmtPip)
$firewall | Set-AzFirewall
```
In diesem Beispiel wird der Firewall eine öffentliche Verwaltungs-IP-Adresse und ein Subnetz für erzwungene Tunnel Szenarien zugewiesen. Der VNet muss ein Subnetz mit dem Namen "AzureFirewallManagementSubnet" enthalten.

### 6: Hinzufügen einer öffentlichen IP-Adresse zu einer Azure-Firewall
```
$pip = New-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.AddPublicIpAddress($pip)

$azFw | Set-AzFirewall
```

In diesem Beispiel wird die öffentliche IP-Adresse "azFwPublicIp1" an die Firewall angefügt.

### 7: Entfernen einer öffentlichen IP-Adresse aus einer Azure-Firewall
```
$pip = Get-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg"
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.RemovePublicIpAddress($pip)

$azFw | Set-AzFirewall
```

In diesem Beispiel wird die öffentliche IP-Adresse "azFwPublicIp1" als von der Firewall getrennt.

### 8: Ändern der öffentlichen Verwaltungs-IP-Adresse in einer Azure Firewall
```
$newMgmtPip = New-AzPublicIpAddress -Name "azFwMgmtPublicIp2" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ManagementIpConfiguration.PublicIpAddress = $newMgmtPip

$azFw | Set-AzFirewall
```

In diesem Beispiel wird die öffentliche Verwaltungs-IP-Adresse der Firewall in "AzFwMgmtPublicIp2" geändert.

### 9: Hinzufügen einer DNS-Konfiguration zu einer Azure-Firewall
```
$dnsServers = @("10.10.10.1", "20.20.20.2")
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.DNSEnableProxy = $true
$azFw.DNSServer = $dnsServers

$azFw | Set-AzFirewall
```

In diesem Beispiel ist die Konfiguration des DNS-Proxys und der DNS-Server an die Firewall angefügt.

### 10: Aktualisieren des Ziels einer vorhandenen Regel in einer Firewall-Anwendungsregel Sammlung
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetNetworkRuleCollectionByName("ruleCollectionName")
$rule=$ruleCollection.GetRuleByName("ruleName")
$rule.DestinationAddresses="10.10.10.10"
Set-AzFirewall -AzureFirewall $azFw
```

In diesem Beispiel wird das Ziel einer vorhandenen Regel innerhalb einer Regelsammlung einer Azure-Firewall aktualisiert. So können Sie Ihre Regeln automatisch aktualisieren, wenn IP-Adressen dynamisch geändert werden.

### 11: Zulassen von aktivem FTP auf Azure Firewall
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.AllowActiveFTP = $true

$azFw | Set-AzFirewall
```

In diesem Beispiel ist Active FTP für die Firewall zugelassen.

## Parameter

### -AsJob
Ausführen eines Cmdlets im Hintergrund

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AzureFirewall
Die AzureFirewall

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewall
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

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

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird. Das Cmdlet wird nicht ausgeführt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft. Azure. Commands. Network. Models. PSAzureFirewall

## Ausgaben

### Microsoft. Azure. Commands. Network. Models. PSAzureFirewall

## Notizen

## Verwandte Links

[Get-AzFirewall](./Get-AzFirewall.md)

[Neu – AzFirewall](./New-AzFirewall.md)

[Remove-AzFirewall](./Remove-AzFirewall.md)
