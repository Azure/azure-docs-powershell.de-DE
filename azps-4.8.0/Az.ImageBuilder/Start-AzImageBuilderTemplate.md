---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/start-azimagebuildertemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Start-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Start-AzImageBuilderTemplate.md
ms.openlocfilehash: 710c39adca3f3a82b91b1e27a7f63e0ef1f6b693
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94172962"
---
# <span data-ttu-id="ab3f8-101">Start-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="ab3f8-101">Start-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="ab3f8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ab3f8-102">SYNOPSIS</span></span>
<span data-ttu-id="ab3f8-103">Erstellen von Artefakten aus einer vorhandenen Bildvorlage</span><span class="sxs-lookup"><span data-stu-id="ab3f8-103">Create artifacts from a existing image template</span></span>

## <span data-ttu-id="ab3f8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ab3f8-104">SYNTAX</span></span>

### <span data-ttu-id="ab3f8-105">Ausführen (Standard)</span><span class="sxs-lookup"><span data-stu-id="ab3f8-105">Run (Default)</span></span>
```
Start-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="ab3f8-106">RunViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ab3f8-106">RunViaIdentity</span></span>
```
Start-AzImageBuilderTemplate -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ab3f8-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ab3f8-107">DESCRIPTION</span></span>
<span data-ttu-id="ab3f8-108">Erstellen von Artefakten aus einer vorhandenen Bildvorlage</span><span class="sxs-lookup"><span data-stu-id="ab3f8-108">Create artifacts from a existing image template</span></span>

## <span data-ttu-id="ab3f8-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ab3f8-109">EXAMPLES</span></span>

### <span data-ttu-id="ab3f8-110">Beispiel 1: Starten einer Bildvorlage</span><span class="sxs-lookup"><span data-stu-id="ab3f8-110">Example 1: Start an image template</span></span>
```powershell
PS C:\> Start-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -Name template-name-sn78hg

```

<span data-ttu-id="ab3f8-111">Mit diesem Befehl wird eine Bildvorlage gestartet.</span><span class="sxs-lookup"><span data-stu-id="ab3f8-111">This command starts an image template.</span></span>

### <span data-ttu-id="ab3f8-112">Beispiel 2: Starten einer Bildvorlage</span><span class="sxs-lookup"><span data-stu-id="ab3f8-112">Example 2: Start an image template</span></span>
```powershell
PS C:\> $template = Get-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -Name template-name-sn78hg
PS C:\> Start-AzImageBuilderTemplate -InputObject $template

```

<span data-ttu-id="ab3f8-113">Mit diesem Befehl wird eine Bildvorlage gestartet.</span><span class="sxs-lookup"><span data-stu-id="ab3f8-113">This command starts an image template.</span></span>

## <span data-ttu-id="ab3f8-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="ab3f8-114">PARAMETERS</span></span>

### <span data-ttu-id="ab3f8-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ab3f8-115">-AsJob</span></span>
<span data-ttu-id="ab3f8-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="ab3f8-116">Run the command as a job</span></span>

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

### <span data-ttu-id="ab3f8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab3f8-117">-DefaultProfile</span></span>
<span data-ttu-id="ab3f8-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ab3f8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab3f8-119">-Imagetemplatename</span><span class="sxs-lookup"><span data-stu-id="ab3f8-119">-ImageTemplateName</span></span>
<span data-ttu-id="ab3f8-120">Der Name der Bildvorlage</span><span class="sxs-lookup"><span data-stu-id="ab3f8-120">The name of the image Template</span></span>

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

### <span data-ttu-id="ab3f8-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ab3f8-121">-InputObject</span></span>
<span data-ttu-id="ab3f8-122">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="ab3f8-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ab3f8-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="ab3f8-123">-NoWait</span></span>
<span data-ttu-id="ab3f8-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="ab3f8-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ab3f8-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ab3f8-125">-PassThru</span></span>
<span data-ttu-id="ab3f8-126">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="ab3f8-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ab3f8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab3f8-127">-ResourceGroupName</span></span>
<span data-ttu-id="ab3f8-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ab3f8-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="ab3f8-129">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="ab3f8-129">-SubscriptionId</span></span>
<span data-ttu-id="ab3f8-130">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="ab3f8-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ab3f8-131">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="ab3f8-131">The subscription Id forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ab3f8-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ab3f8-132">-Confirm</span></span>
<span data-ttu-id="ab3f8-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ab3f8-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab3f8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab3f8-134">-WhatIf</span></span>
<span data-ttu-id="ab3f8-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ab3f8-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab3f8-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ab3f8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab3f8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab3f8-137">CommonParameters</span></span>
<span data-ttu-id="ab3f8-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab3f8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab3f8-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ab3f8-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab3f8-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ab3f8-140">INPUTS</span></span>

### <span data-ttu-id="ab3f8-141">Microsoft. Azure. PowerShell. Cmdlets. ImageBuilder. Models. IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="ab3f8-141">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="ab3f8-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ab3f8-142">OUTPUTS</span></span>

### <span data-ttu-id="ab3f8-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ab3f8-143">System.Boolean</span></span>

## <span data-ttu-id="ab3f8-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="ab3f8-144">NOTES</span></span>

<span data-ttu-id="ab3f8-145">Aliase</span><span class="sxs-lookup"><span data-stu-id="ab3f8-145">ALIASES</span></span>

<span data-ttu-id="ab3f8-146">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ab3f8-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ab3f8-147">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ab3f8-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ab3f8-148">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="ab3f8-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ab3f8-149">Inputobject <IImageBuilderIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="ab3f8-149">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ab3f8-150">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="ab3f8-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ab3f8-151">`[ImageTemplateName <String>]`: Der Name der Bildvorlage</span><span class="sxs-lookup"><span data-stu-id="ab3f8-151">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="ab3f8-152">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ab3f8-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="ab3f8-153">`[RunOutputName <String>]`: Der Name der Run-Ausgabe</span><span class="sxs-lookup"><span data-stu-id="ab3f8-153">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="ab3f8-154">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="ab3f8-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="ab3f8-155">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="ab3f8-155">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="ab3f8-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ab3f8-156">RELATED LINKS</span></span>

