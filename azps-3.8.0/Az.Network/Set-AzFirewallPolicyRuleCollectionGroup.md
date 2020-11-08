---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewallpolicyrulecollectiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicyRuleCollectionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicyRuleCollectionGroup.md
ms.openlocfilehash: 8e1260a636a1be5a42888fcc6cc12cb8b228859c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93997211"
---
# <span data-ttu-id="30055-101">Set-AzFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="30055-101">Set-AzFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="30055-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="30055-102">SYNOPSIS</span></span>
<span data-ttu-id="30055-103">speichert eine geänderte Azure Firewall-Richtlinienregel Sammlungs Gruppe</span><span class="sxs-lookup"><span data-stu-id="30055-103">saves a modified azure firewall policy rule collection group</span></span>

## <span data-ttu-id="30055-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="30055-104">SYNTAX</span></span>

### <span data-ttu-id="30055-105">SetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="30055-105">SetByNameParameterSet</span></span>
```
Set-AzFirewallPolicyRuleCollectionGroup -Name <String> -ResourceGroupName <String> -FirewallPolicyName <String>
 -Priority <UInt32> -RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30055-106">SetByParentInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="30055-106">SetByParentInputObjectParameterSet</span></span>
```
Set-AzFirewallPolicyRuleCollectionGroup -Name <String> -FirewallPolicyObject <PSAzureFirewallPolicy>
 -Priority <UInt32> -RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30055-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="30055-107">SetByInputObjectParameterSet</span></span>
```
Set-AzFirewallPolicyRuleCollectionGroup -InputObject <PSAzureFirewallPolicyRuleCollectionGroupWrapper>
 [-Priority <UInt32>] [-RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30055-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="30055-108">SetByResourceIdParameterSet</span></span>
```
Set-AzFirewallPolicyRuleCollectionGroup -ResourceId <String> -Priority <UInt32>
 -RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30055-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="30055-109">DESCRIPTION</span></span>
<span data-ttu-id="30055-110">Das Cmdlet " **Satz-AzFirewallPolicyRuleCollectionGroup** " aktualisiert eine Regel Sammlungs Gruppe in einer Azure Firewall-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="30055-110">The **Set-AzFirewallPolicyRuleCollectionGroup** cmdlet updates a rule collection groups in an Azure Firewall Policy.</span></span>

## <span data-ttu-id="30055-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="30055-111">EXAMPLES</span></span>

### <span data-ttu-id="30055-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="30055-112">Example 1</span></span>
```powershell
PS C:\> Set-AzFirewallPolicyRuleCollectionGroup -Name rg1 -ResourceGroupName TestRg -Priority 200 -RuleCollection $filterRule1 -AzureFirewallPolicy $fp
```

<span data-ttu-id="30055-113">In diesem Beispiel wird eine Regel Sammlungs Gruppe in der Firewall-Richtlinie aktualisiert $FP</span><span class="sxs-lookup"><span data-stu-id="30055-113">This example updates a rule collection group in the firewall policy $fp</span></span>

## <span data-ttu-id="30055-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="30055-114">PARAMETERS</span></span>

### <span data-ttu-id="30055-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30055-115">-DefaultProfile</span></span>
<span data-ttu-id="30055-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="30055-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30055-117">-FirewallPolicyName</span><span class="sxs-lookup"><span data-stu-id="30055-117">-FirewallPolicyName</span></span>
<span data-ttu-id="30055-118">Der Name der Firewall-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="30055-118">The name of the firewall policy</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30055-119">-FirewallPolicyObject</span><span class="sxs-lookup"><span data-stu-id="30055-119">-FirewallPolicyObject</span></span>
<span data-ttu-id="30055-120">Firewall-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="30055-120">Firewall Policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy
Parameter Sets: SetByParentInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30055-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="30055-121">-InputObject</span></span>
<span data-ttu-id="30055-122">Die Liste der Regeln</span><span class="sxs-lookup"><span data-stu-id="30055-122">The list of rules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroupWrapper
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30055-123">-Name</span><span class="sxs-lookup"><span data-stu-id="30055-123">-Name</span></span>
<span data-ttu-id="30055-124">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="30055-124">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByParentInputObjectParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30055-125">-Priorität</span><span class="sxs-lookup"><span data-stu-id="30055-125">-Priority</span></span>
<span data-ttu-id="30055-126">Die Priorität der Regelgruppe</span><span class="sxs-lookup"><span data-stu-id="30055-126">The priority of the rule group</span></span>

```yaml
Type: System.UInt32
Parameter Sets: SetByNameParameterSet, SetByParentInputObjectParameterSet, SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.UInt32
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30055-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30055-127">-ResourceGroupName</span></span>
<span data-ttu-id="30055-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="30055-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30055-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="30055-129">-ResourceId</span></span>
<span data-ttu-id="30055-130">Die Ressourcen-ID der Regel Sammlungs Gruppe</span><span class="sxs-lookup"><span data-stu-id="30055-130">The resource Id of the Rule collection groupy</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30055-131">-Rulecollection</span><span class="sxs-lookup"><span data-stu-id="30055-131">-RuleCollection</span></span>
<span data-ttu-id="30055-132">Die Liste der Regelsammlungen</span><span class="sxs-lookup"><span data-stu-id="30055-132">The list of rule collections</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyBaseRuleCollection[]
Parameter Sets: SetByNameParameterSet, SetByParentInputObjectParameterSet, SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyBaseRuleCollection[]
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30055-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="30055-133">-Confirm</span></span>
<span data-ttu-id="30055-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="30055-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30055-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30055-135">-WhatIf</span></span>
<span data-ttu-id="30055-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="30055-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30055-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="30055-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30055-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30055-138">CommonParameters</span></span>
<span data-ttu-id="30055-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30055-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30055-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="30055-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30055-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="30055-141">INPUTS</span></span>

### <span data-ttu-id="30055-142">System. String</span><span class="sxs-lookup"><span data-stu-id="30055-142">System.String</span></span>

### <span data-ttu-id="30055-143">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="30055-143">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

## <span data-ttu-id="30055-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="30055-144">OUTPUTS</span></span>

### <span data-ttu-id="30055-145">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="30055-145">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="30055-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="30055-146">NOTES</span></span>

## <span data-ttu-id="30055-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="30055-147">RELATED LINKS</span></span>
