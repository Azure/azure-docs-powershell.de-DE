---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/remove-azdigitaltwinsendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsEndpoint.md
ms.openlocfilehash: 1c740134cb2613a8efcd950fec4cd780f4f443cf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98302451"
---
# <span data-ttu-id="be414-101">Remove-AzDigitalTwinsEndpoint</span><span class="sxs-lookup"><span data-stu-id="be414-101">Remove-AzDigitalTwinsEndpoint</span></span>

## <span data-ttu-id="be414-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be414-102">SYNOPSIS</span></span>
<span data-ttu-id="be414-103">Löschen Sie einen DigitalTwinsInstance-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="be414-103">Delete a DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="be414-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="be414-104">SYNTAX</span></span>

### <span data-ttu-id="be414-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="be414-105">Delete (Default)</span></span>
```
Remove-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="be414-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="be414-106">DeleteViaIdentity</span></span>
```
Remove-AzDigitalTwinsEndpoint -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="be414-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="be414-107">DESCRIPTION</span></span>
<span data-ttu-id="be414-108">Löschen Sie einen DigitalTwinsInstance-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="be414-108">Delete a DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="be414-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="be414-109">EXAMPLES</span></span>

### <span data-ttu-id="be414-110">Beispiel 1: Löschen von azDigitalTwinsEndPoint nach EndPointName</span><span class="sxs-lookup"><span data-stu-id="be414-110">Example 1: Delete the azDigitalTwinsEndPoint by EndPointName</span></span>
```powershell
PS C:\> Remove-AzDigitalTwinsEndpoint -ResourceGroupName youritemp -EndpointName youriEHEndpoint -ResourceName youriDigitalTwinsTest

```

<span data-ttu-id="be414-111">Löschen sie "azDigitalTwinsEndPoint" nach "EndPointName ResourceGroupName" und "ResourceName".</span><span class="sxs-lookup"><span data-stu-id="be414-111">Delete the azDigitalTwinsEndPoint by EndPointName ResourceGroupName and ResourceName</span></span>

### <span data-ttu-id="be414-112">Beispiel 2: Löschen von azDigitalTwinsEndPoint nach Objekt</span><span class="sxs-lookup"><span data-stu-id="be414-112">Example 2: Delete the azDigitalTwinsEndPoint by Object</span></span>
```powershell
PS C:\> $GetAzdigitalTwinsEndpoint = Get-AzDigitalTwinsEndpoint -EndpointName youriEHEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
Remove-AzDigitalTwinsEndpoint -InputObject $GetAzdigitalTwinsEndpoint

```

<span data-ttu-id="be414-113">Löschen von azDigitalTwinsEndPoint nach Objekt</span><span class="sxs-lookup"><span data-stu-id="be414-113">Delete the azDigitalTwinsEndPoint by Object</span></span>

## <span data-ttu-id="be414-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="be414-114">PARAMETERS</span></span>

### <span data-ttu-id="be414-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="be414-115">-AsJob</span></span>
<span data-ttu-id="be414-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="be414-116">Run the command as a job</span></span>

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

### <span data-ttu-id="be414-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be414-117">-DefaultProfile</span></span>
<span data-ttu-id="be414-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="be414-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be414-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="be414-119">-EndpointName</span></span>
<span data-ttu-id="be414-120">Name der Endpunktressource.</span><span class="sxs-lookup"><span data-stu-id="be414-120">Name of Endpoint Resource.</span></span>

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

### <span data-ttu-id="be414-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="be414-121">-InputObject</span></span>
<span data-ttu-id="be414-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="be414-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="be414-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="be414-123">-NoWait</span></span>
<span data-ttu-id="be414-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="be414-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="be414-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="be414-125">-PassThru</span></span>
<span data-ttu-id="be414-126">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="be414-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="be414-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be414-127">-ResourceGroupName</span></span>
<span data-ttu-id="be414-128">Der Name der Ressourcengruppe, die "DigitalTwinsInstance" enthält.</span><span class="sxs-lookup"><span data-stu-id="be414-128">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="be414-129">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="be414-129">-ResourceName</span></span>
<span data-ttu-id="be414-130">Der Name von "DigitalTwinsInstance".</span><span class="sxs-lookup"><span data-stu-id="be414-130">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="be414-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="be414-131">-SubscriptionId</span></span>
<span data-ttu-id="be414-132">Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="be414-132">The subscription identifier.</span></span>

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

### <span data-ttu-id="be414-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="be414-133">-Confirm</span></span>
<span data-ttu-id="be414-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="be414-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be414-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="be414-135">-WhatIf</span></span>
<span data-ttu-id="be414-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="be414-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be414-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="be414-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be414-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be414-138">CommonParameters</span></span>
<span data-ttu-id="be414-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be414-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be414-140">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="be414-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be414-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="be414-141">INPUTS</span></span>

### <span data-ttu-id="be414-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="be414-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="be414-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="be414-143">OUTPUTS</span></span>

### <span data-ttu-id="be414-144">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span><span class="sxs-lookup"><span data-stu-id="be414-144">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="be414-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="be414-145">NOTES</span></span>

<span data-ttu-id="be414-146">ALIASE</span><span class="sxs-lookup"><span data-stu-id="be414-146">ALIASES</span></span>

<span data-ttu-id="be414-147">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="be414-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="be414-148">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="be414-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="be414-149">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="be414-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="be414-150">INPUTOBJECT <IDigitalTwinsIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="be414-150">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="be414-151">`[EndpointName <String>]`: Name der Endpunktressource.</span><span class="sxs-lookup"><span data-stu-id="be414-151">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="be414-152">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="be414-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="be414-153">`[Location <String>]`: Speicherort von DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="be414-153">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="be414-154">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die "DigitalTwinsInstance" enthält.</span><span class="sxs-lookup"><span data-stu-id="be414-154">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="be414-155">`[ResourceName <String>]`: Der Name von "DigitalTwinsInstance".</span><span class="sxs-lookup"><span data-stu-id="be414-155">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="be414-156">`[SubscriptionId <String>]`: Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="be414-156">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="be414-157">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="be414-157">RELATED LINKS</span></span>

