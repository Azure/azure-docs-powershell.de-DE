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
# <span data-ttu-id="71193-101">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="71193-101">Set-AzFirewall</span></span>

## <span data-ttu-id="71193-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="71193-102">SYNOPSIS</span></span>
<span data-ttu-id="71193-103">Speichert eine geänderte Firewall.</span><span class="sxs-lookup"><span data-stu-id="71193-103">Saves a modified Firewall.</span></span>

## <span data-ttu-id="71193-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="71193-104">SYNTAX</span></span>

```
Set-AzFirewall -AzureFirewall <PSAzureFirewall> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71193-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="71193-105">DESCRIPTION</span></span>
<span data-ttu-id="71193-106">Das Cmdlet " **Satz-AzFirewall** " aktualisiert eine Azure-Firewall.</span><span class="sxs-lookup"><span data-stu-id="71193-106">The **Set-AzFirewall** cmdlet updates an Azure Firewall.</span></span>

## <span data-ttu-id="71193-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="71193-107">EXAMPLES</span></span>

### <span data-ttu-id="71193-108">1: Aktualisieren der Priorität einer Firewall-Anwendungsregel Sammlung</span><span class="sxs-lookup"><span data-stu-id="71193-108">1:  Update priority of a Firewall application rule collection</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetApplicationRuleCollectionByName("ruleCollectionName")
$ruleCollection.Priority = 101
Set-AzFirewall -AzureFirewall $azFw
```

<span data-ttu-id="71193-109">In diesem Beispiel wird die Priorität einer vorhandenen Regelsammlung einer Azure-Firewall aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="71193-109">This example updates the priority of an existing rule collection of an Azure Firewall.</span></span>
<span data-ttu-id="71193-110">Wenn die Azure Firewall "AzureFirewall" in der Ressourcengruppe "RG" eine Anwendungsregel Sammlung mit dem Namen "ruleCollectionName" enthält, werden die oben aufgeführten Befehle die Priorität dieser Regelsammlung ändern und anschließend die Azure-Firewall aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="71193-110">Assuming Azure Firewall "AzureFirewall" in resource group "rg" contains an application rule collection named "ruleCollectionName", the commands above will change the priority of that rule collection and update the Azure Firewall afterwards.</span></span> <span data-ttu-id="71193-111">Ohne den Befehl Set-AzFirewall werden alle Vorgänge, die für das lokale $azFw Objekt ausgeführt werden, nicht auf dem Server widergespiegelt.</span><span class="sxs-lookup"><span data-stu-id="71193-111">Without the Set-AzFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

### <span data-ttu-id="71193-112">2: Erstellen einer Azure Firewall und späteres Einrichten einer Anwendungsregel Sammlung</span><span class="sxs-lookup"><span data-stu-id="71193-112">2:  Create a Azure Firewall and set an application rule collection later</span></span>
```
$azFw = New-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg" -VirtualNetworkName "vnet-name" -PublicIpName "pip-name"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$RuleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
$azFw.ApplicationRuleCollections = $RuleCollection

$azFw | Set-AzFirewall
```

<span data-ttu-id="71193-113">In diesem Beispiel wird zunächst eine Firewall ohne Anwendungsregel Sammlungen erstellt.</span><span class="sxs-lookup"><span data-stu-id="71193-113">In this example, a Firewall is created first without any application rule collections.</span></span> <span data-ttu-id="71193-114">Anschließend werden eine Anwendungsregel und eine Anwendungsregel Sammlung erstellt, und das firewallobjekt wird im Arbeitsspeicher geändert, ohne dass sich dies auf die reale Konfiguration in der Cloud auswirkt.</span><span class="sxs-lookup"><span data-stu-id="71193-114">Afterwards a Application Rule and Application Rule Collection are created, then the Firewall object is modified in memory, without affecting the real configuration in cloud.</span></span> <span data-ttu-id="71193-115">Damit Änderungen in der Cloud wiedergegeben werden, müssen Set-AzFirewall aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="71193-115">For changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>

### <span data-ttu-id="71193-116">3: Aktualisieren des Bedrohungs-Intel-Betriebsmodus der Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="71193-116">3:  Update Threat Intel operation mode of Azure Firewall</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ThreatIntelMode = "Deny"
Set-AzFirewall -Firewall $azFw
```

<span data-ttu-id="71193-117">In diesem Beispiel wird der Bedrohungs-Intel-Betriebsmodus der Azure Firewall "AzureFirewall" in der Ressourcengruppe "RG" aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="71193-117">This example updates the Threat Intel operation mode of Azure Firewall "AzureFirewall" in resource group "rg".</span></span>
<span data-ttu-id="71193-118">Ohne den Befehl Set-AzFirewall werden alle Vorgänge, die für das lokale $azFw Objekt ausgeführt werden, nicht auf dem Server widergespiegelt.</span><span class="sxs-lookup"><span data-stu-id="71193-118">Without the Set-AzFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

### <span data-ttu-id="71193-119">4: Freigeben und Zuweisen der Firewall</span><span class="sxs-lookup"><span data-stu-id="71193-119">4: Deallocate and allocate the Firewall</span></span>
```
$firewall=Get-AzFirewall -ResourceGroupName rgName -Name azFw
$firewall.Deallocate()
$firewall | Set-AzFirewall

