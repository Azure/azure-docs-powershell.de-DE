---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/add-azeventhubiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Add-AzEventHubIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Add-AzEventHubIPRule.md
ms.openlocfilehash: 54846520fd8370d171a20970eda1d42af81e4d0c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458700"
---
# <span data-ttu-id="d947d-101">Add-AzEventHubIPRule</span><span class="sxs-lookup"><span data-stu-id="d947d-101">Add-AzEventHubIPRule</span></span>

## <span data-ttu-id="d947d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d947d-102">SYNOPSIS</span></span>
<span data-ttu-id="d947d-103">Hinzufügen einer einzelnen IP-Regel zum NetworkRuleSet des angegebenen Namespaces</span><span class="sxs-lookup"><span data-stu-id="d947d-103">Add a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="d947d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d947d-104">SYNTAX</span></span>

### <span data-ttu-id="d947d-105">IPRulePropertiesParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d947d-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Add-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String> [-Action <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d947d-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d947d-106">IPRuleInputObjectParameterSet</span></span>
```
Add-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d947d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d947d-107">DESCRIPTION</span></span>
<span data-ttu-id="d947d-108">Hinzufügen einer einzelnen IP-Regel zum NetworkRuleSet des angegebenen Namespaces</span><span class="sxs-lookup"><span data-stu-id="d947d-108">Add a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="d947d-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d947d-109">EXAMPLES</span></span>

### <span data-ttu-id="d947d-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d947d-110">Example 1</span></span>
```powershell
PS C:\> Add-AzEventHubIPRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -IpMask "11.22.33.44" -Action Allow
```
<span data-ttu-id="d947d-111">Name: defaultAction : Allow Id : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default Type: Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules : {11.22.33.44, Allow} VirtualNetworkRules :</span><span class="sxs-lookup"><span data-stu-id="d947d-111">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="d947d-112">fügen Sie die IPRule mit IpMask "11.22.33.44" und "Action Allow" für den angegebenen Namespace hinzu.</span><span class="sxs-lookup"><span data-stu-id="d947d-112">add the IPRule with IpMask "11.22.33.44" and Action Allow for the given namespace.</span></span>

### <span data-ttu-id="d947d-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d947d-113">Example 2</span></span>
```powershell
PS C:\> Add-AzEventHubIPRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -IpRuleObject $ipruleobject
```
<span data-ttu-id="d947d-114">Name: defaultAction : Allow Id : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default Type: Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules : {11.22.33.44, Allow} VirtualNetworkRules :</span><span class="sxs-lookup"><span data-stu-id="d947d-114">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="d947d-115">fügen Sie die IPRule mit IpMask "11.22.33.44" und "Action Allow" für den angegebenen Namespace hinzu.</span><span class="sxs-lookup"><span data-stu-id="d947d-115">add the IPRule with IpMask "11.22.33.44" and Action Allow for the given namespace.</span></span>

## <span data-ttu-id="d947d-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d947d-116">PARAMETERS</span></span>

### <span data-ttu-id="d947d-117">-Aktion</span><span class="sxs-lookup"><span data-stu-id="d947d-117">-Action</span></span>
<span data-ttu-id="d947d-118">Die Aktion "IP-Filter"</span><span class="sxs-lookup"><span data-stu-id="d947d-118">The IP Filter Action</span></span>

```yaml
Type: System.String
Parameter Sets: IPRulePropertiesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d947d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d947d-119">-DefaultProfile</span></span>
<span data-ttu-id="d947d-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d947d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d947d-121">-IpMask</span><span class="sxs-lookup"><span data-stu-id="d947d-121">-IpMask</span></span>
<span data-ttu-id="d947d-122">Subnetzressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="d947d-122">Subnet Resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: IPRulePropertiesParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d947d-123">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="d947d-123">-IpRuleObject</span></span>
<span data-ttu-id="d947d-124">Zu hinzufügende IPRule-Konfigurationsobjekt</span><span class="sxs-lookup"><span data-stu-id="d947d-124">IPRule Configuration Object to be added</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes
Parameter Sets: IPRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d947d-125">-Name</span><span class="sxs-lookup"><span data-stu-id="d947d-125">-Name</span></span>
<span data-ttu-id="d947d-126">Namespacename</span><span class="sxs-lookup"><span data-stu-id="d947d-126">Namespace Name</span></span>

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

### <span data-ttu-id="d947d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d947d-127">-ResourceGroupName</span></span>
<span data-ttu-id="d947d-128">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="d947d-128">Resource Group Name</span></span>

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

### <span data-ttu-id="d947d-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d947d-129">-Confirm</span></span>
<span data-ttu-id="d947d-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d947d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d947d-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d947d-131">-WhatIf</span></span>
<span data-ttu-id="d947d-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d947d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d947d-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d947d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d947d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d947d-134">CommonParameters</span></span>
<span data-ttu-id="d947d-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d947d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d947d-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d947d-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d947d-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d947d-137">INPUTS</span></span>

### <span data-ttu-id="d947d-138">System.String</span><span class="sxs-lookup"><span data-stu-id="d947d-138">System.String</span></span>

### <span data-ttu-id="d947d-139">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="d947d-139">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="d947d-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d947d-140">OUTPUTS</span></span>

### <span data-ttu-id="d947d-141">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="d947d-141">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="d947d-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d947d-142">NOTES</span></span>

## <span data-ttu-id="d947d-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d947d-143">RELATED LINKS</span></span>
