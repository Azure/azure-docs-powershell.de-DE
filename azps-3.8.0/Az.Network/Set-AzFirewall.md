---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40E56EC1-3327-4DFF-8262-E2EEBB5E4447
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
ms.openlocfilehash: 36ba29104fbc9e87ae2776504dc48bed8a5b9ffa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996033"
---
# <span data-ttu-id="47042-101">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="47042-101">Set-AzFirewall</span></span>

## <span data-ttu-id="47042-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="47042-102">SYNOPSIS</span></span>
<span data-ttu-id="47042-103">Speichert eine geänderte Firewall.</span><span class="sxs-lookup"><span data-stu-id="47042-103">Saves a modified Firewall.</span></span>

## <span data-ttu-id="47042-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="47042-104">SYNTAX</span></span>

```
Set-AzFirewall -AzureFirewall <PSAzureFirewall> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47042-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="47042-105">DESCRIPTION</span></span>
<span data-ttu-id="47042-106">Das Cmdlet " **Satz-AzFirewall** " aktualisiert eine Azure-Firewall.</span><span class="sxs-lookup"><span data-stu-id="47042-106">The **Set-AzFirewall** cmdlet updates an Azure Firewall.</span></span>

## <span data-ttu-id="47042-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="47042-107">EXAMPLES</span></span>

### <span data-ttu-id="47042-108">1: Aktualisieren der Priorität einer Firewall-Anwendungsregel Sammlung</span><span class="sxs-lookup"><span data-stu-id="47042-108">1:  Update priority of a Firewall application rule collection</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetApplicationRuleCollectionByName("ruleCollectionName")
$ruleCollection.Priority = 101
Set-AzFirewall -AzureFirewall $azFw
```

<span data-ttu-id="47042-109">In diesem Beispiel wird die Priorität einer vorhandenen Regelsammlung einer Azure-Firewall aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="47042-109">This example updates the priority of an existing rule collection of an Azure Firewall.</span></span>
<span data-ttu-id="47042-110">Wenn die Azure Firewall "AzureFirewall" in der Ressourcengruppe "RG" eine Anwendungsregel Sammlung mit dem Namen "ruleCollectionName" enthält, werden die oben aufgeführten Befehle die Priorität dieser Regelsammlung ändern und anschließend die Azure-Firewall aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="47042-110">Assuming Azure Firewall "AzureFirewall" in resource group "rg" contains an application rule collection named "ruleCollectionName", the commands above will change the priority of that rule collection and update the Azure Firewall afterwards.</span></span> <span data-ttu-id="47042-111">Ohne den Befehl Set-AzFirewall werden alle Vorgänge, die für das lokale $azFw Objekt ausgeführt werden, nicht auf dem Server widergespiegelt.</span><span class="sxs-lookup"><span data-stu-id="47042-111">Without the Set-AzFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

### <span data-ttu-id="47042-112">2: Erstellen einer Azure Firewall und späteres Einrichten einer Anwendungsregel Sammlung</span><span class="sxs-lookup"><span data-stu-id="47042-112">2:  Create a Azure Firewall and set an application rule collection later</span></span>
```
$azFw = New-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg" -VirtualNetworkName "vnet-name" -PublicIpName "pip-name"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$RuleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
$azFw.ApplicationRuleCollections = $RuleCollection

$azFw | Set-AzFirewall
```

<span data-ttu-id="47042-113">In diesem Beispiel wird zunächst eine Firewall ohne Anwendungsregel Sammlungen erstellt.</span><span class="sxs-lookup"><span data-stu-id="47042-113">In this example, a Firewall is created first without any application rule collections.</span></span> <span data-ttu-id="47042-114">Anschließend werden eine Anwendungsregel und eine Anwendungsregel Sammlung erstellt, und das firewallobjekt wird im Arbeitsspeicher geändert, ohne dass sich dies auf die reale Konfiguration in der Cloud auswirkt.</span><span class="sxs-lookup"><span data-stu-id="47042-114">Afterwards a Application Rule and Application Rule Collection are created, then the Firewall object is modified in memory, without affecting the real configuration in cloud.</span></span> <span data-ttu-id="47042-115">Damit Änderungen in der Cloud wiedergegeben werden, müssen Set-AzFirewall aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="47042-115">For changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>

