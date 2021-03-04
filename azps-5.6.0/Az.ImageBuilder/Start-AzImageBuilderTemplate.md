---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/powershell/module/az.imagebuilder/start-azimagebuildertemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Start-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Start-AzImageBuilderTemplate.md
ms.openlocfilehash: 75065d50b8176b256c5cf91c136f4f4588232e55
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924947"
---
# <span data-ttu-id="55eab-101">Start-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="55eab-101">Start-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="55eab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55eab-102">SYNOPSIS</span></span>
<span data-ttu-id="55eab-103">Erstellen von Artefakten aus einer vorhandenen Bildvorlage</span><span class="sxs-lookup"><span data-stu-id="55eab-103">Create artifacts from a existing image template</span></span>

## <span data-ttu-id="55eab-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="55eab-104">SYNTAX</span></span>

### <span data-ttu-id="55eab-105">Ausführen (Standard)</span><span class="sxs-lookup"><span data-stu-id="55eab-105">Run (Default)</span></span>
```
Start-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="55eab-106">RunViaIdentity</span><span class="sxs-lookup"><span data-stu-id="55eab-106">RunViaIdentity</span></span>
```
Start-AzImageBuilderTemplate -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="55eab-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="55eab-107">DESCRIPTION</span></span>
<span data-ttu-id="55eab-108">Erstellen von Artefakten aus einer vorhandenen Bildvorlage</span><span class="sxs-lookup"><span data-stu-id="55eab-108">Create artifacts from a existing image template</span></span>

## <span data-ttu-id="55eab-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="55eab-109">EXAMPLES</span></span>

### <span data-ttu-id="55eab-110">Beispiel 1: Starten einer Bildvorlage</span><span class="sxs-lookup"><span data-stu-id="55eab-110">Example 1: Start an image template</span></span>
```powershell
PS C:\> Start-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -Name template-name-sn78hg

```

<span data-ttu-id="55eab-111">Mit diesem Befehl wird eine Bildvorlage gestartet.</span><span class="sxs-lookup"><span data-stu-id="55eab-111">This command starts an image template.</span></span>

### <span data-ttu-id="55eab-112">Beispiel 2: Starten einer Bildvorlage</span><span class="sxs-lookup"><span data-stu-id="55eab-112">Example 2: Start an image template</span></span>
```powershell
PS C:\> $template = Get-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -Name template-name-sn78hg
PS C:\> Start-AzImageBuilderTemplate -InputObject $template

```

<span data-ttu-id="55eab-113">Mit diesem Befehl wird eine Bildvorlage gestartet.</span><span class="sxs-lookup"><span data-stu-id="55eab-113">This command starts an image template.</span></span>

## <span data-ttu-id="55eab-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="55eab-114">PARAMETERS</span></span>

### <span data-ttu-id="55eab-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="55eab-115">-AsJob</span></span>
<span data-ttu-id="55eab-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="55eab-116">Run the command as a job</span></span>

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

### <span data-ttu-id="55eab-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55eab-117">-DefaultProfile</span></span>
<span data-ttu-id="55eab-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="55eab-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55eab-119">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="55eab-119">-ImageTemplateName</span></span>
<span data-ttu-id="55eab-120">Der Name der Bildvorlage</span><span class="sxs-lookup"><span data-stu-id="55eab-120">The name of the image Template</span></span>

```yaml
Type: System.String
Parameter Sets: Run
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55eab-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="55eab-121">-InputObject</span></span>
<span data-ttu-id="55eab-122">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="55eab-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity
Parameter Sets: RunViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55eab-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="55eab-123">-NoWait</span></span>
<span data-ttu-id="55eab-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="55eab-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="55eab-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="55eab-125">-PassThru</span></span>
<span data-ttu-id="55eab-126">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="55eab-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="55eab-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55eab-127">-ResourceGroupName</span></span>
<span data-ttu-id="55eab-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="55eab-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Run
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55eab-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="55eab-129">-SubscriptionId</span></span>
<span data-ttu-id="55eab-130">Abonnementanmeldeinformationen, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="55eab-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="55eab-131">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="55eab-131">The subscription Id forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Run
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55eab-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="55eab-132">-Confirm</span></span>
<span data-ttu-id="55eab-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="55eab-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55eab-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55eab-134">-WhatIf</span></span>
<span data-ttu-id="55eab-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="55eab-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55eab-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="55eab-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55eab-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55eab-137">CommonParameters</span></span>
<span data-ttu-id="55eab-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55eab-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55eab-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="55eab-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55eab-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="55eab-140">INPUTS</span></span>

### <span data-ttu-id="55eab-141">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="55eab-141">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="55eab-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="55eab-142">OUTPUTS</span></span>

### <span data-ttu-id="55eab-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="55eab-143">System.Boolean</span></span>

## <span data-ttu-id="55eab-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="55eab-144">NOTES</span></span>

<span data-ttu-id="55eab-145">ALIASE</span><span class="sxs-lookup"><span data-stu-id="55eab-145">ALIASES</span></span>

<span data-ttu-id="55eab-146">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="55eab-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="55eab-147">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="55eab-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="55eab-148">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="55eab-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="55eab-149">INPUTOBJECT <IImageBuilderIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="55eab-149">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="55eab-150">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="55eab-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="55eab-151">`[ImageTemplateName <String>]`: Der Name der Bildvorlage</span><span class="sxs-lookup"><span data-stu-id="55eab-151">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="55eab-152">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="55eab-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="55eab-153">`[RunOutputName <String>]`: Der Name der Ausführungsausgabe</span><span class="sxs-lookup"><span data-stu-id="55eab-153">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="55eab-154">`[SubscriptionId <String>]`: Abonnementanmeldeinformationen, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="55eab-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="55eab-155">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="55eab-155">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="55eab-156">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="55eab-156">RELATED LINKS</span></span>