$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress - ResourceGroupName rgName -Name publicIpName
$firewall.Allocate($vnet, $pip)
$firewall | Set-AzFirewall
```
<span data-ttu-id="71193-120">In diesem Beispiel wird eine Firewall abgerufen, die Firewall dereserviert und gespeichert.</span><span class="sxs-lookup"><span data-stu-id="71193-120">This example retrieves a Firewall, deallocates the firewall, and saves it.</span></span> <span data-ttu-id="71193-121">Mit dem Befehl "freigeben" wird der ausgeführte Dienst entfernt, die Konfiguration der Firewall bleibt jedoch erhalten.</span><span class="sxs-lookup"><span data-stu-id="71193-121">The Deallocate command removes the running service but preserves the firewall's configuration.</span></span> <span data-ttu-id="71193-122">Damit Änderungen in der Cloud wiedergegeben werden, müssen Set-AzFirewall aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="71193-122">For changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>
<span data-ttu-id="71193-123">Wenn der Benutzer den Dienst erneut starten möchte, sollte die Allocate-Methode für die Firewall aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="71193-123">If user wants to start the service again, the Allocate method should be called on the firewall.</span></span>
<span data-ttu-id="71193-124">Das neue VNet und die öffentliche IP-Adresse müssen sich in derselben Ressourcengruppe wie die Firewall befinden.</span><span class="sxs-lookup"><span data-stu-id="71193-124">The new VNet and Public IP must be in the same resource group as the Firewall.</span></span> <span data-ttu-id="71193-125">Damit Änderungen in der Cloud wiedergegeben werden, müssen Set-AzFirewall aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="71193-125">Again, for changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>

### <span data-ttu-id="71193-126">5: Zuweisen mit einer öffentlichen Verwaltungs-IP-Adresse für erzwungene Tunneling-Szenarien</span><span class="sxs-lookup"><span data-stu-id="71193-126">5: Allocate with a management public IP address for forced tunneling scenarios</span></span>
```
$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress - ResourceGroupName rgName -Name publicIpName
$mgmtPip = Get-AzPublicIpAddress - ResourceGroupName rgName -Name MgmtPublicIpName
$firewall.Allocate($vnet, $pip, $mgmtPip)
$firewall | Set-AzFirewall
```
<span data-ttu-id="71193-127">In diesem Beispiel wird der Firewall eine öffentliche Verwaltungs-IP-Adresse und ein Subnetz für erzwungene Tunnel Szenarien zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="71193-127">This example allocates the firewall with a management public IP address and subnet for forced tunneling scenarios.</span></span> <span data-ttu-id="71193-128">Der VNet muss ein Subnetz mit dem Namen "AzureFirewallManagementSubnet" enthalten.</span><span class="sxs-lookup"><span data-stu-id="71193-128">The VNet must contain a subnet called "AzureFirewallManagementSubnet".</span></span>

### <span data-ttu-id="71193-129">6: Hinzufügen einer öffentlichen IP-Adresse zu einer Azure-Firewall</span><span class="sxs-lookup"><span data-stu-id="71193-129">6:  Add a Public IP address to an Azure Firewall</span></span>
```
$pip = New-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.AddPublicIpAddress($pip)

$azFw | Set-AzFirewall
```

<span data-ttu-id="71193-130">In diesem Beispiel wird die öffentliche IP-Adresse "azFwPublicIp1" an die Firewall angefügt.</span><span class="sxs-lookup"><span data-stu-id="71193-130">In this example, the Public IP Address "azFwPublicIp1" as attached to the Firewall.</span></span>

### <span data-ttu-id="71193-131">7: Entfernen einer öffentlichen IP-Adresse aus einer Azure-Firewall</span><span class="sxs-lookup"><span data-stu-id="71193-131">7:  Remove a Public IP address from an Azure Firewall</span></span>
```
$pip = Get-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg"
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.RemovePublicIpAddress($pip)

$azFw | Set-AzFirewall
```

<span data-ttu-id="71193-132">In diesem Beispiel wird die öffentliche IP-Adresse "azFwPublicIp1" als von der Firewall getrennt.</span><span class="sxs-lookup"><span data-stu-id="71193-132">In this example, the Public IP Address "azFwPublicIp1" as detached from the Firewall.</span></span>

### <span data-ttu-id="71193-133">8: Ändern der öffentlichen Verwaltungs-IP-Adresse in einer Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="71193-133">8:  Change the management public IP address on an Azure Firewall</span></span>
```
$newMgmtPip = New-AzPublicIpAddress -Name "azFwMgmtPublicIp2" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ManagementIpConfiguration.PublicIpAddress = $newMgmtPip