### <span data-ttu-id="47042-116">3: Aktualisieren des Bedrohungs-Intel-Betriebsmodus der Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="47042-116">3:  Update Threat Intel operation mode of Azure Firewall</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ThreatIntelMode = "Deny"
Set-AzFirewall -Firewall $azFw
```

<span data-ttu-id="47042-117">In diesem Beispiel wird der Bedrohungs-Intel-Betriebsmodus der Azure Firewall "AzureFirewall" in der Ressourcengruppe "RG" aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="47042-117">This example updates the Threat Intel operation mode of Azure Firewall "AzureFirewall" in resource group "rg".</span></span>
<span data-ttu-id="47042-118">Ohne den Befehl Set-AzFirewall werden alle Vorgänge, die für das lokale $azFw Objekt ausgeführt werden, nicht auf dem Server widergespiegelt.</span><span class="sxs-lookup"><span data-stu-id="47042-118">Without the Set-AzFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

### <span data-ttu-id="47042-119">4: Freigeben und Zuweisen der Firewall</span><span class="sxs-lookup"><span data-stu-id="47042-119">4: Deallocate and allocate the Firewall</span></span>
```
$firewall=Get-AzFirewall -ResourceGroupName rgName -Name azFw
$firewall.Deallocate()
$firewall | Set-AzFirewall

$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress - ResourceGroupName rgName -Name publicIpName
$firewall.Allocate($vnet, $pip)
$firewall | Set-AzFirewall
```
<span data-ttu-id="47042-120">In diesem Beispiel wird eine Firewall abgerufen, die Firewall dereserviert und gespeichert.</span><span class="sxs-lookup"><span data-stu-id="47042-120">This example retrieves a Firewall, deallocates the firewall, and saves it.</span></span> <span data-ttu-id="47042-121">Mit dem Befehl "freigeben" wird der ausgeführte Dienst entfernt, die Konfiguration der Firewall bleibt jedoch erhalten.</span><span class="sxs-lookup"><span data-stu-id="47042-121">The Deallocate command removes the running service but preserves the firewall's configuration.</span></span> <span data-ttu-id="47042-122">Damit Änderungen in der Cloud wiedergegeben werden, müssen Set-AzFirewall aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="47042-122">For changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>
<span data-ttu-id="47042-123">Wenn der Benutzer den Dienst erneut starten möchte, sollte die Allocate-Methode für die Firewall aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="47042-123">If user wants to start the service again, the Allocate method should be called on the firewall.</span></span>
<span data-ttu-id="47042-124">Das neue VNet und die öffentliche IP-Adresse müssen sich in derselben Ressourcengruppe wie die Firewall befinden.</span><span class="sxs-lookup"><span data-stu-id="47042-124">The new VNet and Public IP must be in the same resource group as the Firewall.</span></span> <span data-ttu-id="47042-125">Damit Änderungen in der Cloud wiedergegeben werden, müssen Set-AzFirewall aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="47042-125">Again, for changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>

### <span data-ttu-id="47042-126">5: Zuweisen mit einer öffentlichen Verwaltungs-IP-Adresse für erzwungene Tunneling-Szenarien</span><span class="sxs-lookup"><span data-stu-id="47042-126">5: Allocate with a management public IP address for forced tunneling scenarios</span></span>
```
$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress - ResourceGroupName rgName -Name publicIpName
$mgmtPip = Get-AzPublicIpAddress - ResourceGroupName rgName -Name MgmtPublicIpName
$firewall.Allocate($vnet, $pip, $mgmtPip)
$firewall | Set-AzFirewall
```
<span data-ttu-id="47042-127">In diesem Beispiel wird der Firewall eine öffentliche Verwaltungs-IP-Adresse und ein Subnetz für erzwungene Tunnel Szenarien zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="47042-127">This example allocates the firewall with a management public IP address and subnet for forced tunneling scenarios.</span></span> <span data-ttu-id="47042-128">Der VNet muss ein Subnetz mit dem Namen "AzureFirewallManagementSubnet" enthalten.</span><span class="sxs-lookup"><span data-stu-id="47042-128">The VNet must contain a subnet called "AzureFirewallManagementSubnet".</span></span>

### <span data-ttu-id="47042-129">6: Hinzufügen einer öffentlichen IP-Adresse zu einer Azure-Firewall</span><span class="sxs-lookup"><span data-stu-id="47042-129">6:  Add a Public IP address to an Azure Firewall</span></span>
```
$pip = New-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.AddPublicIpAddress($pip)

