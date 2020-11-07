---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40E56EC1-3327-4DFF-8262-E2EEBB5E4447
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
ms.openlocfilehash: 7937af38c7dd0becd57604a0a7c00e5d1f584e6c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660220"
---
# <span data-ttu-id="1d35d-101">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="1d35d-101">Set-AzFirewall</span></span>

## <span data-ttu-id="1d35d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1d35d-102">SYNOPSIS</span></span>
<span data-ttu-id="1d35d-103">Speichert eine geänderte Firewall.</span><span class="sxs-lookup"><span data-stu-id="1d35d-103">Saves a modified Firewall.</span></span>

## <span data-ttu-id="1d35d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1d35d-104">SYNTAX</span></span>

```
Set-AzFirewall -AzureFirewall <PSAzureFirewall> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d35d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1d35d-105">DESCRIPTION</span></span>
<span data-ttu-id="1d35d-106">Das Cmdlet " **Satz-AzFirewall** " aktualisiert eine Azure-Firewall.</span><span class="sxs-lookup"><span data-stu-id="1d35d-106">The **Set-AzFirewall** cmdlet updates an Azure Firewall.</span></span>

## <span data-ttu-id="1d35d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1d35d-107">EXAMPLES</span></span>

### <span data-ttu-id="1d35d-108">1: Aktualisieren der Priorität einer Firewall-Anwendungsregel Sammlung</span><span class="sxs-lookup"><span data-stu-id="1d35d-108">1:  Update priority of a Firewall application rule collection</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetApplicationRuleCollectionByName("ruleCollectionName")
$ruleCollection.Priority = 101
Set-AzFirewall -AzureFirewall $azFw
```

<span data-ttu-id="1d35d-109">In diesem Beispiel wird die Priorität einer vorhandenen Regelsammlung einer Azure-Firewall aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="1d35d-109">This example updates the priority of an existing rule collection of an Azure Firewall.</span></span>
<span data-ttu-id="1d35d-110">Wenn die Azure Firewall "AzureFirewall" in der Ressourcengruppe "RG" eine Anwendungsregel Sammlung mit dem Namen "ruleCollectionName" enthält, werden die oben aufgeführten Befehle die Priorität dieser Regelsammlung ändern und anschließend die Azure-Firewall aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="1d35d-110">Assuming Azure Firewall "AzureFirewall" in resource group "rg" contains an application rule collection named "ruleCollectionName", the commands above will change the priority of that rule collection and update the Azure Firewall afterwards.</span></span> <span data-ttu-id="1d35d-111">Ohne den Befehl Set-AzFirewall werden alle Vorgänge, die für das lokale $azFw Objekt ausgeführt werden, nicht auf dem Server widergespiegelt.</span><span class="sxs-lookup"><span data-stu-id="1d35d-111">Without the Set-AzFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

### <span data-ttu-id="1d35d-112">2: Erstellen einer Azure Firewall und späteres Einrichten einer Anwendungsregel Sammlung</span><span class="sxs-lookup"><span data-stu-id="1d35d-112">2:  Create a Azure Firewall and set an application rule collection later</span></span>
```
$azFw = New-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg" -VirtualNetworkName "vnet-name" -PublicIpName "pip-name"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$RuleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
$azFw.ApplicationRuleCollections = $RuleCollection

$azFw | Set-AzFirewall
```

<span data-ttu-id="1d35d-113">In diesem Beispiel wird zunächst eine Firewall ohne Anwendungsregel Sammlungen erstellt.</span><span class="sxs-lookup"><span data-stu-id="1d35d-113">In this example, a Firewall is created first without any application rule collections.</span></span> <span data-ttu-id="1d35d-114">Anschließend werden eine Anwendungsregel und eine Anwendungsregel Sammlung erstellt, und das firewallobjekt wird im Arbeitsspeicher geändert, ohne dass sich dies auf die reale Konfiguration in der Cloud auswirkt.</span><span class="sxs-lookup"><span data-stu-id="1d35d-114">Afterwards a Application Rule and Application Rule Collection are created, then the Firewall object is modified in memory, without affecting the real configuration in cloud.</span></span> <span data-ttu-id="1d35d-115">Damit Änderungen in der Cloud wiedergegeben werden, müssen Set-AzFirewall aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="1d35d-115">For changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>

### <span data-ttu-id="1d35d-116">3: Aktualisieren des Bedrohungs-Intel-Betriebsmodus der Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="1d35d-116">3:  Update Threat Intel operation mode of Azure Firewall</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ThreatIntelMode = "Deny"
Set-AzFirewall -Firewall $azFw
```

<span data-ttu-id="1d35d-117">In diesem Beispiel wird der Bedrohungs-Intel-Betriebsmodus der Azure Firewall "AzureFirewall" in der Ressourcengruppe "RG" aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="1d35d-117">This example updates the Threat Intel operation mode of Azure Firewall "AzureFirewall" in resource group "rg".</span></span>
<span data-ttu-id="1d35d-118">Ohne den Befehl Set-AzFirewall werden alle Vorgänge, die für das lokale $azFw Objekt ausgeführt werden, nicht auf dem Server widergespiegelt.</span><span class="sxs-lookup"><span data-stu-id="1d35d-118">Without the Set-AzFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

## <span data-ttu-id="1d35d-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="1d35d-119">PARAMETERS</span></span>

### <span data-ttu-id="1d35d-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1d35d-120">-AsJob</span></span>
<span data-ttu-id="1d35d-121">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="1d35d-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1d35d-122">-AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="1d35d-122">-AzureFirewall</span></span>
<span data-ttu-id="1d35d-123">Die AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="1d35d-123">The AzureFirewall</span></span>

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

### <span data-ttu-id="1d35d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d35d-124">-DefaultProfile</span></span>
<span data-ttu-id="1d35d-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1d35d-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d35d-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1d35d-126">-Confirm</span></span>
<span data-ttu-id="1d35d-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1d35d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d35d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d35d-128">-WhatIf</span></span>
<span data-ttu-id="1d35d-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1d35d-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1d35d-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1d35d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d35d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d35d-131">CommonParameters</span></span>
<span data-ttu-id="1d35d-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d35d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d35d-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d35d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d35d-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1d35d-134">INPUTS</span></span>

### <span data-ttu-id="1d35d-135">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="1d35d-135">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="1d35d-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1d35d-136">OUTPUTS</span></span>

### <span data-ttu-id="1d35d-137">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="1d35d-137">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="1d35d-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="1d35d-138">NOTES</span></span>

## <span data-ttu-id="1d35d-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1d35d-139">RELATED LINKS</span></span>

[<span data-ttu-id="1d35d-140">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="1d35d-140">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="1d35d-141">Neu – AzFirewall</span><span class="sxs-lookup"><span data-stu-id="1d35d-141">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="1d35d-142">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="1d35d-142">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)
