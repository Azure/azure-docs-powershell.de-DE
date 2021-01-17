---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubIPRule.md
ms.openlocfilehash: 00213d4829d4b389f19a01ad9748517608657136
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458691"
---
# <span data-ttu-id="3e61b-101">Remove-AzEventHubIPRule</span><span class="sxs-lookup"><span data-stu-id="3e61b-101">Remove-AzEventHubIPRule</span></span>

## <span data-ttu-id="3e61b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e61b-102">SYNOPSIS</span></span>
<span data-ttu-id="3e61b-103">Entfernen einer einzelnen IP-Regel in das NetworkRuleSet des angegebenen Namespaces</span><span class="sxs-lookup"><span data-stu-id="3e61b-103">Remove a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="3e61b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3e61b-104">SYNTAX</span></span>

### <span data-ttu-id="3e61b-105">IPRulePropertiesParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3e61b-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Remove-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e61b-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e61b-106">IPRuleInputObjectParameterSet</span></span>
```
Remove-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3e61b-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3e61b-107">DESCRIPTION</span></span>
<span data-ttu-id="3e61b-108">Entfernen einer einzelnen IP-Regel in das NetworkRuleSet des angegebenen Namespaces</span><span class="sxs-lookup"><span data-stu-id="3e61b-108">Remove a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="3e61b-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3e61b-109">EXAMPLES</span></span>

### <span data-ttu-id="3e61b-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3e61b-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubIPRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -IpMask "11.22.33.44"
```

<span data-ttu-id="3e61b-111">Entfernt "IpMask" vom "NetworkRuleSet" des angegebenen Namespaces.</span><span class="sxs-lookup"><span data-stu-id="3e61b-111">Removes IpMask of the NetworkRuleSet of the given namespace</span></span>

## <span data-ttu-id="3e61b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3e61b-112">PARAMETERS</span></span>

### <span data-ttu-id="3e61b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3e61b-113">-AsJob</span></span>
<span data-ttu-id="3e61b-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="3e61b-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3e61b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e61b-115">-DefaultProfile</span></span>
<span data-ttu-id="3e61b-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3e61b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e61b-117">-IpMask</span><span class="sxs-lookup"><span data-stu-id="3e61b-117">-IpMask</span></span>
<span data-ttu-id="3e61b-118">Subnetzressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="3e61b-118">Subnet Resource ID</span></span>

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

### <span data-ttu-id="3e61b-119">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="3e61b-119">-IpRuleObject</span></span>
<span data-ttu-id="3e61b-120">IPRule Configuration Object</span><span class="sxs-lookup"><span data-stu-id="3e61b-120">IPRule Configuration Object</span></span>

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

### <span data-ttu-id="3e61b-121">-Name</span><span class="sxs-lookup"><span data-stu-id="3e61b-121">-Name</span></span>
<span data-ttu-id="3e61b-122">Namespacename</span><span class="sxs-lookup"><span data-stu-id="3e61b-122">Namespace Name</span></span>

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

### <span data-ttu-id="3e61b-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3e61b-123">-PassThru</span></span>
<span data-ttu-id="3e61b-124">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="3e61b-124">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="3e61b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e61b-125">-ResourceGroupName</span></span>
<span data-ttu-id="3e61b-126">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="3e61b-126">Resource Group Name</span></span>

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

### <span data-ttu-id="3e61b-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3e61b-127">-Confirm</span></span>
<span data-ttu-id="3e61b-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3e61b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e61b-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="3e61b-129">-WhatIf</span></span>
<span data-ttu-id="3e61b-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3e61b-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e61b-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3e61b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e61b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e61b-132">CommonParameters</span></span>
<span data-ttu-id="3e61b-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e61b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="3e61b-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e61b-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e61b-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3e61b-135">INPUTS</span></span>

### <span data-ttu-id="3e61b-136">System.String</span><span class="sxs-lookup"><span data-stu-id="3e61b-136">System.String</span></span>

### <span data-ttu-id="3e61b-137">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="3e61b-137">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="3e61b-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3e61b-138">OUTPUTS</span></span>

### <span data-ttu-id="3e61b-139">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="3e61b-139">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="3e61b-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3e61b-140">NOTES</span></span>

## <span data-ttu-id="3e61b-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3e61b-141">RELATED LINKS</span></span>