$azFw | Set-AzFirewall
```

<span data-ttu-id="71193-134">In diesem Beispiel wird die öffentliche Verwaltungs-IP-Adresse der Firewall in "AzFwMgmtPublicIp2" geändert.</span><span class="sxs-lookup"><span data-stu-id="71193-134">In this example, the management public IP address of the firewall will be changed to "AzFwMgmtPublicIp2"</span></span>

### <span data-ttu-id="71193-135">9: Hinzufügen einer DNS-Konfiguration zu einer Azure-Firewall</span><span class="sxs-lookup"><span data-stu-id="71193-135">9:  Add DNS configuration to an Azure Firewall</span></span>
```
$dnsServers = @("10.10.10.1", "20.20.20.2")
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.DNSEnableProxy = $true
$azFw.DNSServer = $dnsServers

$azFw | Set-AzFirewall
```

<span data-ttu-id="71193-136">In diesem Beispiel ist die Konfiguration des DNS-Proxys und der DNS-Server an die Firewall angefügt.</span><span class="sxs-lookup"><span data-stu-id="71193-136">In this example, DNS Proxy and DNS Server configuration is attached to the Firewall.</span></span>

### <span data-ttu-id="71193-137">10: Aktualisieren des Ziels einer vorhandenen Regel in einer Firewall-Anwendungsregel Sammlung</span><span class="sxs-lookup"><span data-stu-id="71193-137">10: Update destination of an existing rule within a Firewall application rule collection</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetNetworkRuleCollectionByName("ruleCollectionName")
$rule=$ruleCollection.GetRuleByName("ruleName")
$rule.DestinationAddresses="10.10.10.10"
Set-AzFirewall -AzureFirewall $azFw
```

<span data-ttu-id="71193-138">In diesem Beispiel wird das Ziel einer vorhandenen Regel innerhalb einer Regelsammlung einer Azure-Firewall aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="71193-138">This example updates the destination of an existing rule within a rule collection of an Azure Firewall.</span></span> <span data-ttu-id="71193-139">So können Sie Ihre Regeln automatisch aktualisieren, wenn IP-Adressen dynamisch geändert werden.</span><span class="sxs-lookup"><span data-stu-id="71193-139">This allows you to automatically update your rules when IP addresses change dynamically.</span></span>

### <span data-ttu-id="71193-140">11: Zulassen von aktivem FTP auf Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="71193-140">11: Allow Active FTP on Azure Firewall</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.AllowActiveFTP = $true

$azFw | Set-AzFirewall
```

<span data-ttu-id="71193-141">In diesem Beispiel ist Active FTP für die Firewall zugelassen.</span><span class="sxs-lookup"><span data-stu-id="71193-141">In this example, Active FTP is allowed on the Firewall.</span></span>

## <span data-ttu-id="71193-142">Parameter</span><span class="sxs-lookup"><span data-stu-id="71193-142">PARAMETERS</span></span>

### <span data-ttu-id="71193-143">-AsJob</span><span class="sxs-lookup"><span data-stu-id="71193-143">-AsJob</span></span>
<span data-ttu-id="71193-144">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="71193-144">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="71193-145">-AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="71193-145">-AzureFirewall</span></span>
<span data-ttu-id="71193-146">Die AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="71193-146">The AzureFirewall</span></span>

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

### <span data-ttu-id="71193-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71193-147">-DefaultProfile</span></span>
<span data-ttu-id="71193-148">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="71193-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71193-149">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="71193-149">-Confirm</span></span>
<span data-ttu-id="71193-150">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="71193-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71193-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71193-151">-WhatIf</span></span>
<span data-ttu-id="71193-152">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="71193-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="71193-153">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="71193-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71193-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71193-154">CommonParameters</span></span>
<span data-ttu-id="71193-155">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71193-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71193-156">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71193-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71193-157">Eingaben</span><span class="sxs-lookup"><span data-stu-id="71193-157">INPUTS</span></span>

### <span data-ttu-id="71193-158">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="71193-158">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="71193-159">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="71193-159">OUTPUTS</span></span>

### <span data-ttu-id="71193-160">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="71193-160">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="71193-161">Notizen</span><span class="sxs-lookup"><span data-stu-id="71193-161">NOTES</span></span>

## <span data-ttu-id="71193-162">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="71193-162">RELATED LINKS</span></span>

[<span data-ttu-id="71193-163">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="71193-163">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="71193-164">Neu – AzFirewall</span><span class="sxs-lookup"><span data-stu-id="71193-164">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="71193-165">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="71193-165">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)
