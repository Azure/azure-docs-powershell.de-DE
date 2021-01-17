---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/test-azdigitaltwinsinstancenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Test-AzDigitalTwinsInstanceNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Test-AzDigitalTwinsInstanceNameAvailability.md
ms.openlocfilehash: af911fc4eb4cccbd3f22e0d54a8aad2933b5db46
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458784"
---
# <span data-ttu-id="c423b-101">Test-AzDigitalTwinsInstanceNameAvailability</span><span class="sxs-lookup"><span data-stu-id="c423b-101">Test-AzDigitalTwinsInstanceNameAvailability</span></span>

## <span data-ttu-id="c423b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c423b-102">SYNOPSIS</span></span>
<span data-ttu-id="c423b-103">Überprüfen Sie, ob ein Name von "DigitalTwinsInstance" verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="c423b-103">Check if a DigitalTwinsInstance name is available.</span></span>

## <span data-ttu-id="c423b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c423b-104">SYNTAX</span></span>

### <span data-ttu-id="c423b-105">CheckExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="c423b-105">CheckExpanded (Default)</span></span>
```
Test-AzDigitalTwinsInstanceNameAvailability -Location <String> -Name <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c423b-106">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="c423b-106">Check</span></span>
```
Test-AzDigitalTwinsInstanceNameAvailability -Location <String>
 -DigitalTwinsInstanceCheckName <ICheckNameRequest> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c423b-107">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c423b-107">CheckViaIdentity</span></span>
```
Test-AzDigitalTwinsInstanceNameAvailability -InputObject <IDigitalTwinsIdentity>
 -DigitalTwinsInstanceCheckName <ICheckNameRequest> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="c423b-108">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="c423b-108">CheckViaIdentityExpanded</span></span>
```
Test-AzDigitalTwinsInstanceNameAvailability -InputObject <IDigitalTwinsIdentity> -Name <String>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c423b-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c423b-109">DESCRIPTION</span></span>
<span data-ttu-id="c423b-110">Überprüfen Sie, ob ein Name von "DigitalTwinsInstance" verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="c423b-110">Check if a DigitalTwinsInstance name is available.</span></span>

## <span data-ttu-id="c423b-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c423b-111">EXAMPLES</span></span>

### <span data-ttu-id="c423b-112">Beispiel 1: Überprüfen Sie den Namen nach Ort und Name.</span><span class="sxs-lookup"><span data-stu-id="c423b-112">Example 1: Check the name by location and name.</span></span>
```powershell
PS C:\> Test-AzDigitalTwinsInstanceNameAvailability -Location eastus -name youriTestName

Message                       NameAvailable Reason
-------                       ------------- ------
'youriTestName' is available. True
```

<span data-ttu-id="c423b-113">Überprüfen Sie die Verfügbarkeit des Namens nach Ort und Name.</span><span class="sxs-lookup"><span data-stu-id="c423b-113">Check the availability of the name by location and name.</span></span>

### <span data-ttu-id="c423b-114">Beispiel 2: Überprüfen Sie den Namen von "DigitalTwinsObject" und "CheckNameObject".</span><span class="sxs-lookup"><span data-stu-id="c423b-114">Example 2: Check the name by DigitalTwinsObject and CheckNameObject.</span></span>
```powershell
PS C:\> $getAzDT =Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest 
$checkName = New-AzDigitalTwinsCheckNameRequestObject -name youriTestName
Test-AzDigitalTwinsInstanceNameAvailability -InputObject $getAzDT -DigitalTwinsInstanceCheckName $checkName

Message                     NameAvailable Reason
-------                     ------------- ------
'youriTestName' is available. True
```

<span data-ttu-id="c423b-115">Holen Sie sich ein "DigitalTwinsInstance", und erstellen Sie ein "Requset-Objekt", um die Verfügbarkeit des Namens zu testen.</span><span class="sxs-lookup"><span data-stu-id="c423b-115">Get A DigitalTwinsInstance and create a Requset Object to Test the availability of the name.</span></span>

## <span data-ttu-id="c423b-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c423b-116">PARAMETERS</span></span>

