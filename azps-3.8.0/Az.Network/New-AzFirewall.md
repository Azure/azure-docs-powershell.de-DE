---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A3D60CF1-2E66-4EE5-9C68-932DD8DF80BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
ms.openlocfilehash: 3b4014b56a36228fe53221430ffe79a43118f8fe
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845008"
---
# New-AzFirewall

## Synopsis
Erstellt eine neue Firewall in einer Ressourcengruppe.

## Syntax

### Standard (Standard)
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String>
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-Zone <String[]>] [-Sku <String>] [-VirtualHubId <String>] [-FirewallPolicyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### OldIpConfigurationParameterValues
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetworkName <String>
 -PublicIpName <String> [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-Zone <String[]>] [-Sku <String>] [-VirtualHubId <String>] [-FirewallPolicyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### IpConfigurationParameterValues
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetwork <PSVirtualNetwork>
 -PublicIpAddress <PSPublicIpAddress[]> [-ManagementPublicIpAddress <PSPublicIpAddress>]
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-Zone <String[]>] [-Sku <String>] [-VirtualHubId <String>] [-FirewallPolicyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzFirewall** erstellt eine Azure-Firewall.

## Beispiele

### 1: Erstellen einer Firewall, die mit einem virtuellen Netzwerk verbunden ist
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip
```

In diesem Beispiel wird eine Firewall erstellt, die mit dem virtuellen Netzwerk "vnet" in derselben Ressourcengruppe wie die Firewall verbunden ist.
Da keine Regeln angegeben wurden, blockiert die Firewall den gesamten Datenverkehr (Standardverhalten).
Threat Intel wird auch im Standardmodus-Alert ausgeführt – was bedeutet, dass böswilliger Datenverkehr protokolliert, aber nicht verweigert wird.

### 2: Erstellen einer Firewall, die den gesamten HTTPS-Datenverkehr zulässt
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "https:443" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection
```

In diesem Beispiel wird eine Firewall erstellt, die den gesamten HTTPS-Datenverkehr auf Port 443 ermöglicht.
Threat Intel wird im Standardmodus-Alert ausgeführt – was bedeutet, dass böswilliger Datenverkehr protokolliert, aber nicht verweigert wird.

### 3: DNAT-Umleiten von Datenverkehr bestimmt zu 10.1.2.3:80 zu 10.2.3.4:8080
```
$rule = New-AzFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.2.3.4" -TranslatedPort "8080"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "NatRuleCollection" -Priority 1000 -Rule $rule
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -NatRuleCollection $ruleCollection -ThreatIntelMode Off
```

In diesem Beispiel wurde eine Firewall erstellt, die die Ziel-IP-Adresse und den Port aller Pakete übersetzte, die zu 10.1.2.3:80 zu 10.2.3.4:8080 Threat Intel in diesem Beispiel deaktiviert ist.

### 4: Erstellen einer Firewall ohne Regeln und mit Threat Intel im Warnungsmodus
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ThreatIntelMode Alert
```

In diesem Beispiel wird eine Firewall erstellt, die den gesamten Datenverkehr (Standardverhalten) blockiert und im Warnungsmodus eine Bedrohung für Intel ausführt.
Dies bedeutet, dass Warnungsprotokolle für böswilligen Datenverkehr ausgegeben werden, bevor die anderen Regeln angewendet werden (in diesem Fall nur die Standardregel – alle verweigern).

### 5: Erstellen einer Firewall, die den gesamten HTTP-Datenverkehr auf Port 8080 zulässt, blockiert aber bösartige Domänen, die von Threat Intel identifiziert werden
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:8080" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

In diesem Beispiel wird eine Firewall erstellt, die den gesamten HTTP-Datenverkehr auf Port 8080 zulässt, es sei denn, Sie wird von Intel als bösartig eingestuft.
Bei der Ausführung im Modus "verweigern", im Gegensatz zu "Warnung", wird der Datenverkehr, der als böswillige Bedrohung angesehen wird, nicht nur protokolliert, sondern auch blockiert.

### 6: Erstellen einer Firewall ohne Regeln und mit Verfügbarkeits Zonen
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetworkName $vnet.Name -PublicIpName $pip.Name -Zone 1,2,3
```

In diesem Beispiel wird eine Firewall mit allen verfügbaren Verfügbarkeits Zonen erstellt.

### 7: Erstellen einer Firewall mit zwei oder mehr öffentlichen IP-Adressen
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -Name "vnet" -ResourceGroupName $rgName
$pip1 = New-AzPublicIpAddress -Name "AzFwPublicIp1" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$pip2 = New-AzPublicIpAddress -Name "AzFwPublicIp2" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress @($pip1, $pip2)
```

In diesem Beispiel wird eine Firewall erstellt, die mit dem virtuellen Netzwerk "vnet" mit zwei öffentlichen IP-Adressen verbunden ist.

### 8: Erstellen einer Firewall, die MSSQL-Datenverkehr zu einer bestimmten SQL-Datenbank ermöglicht
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "mssql:1433" -TargetFqdn "sql1.database.windows.net"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

In diesem Beispiel wird eine Firewall erstellt, die den MSSQL-Datenverkehr auf dem Standard Port 1433 in die SQL-Datenbank SQL1.Database.Windows.net.

### 9: Erstellen einer Firewall, die mit einem virtuellen Hub verbunden ist
```
$rgName = "resourceGroupName"
$fp = Get-AzFirewallPolicy -ResourceGroupName $rgName -Name "fp"
$fpId = $fp.Id
$vHub = Get-AzVirtualHub -Name "hub"
$vHubId = $vHub.Id

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -Sku AZFW_Hub -VirtualHubId $vHubId -FirewallPolicyId -$fpId
```

In diesem Beispiel wird eine Firewall erstellt, die mit dem virtuellen Hub "vHub" verbunden ist. Eine Firewall-Richtlinien $FP wird an die Firewall angefügt. Diese Firewall erlaubt/verweigert den Datenverkehr basierend auf den Regeln, die in der Firewall-Richtlinie $FP erwähnt werden. Der virtuelle Hub und die Firewall sollten sich in denselben Regionen befinden.

### 10: Erstellen einer Firewall mit der Einrichtung von Threat Intelligence-Whitelists
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$tiWhitelist = New-AzFirewallThreatIntelWhitelist -FQDN @("www.microsoft.com") -IpAddresses @("8.8.8.8")
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ThreatIntelWhitelist $tiWhitelist
```

In diesem Beispiel wird eine Firewall erstellt, die "www.Microsoft.com" und "8.8.8.8" aus "Threat Intelligence" Whitelist

### 11: Erstellen einer Firewall mit angepasster privater Bereichs Einrichtung
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -PrivateRange @("99.99.99.0/24", "66.66.0.0/16")
```

In diesem Beispiel wird eine Firewall erstellt, die "99.99.99.0/24" und "66.66.0.0/16" als private IP-Bereiche behandelt und Datenverkehr nicht an diese Adressen SNAT.

### 12: Erstellen einer Firewall mit einem Verwaltungs-Subnetz und einer öffentlichen IP-Adresse
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
$mgmtPip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "managementPublicIpName"

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ManagementPublicIpAddress $mgmtPip
```

In diesem Beispiel wird eine Firewall erstellt, die mit dem virtuellen Netzwerk "vnet" in derselben Ressourcengruppe wie die Firewall verbunden ist.
Da keine Regeln angegeben wurden, blockiert die Firewall den gesamten Datenverkehr (Standardverhalten).
Threat Intel wird auch im Standardmodus-Alert ausgeführt – was bedeutet, dass böswilliger Datenverkehr protokolliert, aber nicht verweigert wird.

Zur Unterstützung von Szenarien mit erzwungenem Tunneling verwendet diese Firewall das Subnetz "AzureFirewallManagementSubnet" und die öffentliche Verwaltungs-IP-Adresse für den Verwaltungsdatenverkehr.

### 13: Erstellen einer Firewall mit einer mit einem virtuellen Netzwerk verbundenen Firewall-Richtlinie
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
$fp = Get-AzFirewallPolicy -ResourceGroupName $rgName -Name "fp"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -FirewallPolicyId $fp
```

In diesem Beispiel wird eine Firewall erstellt, die mit dem virtuellen Netzwerk "vnet" in derselben Ressourcengruppe wie die Firewall verbunden ist.
Die Regeln und Bedrohungsinformationen, die auf die Firewall angewendet werden, werden aus der Firewall-Richtlinie übernommen.

## Parameter

### -ApplicationRuleCollection
Gibt die Sammlungen von Anwendungsregeln für die neue Firewall an.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -FirewallPolicyId
Die Firewall-Richtlinie, die an die Firewall angefügt ist

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.

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

### -Standort
Gibt den Bereich für die Firewall an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ManagementPublicIpAddress
Eine oder mehrere öffentliche IP-Adressen, die für den Verwaltungsdatenverkehr verwendet werden sollen. Die öffentlichen IP-Adressen müssen die Standard-SKU verwenden und der gleichen Ressourcengruppe wie die Firewall angehören.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Gibt den Namen der Azure-Firewall an, die von diesem Cmdlet erstellt wird.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NatRuleCollection
Die Liste der AzureFirewallNatRuleCollections

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NetworkRuleCollection
Die Liste der AzureFirewallNetworkRuleCollections

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PrivateRange
Die privaten IP-Bereiche, in denen der Datenverkehr nicht SNAT'ed werden soll

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicIpAddress
Eine oder mehrere öffentliche IP-Adressen. Die öffentlichen IP-Adressen müssen die Standard-SKU verwenden und der gleichen Ressourcengruppe wie die Firewall angehören.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress[]
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicIpName
Öffentlicher IP-Name. Die öffentliche IP-Adresse muss die Standard-SKU verwenden und der gleichen Ressourcengruppe wie die Firewall angehören.

```yaml
Type: System.String
Parameter Sets: OldIpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen einer Ressourcengruppe an, die die Firewall enthalten soll.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SKU
Der SKU-Typ für Firewall

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AZFW_Hub, AZFW_VNet

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Schlüssel-Wert-Paare in Form einer Hashtabelle Zum Beispiel:

@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ThreatIntelMode
Gibt den Vorgangsmodus für Threat Intelligence an. Der Standardmodus ist "Alert", nicht "aus".

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Alert, Deny, Off

Required: False
Position: Named
Default value: Alert
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ThreatIntelWhitelist
Die Whitelist für Threat Intelligence

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallThreatIntelWhitelist
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualHubId
Der virtuelle Hub, an den eine Firewall angefügt ist

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetwork
Virtuelles Netzwerk

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VirtualNetworkName
Gibt den Namen des virtuellen Netzwerks an, für das die Firewall bereitgestellt wird. Virtuelles Netzwerk und Firewall müssen derselben Ressourcengruppe angehören.

```yaml
Type: System.String
Parameter Sets: OldIpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Zone
Eine Liste der Verfügbarkeits Zonen, die angibt, woher die Firewall stammen muss.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

### Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork

### Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress []

### Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress

### Microsoft. Azure. Commands. Network. Models. PSAzureFirewallApplicationRuleCollection []

### Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNatRuleCollection []

### Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNetworkRuleCollection []

### System. Collections. Hashtable

## Ausgaben

### Microsoft. Azure. Commands. Network. Models. PSAzureFirewall

## Notizen

## Verwandte Links

[Get-AzFirewall](./Get-AzFirewall.md)

[Remove-AzFirewall](./Remove-AzFirewall.md)

[Satz-AzFirewall](./Set-AzFirewall.md)

[Neu – AzFirewallApplicationRuleCollection](./New-AzFirewallApplicationRuleCollection.md)

[Neu – AzFirewallNatRuleCollection](./New-AzFirewallNatRuleCollection.md)

[Neu – AzFirewallNetworkRuleCollection](./New-AzFirewallNetworkRuleCollection.md)
