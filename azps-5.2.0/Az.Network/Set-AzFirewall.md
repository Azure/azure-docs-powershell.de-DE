---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40E56EC1-3327-4DFF-8262-E2EEBB5E4447
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
ms.openlocfilehash: 9ef4d8f2638fdb853fa83b896bb51f95d1ef119e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98291430"
---
# Set-AzFirewall

## SYNOPSIS
Speichert eine geänderte Firewall.

## SYNTAX

```
Set-AzFirewall -AzureFirewall <PSAzureFirewall> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet Set-AzFirewall** aktualisiert eine Azure-Firewall.

## BEISPIELE

### 1: Updatepriorität einer Regelsammlung für eine Firewallanwendung
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetApplicationRuleCollectionByName("ruleCollectionName")
$ruleCollection.Priority = 101
Set-AzFirewall -AzureFirewall $azFw
```

In diesem Beispiel wird die Priorität einer vorhandenen Regelsammlung einer Azure Firewall aktualisiert.
Wenn die Azure Firewall "AzureFirewall" in der Ressourcengruppe "rg" eine Anwendungsregelauflistung namens "ruleCollectionName" enthält, ändern die obigen Befehle die Priorität dieser Regelsammlung und aktualisieren anschließend die Azure-Firewall. Ohne den Set-AzFirewall werden alle vorgänge, die für das lokale $azFw ausgeführt werden, nicht auf dem Server angezeigt.

### 2: Erstellen einer Azure-Firewall und Späteres Festlegen einer Anwendungsregelsammlung
```
$azFw = New-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg" -VirtualNetworkName "vnet-name" -PublicIpName "pip-name"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$RuleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
$azFw.ApplicationRuleCollections = $RuleCollection

$azFw | Set-AzFirewall
```

In diesem Beispiel wird zuerst eine Firewall ohne Anwendungsregelsammlungen erstellt. Anschließend werden eine Anwendungsregel- und Anwendungsregelsammlung erstellt. Anschließend wird das Firewallobjekt im Arbeitsspeicher geändert, ohne dass sich dies auf die tatsächliche Konfiguration in der Cloud ausdingt. Damit Änderungen in der Cloud widererspiegelt werden, Set-AzFirewall sie aufgerufen werden.

### 3: Aktualisieren des Threat -Intel-Betriebsmodus der Azure Firewall
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ThreatIntelMode = "Deny"
Set-AzFirewall -Firewall $azFw
```

In diesem Beispiel wird der Threat -Intel-Betriebsmodus der Azure Firewall "AzureFirewall" in der Ressourcengruppe "rg" aktualisiert.
Ohne den Set-AzFirewall werden alle vorgänge, die für das lokale $azFw-Objekt ausgeführt werden, nicht auf dem Server angezeigt.

### 4: Zuweisen und Zuweisen der Firewall
```
$firewall=Get-AzFirewall -ResourceGroupName rgName -Name azFw
$firewall.Deallocate()
$firewall | Set-AzFirewall

$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress - ResourceGroupName rgName -Name publicIpName
$firewall.Allocate($vnet, $pip)
$firewall | Set-AzFirewall
```
In diesem Beispiel wird eine Firewall abgerufen, die Firewall neu zugewiesen und von ihr speichert. Der Befehl "Deallocate" entfernt den ausgeführten Dienst, behält jedoch die Konfiguration der Firewall bei. Damit Änderungen in der Cloud widererspiegelt werden, Set-AzFirewall sie aufgerufen werden.
Wenn der Benutzer den Dienst erneut starten möchte, sollte die "Allocate"-Methode in der Firewall aufgerufen werden.
Der neue VNet und die öffentliche IP müssen sich in derselben Ressourcengruppe wie die Firewall befinden. Auch hier müssen Änderungen aufgerufen werden, damit sie in Set-AzFirewall werden.

### 5: Zuweisen einer öffentlichen Verwaltungs-IP-Adresse für Szenarien mit erzwungenen Tunneln
```
$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress - ResourceGroupName rgName -Name publicIpName
$mgmtPip = Get-AzPublicIpAddress - ResourceGroupName rgName -Name MgmtPublicIpName
$firewall.Allocate($vnet, $pip, $mgmtPip)
$firewall | Set-AzFirewall
```
In diesem Beispiel wird der Firewall eine öffentliche Verwaltungs-IP-Adresse und ein Subnetz für Szenarien mit erzwungenen Tunneln zugewiesen. Das VNet muss ein Subnetz namens "AzureFirewallManagementSubnet" enthalten.

### 6: Hinzufügen einer öffentlichen IP-Adresse zu einer Azure Firewall
```
$pip = New-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.AddPublicIpAddress($pip)

$azFw | Set-AzFirewall
```

In diesem Beispiel ist die öffentliche IP-Adresse "azFwPublicIp1" an die Firewall angefügt.

### 7: Entfernen einer öffentlichen IP-Adresse aus einer Azure Firewall
```
$pip = Get-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg"
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.RemovePublicIpAddress($pip)

$azFw | Set-AzFirewall
```

In diesem Beispiel wird die öffentliche IP-Adresse "azFwPublicIp1" getrennt von der Firewall verwendet.

### 8: Ändern der öffentlichen VERWALTUNGS-IP-Adresse für eine Azure-Firewall
```
$newMgmtPip = New-AzPublicIpAddress -Name "azFwMgmtPublicIp2" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ManagementIpConfiguration.PublicIpAddress = $newMgmtPip

$azFw | Set-AzFirewall
```

In diesem Beispiel wird die öffentliche Verwaltungs-IP-Adresse der Firewall in "AzFwMgmtPublicIp2" geändert.

### 9: Hinzufügen einer DNS-Konfiguration zu einer Azure Firewall
```
$dnsServers = @("10.10.10.1", "20.20.20.2")
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.DNSEnableProxy = $true
$azFw.DNSServer = $dnsServers

$azFw | Set-AzFirewall
```

In diesem Beispiel ist die Konfiguration des DNS-Proxys und des DNS-Servers an die Firewall angefügt.

### 10: Aktualisieren des Ziels einer vorhandenen Regel in einer Firewallanwendungsregelsammlung
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetNetworkRuleCollectionByName("ruleCollectionName")
$rule=$ruleCollection.GetRuleByName("ruleName")
$rule.DestinationAddresses="10.10.10.10"
Set-AzFirewall -AzureFirewall $azFw
```

In diesem Beispiel wird das Ziel einer vorhandenen Regel in einer Regelsammlung einer Azure Firewall aktualisiert. Auf diese Weise können Sie Ihre Regeln automatisch aktualisieren, wenn sich die IP-Adressen dynamisch ändern.

### 11: Active FTP für die Firewall von Azure zulassen
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.AllowActiveFTP = $true

$azFw | Set-AzFirewall
```

In diesem Beispiel ist Active FTP für die Firewall zulässig.

## PARAMETERS

### -AsJob
Ausführen des Cmdlets im Hintergrund

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
The AzureFirewall

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
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

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

### -Confirm
Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.

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

### -Waswenn
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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Microsoft.Azure.Commands.Network.Models.PSAzureFirewall

## AUSGABEN

### Microsoft.Azure.Commands.Network.Models.PSAzureFirewall

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Get-AzFirewall](./Get-AzFirewall.md)

[New-AzFirewall](./New-AzFirewall.md)

[Remove-AzFirewall](./Remove-AzFirewall.md)
