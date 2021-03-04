---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/powershell/module/az.digitaltwins/remove-azdigitaltwinsendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsEndpoint.md
ms.openlocfilehash: f7d8b5665ff150e0501d77a76c2dde7e4a947cb5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935120"
---
# <span data-ttu-id="dbc34-101">Remove-AzDigitalTwinsEndpoint</span><span class="sxs-lookup"><span data-stu-id="dbc34-101">Remove-AzDigitalTwinsEndpoint</span></span>

## <span data-ttu-id="dbc34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbc34-102">SYNOPSIS</span></span>
<span data-ttu-id="dbc34-103">Löschen Sie einen DigitalTwinsInstance-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="dbc34-103">Delete a DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="dbc34-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dbc34-104">SYNTAX</span></span>

### <span data-ttu-id="dbc34-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="dbc34-105">Delete (Default)</span></span>
```
Remove-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="dbc34-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="dbc34-106">DeleteViaIdentity</span></span>
```
Remove-AzDigitalTwinsEndpoint -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="dbc34-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dbc34-107">DESCRIPTION</span></span>
<span data-ttu-id="dbc34-108">Löschen Sie einen DigitalTwinsInstance-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="dbc34-108">Delete a DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="dbc34-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="dbc34-109">EXAMPLES</span></span>

### <span data-ttu-id="dbc34-110">Beispiel 1: Löschen des azDigitalTwinsEndPoint nach EndPointName</span><span class="sxs-lookup"><span data-stu-id="dbc34-110">Example 1: Delete the azDigitalTwinsEndPoint by EndPointName</span></span>
```powershell
PS C:\> Remove-AzDigitalTwinsEndpoint -ResourceGroupName youritemp -EndpointName youriEHEndpoint -ResourceName youriDigitalTwinsTest

```

<span data-ttu-id="dbc34-111">Löschen des azDigitalTwinsEndPoint nach EndPointName ResourceGroupName und ResourceName</span><span class="sxs-lookup"><span data-stu-id="dbc34-111">Delete the azDigitalTwinsEndPoint by EndPointName ResourceGroupName and ResourceName</span></span>

### <span data-ttu-id="dbc34-112">Beispiel 2: Löschen des azDigitalTwinsEndPoint nach Object</span><span class="sxs-lookup"><span data-stu-id="dbc34-112">Example 2: Delete the azDigitalTwinsEndPoint by Object</span></span>
```powershell
PS C:\> $GetAzdigitalTwinsEndpoint = Get-AzDigitalTwinsEndpoint -EndpointName youriEHEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
Remove-AzDigitalTwinsEndpoint -InputObject $GetAzdigitalTwinsEndpoint

```

<span data-ttu-id="dbc34-113">Löschen des azDigitalTwinsEndPoint nach Object</span><span class="sxs-lookup"><span data-stu-id="dbc34-113">Delete the azDigitalTwinsEndPoint by Object</span></span>

## <span data-ttu-id="dbc34-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="dbc34-114">PARAMETERS</span></span>

### <span data-ttu-id="dbc34-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dbc34-115">-AsJob</span></span>
<span data-ttu-id="dbc34-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="dbc34-116">Run the command as a job</span></span>

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

### <span data-ttu-id="dbc34-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbc34-117">-DefaultProfile</span></span>
<span data-ttu-id="dbc34-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dbc34-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbc34-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="dbc34-119">-EndpointName</span></span>
<span data-ttu-id="dbc34-120">Name der Endpunktressource.</span><span class="sxs-lookup"><span data-stu-id="dbc34-120">Name of Endpoint Resource.</span></span>

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

### <span data-ttu-id="dbc34-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dbc34-121">-InputObject</span></span>
<span data-ttu-id="dbc34-122">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="dbc34-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="dbc34-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="dbc34-123">-NoWait</span></span>
<span data-ttu-id="dbc34-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="dbc34-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="dbc34-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dbc34-125">-PassThru</span></span>
<span data-ttu-id="dbc34-126">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dbc34-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="dbc34-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbc34-127">-ResourceGroupName</span></span>
<span data-ttu-id="dbc34-128">Der Name der Ressourcengruppe, die den DigitalTwinsInstance enthält.</span><span class="sxs-lookup"><span data-stu-id="dbc34-128">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="dbc34-129">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="dbc34-129">-ResourceName</span></span>
<span data-ttu-id="dbc34-130">Der Name der DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="dbc34-130">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="dbc34-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dbc34-131">-SubscriptionId</span></span>
<span data-ttu-id="dbc34-132">Der Abonnementbezeichner.</span><span class="sxs-lookup"><span data-stu-id="dbc34-132">The subscription identifier.</span></span>

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

### <span data-ttu-id="dbc34-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dbc34-133">-Confirm</span></span>
<span data-ttu-id="dbc34-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dbc34-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbc34-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbc34-135">-WhatIf</span></span>
<span data-ttu-id="dbc34-136">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dbc34-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbc34-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dbc34-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbc34-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbc34-138">CommonParameters</span></span>
<span data-ttu-id="dbc34-139">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbc34-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbc34-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dbc34-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbc34-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="dbc34-141">INPUTS</span></span>

### <span data-ttu-id="dbc34-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="dbc34-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="dbc34-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="dbc34-143">OUTPUTS</span></span>

### <span data-ttu-id="dbc34-144">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span><span class="sxs-lookup"><span data-stu-id="dbc34-144">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="dbc34-145">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="dbc34-145">NOTES</span></span>

<span data-ttu-id="dbc34-146">ALIASE</span><span class="sxs-lookup"><span data-stu-id="dbc34-146">ALIASES</span></span>

<span data-ttu-id="dbc34-147">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="dbc34-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="dbc34-148">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="dbc34-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dbc34-149">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="dbc34-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="dbc34-150">INPUTOBJECT <IDigitalTwinsIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="dbc34-150">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="dbc34-151">`[EndpointName <String>]`: Name der Endpunktressource.</span><span class="sxs-lookup"><span data-stu-id="dbc34-151">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="dbc34-152">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="dbc34-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dbc34-153">`[Location <String>]`: Speicherort von DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="dbc34-153">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="dbc34-154">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den DigitalTwinsInstance enthält.</span><span class="sxs-lookup"><span data-stu-id="dbc34-154">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="dbc34-155">`[ResourceName <String>]`: Der Name der DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="dbc34-155">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="dbc34-156">`[SubscriptionId <String>]`: Der Abonnementbezeichner.</span><span class="sxs-lookup"><span data-stu-id="dbc34-156">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="dbc34-157">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="dbc34-157">RELATED LINKS</span></span>

