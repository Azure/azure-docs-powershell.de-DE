---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/powershell/module/az.digitaltwins/remove-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsInstance.md
ms.openlocfilehash: ff83b10755789f807e1ec28b1f247c9ebee1da18
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935115"
---
# <span data-ttu-id="2327d-101">Remove-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="2327d-101">Remove-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="2327d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2327d-102">SYNOPSIS</span></span>
<span data-ttu-id="2327d-103">Löschen Sie eine DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="2327d-103">Delete a DigitalTwinsInstance.</span></span>

## <span data-ttu-id="2327d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2327d-104">SYNTAX</span></span>

### <span data-ttu-id="2327d-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="2327d-105">Delete (Default)</span></span>
```
Remove-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2327d-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2327d-106">DeleteViaIdentity</span></span>
```
Remove-AzDigitalTwinsInstance -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2327d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2327d-107">DESCRIPTION</span></span>
<span data-ttu-id="2327d-108">Löschen Sie eine DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="2327d-108">Delete a DigitalTwinsInstance.</span></span>

## <span data-ttu-id="2327d-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2327d-109">EXAMPLES</span></span>

### <span data-ttu-id="2327d-110">Beispiel 1: Entfernen einer AzDigitalTwinsInstance nach Name</span><span class="sxs-lookup"><span data-stu-id="2327d-110">Example 1: Remove an AzDigitalTwinsInstance by name</span></span>
```powershell
PS C:\> Remove-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwin


```

<span data-ttu-id="2327d-111">Mit diesem Befehl wird eine AzDigitalTwinsInstance nach Name entfernt.</span><span class="sxs-lookup"><span data-stu-id="2327d-111">This command removes an AzDigitalTwinsInstance by name</span></span>

### <span data-ttu-id="2327d-112">Beispiel 2: Entfernen einer AzDigitalTwinsInstance von InputObject</span><span class="sxs-lookup"><span data-stu-id="2327d-112">Example 2: Remove an AzDigitalTwinsInstance by InputObject</span></span>
```powershell
PS C:\> $GetAzDigitalTwins =  Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
Remove-AzDigitalTwinsInstance -InputObject $GetAzDigitalTwins


```

<span data-ttu-id="2327d-113">Mit diesem Befehl wird eine AzDigitalTwinsInstance nach Name entfernt.</span><span class="sxs-lookup"><span data-stu-id="2327d-113">This command removes an AzDigitalTwinsInstance by name</span></span>

## <span data-ttu-id="2327d-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2327d-114">PARAMETERS</span></span>

### <span data-ttu-id="2327d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2327d-115">-AsJob</span></span>
<span data-ttu-id="2327d-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="2327d-116">Run the command as a job</span></span>

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

### <span data-ttu-id="2327d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2327d-117">-DefaultProfile</span></span>
<span data-ttu-id="2327d-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2327d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2327d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2327d-119">-InputObject</span></span>
<span data-ttu-id="2327d-120">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="2327d-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2327d-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2327d-121">-NoWait</span></span>
<span data-ttu-id="2327d-122">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="2327d-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2327d-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2327d-123">-PassThru</span></span>
<span data-ttu-id="2327d-124">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2327d-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="2327d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2327d-125">-ResourceGroupName</span></span>
<span data-ttu-id="2327d-126">Der Name der Ressourcengruppe, die den DigitalTwinsInstance enthält.</span><span class="sxs-lookup"><span data-stu-id="2327d-126">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="2327d-127">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="2327d-127">-ResourceName</span></span>
<span data-ttu-id="2327d-128">Der Name der DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="2327d-128">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="2327d-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2327d-129">-SubscriptionId</span></span>
<span data-ttu-id="2327d-130">Der Abonnementbezeichner.</span><span class="sxs-lookup"><span data-stu-id="2327d-130">The subscription identifier.</span></span>

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

### <span data-ttu-id="2327d-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2327d-131">-Confirm</span></span>
<span data-ttu-id="2327d-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2327d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2327d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2327d-133">-WhatIf</span></span>
<span data-ttu-id="2327d-134">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2327d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2327d-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2327d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2327d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2327d-136">CommonParameters</span></span>
<span data-ttu-id="2327d-137">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2327d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2327d-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2327d-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2327d-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2327d-139">INPUTS</span></span>

### <span data-ttu-id="2327d-140">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="2327d-140">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="2327d-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2327d-141">OUTPUTS</span></span>

### <span data-ttu-id="2327d-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="2327d-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="2327d-143">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="2327d-143">NOTES</span></span>

<span data-ttu-id="2327d-144">ALIASE</span><span class="sxs-lookup"><span data-stu-id="2327d-144">ALIASES</span></span>

<span data-ttu-id="2327d-145">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="2327d-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2327d-146">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="2327d-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2327d-147">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2327d-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2327d-148">INPUTOBJECT <IDigitalTwinsIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="2327d-148">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2327d-149">`[EndpointName <String>]`: Name der Endpunktressource.</span><span class="sxs-lookup"><span data-stu-id="2327d-149">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="2327d-150">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="2327d-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2327d-151">`[Location <String>]`: Speicherort von DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="2327d-151">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="2327d-152">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den DigitalTwinsInstance enthält.</span><span class="sxs-lookup"><span data-stu-id="2327d-152">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="2327d-153">`[ResourceName <String>]`: Der Name der DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="2327d-153">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="2327d-154">`[SubscriptionId <String>]`: Der Abonnementbezeichner.</span><span class="sxs-lookup"><span data-stu-id="2327d-154">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="2327d-155">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="2327d-155">RELATED LINKS</span></span>

