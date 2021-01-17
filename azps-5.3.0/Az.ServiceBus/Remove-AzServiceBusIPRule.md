---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusIPRule.md
ms.openlocfilehash: 90c832d36017aa02a05d972a7b6e26fffd93937e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471884"
---
# <span data-ttu-id="6f705-101">Remove-AzServiceBusIPRule</span><span class="sxs-lookup"><span data-stu-id="6f705-101">Remove-AzServiceBusIPRule</span></span>

## <span data-ttu-id="6f705-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f705-102">SYNOPSIS</span></span>
<span data-ttu-id="6f705-103">Entfernen einer einzelnen IP-Regel in das NetworkRuleSet des angegebenen Namespaces</span><span class="sxs-lookup"><span data-stu-id="6f705-103">Remove a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="6f705-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6f705-104">SYNTAX</span></span>

### <span data-ttu-id="6f705-105">IPRulePropertiesParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="6f705-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Remove-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f705-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f705-106">IPRuleInputObjectParameterSet</span></span>
```
Remove-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f705-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6f705-107">DESCRIPTION</span></span>
<span data-ttu-id="6f705-108">Entfernen einer einzelnen IP-Regel in das NetworkRuleSet des angegebenen Namespaces</span><span class="sxs-lookup"><span data-stu-id="6f705-108">Remove a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="6f705-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6f705-109">EXAMPLES</span></span>

### <span data-ttu-id="6f705-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6f705-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusIPRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -IpMask "11.22.33.44"
```

<span data-ttu-id="6f705-111">Entfernt "IpMask" vom "NetworkRuleSet" des angegebenen Namespaces.</span><span class="sxs-lookup"><span data-stu-id="6f705-111">Removes IpMask of the NetworkRuleSet of the given namespace</span></span>

## <span data-ttu-id="6f705-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6f705-112">PARAMETERS</span></span>

### <span data-ttu-id="6f705-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6f705-113">-AsJob</span></span>
<span data-ttu-id="6f705-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="6f705-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6f705-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f705-115">-DefaultProfile</span></span>
<span data-ttu-id="6f705-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6f705-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f705-117">-IpMask</span><span class="sxs-lookup"><span data-stu-id="6f705-117">-IpMask</span></span>
<span data-ttu-id="6f705-118">Subnetzressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="6f705-118">Subnet Resource ID</span></span>

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

### <span data-ttu-id="6f705-119">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="6f705-119">-IpRuleObject</span></span>
<span data-ttu-id="6f705-120">IPRule Configuration Object</span><span class="sxs-lookup"><span data-stu-id="6f705-120">IPRule Configuration Object</span></span>

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

### <span data-ttu-id="6f705-121">-Name</span><span class="sxs-lookup"><span data-stu-id="6f705-121">-Name</span></span>
<span data-ttu-id="6f705-122">Namespacename</span><span class="sxs-lookup"><span data-stu-id="6f705-122">Namespace Name</span></span>

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

### <span data-ttu-id="6f705-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6f705-123">-PassThru</span></span>
<span data-ttu-id="6f705-124">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="6f705-124">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="6f705-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f705-125">-ResourceGroupName</span></span>
<span data-ttu-id="6f705-126">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="6f705-126">Resource Group Name</span></span>

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

### <span data-ttu-id="6f705-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6f705-127">-Confirm</span></span>
<span data-ttu-id="6f705-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6f705-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f705-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="6f705-129">-WhatIf</span></span>
<span data-ttu-id="6f705-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6f705-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f705-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6f705-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f705-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f705-132">CommonParameters</span></span>
<span data-ttu-id="6f705-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f705-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="6f705-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f705-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f705-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6f705-135">INPUTS</span></span>

### <span data-ttu-id="6f705-136">System.String</span><span class="sxs-lookup"><span data-stu-id="6f705-136">System.String</span></span>

### <span data-ttu-id="6f705-137">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="6f705-137">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="6f705-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6f705-138">OUTPUTS</span></span>

### <span data-ttu-id="6f705-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="6f705-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="6f705-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6f705-140">NOTES</span></span>

## <span data-ttu-id="6f705-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6f705-141">RELATED LINKS</span></span>
