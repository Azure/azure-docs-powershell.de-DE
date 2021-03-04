---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/powershell/module/az.imagebuilder/remove-azimagebuildertemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Remove-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Remove-AzImageBuilderTemplate.md
ms.openlocfilehash: 3d22fa9626d7e0e6de8baf36a07ae679ffb9ed0a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101949123"
---
# <span data-ttu-id="88867-101">Remove-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="88867-101">Remove-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="88867-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88867-102">SYNOPSIS</span></span>
<span data-ttu-id="88867-103">Löschen einer Bildvorlage für einen virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="88867-103">Delete a virtual machine image template</span></span>

## <span data-ttu-id="88867-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="88867-104">SYNTAX</span></span>

### <span data-ttu-id="88867-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="88867-105">Delete (Default)</span></span>
```
Remove-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="88867-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="88867-106">DeleteViaIdentity</span></span>
```
Remove-AzImageBuilderTemplate -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="88867-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="88867-107">DESCRIPTION</span></span>
<span data-ttu-id="88867-108">Löschen einer Bildvorlage für einen virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="88867-108">Delete a virtual machine image template</span></span>

## <span data-ttu-id="88867-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="88867-109">EXAMPLES</span></span>

### <span data-ttu-id="88867-110">Beispiel 1: Entfernen einer Bildvorlage</span><span class="sxs-lookup"><span data-stu-id="88867-110">Example 1: Remove a image template</span></span>
```powershell
PS C:\> Remove-AzImageBuilderTemplate -ImageTemplateName template-name-dmt6ze -ResourceGroupName wyunchi-imagebuilder

```

<span data-ttu-id="88867-111">Mit diesem Befehl wird eine Bildvorlage entfernt.</span><span class="sxs-lookup"><span data-stu-id="88867-111">This command removes a image template.</span></span>

### <span data-ttu-id="88867-112">Beispiel 2: Entfernen einer Bildvorlage</span><span class="sxs-lookup"><span data-stu-id="88867-112">Example 2: Remove a image template</span></span>
```powershell
PS C:\> $template = Get-AzImageBuilderTemplate -ImageTemplateName template-name-3uo8p6 -ResourceGroupName wyunchi-imagebuilder
PS C:\> Remove-AzImageBuilderTemplate -InputObject $template

```

<span data-ttu-id="88867-113">Mit diesem Befehl wird eine Bildvorlage entfernt.</span><span class="sxs-lookup"><span data-stu-id="88867-113">This command removes a image template.</span></span>

## <span data-ttu-id="88867-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="88867-114">PARAMETERS</span></span>

### <span data-ttu-id="88867-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="88867-115">-AsJob</span></span>
<span data-ttu-id="88867-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="88867-116">Run the command as a job</span></span>

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

### <span data-ttu-id="88867-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88867-117">-DefaultProfile</span></span>
<span data-ttu-id="88867-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="88867-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88867-119">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="88867-119">-ImageTemplateName</span></span>
<span data-ttu-id="88867-120">Der Name der Bildvorlage</span><span class="sxs-lookup"><span data-stu-id="88867-120">The name of the image Template</span></span>

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

### <span data-ttu-id="88867-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="88867-121">-InputObject</span></span>
<span data-ttu-id="88867-122">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="88867-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="88867-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="88867-123">-NoWait</span></span>
<span data-ttu-id="88867-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="88867-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="88867-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="88867-125">-PassThru</span></span>
<span data-ttu-id="88867-126">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="88867-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="88867-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88867-127">-ResourceGroupName</span></span>
<span data-ttu-id="88867-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="88867-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="88867-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="88867-129">-SubscriptionId</span></span>
<span data-ttu-id="88867-130">Abonnementanmeldeinformationen, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="88867-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="88867-131">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="88867-131">The subscription Id forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="88867-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="88867-132">-Confirm</span></span>
<span data-ttu-id="88867-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="88867-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88867-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88867-134">-WhatIf</span></span>
<span data-ttu-id="88867-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="88867-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88867-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="88867-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88867-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88867-137">CommonParameters</span></span>
<span data-ttu-id="88867-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88867-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88867-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="88867-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88867-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="88867-140">INPUTS</span></span>

### <span data-ttu-id="88867-141">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="88867-141">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="88867-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="88867-142">OUTPUTS</span></span>

### <span data-ttu-id="88867-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="88867-143">System.Boolean</span></span>

## <span data-ttu-id="88867-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="88867-144">NOTES</span></span>

<span data-ttu-id="88867-145">ALIASE</span><span class="sxs-lookup"><span data-stu-id="88867-145">ALIASES</span></span>

<span data-ttu-id="88867-146">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="88867-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="88867-147">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="88867-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="88867-148">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="88867-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="88867-149">INPUTOBJECT <IImageBuilderIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="88867-149">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="88867-150">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="88867-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="88867-151">`[ImageTemplateName <String>]`: Der Name der Bildvorlage</span><span class="sxs-lookup"><span data-stu-id="88867-151">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="88867-152">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="88867-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="88867-153">`[RunOutputName <String>]`: Der Name der Ausführungsausgabe</span><span class="sxs-lookup"><span data-stu-id="88867-153">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="88867-154">`[SubscriptionId <String>]`: Abonnementanmeldeinformationen, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="88867-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="88867-155">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="88867-155">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="88867-156">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="88867-156">RELATED LINKS</span></span>

