---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/stop-azimagebuildertemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Stop-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Stop-AzImageBuilderTemplate.md
ms.openlocfilehash: 01fd95dd41a7ee76c06f0423d33c4aba34329c18
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98297268"
---
# <span data-ttu-id="4ac15-101">Stop-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="4ac15-101">Stop-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="4ac15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ac15-102">SYNOPSIS</span></span>
<span data-ttu-id="4ac15-103">Abbrechen des langfristigen Bildaufbaus basierend auf der Bildvorlage</span><span class="sxs-lookup"><span data-stu-id="4ac15-103">Cancel the long running image build based on the image template</span></span>

## <span data-ttu-id="4ac15-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4ac15-104">SYNTAX</span></span>

### <span data-ttu-id="4ac15-105">Abbrechen (Standard)</span><span class="sxs-lookup"><span data-stu-id="4ac15-105">Cancel (Default)</span></span>
```
Stop-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4ac15-106">CancelViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4ac15-106">CancelViaIdentity</span></span>
```
Stop-AzImageBuilderTemplate -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4ac15-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4ac15-107">DESCRIPTION</span></span>
<span data-ttu-id="4ac15-108">Abbrechen des langfristigen Bildaufbaus basierend auf der Bildvorlage</span><span class="sxs-lookup"><span data-stu-id="4ac15-108">Cancel the long running image build based on the image template</span></span>

## <span data-ttu-id="4ac15-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4ac15-109">EXAMPLES</span></span>

### <span data-ttu-id="4ac15-110">Beispiel 1: Beenden der Erstellung von Bildvorlagen</span><span class="sxs-lookup"><span data-stu-id="4ac15-110">Example 1: Stop image template creation</span></span>
```powershell
PS C:\> Start-AzImageBuilderTemplate -ImageTemplateName template-name-sn78hg -ResourceGroupName wyunchi-imagebuilder -AsJob 

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Start-AzImageB…                 Running       True            localhost            Start-AzImageBuilderTemp…

PS C:\> Stop-AzImageBuilderTemplate -ImageTemplateName template-name-sn78hg -ResourceGroupName wyunchi-imagebuilder

```

<span data-ttu-id="4ac15-111">Mit diesem Befehl wird die Erstellung von Bildvorlagen beendet.</span><span class="sxs-lookup"><span data-stu-id="4ac15-111">This command stops image template creation.</span></span>

### <span data-ttu-id="4ac15-112">Beispiel 2: Beenden der Erstellung von Bildvorlagen</span><span class="sxs-lookup"><span data-stu-id="4ac15-112">Example 2: Stop image template creation</span></span>
```powershell
PS C:\> Start-AzImageBuilderTemplate -ImageTemplateName template-name-sn78hg -ResourceGroupName wyunchi-imagebuilder -AsJob 

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
2      Start-AzImageB…                 Running       True            localhost            Start-AzImageBuilderTemp…

PS C:\> $template = Get-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -Name template-name-sn78hg
PS C:\> Stop-AzImageBuilderTemplate -InputObject $template 

```

<span data-ttu-id="4ac15-113">Mit diesem Befehl wird die Erstellung von Bildvorlagen beendet.</span><span class="sxs-lookup"><span data-stu-id="4ac15-113">This command stops image template creation.</span></span>

## <span data-ttu-id="4ac15-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4ac15-114">PARAMETERS</span></span>

### <span data-ttu-id="4ac15-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4ac15-115">-AsJob</span></span>
<span data-ttu-id="4ac15-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="4ac15-116">Run the command as a job</span></span>

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

### <span data-ttu-id="4ac15-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ac15-117">-DefaultProfile</span></span>
<span data-ttu-id="4ac15-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4ac15-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ac15-119">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="4ac15-119">-ImageTemplateName</span></span>
<span data-ttu-id="4ac15-120">Der Name der Bildvorlage</span><span class="sxs-lookup"><span data-stu-id="4ac15-120">The name of the image Template</span></span>

```yaml
Type: System.String
Parameter Sets: Cancel
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ac15-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4ac15-121">-InputObject</span></span>
<span data-ttu-id="4ac15-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="4ac15-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity
Parameter Sets: CancelViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ac15-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="4ac15-123">-NoWait</span></span>
<span data-ttu-id="4ac15-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="4ac15-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4ac15-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4ac15-125">-PassThru</span></span>
<span data-ttu-id="4ac15-126">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="4ac15-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="4ac15-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ac15-127">-ResourceGroupName</span></span>
<span data-ttu-id="4ac15-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4ac15-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Cancel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ac15-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4ac15-129">-SubscriptionId</span></span>
<span data-ttu-id="4ac15-130">Abonnementanmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="4ac15-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="4ac15-131">Die Abonnement-ID ist teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="4ac15-131">The subscription Id forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Cancel
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ac15-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4ac15-132">-Confirm</span></span>
<span data-ttu-id="4ac15-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4ac15-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ac15-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4ac15-134">-WhatIf</span></span>
<span data-ttu-id="4ac15-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4ac15-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ac15-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4ac15-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ac15-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ac15-137">CommonParameters</span></span>
<span data-ttu-id="4ac15-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ac15-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ac15-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4ac15-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ac15-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4ac15-140">INPUTS</span></span>

### <span data-ttu-id="4ac15-141">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="4ac15-141">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="4ac15-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4ac15-142">OUTPUTS</span></span>

### <span data-ttu-id="4ac15-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4ac15-143">System.Boolean</span></span>

## <span data-ttu-id="4ac15-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4ac15-144">NOTES</span></span>

<span data-ttu-id="4ac15-145">ALIASE</span><span class="sxs-lookup"><span data-stu-id="4ac15-145">ALIASES</span></span>

<span data-ttu-id="4ac15-146">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="4ac15-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4ac15-147">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4ac15-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4ac15-148">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4ac15-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4ac15-149">INPUTOBJECT <IImageBuilderIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="4ac15-149">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4ac15-150">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="4ac15-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4ac15-151">`[ImageTemplateName <String>]`: Der Name der Bildvorlage</span><span class="sxs-lookup"><span data-stu-id="4ac15-151">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="4ac15-152">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4ac15-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="4ac15-153">`[RunOutputName <String>]`: Der Name der Ausgabe der Ausführung</span><span class="sxs-lookup"><span data-stu-id="4ac15-153">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="4ac15-154">`[SubscriptionId <String>]`: Abonnementanmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="4ac15-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="4ac15-155">Die Abonnement-ID ist teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="4ac15-155">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="4ac15-156">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4ac15-156">RELATED LINKS</span></span>

