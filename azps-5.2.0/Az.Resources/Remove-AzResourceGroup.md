---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 880D321E-30F2-4CAE-B14A-5F6DD8E1DB99
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroup.md
ms.openlocfilehash: e53e5311b4553dc3803a4a6d9ac31d6a2569bbc0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98291275"
---
# <span data-ttu-id="9f916-101">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9f916-101">Remove-AzResourceGroup</span></span>

## <span data-ttu-id="9f916-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f916-102">SYNOPSIS</span></span>
<span data-ttu-id="9f916-103">Entfernt eine Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9f916-103">Removes a resource group.</span></span>

## <span data-ttu-id="9f916-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9f916-104">SYNTAX</span></span>

### <span data-ttu-id="9f916-105">RemoveByResourceGroupName (Standard)</span><span class="sxs-lookup"><span data-stu-id="9f916-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzResourceGroup [-Name] <String> [-Force] [-AsJob] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f916-106">RemoveByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="9f916-106">RemoveByResourceGroupId</span></span>
```
Remove-AzResourceGroup -Id <String> [-Force] [-AsJob] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f916-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9f916-107">DESCRIPTION</span></span>
<span data-ttu-id="9f916-108">Das **Cmdlet "Remove-AzResourceGroup"** entfernt eine Azure-Ressourcengruppe und deren Ressourcen aus dem aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9f916-108">The **Remove-AzResourceGroup** cmdlet removes an Azure resource group and its resources from the current subscription.</span></span>
<span data-ttu-id="9f916-109">Wenn Sie eine Ressource löschen, aber die Ressourcengruppe verlassen möchten, verwenden Sie Remove-AzResource-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f916-109">To delete a resource, but leave the resource group, use the Remove-AzResource cmdlet.</span></span>

## <span data-ttu-id="9f916-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9f916-110">EXAMPLES</span></span>

### <span data-ttu-id="9f916-111">Beispiel 1: Entfernen einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="9f916-111">Example 1: Remove a resource group</span></span>
```
PS C:\>Remove-AzResourceGroup -Name "ContosoRG01"
```

<span data-ttu-id="9f916-112">Mit diesem Befehl wird die Ressourcengruppe "ContosoRG01" aus dem Abonnement entfernt.</span><span class="sxs-lookup"><span data-stu-id="9f916-112">This command removes the ContosoRG01 resource group from the subscription.</span></span>
<span data-ttu-id="9f916-113">Das Cmdlet fordert Sie zur Bestätigung auf und gibt keine Ausgabe zurück.</span><span class="sxs-lookup"><span data-stu-id="9f916-113">The cmdlet prompts you for confirmation and returns no output.</span></span>

### <span data-ttu-id="9f916-114">Beispiel 2: Entfernen einer Ressourcengruppe ohne Bestätigung</span><span class="sxs-lookup"><span data-stu-id="9f916-114">Example 2: Remove a resource group without confirmation</span></span>
```
PS C:\>Get-AzResourceGroup -Name "ContosoRG01" | Remove-AzResourceGroup -Force
```

<span data-ttu-id="9f916-115">Dieser Befehl verwendet das cmdlet Get-AzResourceGroup, um die Ressourcengruppe "ContosoRG01" zu erhalten, und übergibt ihn dann mithilfe des Pipelineoperators an **"Remove-AzResourceGroup".**</span><span class="sxs-lookup"><span data-stu-id="9f916-115">This command uses the Get-AzResourceGroup cmdlet to get the resource group ContosoRG01, and then passes it to **Remove-AzResourceGroup** by using the pipeline operator.</span></span> <span data-ttu-id="9f916-116">Der *Parameter "Force"* unterdrückt die Bestätigungsaufforderung.</span><span class="sxs-lookup"><span data-stu-id="9f916-116">The *Force* parameter suppresses the confirmation prompt.</span></span>

### <span data-ttu-id="9f916-117">Beispiel 3: Entfernen aller Ressourcengruppen</span><span class="sxs-lookup"><span data-stu-id="9f916-117">Example 3: Remove all resource groups</span></span>
```
PS C:\>Get-AzResourceGroup | Remove-AzResourceGroup
```

<span data-ttu-id="9f916-118">Dieser Befehl verwendet das **Cmdlet "Get-AzResourceGroup",** um alle Ressourcengruppen zu erhalten, und übergibt sie dann mithilfe des Pipelineoperators an **"Remove-AzResourceGroup".**</span><span class="sxs-lookup"><span data-stu-id="9f916-118">This command uses the **Get-AzResourceGroup** cmdlet to get all resource groups, and then passes them to **Remove-AzResourceGroup** by using the pipeline operator.</span></span>

## <span data-ttu-id="9f916-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9f916-119">PARAMETERS</span></span>

### <span data-ttu-id="9f916-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9f916-120">-ApiVersion</span></span>
<span data-ttu-id="9f916-121">Gibt die vom Ressourcenanbieter unterstützte API-Version an.</span><span class="sxs-lookup"><span data-stu-id="9f916-121">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="9f916-122">Sie können eine andere Version als die Standardversion angeben.</span><span class="sxs-lookup"><span data-stu-id="9f916-122">You can specify a different version than the default version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f916-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9f916-123">-AsJob</span></span>
<span data-ttu-id="9f916-124">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="9f916-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9f916-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f916-125">-DefaultProfile</span></span>
<span data-ttu-id="9f916-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="9f916-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9f916-127">-Force</span><span class="sxs-lookup"><span data-stu-id="9f916-127">-Force</span></span>
<span data-ttu-id="9f916-128">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="9f916-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9f916-129">-ID</span><span class="sxs-lookup"><span data-stu-id="9f916-129">-Id</span></span>
<span data-ttu-id="9f916-130">Gibt die ID der zu entfernenden Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="9f916-130">Specifies the ID of resource group to remove.</span></span>
<span data-ttu-id="9f916-131">Platzhalterzeichen sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="9f916-131">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f916-132">-Name</span><span class="sxs-lookup"><span data-stu-id="9f916-132">-Name</span></span>
<span data-ttu-id="9f916-133">Gibt die Namen der zu entfernenden Ressourcengruppen an.</span><span class="sxs-lookup"><span data-stu-id="9f916-133">Specifies the names of resource groups to remove.</span></span>
<span data-ttu-id="9f916-134">Platzhalterzeichen sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="9f916-134">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupName
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f916-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="9f916-135">-Pre</span></span>
<span data-ttu-id="9f916-136">Gibt an, dass dieses Cmdlet Vorabversions-API-Versionen berücksichtigt, wenn automatisch bestimmt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9f916-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="9f916-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9f916-137">-Confirm</span></span>
<span data-ttu-id="9f916-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9f916-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f916-139">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="9f916-139">-WhatIf</span></span>
<span data-ttu-id="9f916-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9f916-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f916-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9f916-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f916-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f916-142">CommonParameters</span></span>
<span data-ttu-id="9f916-143">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f916-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f916-144">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9f916-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f916-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9f916-145">INPUTS</span></span>

### <span data-ttu-id="9f916-146">System.String</span><span class="sxs-lookup"><span data-stu-id="9f916-146">System.String</span></span>

## <span data-ttu-id="9f916-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9f916-147">OUTPUTS</span></span>

### <span data-ttu-id="9f916-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9f916-148">System.Boolean</span></span>

## <span data-ttu-id="9f916-149">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9f916-149">NOTES</span></span>

## <span data-ttu-id="9f916-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9f916-150">RELATED LINKS</span></span>

[<span data-ttu-id="9f916-151">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9f916-151">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="9f916-152">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9f916-152">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="9f916-153">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9f916-153">Set-AzResourceGroup</span></span>](./Set-AzResourceGroup.md)


