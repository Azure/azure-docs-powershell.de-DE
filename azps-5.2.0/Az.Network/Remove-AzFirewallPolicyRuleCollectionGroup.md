---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azfirewallpolicyrulecollectiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicyRuleCollectionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicyRuleCollectionGroup.md
ms.openlocfilehash: 3c9b307b34d07ff6c9331dc8d72c1149c83ef374
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363528"
---
# <span data-ttu-id="e0b91-101">Remove-AzFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="e0b91-101">Remove-AzFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="e0b91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0b91-102">SYNOPSIS</span></span>
<span data-ttu-id="e0b91-103">Entfernt eine Gruppe der Azure-Firewallrichtlinien-Regelsammlung in einer Azure-Firewallrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="e0b91-103">Removes a Azure Firewall Policy Rule Collection Group in a Azure firewall policy</span></span>

## <span data-ttu-id="e0b91-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e0b91-104">SYNTAX</span></span>

### <span data-ttu-id="e0b91-105">RemoveByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e0b91-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -Name <String> -ResourceGroupName <String>
 -AzureFirewallPolicyName <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0b91-106">RemoveByParentInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0b91-106">RemoveByParentInputObjectParameterSet</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -Name <String> -FirewallPolicyObject <PSAzureFirewallPolicy>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e0b91-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0b91-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -InputObject <PSAzureFirewallPolicyRuleCollectionGroupWrapper>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e0b91-108">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0b91-108">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0b91-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e0b91-109">DESCRIPTION</span></span>
<span data-ttu-id="e0b91-110">Das **Cmdlet "Remove-AzFirewallPolicyRuleCollectionGroup"** entfernt eine Regelsammlungsgruppe aus einer Azure-Firewallrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="e0b91-110">The **Remove-AzFirewallPolicyRuleCollectionGroup** cmdlet removes a rule collection group from an Azure Firewall Policy.</span></span>

## <span data-ttu-id="e0b91-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e0b91-111">EXAMPLES</span></span>

### <span data-ttu-id="e0b91-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e0b91-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicyRuleCollectionGroup -Name testRcGroup -FirewallPolicyObject $fp
```

<span data-ttu-id="e0b91-113">In diesem Beispiel wird die Spaltengruppe für Firewallrichtlinienregeln mit dem Namen "testRcGroup" im Firewallrichtlinienobjekt $fp</span><span class="sxs-lookup"><span data-stu-id="e0b91-113">This example removes the firewall policy rule colelction group named "testRcGroup" in the firewall policy object $fp</span></span>

### <span data-ttu-id="e0b91-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e0b91-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicyRuleCollectionGroup -Name testRcGroup -ResourceGroupName testRg -AzureFirewallPolicyName fpName 
```

<span data-ttu-id="e0b91-115">In diesem Beispiel wird die Spaltengruppe für Firewallrichtlinienregeln mit dem Namen "testRcGroup" in der Firewall mit dem Namen "fpName" frpm der Ressourcengruppennamen "testRg" entfernt.</span><span class="sxs-lookup"><span data-stu-id="e0b91-115">This example removes the firewall policy rule colelction group named "testRcGroup" in the firewall named "fpName" frpm the resourcegroup names "testRg"</span></span>

## <span data-ttu-id="e0b91-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0b91-116">PARAMETERS</span></span>

### <span data-ttu-id="e0b91-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e0b91-117">-AsJob</span></span>
<span data-ttu-id="e0b91-118">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="e0b91-118">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0b91-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0b91-119">-DefaultProfile</span></span>
<span data-ttu-id="e0b91-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e0b91-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0b91-121">-AzureFirewallPolicyName</span><span class="sxs-lookup"><span data-stu-id="e0b91-121">-AzureFirewallPolicyName</span></span>
<span data-ttu-id="e0b91-122">Der Name der Firewallrichtlinie</span><span class="sxs-lookup"><span data-stu-id="e0b91-122">The name of the firewall policy</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0b91-123">-FirewallPolicyObject</span><span class="sxs-lookup"><span data-stu-id="e0b91-123">-FirewallPolicyObject</span></span>
<span data-ttu-id="e0b91-124">Firewallrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="e0b91-124">Firewall Policy.</span></span>

```yaml
Type: PSAzureFirewallPolicy
Parameter Sets: RemoveByParentInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0b91-125">-Force</span><span class="sxs-lookup"><span data-stu-id="e0b91-125">-Force</span></span>
<span data-ttu-id="e0b91-126">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="e0b91-126">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0b91-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e0b91-127">-InputObject</span></span>
<span data-ttu-id="e0b91-128">Gruppenobjekt "Firewallrichtlinienregel"</span><span class="sxs-lookup"><span data-stu-id="e0b91-128">Firewall Policy Rule collection group object</span></span>

```yaml
Type: PSAzureFirewallPolicyRuleCollectionGroupWrapper
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0b91-129">-Name</span><span class="sxs-lookup"><span data-stu-id="e0b91-129">-Name</span></span>
<span data-ttu-id="e0b91-130">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="e0b91-130">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: RemoveByParentInputObjectParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0b91-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e0b91-131">-PassThru</span></span>
<span data-ttu-id="e0b91-132">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="e0b91-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e0b91-133">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="e0b91-133">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0b91-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0b91-134">-ResourceGroupName</span></span>
<span data-ttu-id="e0b91-135">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e0b91-135">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0b91-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e0b91-136">-ResourceId</span></span>
<span data-ttu-id="e0b91-137">Die Ressourcen-ID der Gruppe 'Regelsammlung'</span><span class="sxs-lookup"><span data-stu-id="e0b91-137">The resource Id of the Rule collection groupy</span></span>

```yaml
Type: String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0b91-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e0b91-138">-Confirm</span></span>
<span data-ttu-id="e0b91-139">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e0b91-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0b91-140">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="e0b91-140">-WhatIf</span></span>
<span data-ttu-id="e0b91-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e0b91-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0b91-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e0b91-142">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0b91-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0b91-143">CommonParameters</span></span>
<span data-ttu-id="e0b91-144">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0b91-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0b91-145">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e0b91-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0b91-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e0b91-146">INPUTS</span></span>

### <span data-ttu-id="e0b91-147">System.String</span><span class="sxs-lookup"><span data-stu-id="e0b91-147">System.String</span></span>

### <span data-ttu-id="e0b91-148">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="e0b91-148">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

### <span data-ttu-id="e0b91-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroupWrapper</span><span class="sxs-lookup"><span data-stu-id="e0b91-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroupWrapper</span></span>

## <span data-ttu-id="e0b91-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e0b91-150">OUTPUTS</span></span>

### <span data-ttu-id="e0b91-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e0b91-151">System.Boolean</span></span>

## <span data-ttu-id="e0b91-152">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e0b91-152">NOTES</span></span>

## <span data-ttu-id="e0b91-153">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e0b91-153">RELATED LINKS</span></span>
