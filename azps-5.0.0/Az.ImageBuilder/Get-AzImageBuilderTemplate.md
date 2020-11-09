---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/get-azimagebuildertemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderTemplate.md
ms.openlocfilehash: d159a59f6fb94523868b4aa6109553900f1b289d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296278"
---
# <span data-ttu-id="466dd-101">Get-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="466dd-101">Get-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="466dd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="466dd-102">SYNOPSIS</span></span>
<span data-ttu-id="466dd-103">Abrufen von Informationen zu einer Bildvorlage für einen virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="466dd-103">Get information about a virtual machine image template</span></span>

## <span data-ttu-id="466dd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="466dd-104">SYNTAX</span></span>

### <span data-ttu-id="466dd-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="466dd-105">List (Default)</span></span>
```
Get-AzImageBuilderTemplate [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="466dd-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="466dd-106">Get</span></span>
```
Get-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="466dd-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="466dd-107">GetViaIdentity</span></span>
```
Get-AzImageBuilderTemplate -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="466dd-108">List1</span><span class="sxs-lookup"><span data-stu-id="466dd-108">List1</span></span>
```
Get-AzImageBuilderTemplate -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="466dd-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="466dd-109">DESCRIPTION</span></span>
<span data-ttu-id="466dd-110">Abrufen von Informationen zu einer Bildvorlage für einen virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="466dd-110">Get information about a virtual machine image template</span></span>

## <span data-ttu-id="466dd-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="466dd-111">EXAMPLES</span></span>

### <span data-ttu-id="466dd-112">Beispiel 1: Auflisten aller Vorlagen unter einem Abonnement</span><span class="sxs-lookup"><span data-stu-id="466dd-112">Example 1: List all template under a subscription</span></span>
```powershell
PS C:\> Get-AzImageBuilderTemplate

Location Name                      Type
-------- ----                      ----
eastus   HelloImageTemplateLinux01 Microsoft.VirtualMachineImages/imageTemplates
eastus   lucas-imagetemplate       Microsoft.VirtualMachineImages/imageTemplates
eastus   test-imagebuilder         Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="466dd-113">Dieser Befehl listet alle Vorlagen unter einem Abonnement auf.</span><span class="sxs-lookup"><span data-stu-id="466dd-113">This command lists all template under a subscription.</span></span>

### <span data-ttu-id="466dd-114">Beispiel 2: Auflisten aller Vorlagen unter einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="466dd-114">Example 2: List all template under a resource group</span></span>
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

<span data-ttu-id="466dd-115">Dieser Befehl listet alle Vorlagen unter einer Ressourcengruppe auf.</span><span class="sxs-lookup"><span data-stu-id="466dd-115">This command lists all template under a resource group.</span></span>

### <span data-ttu-id="466dd-116">Beispiel 3: Abrufen einer Vorlage unter einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="466dd-116">Example 3: Get a template under a resource group</span></span>
```powershell
PS C:\> Get-AzImageBuilderTemplate -ImageTemplateName lucas-imagetemplate -ResourceGroupName wyunchi-imagebuilder

Location Name                Type
-------- ----                ----
eastus   lucas-imagetemplate Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="466dd-117">Dieser Befehl ruft eine Vorlage unter einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="466dd-117">This command gets a template under a resource group.</span></span>

### <span data-ttu-id="466dd-118">Beispiel 4: Abrufen einer Vorlage unter einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="466dd-118">Example 4: Get a template under a resource group</span></span>
```powershell
PS C:\> $template = Get-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -ImageTemplateName template-name-ep5z7v
PS C:\> Get-AzImageBuilderTemplate -InputObject $template

Location Name                 Type
-------- ----                 ----
eastus   template-name-ep5z7v Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="466dd-119">Dieser Befehl ruft eine Vorlage unter einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="466dd-119">This command gets a template under a resource group.</span></span>

## <span data-ttu-id="466dd-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="466dd-120">PARAMETERS</span></span>

### <span data-ttu-id="466dd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="466dd-121">-DefaultProfile</span></span>
<span data-ttu-id="466dd-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="466dd-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="466dd-123">-Imagetemplatename</span><span class="sxs-lookup"><span data-stu-id="466dd-123">-ImageTemplateName</span></span>
<span data-ttu-id="466dd-124">Der Name der Bildvorlage</span><span class="sxs-lookup"><span data-stu-id="466dd-124">The name of the image Template</span></span>

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

### <span data-ttu-id="466dd-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="466dd-125">-InputObject</span></span>
<span data-ttu-id="466dd-126">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="466dd-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="466dd-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="466dd-127">-ResourceGroupName</span></span>
<span data-ttu-id="466dd-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="466dd-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="466dd-129">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="466dd-129">-SubscriptionId</span></span>
<span data-ttu-id="466dd-130">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="466dd-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="466dd-131">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="466dd-131">The subscription Id forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="466dd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="466dd-132">CommonParameters</span></span>
<span data-ttu-id="466dd-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="466dd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="466dd-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="466dd-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="466dd-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="466dd-135">INPUTS</span></span>

### <span data-ttu-id="466dd-136">Microsoft. Azure. PowerShell. Cmdlets. ImageBuilder. Models. IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="466dd-136">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="466dd-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="466dd-137">OUTPUTS</span></span>

### <span data-ttu-id="466dd-138">Microsoft. Azure. PowerShell. Cmdlets. ImageBuilder. Models. Api20200214. IImageTemplate</span><span class="sxs-lookup"><span data-stu-id="466dd-138">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplate</span></span>

## <span data-ttu-id="466dd-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="466dd-139">NOTES</span></span>

<span data-ttu-id="466dd-140">Aliase</span><span class="sxs-lookup"><span data-stu-id="466dd-140">ALIASES</span></span>

<span data-ttu-id="466dd-141">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="466dd-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="466dd-142">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="466dd-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="466dd-143">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="466dd-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="466dd-144">Inputobject <IImageBuilderIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="466dd-144">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="466dd-145">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="466dd-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="466dd-146">`[ImageTemplateName <String>]`: Der Name der Bildvorlage</span><span class="sxs-lookup"><span data-stu-id="466dd-146">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="466dd-147">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="466dd-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="466dd-148">`[RunOutputName <String>]`: Der Name der Run-Ausgabe</span><span class="sxs-lookup"><span data-stu-id="466dd-148">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="466dd-149">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="466dd-149">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="466dd-150">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="466dd-150">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="466dd-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="466dd-151">RELATED LINKS</span></span>

