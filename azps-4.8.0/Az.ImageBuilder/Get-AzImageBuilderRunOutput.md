---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/get-azimagebuilderrunoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderRunOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderRunOutput.md
ms.openlocfilehash: 4cc45f3b4cd21e41f1b2e410dd2b76b9571a4431
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173580"
---
# <span data-ttu-id="9fc98-101">Get-AzImageBuilderRunOutput</span><span class="sxs-lookup"><span data-stu-id="9fc98-101">Get-AzImageBuilderRunOutput</span></span>

## <span data-ttu-id="9fc98-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9fc98-102">SYNOPSIS</span></span>
<span data-ttu-id="9fc98-103">Abrufen der angegebenen Run-Ausgabe für die angegebene Bildvorlagen Ressource</span><span class="sxs-lookup"><span data-stu-id="9fc98-103">Get the specified run output for the specified image template resource</span></span>

## <span data-ttu-id="9fc98-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9fc98-104">SYNTAX</span></span>

### <span data-ttu-id="9fc98-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="9fc98-105">List (Default)</span></span>
```
Get-AzImageBuilderRunOutput -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9fc98-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="9fc98-106">Get</span></span>
```
Get-AzImageBuilderRunOutput -ImageTemplateName <String> -ResourceGroupName <String> -RunOutputName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9fc98-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9fc98-107">GetViaIdentity</span></span>
```
Get-AzImageBuilderRunOutput -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="9fc98-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9fc98-108">DESCRIPTION</span></span>
<span data-ttu-id="9fc98-109">Abrufen der angegebenen Run-Ausgabe für die angegebene Bildvorlagen Ressource</span><span class="sxs-lookup"><span data-stu-id="9fc98-109">Get the specified run output for the specified image template resource</span></span>

## <span data-ttu-id="9fc98-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9fc98-110">EXAMPLES</span></span>

### <span data-ttu-id="9fc98-111">Beispiel 1: Auflisten aller Ausführungsergebnisse unter einer Vorlage</span><span class="sxs-lookup"><span data-stu-id="9fc98-111">Example 1: List all run results under a template</span></span>
```powershell
PS C:\> Get-AzImageBuilderRunOutput -ImageTemplateName lucas-imagetemplate -ResourceGroupName wyunchi-imagebuilder

Name          Type
----          ----
image_lucas_1 Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="9fc98-112">Dieser Befehl listet alle Ausführungsergebnisse unter einer Vorlage auf.</span><span class="sxs-lookup"><span data-stu-id="9fc98-112">This command lists all run results under a template.</span></span>

### <span data-ttu-id="9fc98-113">Beispiel 2: Abrufen eines Ausführungsergebnisses unter einer Vorlage</span><span class="sxs-lookup"><span data-stu-id="9fc98-113">Example 2: Get a run result under a template</span></span>
```powershell
PS C:\> Get-AzImageBuilderRunOutput -ImageTemplateName template-name-u7gjqx -ResourceGroupName wyunchi-imagebuilder -RunOutputName runout-template-name-u7gjqx 

Name                        Type
----                        ----
runout-template-name-u7gjqx Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="9fc98-114">Dieser Befehl ruft ein Ausführungsergebnis unter einer Vorlage ab.</span><span class="sxs-lookup"><span data-stu-id="9fc98-114">This command gets a run result under a template.</span></span>

### <span data-ttu-id="9fc98-115">Beispiel 3: Abrufen eines Ausführungsergebnisses unter einer Vorlage</span><span class="sxs-lookup"><span data-stu-id="9fc98-115">Example 3: Get a run result under a template</span></span>
```powershell
PS C:\> $result = Get-AzImageBuilderRunOutput -ImageTemplateName template-name-u7gjqx -ResourceGroupName wyunchi-imagebuilder -RunOutputName runout-template-name-u7gjqx
PS C:\> Get-AzImageBuilderRunOutput -InputObject $result

Name                        Type
----                        ----
runout-template-name-u7gjqx Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="9fc98-116">Dieser Befehl ruft ein Ausführungsergebnis unter einer Vorlage ab.</span><span class="sxs-lookup"><span data-stu-id="9fc98-116">This command gets a run result under a template.</span></span>

## <span data-ttu-id="9fc98-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="9fc98-117">PARAMETERS</span></span>

### <span data-ttu-id="9fc98-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fc98-118">-DefaultProfile</span></span>
<span data-ttu-id="9fc98-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9fc98-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9fc98-120">-Imagetemplatename</span><span class="sxs-lookup"><span data-stu-id="9fc98-120">-ImageTemplateName</span></span>
<span data-ttu-id="9fc98-121">Der Name der Bildvorlage</span><span class="sxs-lookup"><span data-stu-id="9fc98-121">The name of the image Template</span></span>

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

### <span data-ttu-id="9fc98-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9fc98-122">-InputObject</span></span>
<span data-ttu-id="9fc98-123">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="9fc98-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9fc98-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fc98-124">-ResourceGroupName</span></span>
<span data-ttu-id="9fc98-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9fc98-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="9fc98-126">-RunOutputName</span><span class="sxs-lookup"><span data-stu-id="9fc98-126">-RunOutputName</span></span>
<span data-ttu-id="9fc98-127">Der Name der Run-Ausgabe</span><span class="sxs-lookup"><span data-stu-id="9fc98-127">The name of the run output</span></span>

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

### <span data-ttu-id="9fc98-128">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="9fc98-128">-SubscriptionId</span></span>
<span data-ttu-id="9fc98-129">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="9fc98-129">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="9fc98-130">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="9fc98-130">The subscription Id forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="9fc98-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fc98-131">CommonParameters</span></span>
<span data-ttu-id="9fc98-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fc98-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fc98-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9fc98-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fc98-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9fc98-134">INPUTS</span></span>

### <span data-ttu-id="9fc98-135">Microsoft. Azure. PowerShell. Cmdlets. ImageBuilder. Models. IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="9fc98-135">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="9fc98-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9fc98-136">OUTPUTS</span></span>

### <span data-ttu-id="9fc98-137">Microsoft. Azure. PowerShell. Cmdlets. ImageBuilder. Models. Api20200214. IRunOutput</span><span class="sxs-lookup"><span data-stu-id="9fc98-137">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IRunOutput</span></span>

## <span data-ttu-id="9fc98-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="9fc98-138">NOTES</span></span>

<span data-ttu-id="9fc98-139">Aliase</span><span class="sxs-lookup"><span data-stu-id="9fc98-139">ALIASES</span></span>

<span data-ttu-id="9fc98-140">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9fc98-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9fc98-141">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9fc98-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9fc98-142">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="9fc98-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9fc98-143">Inputobject <IImageBuilderIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="9fc98-143">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9fc98-144">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="9fc98-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9fc98-145">`[ImageTemplateName <String>]`: Der Name der Bildvorlage</span><span class="sxs-lookup"><span data-stu-id="9fc98-145">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="9fc98-146">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9fc98-146">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="9fc98-147">`[RunOutputName <String>]`: Der Name der Run-Ausgabe</span><span class="sxs-lookup"><span data-stu-id="9fc98-147">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="9fc98-148">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="9fc98-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="9fc98-149">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="9fc98-149">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="9fc98-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9fc98-150">RELATED LINKS</span></span>

