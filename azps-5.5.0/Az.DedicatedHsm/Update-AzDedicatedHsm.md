---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/en-us/powershell/module/az.dedicatedhsm/update-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Update-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Update-AzDedicatedHsm.md
ms.openlocfilehash: 5aa286eeedb08e6f582210d98a1d29bcd0074031
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165257"
---
# <span data-ttu-id="01706-101">Update-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="01706-101">Update-AzDedicatedHsm</span></span>

## <span data-ttu-id="01706-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01706-102">SYNOPSIS</span></span>
<span data-ttu-id="01706-103">Aktualisieren Sie einen dedizierten HSM im angegebenen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="01706-103">Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="01706-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="01706-104">SYNTAX</span></span>

### <span data-ttu-id="01706-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="01706-105">UpdateExpanded (Default)</span></span>
```
Update-AzDedicatedHsm -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="01706-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="01706-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzDedicatedHsm -InputObject <IDedicatedHsmIdentity> [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="01706-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="01706-107">DESCRIPTION</span></span>
<span data-ttu-id="01706-108">Aktualisieren Sie einen dedizierten HSM im angegebenen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="01706-108">Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="01706-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="01706-109">EXAMPLES</span></span>

### <span data-ttu-id="01706-110">Beispiel 1: Aktualisieren des Parametertags des dedicated HSM nach Name</span><span class="sxs-lookup"><span data-stu-id="01706-110">Example 1: Update the parameter tag of the Dedicated HSM by name</span></span>
```powershell
PS C:\> Update-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz -Tag @{'key1' = '1'; 'key2' = 2; 'key3' = 3}

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="01706-111">Mit diesem Befehl wird das Parametertag des dedicated HSM nach Name aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="01706-111">This command updates the parameter tag of the Dedicated HSM by name</span></span>

### <span data-ttu-id="01706-112">Beispiel 2: Aktualisieren des Parametertags des dedicated HSM nach Objekt</span><span class="sxs-lookup"><span data-stu-id="01706-112">Example 2: Update the parameter tag of the Dedicated HSM by object</span></span>
```powershell
PS C:\> $hsm = Get-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz 
PS C:\> Update-AzDedicatedHsm -InputObject -Tag @{'key1' = '1'; 'key2' = 2; 'key3' = 3}

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="01706-113">Mit diesem Befehl wird das Parametertag des dedicated HSM nach Objekt aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="01706-113">This command updates the parameter tag of the Dedicated HSM by object</span></span>

## <span data-ttu-id="01706-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01706-114">PARAMETERS</span></span>

### <span data-ttu-id="01706-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="01706-115">-AsJob</span></span>
<span data-ttu-id="01706-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="01706-116">Run the command as a job</span></span>

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

### <span data-ttu-id="01706-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01706-117">-DefaultProfile</span></span>
<span data-ttu-id="01706-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="01706-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01706-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="01706-119">-InputObject</span></span>
<span data-ttu-id="01706-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="01706-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="01706-121">-Name</span><span class="sxs-lookup"><span data-stu-id="01706-121">-Name</span></span>
<span data-ttu-id="01706-122">Name des dedizierten HSM</span><span class="sxs-lookup"><span data-stu-id="01706-122">Name of the dedicated HSM</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01706-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="01706-123">-NoWait</span></span>
<span data-ttu-id="01706-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="01706-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="01706-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01706-125">-ResourceGroupName</span></span>
<span data-ttu-id="01706-126">Der Name der Ressourcengruppe, zu der der Server gehört.</span><span class="sxs-lookup"><span data-stu-id="01706-126">The name of the Resource Group to which the server belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01706-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="01706-127">-SubscriptionId</span></span>
<span data-ttu-id="01706-128">Abonnementanmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="01706-128">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="01706-129">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="01706-129">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01706-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="01706-130">-Tag</span></span>
<span data-ttu-id="01706-131">Ressourcentags</span><span class="sxs-lookup"><span data-stu-id="01706-131">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01706-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="01706-132">-Confirm</span></span>
<span data-ttu-id="01706-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="01706-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01706-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="01706-134">-WhatIf</span></span>
<span data-ttu-id="01706-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="01706-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01706-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="01706-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01706-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01706-137">CommonParameters</span></span>
<span data-ttu-id="01706-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01706-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01706-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="01706-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01706-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="01706-140">INPUTS</span></span>

### <span data-ttu-id="01706-141">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span><span class="sxs-lookup"><span data-stu-id="01706-141">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span></span>

## <span data-ttu-id="01706-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="01706-142">OUTPUTS</span></span>

### <span data-ttu-id="01706-143">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="01706-143">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span></span>

## <span data-ttu-id="01706-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="01706-144">NOTES</span></span>

<span data-ttu-id="01706-145">ALIASE</span><span class="sxs-lookup"><span data-stu-id="01706-145">ALIASES</span></span>

<span data-ttu-id="01706-146">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="01706-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="01706-147">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="01706-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="01706-148">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="01706-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="01706-149">INPUTOBJECT <IDedicatedHsmIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="01706-149">INPUTOBJECT <IDedicatedHsmIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="01706-150">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="01706-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="01706-151">`[Name <String>]`: Name des dedizierten Hsm</span><span class="sxs-lookup"><span data-stu-id="01706-151">`[Name <String>]`: Name of the dedicated Hsm</span></span>
  - <span data-ttu-id="01706-152">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, zu der die Ressource gehört.</span><span class="sxs-lookup"><span data-stu-id="01706-152">`[ResourceGroupName <String>]`: The name of the Resource Group to which the resource belongs.</span></span>
  - <span data-ttu-id="01706-153">`[SubscriptionId <String>]`: Abonnementanmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="01706-153">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="01706-154">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="01706-154">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="01706-155">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="01706-155">RELATED LINKS</span></span>

