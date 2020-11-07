---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubVirtualNetworkRule.md
ms.openlocfilehash: 68aa2d4d0d5ba29cdb2c8ddf86d49c6be1280c88
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845591"
---
# <span data-ttu-id="3a996-101">Remove-AzEventHubVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="3a996-101">Remove-AzEventHubVirtualNetworkRule</span></span>

## <span data-ttu-id="3a996-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3a996-102">SYNOPSIS</span></span>
<span data-ttu-id="3a996-103">Entfernt den einzelnen angegebenen VirtualNetworkRule für die NetworkRuleSet des Namespaces.</span><span class="sxs-lookup"><span data-stu-id="3a996-103">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

## <span data-ttu-id="3a996-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a996-104">SYNTAX</span></span>

### <span data-ttu-id="3a996-105">VirtualNetworkRulePropertiesParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3a996-105">VirtualNetworkRulePropertiesParameterSet (Default)</span></span>
```
Remove-AzEventHubVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String> [-SubnetId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a996-106">VirtualNetworkRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a996-106">VirtualNetworkRuleInputObjectParameterSet</span></span>
```
Remove-AzEventHubVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 [-VirtualNetworkRuleObject] <PSNWRuleSetVirtualNetworkRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a996-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3a996-107">DESCRIPTION</span></span>
<span data-ttu-id="3a996-108">Entfernt den einzelnen angegebenen VirtualNetworkRule für die NetworkRuleSet des Namespaces.</span><span class="sxs-lookup"><span data-stu-id="3a996-108">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

## <span data-ttu-id="3a996-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3a996-109">EXAMPLES</span></span>

### <span data-ttu-id="3a996-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3a996-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -SubnetId "/subscriptions/SubscriptionId/resourcegroups/ResourceGroup/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/sbdefault01"
```

<span data-ttu-id="3a996-111">Entfernt den einzelnen angegebenen VirtualNetworkRule für die NetworkRuleSet des Namespaces.</span><span class="sxs-lookup"><span data-stu-id="3a996-111">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

### <span data-ttu-id="3a996-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="3a996-112">Example 2</span></span>
```powershell
PS C:\> Remove-AzEventHubVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -VirtualNetworkRuleObject $virtualruleset1
```

<span data-ttu-id="3a996-113">Entfernen des $virtualruleset 1 von NetworkRuleSet für den angegebenen Namespace</span><span class="sxs-lookup"><span data-stu-id="3a996-113">Remove the $virtualruleset1 of NetworkRuleSet for the given Namespace</span></span>


## <span data-ttu-id="3a996-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="3a996-114">PARAMETERS</span></span>

### <span data-ttu-id="3a996-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3a996-115">-AsJob</span></span>
<span data-ttu-id="3a996-116">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="3a996-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3a996-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a996-117">-DefaultProfile</span></span>
<span data-ttu-id="3a996-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3a996-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a996-119">-Name</span><span class="sxs-lookup"><span data-stu-id="3a996-119">-Name</span></span>
<span data-ttu-id="3a996-120">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="3a996-120">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a996-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3a996-121">-PassThru</span></span>
<span data-ttu-id="3a996-122">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="3a996-122">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="3a996-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a996-123">-ResourceGroupName</span></span>
<span data-ttu-id="3a996-124">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="3a996-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a996-125">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="3a996-125">-SubnetId</span></span>
<span data-ttu-id="3a996-126">Subnet-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="3a996-126">Subnet Resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualNetworkRulePropertiesParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a996-127">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="3a996-127">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="3a996-128">IPRule-Konfigurationsobjekt</span><span class="sxs-lookup"><span data-stu-id="3a996-128">IPRule Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes
Parameter Sets: VirtualNetworkRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a996-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3a996-129">-Confirm</span></span>
<span data-ttu-id="3a996-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3a996-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a996-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a996-131">-WhatIf</span></span>
<span data-ttu-id="3a996-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3a996-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a996-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3a996-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a996-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a996-134">CommonParameters</span></span>
<span data-ttu-id="3a996-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a996-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="3a996-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a996-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a996-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3a996-137">INPUTS</span></span>

### <span data-ttu-id="3a996-138">System. String</span><span class="sxs-lookup"><span data-stu-id="3a996-138">System.String</span></span>

### <span data-ttu-id="3a996-139">Microsoft. Azure. Commands. EventHub. Models. PSNWRuleSetVirtualNetworkRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="3a996-139">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span></span>

## <span data-ttu-id="3a996-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3a996-140">OUTPUTS</span></span>

### <span data-ttu-id="3a996-141">Microsoft. Azure. Commands. EventHub. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="3a996-141">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="3a996-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="3a996-142">NOTES</span></span>

## <span data-ttu-id="3a996-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3a996-143">RELATED LINKS</span></span>