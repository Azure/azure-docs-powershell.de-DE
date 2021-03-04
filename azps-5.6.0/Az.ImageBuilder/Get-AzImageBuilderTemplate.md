---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/powershell/module/az.imagebuilder/get-azimagebuildertemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderTemplate.md
ms.openlocfilehash: 82730525f6330336be72e922881d743345515926
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101949147"
---
# <span data-ttu-id="bdf5d-101">Get-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="bdf5d-101">Get-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="bdf5d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bdf5d-102">SYNOPSIS</span></span>
<span data-ttu-id="bdf5d-103">Informationen zu einer Bildvorlage für einen virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="bdf5d-103">Get information about a virtual machine image template</span></span>

## <span data-ttu-id="bdf5d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bdf5d-104">SYNTAX</span></span>

### <span data-ttu-id="bdf5d-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="bdf5d-105">List (Default)</span></span>
```
Get-AzImageBuilderTemplate [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="bdf5d-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="bdf5d-106">Get</span></span>
```
Get-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="bdf5d-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="bdf5d-107">GetViaIdentity</span></span>
```
Get-AzImageBuilderTemplate -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="bdf5d-108">Liste1</span><span class="sxs-lookup"><span data-stu-id="bdf5d-108">List1</span></span>
```
Get-AzImageBuilderTemplate -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="bdf5d-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bdf5d-109">DESCRIPTION</span></span>
<span data-ttu-id="bdf5d-110">Informationen zu einer Bildvorlage für einen virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="bdf5d-110">Get information about a virtual machine image template</span></span>

## <span data-ttu-id="bdf5d-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bdf5d-111">EXAMPLES</span></span>

### <span data-ttu-id="bdf5d-112">Beispiel 1: Auflisten aller Vorlagen unter einem Abonnement</span><span class="sxs-lookup"><span data-stu-id="bdf5d-112">Example 1: List all template under a subscription</span></span>
```powershell
PS C:\> Get-AzImageBuilderTemplate

Location Name                      Type
-------- ----                      ----
eastus   HelloImageTemplateLinux01 Microsoft.VirtualMachineImages/imageTemplates
eastus   lucas-imagetemplate       Microsoft.VirtualMachineImages/imageTemplates
eastus   test-imagebuilder         Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="bdf5d-113">Mit diesem Befehl werden alle Vorlagen unter einem Abonnement aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="bdf5d-113">This command lists all template under a subscription.</span></span>

### <span data-ttu-id="bdf5d-114">Beispiel 2: Auflisten aller Vorlagen unter einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="bdf5d-114">Example 2: List all template under a resource group</span></span>
```powershell
PS C:\> Get-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder

Location Name                       Type
-------- ----                       ----
eastus   HelloImageTemplateLinux01  Microsoft.VirtualMachineImages/imageTemplates
eastus   template-name-ax01b7       Microsoft.VirtualMachineImages/imageTemplates
eastus   template-name-ep5z7v       Microsoft.VirtualMachineImages/imageTemplates
eastus   template-name-klcuav       Microsoft.VirtualMachineImages/imageTemplates
eastus   template-name-u7gjqx       Microsoft.VirtualMachineImages/imageTemplates
eastus   test-imagebuilder          Microsoft.VirtualMachineImages/imageTemplates
eastus   tmpl-managedimg-managedimg Microsoft.VirtualMachineImages/imageTemplates
eastus   tmpl-platform-managed      Microsoft.VirtualMachineImages/imageTemplates
eastus   tmpl-shareimg-managedimg   Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="bdf5d-115">Mit diesem Befehl werden alle Vorlagen unter einer Ressourcengruppe aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="bdf5d-115">This command lists all template under a resource group.</span></span>

### <span data-ttu-id="bdf5d-116">Beispiel 3: Erhalten einer Vorlage unter einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="bdf5d-116">Example 3: Get a template under a resource group</span></span>
```powershell
PS C:\> Get-AzImageBuilderTemplate -ImageTemplateName lucas-imagetemplate -ResourceGroupName wyunchi-imagebuilder

Location Name                Type
-------- ----                ----
eastus   lucas-imagetemplate Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="bdf5d-117">Dieser Befehl ruft eine Vorlage unter einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="bdf5d-117">This command gets a template under a resource group.</span></span>

### <span data-ttu-id="bdf5d-118">Beispiel 4: Erhalten einer Vorlage unter einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="bdf5d-118">Example 4: Get a template under a resource group</span></span>
```powershell
PS C:\> $template = Get-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -ImageTemplateName template-name-ep5z7v
PS C:\> Get-AzImageBuilderTemplate -InputObject $template

Location Name                 Type
-------- ----                 ----
eastus   template-name-ep5z7v Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="bdf5d-119">Dieser Befehl ruft eine Vorlage unter einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="bdf5d-119">This command gets a template under a resource group.</span></span>

## <span data-ttu-id="bdf5d-120">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="bdf5d-120">PARAMETERS</span></span>

### <span data-ttu-id="bdf5d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdf5d-121">-DefaultProfile</span></span>
<span data-ttu-id="bdf5d-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bdf5d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bdf5d-123">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="bdf5d-123">-ImageTemplateName</span></span>
<span data-ttu-id="bdf5d-124">Der Name der Bildvorlage</span><span class="sxs-lookup"><span data-stu-id="bdf5d-124">The name of the image Template</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdf5d-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bdf5d-125">-InputObject</span></span>
<span data-ttu-id="bdf5d-126">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="bdf5d-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="bdf5d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdf5d-127">-ResourceGroupName</span></span>
<span data-ttu-id="bdf5d-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="bdf5d-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdf5d-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bdf5d-129">-SubscriptionId</span></span>
<span data-ttu-id="bdf5d-130">Abonnementanmeldeinformationen, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="bdf5d-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="bdf5d-131">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="bdf5d-131">The subscription Id forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdf5d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdf5d-132">CommonParameters</span></span>
<span data-ttu-id="bdf5d-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdf5d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdf5d-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bdf5d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdf5d-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bdf5d-135">INPUTS</span></span>

### <span data-ttu-id="bdf5d-136">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="bdf5d-136">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="bdf5d-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bdf5d-137">OUTPUTS</span></span>

### <span data-ttu-id="bdf5d-138">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplate</span><span class="sxs-lookup"><span data-stu-id="bdf5d-138">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplate</span></span>

## <span data-ttu-id="bdf5d-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="bdf5d-139">NOTES</span></span>

<span data-ttu-id="bdf5d-140">ALIASE</span><span class="sxs-lookup"><span data-stu-id="bdf5d-140">ALIASES</span></span>

<span data-ttu-id="bdf5d-141">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="bdf5d-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bdf5d-142">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="bdf5d-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bdf5d-143">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bdf5d-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bdf5d-144">INPUTOBJECT <IImageBuilderIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="bdf5d-144">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bdf5d-145">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="bdf5d-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bdf5d-146">`[ImageTemplateName <String>]`: Der Name der Bildvorlage</span><span class="sxs-lookup"><span data-stu-id="bdf5d-146">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="bdf5d-147">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="bdf5d-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="bdf5d-148">`[RunOutputName <String>]`: Der Name der Ausführungsausgabe</span><span class="sxs-lookup"><span data-stu-id="bdf5d-148">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="bdf5d-149">`[SubscriptionId <String>]`: Abonnementanmeldeinformationen, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="bdf5d-149">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="bdf5d-150">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="bdf5d-150">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="bdf5d-151">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="bdf5d-151">RELATED LINKS</span></span>

