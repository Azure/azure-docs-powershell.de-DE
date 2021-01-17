---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azfirewallpolicyrulecollectiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicyRuleCollectionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicyRuleCollectionGroup.md
ms.openlocfilehash: 3c9b307b34d07ff6c9331dc8d72c1149c83ef374
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468936"
---
# <span data-ttu-id="37a8b-101">Remove-AzFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="37a8b-101">Remove-AzFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="37a8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37a8b-102">SYNOPSIS</span></span>
<span data-ttu-id="37a8b-103">Entfernt eine Gruppe der Azure-Firewallrichtlinien-Regelsammlung in einer Azure-Firewallrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="37a8b-103">Removes a Azure Firewall Policy Rule Collection Group in a Azure firewall policy</span></span>

## <span data-ttu-id="37a8b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="37a8b-104">SYNTAX</span></span>

### <span data-ttu-id="37a8b-105">RemoveByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="37a8b-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -Name <String> -ResourceGroupName <String>
 -AzureFirewallPolicyName <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37a8b-106">RemoveByParentInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="37a8b-106">RemoveByParentInputObjectParameterSet</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -Name <String> -FirewallPolicyObject <PSAzureFirewallPolicy>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="37a8b-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="37a8b-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -InputObject <PSAzureFirewallPolicyRuleCollectionGroupWrapper>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="37a8b-108">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="37a8b-108">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37a8b-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="37a8b-109">DESCRIPTION</span></span>
<span data-ttu-id="37a8b-110">Das **Cmdlet "Remove-AzFirewallPolicyRuleCollectionGroup"** entfernt eine Regelsammlungsgruppe aus einer Azure-Firewallrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="37a8b-110">The **Remove-AzFirewallPolicyRuleCollectionGroup** cmdlet removes a rule collection group from an Azure Firewall Policy.</span></span>

## <span data-ttu-id="37a8b-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="37a8b-111">EXAMPLES</span></span>

### <span data-ttu-id="37a8b-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="37a8b-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicyRuleCollectionGroup -Name testRcGroup -FirewallPolicyObject $fp
```

<span data-ttu-id="37a8b-113">In diesem Beispiel wird die Spaltengruppe für Firewallrichtlinienregeln mit dem Namen "testRcGroup" im Firewallrichtlinienobjekt $fp</span><span class="sxs-lookup"><span data-stu-id="37a8b-113">This example removes the firewall policy rule colelction group named "testRcGroup" in the firewall policy object $fp</span></span>

### <span data-ttu-id="37a8b-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="37a8b-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicyRuleCollectionGroup -Name testRcGroup -ResourceGroupName testRg -AzureFirewallPolicyName fpName 
```

<span data-ttu-id="37a8b-115">In diesem Beispiel wird die Gruppe der Spaltenregeln der Firewallrichtlinie mit dem Namen "testRcGroup" in der Firewall mit dem Namen "fpName" frpm der Ressourcengruppennamen "testRg" entfernt.</span><span class="sxs-lookup"><span data-stu-id="37a8b-115">This example removes the firewall policy rule colelction group named "testRcGroup" in the firewall named "fpName" frpm the resourcegroup names "testRg"</span></span>

## <span data-ttu-id="37a8b-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="37a8b-116">PARAMETERS</span></span>

### <span data-ttu-id="37a8b-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="37a8b-117">-AsJob</span></span>
<span data-ttu-id="37a8b-118">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="37a8b-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="37a8b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37a8b-119">-DefaultProfile</span></span>
<span data-ttu-id="37a8b-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="37a8b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37a8b-121">-AzureFirewallPolicyName</span><span class="sxs-lookup"><span data-stu-id="37a8b-121">-AzureFirewallPolicyName</span></span>
<span data-ttu-id="37a8b-122">Der Name der Firewallrichtlinie</span><span class="sxs-lookup"><span data-stu-id="37a8b-122">The name of the firewall policy</span></span>

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

### <span data-ttu-id="37a8b-123">-FirewallPolicyObject</span><span class="sxs-lookup"><span data-stu-id="37a8b-123">-FirewallPolicyObject</span></span>
<span data-ttu-id="37a8b-124">Firewallrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="37a8b-124">Firewall Policy.</span></span>

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

### <span data-ttu-id="37a8b-125">-Force</span><span class="sxs-lookup"><span data-stu-id="37a8b-125">-Force</span></span>
<span data-ttu-id="37a8b-126">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="37a8b-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="37a8b-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="37a8b-127">-InputObject</span></span>
<span data-ttu-id="37a8b-128">Gruppenobjekt "Firewallrichtlinienregelsammlung"</span><span class="sxs-lookup"><span data-stu-id="37a8b-128">Firewall Policy Rule collection group object</span></span>

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

### <span data-ttu-id="37a8b-129">-Name</span><span class="sxs-lookup"><span data-stu-id="37a8b-129">-Name</span></span>
<span data-ttu-id="37a8b-130">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="37a8b-130">The resource name.</span></span>

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

### <span data-ttu-id="37a8b-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="37a8b-131">-PassThru</span></span>
<span data-ttu-id="37a8b-132">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="37a8b-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="37a8b-133">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="37a8b-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="37a8b-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37a8b-134">-ResourceGroupName</span></span>
<span data-ttu-id="37a8b-135">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="37a8b-135">The resource group name.</span></span>

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

### <span data-ttu-id="37a8b-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="37a8b-136">-ResourceId</span></span>
<span data-ttu-id="37a8b-137">Die Ressourcen-ID der Gruppe 'Regelsammlung'</span><span class="sxs-lookup"><span data-stu-id="37a8b-137">The resource Id of the Rule collection groupy</span></span>

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

### <span data-ttu-id="37a8b-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="37a8b-138">-Confirm</span></span>
<span data-ttu-id="37a8b-139">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="37a8b-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37a8b-140">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="37a8b-140">-WhatIf</span></span>
<span data-ttu-id="37a8b-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="37a8b-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37a8b-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="37a8b-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37a8b-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37a8b-143">CommonParameters</span></span>
<span data-ttu-id="37a8b-144">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37a8b-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37a8b-145">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="37a8b-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37a8b-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="37a8b-146">INPUTS</span></span>

### <span data-ttu-id="37a8b-147">System.String</span><span class="sxs-lookup"><span data-stu-id="37a8b-147">System.String</span></span>

### <span data-ttu-id="37a8b-148">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="37a8b-148">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

### <span data-ttu-id="37a8b-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroupWrapper</span><span class="sxs-lookup"><span data-stu-id="37a8b-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroupWrapper</span></span>

## <span data-ttu-id="37a8b-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="37a8b-150">OUTPUTS</span></span>

### <span data-ttu-id="37a8b-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="37a8b-151">System.Boolean</span></span>

## <span data-ttu-id="37a8b-152">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="37a8b-152">NOTES</span></span>

## <span data-ttu-id="37a8b-153">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="37a8b-153">RELATED LINKS</span></span>
