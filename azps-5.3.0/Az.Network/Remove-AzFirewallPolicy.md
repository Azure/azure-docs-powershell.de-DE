---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicy.md
ms.openlocfilehash: a6539d1569d3dc4f0d12190b6b1d0670b036c30a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468935"
---
# <span data-ttu-id="327db-101">Remove-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="327db-101">Remove-AzFirewallPolicy</span></span>

## <span data-ttu-id="327db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="327db-102">SYNOPSIS</span></span>
<span data-ttu-id="327db-103">Entfernt eine Azure-Firewall-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="327db-103">Removes an Azure Firewall Policy</span></span>

## <span data-ttu-id="327db-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="327db-104">SYNTAX</span></span>

### <span data-ttu-id="327db-105">RemoveByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="327db-105">RemoveByNameParameterSet</span></span>
```
Remove-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="327db-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="327db-106">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzFirewallPolicy [-Force] [-PassThru] [-AsJob] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="327db-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="327db-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzFirewallPolicy [-Force] [-PassThru] [-AsJob] -InputObject <PSAzureFirewallPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="327db-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="327db-108">DESCRIPTION</span></span>
<span data-ttu-id="327db-109">Das **Cmdlet "Remove-AzFirewallPolicy"** entfernt eine Azure-Firewallrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="327db-109">The **Remove-AzFirewallPolicy** cmdlet removes an Azure Firewall Policy.</span></span>

## <span data-ttu-id="327db-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="327db-110">EXAMPLES</span></span>

### <span data-ttu-id="327db-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="327db-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicy -Name firewallpolicy -ResourceGroupName TestRg
```

<span data-ttu-id="327db-112">In diesem Beispiel wird die Firewallrichtlinie mit dem Namen "firewallpolicy" in der Ressourcengruppe "TestRg" entfernt.</span><span class="sxs-lookup"><span data-stu-id="327db-112">This example removes the firewall policy named "firewallpolicy" in the resourcegroup "TestRg"</span></span>

### <span data-ttu-id="327db-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="327db-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicy -Name firewallpolicy -ResourceId "/subscriptions/12345/resourceGroups/TestRg/providers/Microsoft.Network/firewallpolicies/firewallPolicy1"
```

<span data-ttu-id="327db-114">In diesem Beispiel wird die Firewallrichtlinie durch die ID entfernt.</span><span class="sxs-lookup"><span data-stu-id="327db-114">This example removes the firewall policy by the Id.</span></span>

### <span data-ttu-id="327db-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="327db-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicy -InputObject $fp
```

<span data-ttu-id="327db-116">In diesem Beispiel wird die Firewallrichtlinie $fp</span><span class="sxs-lookup"><span data-stu-id="327db-116">This example removes the firewall policy $fp</span></span>

## <span data-ttu-id="327db-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="327db-117">PARAMETERS</span></span>

### <span data-ttu-id="327db-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="327db-118">-AsJob</span></span>
<span data-ttu-id="327db-119">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="327db-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="327db-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="327db-120">-DefaultProfile</span></span>
<span data-ttu-id="327db-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="327db-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="327db-122">-Force</span><span class="sxs-lookup"><span data-stu-id="327db-122">-Force</span></span>
<span data-ttu-id="327db-123">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="327db-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="327db-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="327db-124">-InputObject</span></span>
<span data-ttu-id="327db-125">Die AzureFirewall-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="327db-125">The AzureFirewall Policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="327db-126">-Name</span><span class="sxs-lookup"><span data-stu-id="327db-126">-Name</span></span>
<span data-ttu-id="327db-127">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="327db-127">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="327db-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="327db-128">-PassThru</span></span>
<span data-ttu-id="327db-129">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="327db-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="327db-130">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="327db-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="327db-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="327db-131">-ResourceGroupName</span></span>
<span data-ttu-id="327db-132">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="327db-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="327db-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="327db-133">-ResourceId</span></span>
<span data-ttu-id="327db-134">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="327db-134">The resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="327db-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="327db-135">-Confirm</span></span>
<span data-ttu-id="327db-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="327db-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="327db-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="327db-137">-WhatIf</span></span>
<span data-ttu-id="327db-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="327db-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="327db-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="327db-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="327db-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="327db-140">CommonParameters</span></span>
<span data-ttu-id="327db-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="327db-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="327db-142">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="327db-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="327db-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="327db-143">INPUTS</span></span>

### <span data-ttu-id="327db-144">System.String</span><span class="sxs-lookup"><span data-stu-id="327db-144">System.String</span></span>

### <span data-ttu-id="327db-145">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="327db-145">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

## <span data-ttu-id="327db-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="327db-146">OUTPUTS</span></span>

### <span data-ttu-id="327db-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="327db-147">System.Boolean</span></span>

## <span data-ttu-id="327db-148">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="327db-148">NOTES</span></span>

## <span data-ttu-id="327db-149">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="327db-149">RELATED LINKS</span></span>
