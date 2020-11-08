---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyrulecollectiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyRuleCollectionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyRuleCollectionGroup.md
ms.openlocfilehash: 1aeb93085fdf8fa362e38843deacdef6e07929d7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996514"
---
# <span data-ttu-id="8e5f4-101">New-AzFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="8e5f4-101">New-AzFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="8e5f4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8e5f4-102">SYNOPSIS</span></span>
<span data-ttu-id="8e5f4-103">Erstellen einer neuen Azure Firewall-Richtlinienregel Sammlungs Gruppe</span><span class="sxs-lookup"><span data-stu-id="8e5f4-103">Create a new Azure Firewall Policy Rule Collection Group</span></span>

## <span data-ttu-id="8e5f4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e5f4-104">SYNTAX</span></span>

### <span data-ttu-id="8e5f4-105">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e5f4-105">SetByInputObjectParameterSet</span></span>
```
New-AzFirewallPolicyRuleCollectionGroup -Name <String> -Priority <UInt32>
 -RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]> -ResourceGroupName <String>
 -FirewallPolicyObject <PSAzureFirewallPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8e5f4-106">SetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e5f4-106">SetByNameParameterSet</span></span>
```
New-AzFirewallPolicyRuleCollectionGroup -Name <String> -Priority <UInt32>
 -RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]> -ResourceGroupName <String>
 -FirewallPolicyName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8e5f4-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8e5f4-107">DESCRIPTION</span></span>
<span data-ttu-id="8e5f4-108">Das Cmdlet **New-AzFirewallPolicyRuleCollectionGroup** erstellt eine Regel Sammlungs Gruppe in einer Azure Firewall-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="8e5f4-108">The **New-AzFirewallPolicyRuleCollectionGroup** cmdlet creates a rule collection group in a Azure Firewall Policy.</span></span>

## <span data-ttu-id="8e5f4-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8e5f4-109">EXAMPLES</span></span>

### <span data-ttu-id="8e5f4-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8e5f4-110">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyRuleCollectionGroup -Name rg1 -ResourceGroupName TestRg -Location westus -Priority 200 -RuleCollection $filterRule1 -AzureFirewallPolicy $fp
```

<span data-ttu-id="8e5f4-111">In diesem Beispiel wird eine Regel Sammlungs Gruppe in der Firewall-Richtlinie erstellt $FP</span><span class="sxs-lookup"><span data-stu-id="8e5f4-111">This example creates a rule collection group in the firewall policy $fp</span></span>

## <span data-ttu-id="8e5f4-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="8e5f4-112">PARAMETERS</span></span>

### <span data-ttu-id="8e5f4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e5f4-113">-DefaultProfile</span></span>
<span data-ttu-id="8e5f4-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8e5f4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e5f4-115">-FirewallPolicyName</span><span class="sxs-lookup"><span data-stu-id="8e5f4-115">-FirewallPolicyName</span></span>
<span data-ttu-id="8e5f4-116">Der Name der Firewall-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="8e5f4-116">The name of the firewall policy</span></span>

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

### <span data-ttu-id="8e5f4-117">-FirewallPolicyObject</span><span class="sxs-lookup"><span data-stu-id="8e5f4-117">-FirewallPolicyObject</span></span>
<span data-ttu-id="8e5f4-118">Firewall-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="8e5f4-118">Firewall Policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e5f4-119">-Name</span><span class="sxs-lookup"><span data-stu-id="8e5f4-119">-Name</span></span>
<span data-ttu-id="8e5f4-120">Der Name der Regelgruppe</span><span class="sxs-lookup"><span data-stu-id="8e5f4-120">The name of the Rule Group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e5f4-121">-Priorität</span><span class="sxs-lookup"><span data-stu-id="8e5f4-121">-Priority</span></span>
<span data-ttu-id="8e5f4-122">Die Priorität der Regelgruppe</span><span class="sxs-lookup"><span data-stu-id="8e5f4-122">The priority of the rule group</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e5f4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e5f4-123">-ResourceGroupName</span></span>
<span data-ttu-id="8e5f4-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8e5f4-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e5f4-125">-Rulecollection</span><span class="sxs-lookup"><span data-stu-id="8e5f4-125">-RuleCollection</span></span>
<span data-ttu-id="8e5f4-126">Die Liste der Regeln</span><span class="sxs-lookup"><span data-stu-id="8e5f4-126">The list of rules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyBaseRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e5f4-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8e5f4-127">-Confirm</span></span>
<span data-ttu-id="8e5f4-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8e5f4-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e5f4-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e5f4-129">-WhatIf</span></span>
<span data-ttu-id="8e5f4-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8e5f4-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e5f4-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8e5f4-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e5f4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e5f4-132">CommonParameters</span></span>
<span data-ttu-id="8e5f4-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e5f4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e5f4-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8e5f4-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e5f4-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8e5f4-135">INPUTS</span></span>

### <span data-ttu-id="8e5f4-136">System. String</span><span class="sxs-lookup"><span data-stu-id="8e5f4-136">System.String</span></span>

### <span data-ttu-id="8e5f4-137">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="8e5f4-137">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

## <span data-ttu-id="8e5f4-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8e5f4-138">OUTPUTS</span></span>

### <span data-ttu-id="8e5f4-139">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="8e5f4-139">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="8e5f4-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="8e5f4-140">NOTES</span></span>

## <span data-ttu-id="8e5f4-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8e5f4-141">RELATED LINKS</span></span>
