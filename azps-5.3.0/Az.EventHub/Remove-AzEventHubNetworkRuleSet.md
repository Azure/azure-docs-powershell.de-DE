---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 9c263e4d31d5d186abb4a08f3849db072aec3721
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386922"
---
# <span data-ttu-id="29cdf-101">Remove-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="29cdf-101">Remove-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="29cdf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29cdf-102">SYNOPSIS</span></span>
<span data-ttu-id="29cdf-103">Entfernt das NetworkRuleSet für den angegebenen Namespace.</span><span class="sxs-lookup"><span data-stu-id="29cdf-103">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="29cdf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="29cdf-104">SYNTAX</span></span>

### <span data-ttu-id="29cdf-105">NetworkRuleSetPropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="29cdf-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Remove-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29cdf-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="29cdf-106">NamespaceInputObjectSet</span></span>
```
Remove-AzEventHubNetworkRuleSet [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29cdf-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="29cdf-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Remove-AzEventHubNetworkRuleSet [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29cdf-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="29cdf-108">DESCRIPTION</span></span>
<span data-ttu-id="29cdf-109">Entfernt das NetworkRuleSet für den angegebenen Namespace.</span><span class="sxs-lookup"><span data-stu-id="29cdf-109">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="29cdf-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="29cdf-110">EXAMPLES</span></span>

### <span data-ttu-id="29cdf-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="29cdf-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace Eventhub-Namespace1-1375 -PassThru
```
<span data-ttu-id="29cdf-112">Name: defaultAction : Allow Id : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type: Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules :</span><span class="sxs-lookup"><span data-stu-id="29cdf-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 


<span data-ttu-id="29cdf-113">Löscht das NetworkRuleSet für den angegebenen "Eventhub-Namespace1-1375"-Namespace.</span><span class="sxs-lookup"><span data-stu-id="29cdf-113">Deletes the NetworkRuleSet for the Given "Eventhub-Namespace1-1375" namespace</span></span> 

### <span data-ttu-id="29cdf-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="29cdf-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -InputObject $result1375
```

<span data-ttu-id="29cdf-115">Löscht das NetworkRuleSet mithilfe von InputObject.</span><span class="sxs-lookup"><span data-stu-id="29cdf-115">Deletes the NetworkRuleSet using InputObject</span></span> 

### <span data-ttu-id="29cdf-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="29cdf-116">Example 3</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-1375 -PassThru
```
<span data-ttu-id="29cdf-117">Name: defaultAction : Allow Id : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type: Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules :</span><span class="sxs-lookup"><span data-stu-id="29cdf-117">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="29cdf-118">Löscht das NetworkRuleSet mithilfe der ResourceId des Namespaces.</span><span class="sxs-lookup"><span data-stu-id="29cdf-118">Deletes the NetworkRuleSet using ResourceId of the Namespace</span></span>


## <span data-ttu-id="29cdf-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="29cdf-119">PARAMETERS</span></span>

### <span data-ttu-id="29cdf-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="29cdf-120">-AsJob</span></span>
<span data-ttu-id="29cdf-121">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="29cdf-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="29cdf-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29cdf-122">-DefaultProfile</span></span>
<span data-ttu-id="29cdf-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="29cdf-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29cdf-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="29cdf-124">-InputObject</span></span>
<span data-ttu-id="29cdf-125">Namespaceobjekt</span><span class="sxs-lookup"><span data-stu-id="29cdf-125">Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="29cdf-126">-Name</span><span class="sxs-lookup"><span data-stu-id="29cdf-126">-Name</span></span>
<span data-ttu-id="29cdf-127">Namespacename</span><span class="sxs-lookup"><span data-stu-id="29cdf-127">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29cdf-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="29cdf-128">-PassThru</span></span>
<span data-ttu-id="29cdf-129">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="29cdf-129">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="29cdf-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29cdf-130">-ResourceGroupName</span></span>
<span data-ttu-id="29cdf-131">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="29cdf-131">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29cdf-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="29cdf-132">-ResourceId</span></span>
<span data-ttu-id="29cdf-133">Namespaceressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="29cdf-133">Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29cdf-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="29cdf-134">-Confirm</span></span>
<span data-ttu-id="29cdf-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="29cdf-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29cdf-136">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="29cdf-136">-WhatIf</span></span>
<span data-ttu-id="29cdf-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="29cdf-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29cdf-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="29cdf-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29cdf-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29cdf-139">CommonParameters</span></span>
<span data-ttu-id="29cdf-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29cdf-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="29cdf-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29cdf-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29cdf-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="29cdf-142">INPUTS</span></span>

### <span data-ttu-id="29cdf-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="29cdf-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="29cdf-144">System.String</span><span class="sxs-lookup"><span data-stu-id="29cdf-144">System.String</span></span>

## <span data-ttu-id="29cdf-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="29cdf-145">OUTPUTS</span></span>

### <span data-ttu-id="29cdf-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="29cdf-146">System.Boolean</span></span>

## <span data-ttu-id="29cdf-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="29cdf-147">NOTES</span></span>

## <span data-ttu-id="29cdf-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="29cdf-148">RELATED LINKS</span></span>