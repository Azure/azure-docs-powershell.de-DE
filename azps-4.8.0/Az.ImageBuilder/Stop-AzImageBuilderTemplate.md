---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/stop-azimagebuildertemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Stop-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Stop-AzImageBuilderTemplate.md
ms.openlocfilehash: 01fd95dd41a7ee76c06f0423d33c4aba34329c18
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94172960"
---
# <span data-ttu-id="cf962-101">Stop-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="cf962-101">Stop-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="cf962-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cf962-102">SYNOPSIS</span></span>
<span data-ttu-id="cf962-103">Abbrechen des auf der Bildvorlage basierenden Bildaufbaus mit langer Laufzeit</span><span class="sxs-lookup"><span data-stu-id="cf962-103">Cancel the long running image build based on the image template</span></span>

## <span data-ttu-id="cf962-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cf962-104">SYNTAX</span></span>

### <span data-ttu-id="cf962-105">Abbrechen (Standard)</span><span class="sxs-lookup"><span data-stu-id="cf962-105">Cancel (Default)</span></span>
```
Stop-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cf962-106">CancelViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cf962-106">CancelViaIdentity</span></span>
```
Stop-AzImageBuilderTemplate -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cf962-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cf962-107">DESCRIPTION</span></span>
<span data-ttu-id="cf962-108">Abbrechen des auf der Bildvorlage basierenden Bildaufbaus mit langer Laufzeit</span><span class="sxs-lookup"><span data-stu-id="cf962-108">Cancel the long running image build based on the image template</span></span>

## <span data-ttu-id="cf962-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cf962-109">EXAMPLES</span></span>

### <span data-ttu-id="cf962-110">Beispiel 1: Beenden der Erstellung von Bildvorlagen</span><span class="sxs-lookup"><span data-stu-id="cf962-110">Example 1: Stop image template creation</span></span>
```powershell
PS C:\> Start-AzImageBuilderTemplate -ImageTemplateName template-name-sn78hg -ResourceGroupName wyunchi-imagebuilder -AsJob 

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Start-AzImageB…                 Running       True            localhost            Start-AzImageBuilderTemp…

PS C:\> Stop-AzImageBuilderTemplate -ImageTemplateName template-name-sn78hg -ResourceGroupName wyunchi-imagebuilder

```

<span data-ttu-id="cf962-111">Mit diesem Befehl wird die Erstellung von Bildvorlagen angehalten.</span><span class="sxs-lookup"><span data-stu-id="cf962-111">This command stops image template creation.</span></span>

### <span data-ttu-id="cf962-112">Beispiel 2: Beenden der Erstellung von Bildvorlagen</span><span class="sxs-lookup"><span data-stu-id="cf962-112">Example 2: Stop image template creation</span></span>
```powershell
PS C:\> Start-AzImageBuilderTemplate -ImageTemplateName template-name-sn78hg -ResourceGroupName wyunchi-imagebuilder -AsJob 

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
2      Start-AzImageB…                 Running       True            localhost            Start-AzImageBuilderTemp…

PS C:\> $template = Get-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -Name template-name-sn78hg
PS C:\> Stop-AzImageBuilderTemplate -InputObject $template 

```

<span data-ttu-id="cf962-113">Mit diesem Befehl wird die Erstellung von Bildvorlagen angehalten.</span><span class="sxs-lookup"><span data-stu-id="cf962-113">This command stops image template creation.</span></span>

## <span data-ttu-id="cf962-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf962-114">PARAMETERS</span></span>

### <span data-ttu-id="cf962-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cf962-115">-AsJob</span></span>
<span data-ttu-id="cf962-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="cf962-116">Run the command as a job</span></span>

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

### <span data-ttu-id="cf962-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf962-117">-DefaultProfile</span></span>
<span data-ttu-id="cf962-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cf962-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf962-119">-Imagetemplatename</span><span class="sxs-lookup"><span data-stu-id="cf962-119">-ImageTemplateName</span></span>
<span data-ttu-id="cf962-120">Der Name der Bildvorlage</span><span class="sxs-lookup"><span data-stu-id="cf962-120">The name of the image Template</span></span>

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

### <span data-ttu-id="cf962-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="cf962-121">-InputObject</span></span>
<span data-ttu-id="cf962-122">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="cf962-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="cf962-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="cf962-123">-NoWait</span></span>
<span data-ttu-id="cf962-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="cf962-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="cf962-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cf962-125">-PassThru</span></span>
<span data-ttu-id="cf962-126">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="cf962-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="cf962-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf962-127">-ResourceGroupName</span></span>
<span data-ttu-id="cf962-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="cf962-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="cf962-129">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="cf962-129">-SubscriptionId</span></span>
<span data-ttu-id="cf962-130">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="cf962-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="cf962-131">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="cf962-131">The subscription Id forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="cf962-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cf962-132">-Confirm</span></span>
<span data-ttu-id="cf962-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cf962-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf962-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf962-134">-WhatIf</span></span>
<span data-ttu-id="cf962-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cf962-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf962-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cf962-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf962-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf962-137">CommonParameters</span></span>
<span data-ttu-id="cf962-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf962-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf962-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cf962-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf962-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cf962-140">INPUTS</span></span>

### <span data-ttu-id="cf962-141">Microsoft. Azure. PowerShell. Cmdlets. ImageBuilder. Models. IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="cf962-141">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="cf962-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cf962-142">OUTPUTS</span></span>

### <span data-ttu-id="cf962-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cf962-143">System.Boolean</span></span>

## <span data-ttu-id="cf962-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="cf962-144">NOTES</span></span>

<span data-ttu-id="cf962-145">Aliase</span><span class="sxs-lookup"><span data-stu-id="cf962-145">ALIASES</span></span>

<span data-ttu-id="cf962-146">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cf962-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cf962-147">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="cf962-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cf962-148">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="cf962-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cf962-149">Inputobject <IImageBuilderIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="cf962-149">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cf962-150">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="cf962-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cf962-151">`[ImageTemplateName <String>]`: Der Name der Bildvorlage</span><span class="sxs-lookup"><span data-stu-id="cf962-151">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="cf962-152">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="cf962-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="cf962-153">`[RunOutputName <String>]`: Der Name der Run-Ausgabe</span><span class="sxs-lookup"><span data-stu-id="cf962-153">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="cf962-154">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="cf962-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="cf962-155">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="cf962-155">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="cf962-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cf962-156">RELATED LINKS</span></span>

