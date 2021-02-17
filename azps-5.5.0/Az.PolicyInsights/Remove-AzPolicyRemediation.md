---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/remove-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Remove-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Remove-AzPolicyRemediation.md
ms.openlocfilehash: 969b764be302231f33dda00b32afb79ec04a324e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100172259"
---
# <span data-ttu-id="308e3-101">Remove-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="308e3-101">Remove-AzPolicyRemediation</span></span>

## <span data-ttu-id="308e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="308e3-102">SYNOPSIS</span></span>
<span data-ttu-id="308e3-103">Löscht eine Richtlinienbehebung.</span><span class="sxs-lookup"><span data-stu-id="308e3-103">Deletes a policy remediation.</span></span>

## <span data-ttu-id="308e3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="308e3-104">SYNTAX</span></span>

### <span data-ttu-id="308e3-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="308e3-105">ByName (Default)</span></span>
```
Remove-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-AllowStop] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="308e3-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="308e3-106">ByResourceId</span></span>
```
Remove-AzPolicyRemediation -ResourceId <String> [-AllowStop] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="308e3-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="308e3-107">ByInputObject</span></span>
```
Remove-AzPolicyRemediation -InputObject <PSRemediation> [-AllowStop] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="308e3-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="308e3-108">DESCRIPTION</span></span>
<span data-ttu-id="308e3-109">Das **Cmdlet "Remove-AzPolicyRemediation"** löscht eine Richtlinienbehebung.</span><span class="sxs-lookup"><span data-stu-id="308e3-109">The **Remove-AzPolicyRemediation** cmdlet deletes a policy remediation.</span></span>

## <span data-ttu-id="308e3-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="308e3-110">EXAMPLES</span></span>

### <span data-ttu-id="308e3-111">Beispiel 1: Löschen einer Richtlinienbereinigung im Bereich "Ressourcengruppe"</span><span class="sxs-lookup"><span data-stu-id="308e3-111">Example 1: Delete a policy remediation at resource group scope</span></span>
```
PS C:\> Remove-AzPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1"
```

<span data-ttu-id="308e3-112">Mit diesem Befehl wird die Wartung mit dem Namen "remediation1" in der Ressourcengruppe "myRG" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="308e3-112">This command deletes the remediation named 'remediation1' in resource group 'myRG'.</span></span>

### <span data-ttu-id="308e3-113">Beispiel 2: Löschen einer Wartung einer Verwaltungsgruppe über Piping</span><span class="sxs-lookup"><span data-stu-id="308e3-113">Example 2: Delete a management group remediation via piping</span></span>
```
PS C:\> $remediation = Get-AzPolicyRemediation -ManagementGroupName "mg1" -Name "remediation1"
PS C:\> $remediation | Remove-AzPolicyRemediation -Confirm
```

<span data-ttu-id="308e3-114">Mit diesem Befehl wird die Wartung namens "remediation1" aus der Verwaltungsgruppe "mg1" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="308e3-114">This command deletes the remediation named 'remediation1' from management group 'mg1'.</span></span> <span data-ttu-id="308e3-115">Vor dem Löschen der Ressource wird eine Bestätigungsaufforderung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="308e3-115">A confirmation prompt will be presented before deleting the resource.</span></span>

### <span data-ttu-id="308e3-116">Beispiel 3: Abbrechen und Löschen einer Richtlinienbehebung</span><span class="sxs-lookup"><span data-stu-id="308e3-116">Example 3: Cancel and delete a policy remediation</span></span>
```
PS C:\> Remove-AzPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1" -AllowStop
```

<span data-ttu-id="308e3-117">Mit diesem Befehl wird die Wartung mit dem Namen "remediation1" in der Ressourcengruppe "myRG" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="308e3-117">This command deletes the remediation named 'remediation1' in resource group 'myRG'.</span></span> <span data-ttu-id="308e3-118">Wenn die Wartung gerade ausgeführt wird, wird sie vor dem Löschen abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="308e3-118">If the remediation is in-progress it will be canceled before being deleted.</span></span>

## <span data-ttu-id="308e3-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="308e3-119">PARAMETERS</span></span>

### <span data-ttu-id="308e3-120">-AllowStop</span><span class="sxs-lookup"><span data-stu-id="308e3-120">-AllowStop</span></span>
<span data-ttu-id="308e3-121">Lassen Sie zu, dass die Wartung abgebrochen wird, wenn sie ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="308e3-121">Allow the remediation to be canceled if it is in-progress.</span></span>

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

### <span data-ttu-id="308e3-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="308e3-122">-AsJob</span></span>
<span data-ttu-id="308e3-123">Führen Sie das Cmdlet im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="308e3-123">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="308e3-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="308e3-124">-DefaultProfile</span></span>
<span data-ttu-id="308e3-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="308e3-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="308e3-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="308e3-126">-InputObject</span></span>
<span data-ttu-id="308e3-127">Das Problembehebungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="308e3-127">The Remediation object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="308e3-128">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="308e3-128">-ManagementGroupName</span></span>
<span data-ttu-id="308e3-129">ID der Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="308e3-129">Management group ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="308e3-130">-Name</span><span class="sxs-lookup"><span data-stu-id="308e3-130">-Name</span></span>
<span data-ttu-id="308e3-131">Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="308e3-131">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="308e3-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="308e3-132">-PassThru</span></span>
<span data-ttu-id="308e3-133">Gibt "True" zurück, wenn der Befehl erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="308e3-133">Return True if the command completes successfully.</span></span>

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

### <span data-ttu-id="308e3-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="308e3-134">-ResourceGroupName</span></span>
<span data-ttu-id="308e3-135">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="308e3-135">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="308e3-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="308e3-136">-ResourceId</span></span>
<span data-ttu-id="308e3-137">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="308e3-137">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="308e3-138">-Scope</span><span class="sxs-lookup"><span data-stu-id="308e3-138">-Scope</span></span>
<span data-ttu-id="308e3-139">Umfang der Ressource.</span><span class="sxs-lookup"><span data-stu-id="308e3-139">Scope of the resource.</span></span>
<span data-ttu-id="308e3-140">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="308e3-140">E.g.</span></span>
<span data-ttu-id="308e3-141">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="308e3-141">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="308e3-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="308e3-142">-Confirm</span></span>
<span data-ttu-id="308e3-143">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="308e3-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="308e3-144">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="308e3-144">-WhatIf</span></span>
<span data-ttu-id="308e3-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="308e3-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="308e3-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="308e3-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="308e3-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="308e3-147">CommonParameters</span></span>
<span data-ttu-id="308e3-148">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="308e3-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="308e3-149">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="308e3-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="308e3-150">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="308e3-150">INPUTS</span></span>

### <span data-ttu-id="308e3-151">System.String</span><span class="sxs-lookup"><span data-stu-id="308e3-151">System.String</span></span>

### <span data-ttu-id="308e3-152">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span><span class="sxs-lookup"><span data-stu-id="308e3-152">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="308e3-153">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="308e3-153">OUTPUTS</span></span>

### <span data-ttu-id="308e3-154">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="308e3-154">System.Boolean</span></span>

## <span data-ttu-id="308e3-155">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="308e3-155">NOTES</span></span>

## <span data-ttu-id="308e3-156">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="308e3-156">RELATED LINKS</span></span>
