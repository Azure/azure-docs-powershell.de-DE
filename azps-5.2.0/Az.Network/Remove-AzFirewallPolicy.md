---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicy.md
ms.openlocfilehash: a6539d1569d3dc4f0d12190b6b1d0670b036c30a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358181"
---
# <span data-ttu-id="f0b8e-101">Remove-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="f0b8e-101">Remove-AzFirewallPolicy</span></span>

## <span data-ttu-id="f0b8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0b8e-102">SYNOPSIS</span></span>
<span data-ttu-id="f0b8e-103">Entfernt eine Azure-Firewall-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="f0b8e-103">Removes an Azure Firewall Policy</span></span>

## <span data-ttu-id="f0b8e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f0b8e-104">SYNTAX</span></span>

### <span data-ttu-id="f0b8e-105">RemoveByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0b8e-105">RemoveByNameParameterSet</span></span>
```
Remove-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0b8e-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0b8e-106">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzFirewallPolicy [-Force] [-PassThru] [-AsJob] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0b8e-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0b8e-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzFirewallPolicy [-Force] [-PassThru] [-AsJob] -InputObject <PSAzureFirewallPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0b8e-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f0b8e-108">DESCRIPTION</span></span>
<span data-ttu-id="f0b8e-109">Das **Cmdlet "Remove-AzFirewallPolicy"** entfernt eine Azure-Firewallrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="f0b8e-109">The **Remove-AzFirewallPolicy** cmdlet removes an Azure Firewall Policy.</span></span>

## <span data-ttu-id="f0b8e-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f0b8e-110">EXAMPLES</span></span>

### <span data-ttu-id="f0b8e-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f0b8e-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicy -Name firewallpolicy -ResourceGroupName TestRg
```

<span data-ttu-id="f0b8e-112">In diesem Beispiel wird die Firewallrichtlinie mit dem Namen "firewallpolicy" in der Ressourcengruppe "TestRg" entfernt.</span><span class="sxs-lookup"><span data-stu-id="f0b8e-112">This example removes the firewall policy named "firewallpolicy" in the resourcegroup "TestRg"</span></span>

### <span data-ttu-id="f0b8e-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="f0b8e-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicy -Name firewallpolicy -ResourceId "/subscriptions/12345/resourceGroups/TestRg/providers/Microsoft.Network/firewallpolicies/firewallPolicy1"
```

<span data-ttu-id="f0b8e-114">In diesem Beispiel wird die Firewallrichtlinie durch die ID entfernt.</span><span class="sxs-lookup"><span data-stu-id="f0b8e-114">This example removes the firewall policy by the Id.</span></span>

### <span data-ttu-id="f0b8e-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="f0b8e-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicy -InputObject $fp
```

<span data-ttu-id="f0b8e-116">In diesem Beispiel wird die Firewallrichtlinie $fp</span><span class="sxs-lookup"><span data-stu-id="f0b8e-116">This example removes the firewall policy $fp</span></span>

## <span data-ttu-id="f0b8e-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f0b8e-117">PARAMETERS</span></span>

### <span data-ttu-id="f0b8e-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f0b8e-118">-AsJob</span></span>
<span data-ttu-id="f0b8e-119">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="f0b8e-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f0b8e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0b8e-120">-DefaultProfile</span></span>
<span data-ttu-id="f0b8e-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f0b8e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0b8e-122">-Force</span><span class="sxs-lookup"><span data-stu-id="f0b8e-122">-Force</span></span>
<span data-ttu-id="f0b8e-123">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="f0b8e-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f0b8e-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f0b8e-124">-InputObject</span></span>
<span data-ttu-id="f0b8e-125">Die AzureFirewall-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="f0b8e-125">The AzureFirewall Policy</span></span>

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

### <span data-ttu-id="f0b8e-126">-Name</span><span class="sxs-lookup"><span data-stu-id="f0b8e-126">-Name</span></span>
<span data-ttu-id="f0b8e-127">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="f0b8e-127">The resource name.</span></span>

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

### <span data-ttu-id="f0b8e-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f0b8e-128">-PassThru</span></span>
<span data-ttu-id="f0b8e-129">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="f0b8e-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f0b8e-130">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="f0b8e-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f0b8e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0b8e-131">-ResourceGroupName</span></span>
<span data-ttu-id="f0b8e-132">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f0b8e-132">The resource group name.</span></span>

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

### <span data-ttu-id="f0b8e-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f0b8e-133">-ResourceId</span></span>
<span data-ttu-id="f0b8e-134">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="f0b8e-134">The resource Id.</span></span>

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

### <span data-ttu-id="f0b8e-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f0b8e-135">-Confirm</span></span>
<span data-ttu-id="f0b8e-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f0b8e-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0b8e-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f0b8e-137">-WhatIf</span></span>
<span data-ttu-id="f0b8e-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f0b8e-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0b8e-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f0b8e-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0b8e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0b8e-140">CommonParameters</span></span>
<span data-ttu-id="f0b8e-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0b8e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0b8e-142">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f0b8e-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0b8e-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f0b8e-143">INPUTS</span></span>

### <span data-ttu-id="f0b8e-144">System.String</span><span class="sxs-lookup"><span data-stu-id="f0b8e-144">System.String</span></span>

### <span data-ttu-id="f0b8e-145">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="f0b8e-145">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

## <span data-ttu-id="f0b8e-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f0b8e-146">OUTPUTS</span></span>

### <span data-ttu-id="f0b8e-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f0b8e-147">System.Boolean</span></span>

## <span data-ttu-id="f0b8e-148">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f0b8e-148">NOTES</span></span>

## <span data-ttu-id="f0b8e-149">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f0b8e-149">RELATED LINKS</span></span>