### <span data-ttu-id="c423b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c423b-117">-DefaultProfile</span></span>
<span data-ttu-id="c423b-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c423b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c423b-119">-DigitalTwinsInstanceCheckName</span><span class="sxs-lookup"><span data-stu-id="c423b-119">-DigitalTwinsInstanceCheckName</span></span>
<span data-ttu-id="c423b-120">Das Ergebnis, das von einer Anforderung zur Verfügbarkeit des Datenbanknamens zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="c423b-120">The result returned from a database check name availability request.</span></span>
<span data-ttu-id="c423b-121">Informationen zum Erstellen finden Sie im Abschnitt "NOTES" zu den Eigenschaften "DIGITALTWINSINSTANCECHECKNAME", und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="c423b-121">To construct, see NOTES section for DIGITALTWINSINSTANCECHECKNAME properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.ICheckNameRequest
Parameter Sets: Check, CheckViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c423b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c423b-122">-InputObject</span></span>
<span data-ttu-id="c423b-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="c423b-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity
Parameter Sets: CheckViaIdentity, CheckViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c423b-124">-Location</span><span class="sxs-lookup"><span data-stu-id="c423b-124">-Location</span></span>
<span data-ttu-id="c423b-125">Speicherort von DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="c423b-125">Location of DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Check, CheckExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c423b-126">-Name</span><span class="sxs-lookup"><span data-stu-id="c423b-126">-Name</span></span>
<span data-ttu-id="c423b-127">Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="c423b-127">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded, CheckViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c423b-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c423b-128">-SubscriptionId</span></span>
<span data-ttu-id="c423b-129">Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="c423b-129">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Check, CheckExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c423b-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c423b-130">-Confirm</span></span>
<span data-ttu-id="c423b-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c423b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c423b-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c423b-132">-WhatIf</span></span>
<span data-ttu-id="c423b-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c423b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c423b-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c423b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c423b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c423b-135">CommonParameters</span></span>
<span data-ttu-id="c423b-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c423b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c423b-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c423b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c423b-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c423b-138">INPUTS</span></span>

### <span data-ttu-id="c423b-139">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.ICheckNameRequest</span><span class="sxs-lookup"><span data-stu-id="c423b-139">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.ICheckNameRequest</span></span>

### <span data-ttu-id="c423b-140">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="c423b-140">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="c423b-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c423b-141">OUTPUTS</span></span>

### <span data-ttu-id="c423b-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="c423b-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.ICheckNameResult</span></span>

## <span data-ttu-id="c423b-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c423b-143">NOTES</span></span>

<span data-ttu-id="c423b-144">ALIASE</span><span class="sxs-lookup"><span data-stu-id="c423b-144">ALIASES</span></span>

<span data-ttu-id="c423b-145">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="c423b-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c423b-146">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c423b-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c423b-147">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c423b-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c423b-148">DIGITALTWINSINSTANCECHECKNAME: Das Ergebnis, das von einer Anforderung zur Verfügbarkeit des <ICheckNameRequest> Datenbanknamens zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="c423b-148">DIGITALTWINSINSTANCECHECKNAME <ICheckNameRequest>: The result returned from a database check name availability request.</span></span>
  - <span data-ttu-id="c423b-149">`Name <String>`: Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="c423b-149">`Name <String>`: Resource name.</span></span>

<span data-ttu-id="c423b-150">INPUTOBJECT <IDigitalTwinsIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="c423b-150">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c423b-151">`[EndpointName <String>]`: Name der Endpunktressource.</span><span class="sxs-lookup"><span data-stu-id="c423b-151">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="c423b-152">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="c423b-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c423b-153">`[Location <String>]`: Speicherort von DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="c423b-153">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="c423b-154">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die "DigitalTwinsInstance" enthält.</span><span class="sxs-lookup"><span data-stu-id="c423b-154">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="c423b-155">`[ResourceName <String>]`: Der Name von "DigitalTwinsInstance".</span><span class="sxs-lookup"><span data-stu-id="c423b-155">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="c423b-156">`[SubscriptionId <String>]`: Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="c423b-156">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="c423b-157">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c423b-157">RELATED LINKS</span></span>

