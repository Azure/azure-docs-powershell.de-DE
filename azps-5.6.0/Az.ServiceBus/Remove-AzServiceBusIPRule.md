---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/remove-azservicebusiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusIPRule.md
ms.openlocfilehash: e14d82fbf503487ddb4e4ebac1385400305e9209
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944741"
---
# <span data-ttu-id="fa9b0-101">Remove-AzServiceBusIPRule</span><span class="sxs-lookup"><span data-stu-id="fa9b0-101">Remove-AzServiceBusIPRule</span></span>

## <span data-ttu-id="fa9b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa9b0-102">SYNOPSIS</span></span>
<span data-ttu-id="fa9b0-103">Entfernen einer einzelnen IP-Regel zum NetworkRuleSet des angegebenen Namespaces</span><span class="sxs-lookup"><span data-stu-id="fa9b0-103">Remove a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="fa9b0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fa9b0-104">SYNTAX</span></span>

### <span data-ttu-id="fa9b0-105">IPRulePropertiesParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="fa9b0-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Remove-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa9b0-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa9b0-106">IPRuleInputObjectParameterSet</span></span>
```
Remove-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa9b0-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fa9b0-107">DESCRIPTION</span></span>
<span data-ttu-id="fa9b0-108">Entfernen einer einzelnen IP-Regel zum NetworkRuleSet des angegebenen Namespaces</span><span class="sxs-lookup"><span data-stu-id="fa9b0-108">Remove a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="fa9b0-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fa9b0-109">EXAMPLES</span></span>

### <span data-ttu-id="fa9b0-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fa9b0-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusIPRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -IpMask "11.22.33.44"
```

<span data-ttu-id="fa9b0-111">Entfernt IpMask des NetworkRuleSets des angegebenen Namespaces</span><span class="sxs-lookup"><span data-stu-id="fa9b0-111">Removes IpMask of the NetworkRuleSet of the given namespace</span></span>

## <span data-ttu-id="fa9b0-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="fa9b0-112">PARAMETERS</span></span>

### <span data-ttu-id="fa9b0-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fa9b0-113">-AsJob</span></span>
<span data-ttu-id="fa9b0-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="fa9b0-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fa9b0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa9b0-115">-DefaultProfile</span></span>
<span data-ttu-id="fa9b0-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fa9b0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa9b0-117">-IpMask</span><span class="sxs-lookup"><span data-stu-id="fa9b0-117">-IpMask</span></span>
<span data-ttu-id="fa9b0-118">Subnetzressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="fa9b0-118">Subnet Resource ID</span></span>

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

### <span data-ttu-id="fa9b0-119">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="fa9b0-119">-IpRuleObject</span></span>
<span data-ttu-id="fa9b0-120">IPRule Configuration Object</span><span class="sxs-lookup"><span data-stu-id="fa9b0-120">IPRule Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes
Parameter Sets: IPRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fa9b0-121">-Name</span><span class="sxs-lookup"><span data-stu-id="fa9b0-121">-Name</span></span>
<span data-ttu-id="fa9b0-122">Namespacename</span><span class="sxs-lookup"><span data-stu-id="fa9b0-122">Namespace Name</span></span>

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

### <span data-ttu-id="fa9b0-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fa9b0-123">-PassThru</span></span>
<span data-ttu-id="fa9b0-124">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="fa9b0-124">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="fa9b0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa9b0-125">-ResourceGroupName</span></span>
<span data-ttu-id="fa9b0-126">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="fa9b0-126">Resource Group Name</span></span>

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

### <span data-ttu-id="fa9b0-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fa9b0-127">-Confirm</span></span>
<span data-ttu-id="fa9b0-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fa9b0-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa9b0-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa9b0-129">-WhatIf</span></span>
<span data-ttu-id="fa9b0-130">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fa9b0-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa9b0-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fa9b0-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa9b0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa9b0-132">CommonParameters</span></span>
<span data-ttu-id="fa9b0-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa9b0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="fa9b0-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa9b0-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa9b0-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fa9b0-135">INPUTS</span></span>

### <span data-ttu-id="fa9b0-136">System.String</span><span class="sxs-lookup"><span data-stu-id="fa9b0-136">System.String</span></span>

### <span data-ttu-id="fa9b0-137">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="fa9b0-137">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="fa9b0-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fa9b0-138">OUTPUTS</span></span>

### <span data-ttu-id="fa9b0-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="fa9b0-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="fa9b0-140">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="fa9b0-140">NOTES</span></span>

## <span data-ttu-id="fa9b0-141">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="fa9b0-141">RELATED LINKS</span></span>
