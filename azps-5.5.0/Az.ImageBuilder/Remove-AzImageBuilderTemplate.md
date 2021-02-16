---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/remove-azimagebuildertemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Remove-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Remove-AzImageBuilderTemplate.md
ms.openlocfilehash: 998c4f05e8b6a03749a4872e3f4b069e29ef634d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100161572"
---
# <span data-ttu-id="88a59-101">Remove-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="88a59-101">Remove-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="88a59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88a59-102">SYNOPSIS</span></span>
<span data-ttu-id="88a59-103">Löschen einer Bildvorlage für einen virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="88a59-103">Delete a virtual machine image template</span></span>

## <span data-ttu-id="88a59-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="88a59-104">SYNTAX</span></span>

### <span data-ttu-id="88a59-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="88a59-105">Delete (Default)</span></span>
```
Remove-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="88a59-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="88a59-106">DeleteViaIdentity</span></span>
```
Remove-AzImageBuilderTemplate -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="88a59-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="88a59-107">DESCRIPTION</span></span>
<span data-ttu-id="88a59-108">Löschen einer Bildvorlage für einen virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="88a59-108">Delete a virtual machine image template</span></span>

## <span data-ttu-id="88a59-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="88a59-109">EXAMPLES</span></span>

### <span data-ttu-id="88a59-110">Beispiel 1: Entfernen einer Bildvorlage</span><span class="sxs-lookup"><span data-stu-id="88a59-110">Example 1: Remove a image template</span></span>
```powershell
PS C:\> Remove-AzImageBuilderTemplate -ImageTemplateName template-name-dmt6ze -ResourceGroupName wyunchi-imagebuilder

```

<span data-ttu-id="88a59-111">Mit diesem Befehl wird eine Bildvorlage entfernt.</span><span class="sxs-lookup"><span data-stu-id="88a59-111">This command removes a image template.</span></span>

### <span data-ttu-id="88a59-112">Beispiel 2: Entfernen einer Bildvorlage</span><span class="sxs-lookup"><span data-stu-id="88a59-112">Example 2: Remove a image template</span></span>
```powershell
PS C:\> $template = Get-AzImageBuilderTemplate -ImageTemplateName template-name-3uo8p6 -ResourceGroupName wyunchi-imagebuilder
PS C:\> Remove-AzImageBuilderTemplate -InputObject $template

```

<span data-ttu-id="88a59-113">Mit diesem Befehl wird eine Bildvorlage entfernt.</span><span class="sxs-lookup"><span data-stu-id="88a59-113">This command removes a image template.</span></span>

## <span data-ttu-id="88a59-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="88a59-114">PARAMETERS</span></span>

### <span data-ttu-id="88a59-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="88a59-115">-AsJob</span></span>
<span data-ttu-id="88a59-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="88a59-116">Run the command as a job</span></span>

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

### <span data-ttu-id="88a59-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88a59-117">-DefaultProfile</span></span>
<span data-ttu-id="88a59-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="88a59-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88a59-119">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="88a59-119">-ImageTemplateName</span></span>
<span data-ttu-id="88a59-120">Der Name der Bildvorlage</span><span class="sxs-lookup"><span data-stu-id="88a59-120">The name of the image Template</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88a59-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="88a59-121">-InputObject</span></span>
<span data-ttu-id="88a59-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="88a59-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88a59-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="88a59-123">-NoWait</span></span>
<span data-ttu-id="88a59-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="88a59-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="88a59-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="88a59-125">-PassThru</span></span>
<span data-ttu-id="88a59-126">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="88a59-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="88a59-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88a59-127">-ResourceGroupName</span></span>
<span data-ttu-id="88a59-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="88a59-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88a59-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="88a59-129">-SubscriptionId</span></span>
<span data-ttu-id="88a59-130">Abonnementanmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="88a59-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="88a59-131">Die Abonnement-ID ist teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="88a59-131">The subscription Id forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88a59-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="88a59-132">-Confirm</span></span>
<span data-ttu-id="88a59-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="88a59-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88a59-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="88a59-134">-WhatIf</span></span>
<span data-ttu-id="88a59-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="88a59-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88a59-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="88a59-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88a59-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88a59-137">CommonParameters</span></span>
<span data-ttu-id="88a59-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88a59-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88a59-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="88a59-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88a59-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="88a59-140">INPUTS</span></span>

### <span data-ttu-id="88a59-141">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="88a59-141">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="88a59-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="88a59-142">OUTPUTS</span></span>

### <span data-ttu-id="88a59-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="88a59-143">System.Boolean</span></span>

## <span data-ttu-id="88a59-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="88a59-144">NOTES</span></span>

<span data-ttu-id="88a59-145">ALIASE</span><span class="sxs-lookup"><span data-stu-id="88a59-145">ALIASES</span></span>

<span data-ttu-id="88a59-146">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="88a59-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="88a59-147">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="88a59-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="88a59-148">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="88a59-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="88a59-149">INPUTOBJECT <IImageBuilderIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="88a59-149">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="88a59-150">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="88a59-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="88a59-151">`[ImageTemplateName <String>]`: Der Name der Bildvorlage</span><span class="sxs-lookup"><span data-stu-id="88a59-151">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="88a59-152">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="88a59-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="88a59-153">`[RunOutputName <String>]`: Der Name der Ausgabe der Ausführung</span><span class="sxs-lookup"><span data-stu-id="88a59-153">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="88a59-154">`[SubscriptionId <String>]`: Abonnementanmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="88a59-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="88a59-155">Die Abonnement-ID ist teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="88a59-155">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="88a59-156">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="88a59-156">RELATED LINKS</span></span>

