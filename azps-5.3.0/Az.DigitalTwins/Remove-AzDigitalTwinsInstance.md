---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/remove-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsInstance.md
ms.openlocfilehash: 495fecf922bc27eb43849b7ba6e44793c572b8cd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467768"
---
# <span data-ttu-id="6cfc3-101">Remove-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="6cfc3-101">Remove-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="6cfc3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6cfc3-102">SYNOPSIS</span></span>
<span data-ttu-id="6cfc3-103">Löschen Sie eine DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="6cfc3-103">Delete a DigitalTwinsInstance.</span></span>

## <span data-ttu-id="6cfc3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6cfc3-104">SYNTAX</span></span>

### <span data-ttu-id="6cfc3-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="6cfc3-105">Delete (Default)</span></span>
```
Remove-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6cfc3-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6cfc3-106">DeleteViaIdentity</span></span>
```
Remove-AzDigitalTwinsInstance -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6cfc3-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6cfc3-107">DESCRIPTION</span></span>
<span data-ttu-id="6cfc3-108">Löschen Sie eine DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="6cfc3-108">Delete a DigitalTwinsInstance.</span></span>

## <span data-ttu-id="6cfc3-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6cfc3-109">EXAMPLES</span></span>

### <span data-ttu-id="6cfc3-110">Beispiel 1: Entfernen einer AzDigitalTwinsInstance nach Name</span><span class="sxs-lookup"><span data-stu-id="6cfc3-110">Example 1: Remove an AzDigitalTwinsInstance by name</span></span>
```powershell
PS C:\> Remove-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwin


```

<span data-ttu-id="6cfc3-111">Mit diesem Befehl wird ein AzDigitalTwinsInstance nach Name entfernt.</span><span class="sxs-lookup"><span data-stu-id="6cfc3-111">This command removes an AzDigitalTwinsInstance by name</span></span>

### <span data-ttu-id="6cfc3-112">Beispiel 2: Entfernen einer AzDigitalTwinsInstance von InputObject</span><span class="sxs-lookup"><span data-stu-id="6cfc3-112">Example 2: Remove an AzDigitalTwinsInstance by InputObject</span></span>
```powershell
PS C:\> $GetAzDigitalTwins =  Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
Remove-AzDigitalTwinsInstance -InputObject $GetAzDigitalTwins


```

<span data-ttu-id="6cfc3-113">Mit diesem Befehl wird ein AzDigitalTwinsInstance nach Name entfernt.</span><span class="sxs-lookup"><span data-stu-id="6cfc3-113">This command removes an AzDigitalTwinsInstance by name</span></span>

## <span data-ttu-id="6cfc3-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6cfc3-114">PARAMETERS</span></span>

### <span data-ttu-id="6cfc3-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6cfc3-115">-AsJob</span></span>
<span data-ttu-id="6cfc3-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="6cfc3-116">Run the command as a job</span></span>

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

### <span data-ttu-id="6cfc3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cfc3-117">-DefaultProfile</span></span>
<span data-ttu-id="6cfc3-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6cfc3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6cfc3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6cfc3-119">-InputObject</span></span>
<span data-ttu-id="6cfc3-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="6cfc3-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6cfc3-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="6cfc3-121">-NoWait</span></span>
<span data-ttu-id="6cfc3-122">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="6cfc3-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6cfc3-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6cfc3-123">-PassThru</span></span>
<span data-ttu-id="6cfc3-124">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="6cfc3-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="6cfc3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cfc3-125">-ResourceGroupName</span></span>
<span data-ttu-id="6cfc3-126">Der Name der Ressourcengruppe, die "DigitalTwinsInstance" enthält.</span><span class="sxs-lookup"><span data-stu-id="6cfc3-126">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="6cfc3-127">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="6cfc3-127">-ResourceName</span></span>
<span data-ttu-id="6cfc3-128">Der Name von "DigitalTwinsInstance".</span><span class="sxs-lookup"><span data-stu-id="6cfc3-128">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="6cfc3-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6cfc3-129">-SubscriptionId</span></span>
<span data-ttu-id="6cfc3-130">Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="6cfc3-130">The subscription identifier.</span></span>

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

### <span data-ttu-id="6cfc3-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6cfc3-131">-Confirm</span></span>
<span data-ttu-id="6cfc3-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6cfc3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6cfc3-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="6cfc3-133">-WhatIf</span></span>
<span data-ttu-id="6cfc3-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6cfc3-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6cfc3-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6cfc3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6cfc3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cfc3-136">CommonParameters</span></span>
<span data-ttu-id="6cfc3-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cfc3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cfc3-138">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6cfc3-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cfc3-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6cfc3-139">INPUTS</span></span>

### <span data-ttu-id="6cfc3-140">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="6cfc3-140">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="6cfc3-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6cfc3-141">OUTPUTS</span></span>

### <span data-ttu-id="6cfc3-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="6cfc3-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="6cfc3-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6cfc3-143">NOTES</span></span>

<span data-ttu-id="6cfc3-144">ALIASE</span><span class="sxs-lookup"><span data-stu-id="6cfc3-144">ALIASES</span></span>

<span data-ttu-id="6cfc3-145">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="6cfc3-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6cfc3-146">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6cfc3-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6cfc3-147">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6cfc3-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6cfc3-148">INPUTOBJECT <IDigitalTwinsIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="6cfc3-148">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6cfc3-149">`[EndpointName <String>]`: Name der Endpunktressource.</span><span class="sxs-lookup"><span data-stu-id="6cfc3-149">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="6cfc3-150">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="6cfc3-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6cfc3-151">`[Location <String>]`: Speicherort von DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="6cfc3-151">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="6cfc3-152">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die "DigitalTwinsInstance" enthält.</span><span class="sxs-lookup"><span data-stu-id="6cfc3-152">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="6cfc3-153">`[ResourceName <String>]`: Der Name von "DigitalTwinsInstance".</span><span class="sxs-lookup"><span data-stu-id="6cfc3-153">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="6cfc3-154">`[SubscriptionId <String>]`: Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="6cfc3-154">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="6cfc3-155">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6cfc3-155">RELATED LINKS</span></span>