$azFw | Set-AzFirewall
```

<span data-ttu-id="47042-130">In diesem Beispiel wird die öffentliche IP-Adresse "azFwPublicIp1" an die Firewall angefügt.</span><span class="sxs-lookup"><span data-stu-id="47042-130">In this example, the Public IP Address "azFwPublicIp1" as attached to the Firewall.</span></span>

### <span data-ttu-id="47042-131">7: Entfernen einer öffentlichen IP-Adresse aus einer Azure-Firewall</span><span class="sxs-lookup"><span data-stu-id="47042-131">7:  Remove a Public IP address from an Azure Firewall</span></span>
```
$pip = Get-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg"
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.RemovePublicIpAddress($pip)

$azFw | Set-AzFirewall
```

<span data-ttu-id="47042-132">In diesem Beispiel wird die öffentliche IP-Adresse "azFwPublicIp1" als von der Firewall getrennt.</span><span class="sxs-lookup"><span data-stu-id="47042-132">In this example, the Public IP Address "azFwPublicIp1" as detached from the Firewall.</span></span>

### <span data-ttu-id="47042-133">8: Ändern der öffentlichen Verwaltungs-IP-Adresse in einer Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="47042-133">8:  Change the management public IP address on an Azure Firewall</span></span>
```
$newMgmtPip = New-AzPublicIpAddress -Name "azFwMgmtPublicIp2" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ManagementIpConfiguration.PublicIpAddress = $newMgmtPip

$azFw | Set-AzFirewall
```

<span data-ttu-id="47042-134">In diesem Beispiel wird die öffentliche Verwaltungs-IP-Adresse der Firewall in "AzFwMgmtPublicIp2" geändert.</span><span class="sxs-lookup"><span data-stu-id="47042-134">In this example, the management public IP address of the firewall will be changed to "AzFwMgmtPublicIp2"</span></span>


## <span data-ttu-id="47042-135">Parameter</span><span class="sxs-lookup"><span data-stu-id="47042-135">PARAMETERS</span></span>

### <span data-ttu-id="47042-136">-AsJob</span><span class="sxs-lookup"><span data-stu-id="47042-136">-AsJob</span></span>
<span data-ttu-id="47042-137">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="47042-137">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="47042-138">-AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="47042-138">-AzureFirewall</span></span>
<span data-ttu-id="47042-139">Die AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="47042-139">The AzureFirewall</span></span>

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

### <span data-ttu-id="47042-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47042-140">-DefaultProfile</span></span>
<span data-ttu-id="47042-141">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="47042-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47042-142">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="47042-142">-Confirm</span></span>
<span data-ttu-id="47042-143">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="47042-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47042-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47042-144">-WhatIf</span></span>
<span data-ttu-id="47042-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="47042-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="47042-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="47042-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47042-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47042-147">CommonParameters</span></span>
<span data-ttu-id="47042-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47042-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47042-149">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47042-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47042-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="47042-150">INPUTS</span></span>

### <span data-ttu-id="47042-151">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="47042-151">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="47042-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="47042-152">OUTPUTS</span></span>

### <span data-ttu-id="47042-153">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="47042-153">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="47042-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="47042-154">NOTES</span></span>

## <span data-ttu-id="47042-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="47042-155">RELATED LINKS</span></span>

[<span data-ttu-id="47042-156">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="47042-156">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="47042-157">Neu – AzFirewall</span><span class="sxs-lookup"><span data-stu-id="47042-157">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="47042-158">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="47042-158">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)
