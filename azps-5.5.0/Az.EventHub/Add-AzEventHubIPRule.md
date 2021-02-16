---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/add-azeventhubiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Add-AzEventHubIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Add-AzEventHubIPRule.md
ms.openlocfilehash: 54846520fd8370d171a20970eda1d42af81e4d0c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100175521"
---
# <span data-ttu-id="f880c-101">Add-AzEventHubIPRule</span><span class="sxs-lookup"><span data-stu-id="f880c-101">Add-AzEventHubIPRule</span></span>

## <span data-ttu-id="f880c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f880c-102">SYNOPSIS</span></span>
<span data-ttu-id="f880c-103">Hinzufügen einer einzelnen IP-Regel zum NetworkRuleSet des angegebenen Namespaces</span><span class="sxs-lookup"><span data-stu-id="f880c-103">Add a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="f880c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f880c-104">SYNTAX</span></span>

### <span data-ttu-id="f880c-105">IPRulePropertiesParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f880c-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Add-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String> [-Action <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f880c-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f880c-106">IPRuleInputObjectParameterSet</span></span>
```
Add-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f880c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f880c-107">DESCRIPTION</span></span>
<span data-ttu-id="f880c-108">Hinzufügen einer einzelnen IP-Regel zum NetworkRuleSet des angegebenen Namespace</span><span class="sxs-lookup"><span data-stu-id="f880c-108">Add a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="f880c-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f880c-109">EXAMPLES</span></span>

### <span data-ttu-id="f880c-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f880c-110">Example 1</span></span>
```powershell
PS C:\> Add-AzEventHubIPRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -IpMask "11.22.33.44" -Action Allow
```
<span data-ttu-id="f880c-111">Name: defaultAction : Allow Id : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default Type: Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules : {11.22.33.44, Allow} VirtualNetworkRules :</span><span class="sxs-lookup"><span data-stu-id="f880c-111">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="f880c-112">fügen Sie die IPRule mit IpMask "11.22.33.44" und "Action Allow" für den angegebenen Namespace hinzu.</span><span class="sxs-lookup"><span data-stu-id="f880c-112">add the IPRule with IpMask "11.22.33.44" and Action Allow for the given namespace.</span></span>

### <span data-ttu-id="f880c-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="f880c-113">Example 2</span></span>
```powershell
PS C:\> Add-AzEventHubIPRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -IpRuleObject $ipruleobject
```
<span data-ttu-id="f880c-114">Name: defaultAction : Allow Id : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default Type: Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules : {11.22.33.44, Allow} VirtualNetworkRules :</span><span class="sxs-lookup"><span data-stu-id="f880c-114">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="f880c-115">fügen Sie die IPRule mit IpMask "11.22.33.44" und "Action Allow" für den angegebenen Namespace hinzu.</span><span class="sxs-lookup"><span data-stu-id="f880c-115">add the IPRule with IpMask "11.22.33.44" and Action Allow for the given namespace.</span></span>

## <span data-ttu-id="f880c-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f880c-116">PARAMETERS</span></span>

### <span data-ttu-id="f880c-117">-Aktion</span><span class="sxs-lookup"><span data-stu-id="f880c-117">-Action</span></span>
<span data-ttu-id="f880c-118">Die Aktion "IP-Filter"</span><span class="sxs-lookup"><span data-stu-id="f880c-118">The IP Filter Action</span></span>

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

### <span data-ttu-id="f880c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f880c-119">-DefaultProfile</span></span>
<span data-ttu-id="f880c-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f880c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f880c-121">-IpMask</span><span class="sxs-lookup"><span data-stu-id="f880c-121">-IpMask</span></span>
<span data-ttu-id="f880c-122">Subnetzressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="f880c-122">Subnet Resource ID</span></span>

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

### <span data-ttu-id="f880c-123">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="f880c-123">-IpRuleObject</span></span>
<span data-ttu-id="f880c-124">Zu hinzufügende IPRule-Konfigurationsobjekt</span><span class="sxs-lookup"><span data-stu-id="f880c-124">IPRule Configuration Object to be added</span></span>

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

### <span data-ttu-id="f880c-125">-Name</span><span class="sxs-lookup"><span data-stu-id="f880c-125">-Name</span></span>
<span data-ttu-id="f880c-126">Namespacename</span><span class="sxs-lookup"><span data-stu-id="f880c-126">Namespace Name</span></span>

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

### <span data-ttu-id="f880c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f880c-127">-ResourceGroupName</span></span>
<span data-ttu-id="f880c-128">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="f880c-128">Resource Group Name</span></span>

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

### <span data-ttu-id="f880c-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f880c-129">-Confirm</span></span>
<span data-ttu-id="f880c-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f880c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f880c-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f880c-131">-WhatIf</span></span>
<span data-ttu-id="f880c-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f880c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f880c-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f880c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f880c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f880c-134">CommonParameters</span></span>
<span data-ttu-id="f880c-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f880c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="f880c-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f880c-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f880c-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f880c-137">INPUTS</span></span>

### <span data-ttu-id="f880c-138">System.String</span><span class="sxs-lookup"><span data-stu-id="f880c-138">System.String</span></span>

### <span data-ttu-id="f880c-139">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="f880c-139">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="f880c-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f880c-140">OUTPUTS</span></span>

### <span data-ttu-id="f880c-141">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="f880c-141">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="f880c-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f880c-142">NOTES</span></span>

## <span data-ttu-id="f880c-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f880c-143">RELATED LINKS</span></span>
