---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/get-azimagebuilderrunoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderRunOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderRunOutput.md
ms.openlocfilehash: 4cc45f3b4cd21e41f1b2e410dd2b76b9571a4431
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100159684"
---
# <span data-ttu-id="9c16c-101">Get-AzImageBuilderRunOutput</span><span class="sxs-lookup"><span data-stu-id="9c16c-101">Get-AzImageBuilderRunOutput</span></span>

## <span data-ttu-id="9c16c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c16c-102">SYNOPSIS</span></span>
<span data-ttu-id="9c16c-103">Get the specified run output for the specified image template resource</span><span class="sxs-lookup"><span data-stu-id="9c16c-103">Get the specified run output for the specified image template resource</span></span>

## <span data-ttu-id="9c16c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9c16c-104">SYNTAX</span></span>

### <span data-ttu-id="9c16c-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="9c16c-105">List (Default)</span></span>
```
Get-AzImageBuilderRunOutput -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9c16c-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="9c16c-106">Get</span></span>
```
Get-AzImageBuilderRunOutput -ImageTemplateName <String> -ResourceGroupName <String> -RunOutputName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9c16c-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9c16c-107">GetViaIdentity</span></span>
```
Get-AzImageBuilderRunOutput -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="9c16c-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9c16c-108">DESCRIPTION</span></span>
<span data-ttu-id="9c16c-109">Get the specified run output for the specified image template resource</span><span class="sxs-lookup"><span data-stu-id="9c16c-109">Get the specified run output for the specified image template resource</span></span>

## <span data-ttu-id="9c16c-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9c16c-110">EXAMPLES</span></span>

### <span data-ttu-id="9c16c-111">Beispiel 1: Auflisten aller ausgeführten Ergebnisse unter einer Vorlage</span><span class="sxs-lookup"><span data-stu-id="9c16c-111">Example 1: List all run results under a template</span></span>
```powershell
PS C:\> Get-AzImageBuilderRunOutput -ImageTemplateName lucas-imagetemplate -ResourceGroupName wyunchi-imagebuilder

Name          Type
----          ----
image_lucas_1 Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="9c16c-112">Mit diesem Befehl werden alle ergebnisse der Ausführung unter einer Vorlage aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="9c16c-112">This command lists all run results under a template.</span></span>

### <span data-ttu-id="9c16c-113">Beispiel 2: Erhalten eines Ausführungsergebniss unter einer Vorlage</span><span class="sxs-lookup"><span data-stu-id="9c16c-113">Example 2: Get a run result under a template</span></span>
```powershell
PS C:\> Get-AzImageBuilderRunOutput -ImageTemplateName template-name-u7gjqx -ResourceGroupName wyunchi-imagebuilder -RunOutputName runout-template-name-u7gjqx 

Name                        Type
----                        ----
runout-template-name-u7gjqx Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="9c16c-114">Dieser Befehl ruft ein Ausführungsergebnis unter einer Vorlage ab.</span><span class="sxs-lookup"><span data-stu-id="9c16c-114">This command gets a run result under a template.</span></span>

### <span data-ttu-id="9c16c-115">Beispiel 3: Erhalten eines Ausführungsergebniss unter einer Vorlage</span><span class="sxs-lookup"><span data-stu-id="9c16c-115">Example 3: Get a run result under a template</span></span>
```powershell
PS C:\> $result = Get-AzImageBuilderRunOutput -ImageTemplateName template-name-u7gjqx -ResourceGroupName wyunchi-imagebuilder -RunOutputName runout-template-name-u7gjqx
PS C:\> Get-AzImageBuilderRunOutput -InputObject $result

Name                        Type
----                        ----
runout-template-name-u7gjqx Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="9c16c-116">Dieser Befehl ruft ein Ausführungsergebnis unter einer Vorlage ab.</span><span class="sxs-lookup"><span data-stu-id="9c16c-116">This command gets a run result under a template.</span></span>

## <span data-ttu-id="9c16c-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9c16c-117">PARAMETERS</span></span>

### <span data-ttu-id="9c16c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c16c-118">-DefaultProfile</span></span>
<span data-ttu-id="9c16c-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9c16c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c16c-120">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="9c16c-120">-ImageTemplateName</span></span>
<span data-ttu-id="9c16c-121">Der Name der Bildvorlage</span><span class="sxs-lookup"><span data-stu-id="9c16c-121">The name of the image Template</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c16c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9c16c-122">-InputObject</span></span>
<span data-ttu-id="9c16c-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="9c16c-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c16c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c16c-124">-ResourceGroupName</span></span>
<span data-ttu-id="9c16c-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9c16c-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c16c-126">-RunOutputName</span><span class="sxs-lookup"><span data-stu-id="9c16c-126">-RunOutputName</span></span>
<span data-ttu-id="9c16c-127">Der Name der Ausgabe der Ausführung</span><span class="sxs-lookup"><span data-stu-id="9c16c-127">The name of the run output</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c16c-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9c16c-128">-SubscriptionId</span></span>
<span data-ttu-id="9c16c-129">Abonnementanmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="9c16c-129">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="9c16c-130">Die Abonnement-ID ist teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="9c16c-130">The subscription Id forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c16c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c16c-131">CommonParameters</span></span>
<span data-ttu-id="9c16c-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c16c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c16c-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9c16c-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c16c-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9c16c-134">INPUTS</span></span>

### <span data-ttu-id="9c16c-135">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="9c16c-135">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="9c16c-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9c16c-136">OUTPUTS</span></span>

### <span data-ttu-id="9c16c-137">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IRunOutput</span><span class="sxs-lookup"><span data-stu-id="9c16c-137">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IRunOutput</span></span>

## <span data-ttu-id="9c16c-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9c16c-138">NOTES</span></span>

<span data-ttu-id="9c16c-139">ALIASE</span><span class="sxs-lookup"><span data-stu-id="9c16c-139">ALIASES</span></span>

<span data-ttu-id="9c16c-140">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="9c16c-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9c16c-141">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9c16c-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9c16c-142">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9c16c-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9c16c-143">INPUTOBJECT <IImageBuilderIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="9c16c-143">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9c16c-144">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="9c16c-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9c16c-145">`[ImageTemplateName <String>]`: Der Name der Bildvorlage</span><span class="sxs-lookup"><span data-stu-id="9c16c-145">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="9c16c-146">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9c16c-146">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="9c16c-147">`[RunOutputName <String>]`: Der Name der Ausgabe der Ausführung</span><span class="sxs-lookup"><span data-stu-id="9c16c-147">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="9c16c-148">`[SubscriptionId <String>]`: Abonnementanmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="9c16c-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="9c16c-149">Die Abonnement-ID ist teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="9c16c-149">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="9c16c-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9c16c-150">RELATED LINKS</span></span>

