---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/powershell/module/az.dedicatedhsm/update-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Update-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Update-AzDedicatedHsm.md
ms.openlocfilehash: ba005802294ef4fa1c890230230cbd44bc783216
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932987"
---
# <span data-ttu-id="6a868-101">Update-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="6a868-101">Update-AzDedicatedHsm</span></span>

## <span data-ttu-id="6a868-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a868-102">SYNOPSIS</span></span>
<span data-ttu-id="6a868-103">Aktualisieren Sie ein dediziertes HSM im angegebenen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6a868-103">Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="6a868-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6a868-104">SYNTAX</span></span>

### <span data-ttu-id="6a868-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="6a868-105">UpdateExpanded (Default)</span></span>
```
Update-AzDedicatedHsm -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6a868-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="6a868-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzDedicatedHsm -InputObject <IDedicatedHsmIdentity> [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6a868-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6a868-107">DESCRIPTION</span></span>
<span data-ttu-id="6a868-108">Aktualisieren Sie ein dediziertes HSM im angegebenen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6a868-108">Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="6a868-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6a868-109">EXAMPLES</span></span>

### <span data-ttu-id="6a868-110">Beispiel 1: Aktualisieren des Parametertags des dedizierten HSM nach Name</span><span class="sxs-lookup"><span data-stu-id="6a868-110">Example 1: Update the parameter tag of the Dedicated HSM by name</span></span>
```powershell
PS C:\> Update-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz -Tag @{'key1' = '1'; 'key2' = 2; 'key3' = 3}

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="6a868-111">Mit diesem Befehl wird das Parametertag des Dedizierten HSM nach Name aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="6a868-111">This command updates the parameter tag of the Dedicated HSM by name</span></span>

### <span data-ttu-id="6a868-112">Beispiel 2: Aktualisieren des Parametertags des Dedizierten HSM nach -Objekt</span><span class="sxs-lookup"><span data-stu-id="6a868-112">Example 2: Update the parameter tag of the Dedicated HSM by object</span></span>
```powershell
PS C:\> $hsm = Get-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz 
PS C:\> Update-AzDedicatedHsm -InputObject -Tag @{'key1' = '1'; 'key2' = 2; 'key3' = 3}

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="6a868-113">Mit diesem Befehl wird das Parametertag des Dedizierten HSM nach -Objekts aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="6a868-113">This command updates the parameter tag of the Dedicated HSM by object</span></span>

## <span data-ttu-id="6a868-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6a868-114">PARAMETERS</span></span>

### <span data-ttu-id="6a868-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6a868-115">-AsJob</span></span>
<span data-ttu-id="6a868-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="6a868-116">Run the command as a job</span></span>

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

### <span data-ttu-id="6a868-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a868-117">-DefaultProfile</span></span>
<span data-ttu-id="6a868-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6a868-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a868-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6a868-119">-InputObject</span></span>
<span data-ttu-id="6a868-120">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="6a868-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6a868-121">-Name</span><span class="sxs-lookup"><span data-stu-id="6a868-121">-Name</span></span>
<span data-ttu-id="6a868-122">Name des dedizierten HSM</span><span class="sxs-lookup"><span data-stu-id="6a868-122">Name of the dedicated HSM</span></span>

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

### <span data-ttu-id="6a868-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="6a868-123">-NoWait</span></span>
<span data-ttu-id="6a868-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="6a868-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6a868-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a868-125">-ResourceGroupName</span></span>
<span data-ttu-id="6a868-126">Der Name der Ressourcengruppe, zu der der Server gehört.</span><span class="sxs-lookup"><span data-stu-id="6a868-126">The name of the Resource Group to which the server belongs.</span></span>

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

### <span data-ttu-id="6a868-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6a868-127">-SubscriptionId</span></span>
<span data-ttu-id="6a868-128">Abonnementanmeldeinformationen, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="6a868-128">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="6a868-129">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="6a868-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="6a868-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="6a868-130">-Tag</span></span>
<span data-ttu-id="6a868-131">Ressourcentags</span><span class="sxs-lookup"><span data-stu-id="6a868-131">Resource tags</span></span>

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

### <span data-ttu-id="6a868-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6a868-132">-Confirm</span></span>
<span data-ttu-id="6a868-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6a868-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a868-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a868-134">-WhatIf</span></span>
<span data-ttu-id="6a868-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6a868-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a868-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6a868-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a868-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a868-137">CommonParameters</span></span>
<span data-ttu-id="6a868-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a868-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a868-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6a868-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a868-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6a868-140">INPUTS</span></span>

### <span data-ttu-id="6a868-141">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span><span class="sxs-lookup"><span data-stu-id="6a868-141">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span></span>

## <span data-ttu-id="6a868-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6a868-142">OUTPUTS</span></span>

### <span data-ttu-id="6a868-143">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="6a868-143">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span></span>

## <span data-ttu-id="6a868-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="6a868-144">NOTES</span></span>

<span data-ttu-id="6a868-145">ALIASE</span><span class="sxs-lookup"><span data-stu-id="6a868-145">ALIASES</span></span>

<span data-ttu-id="6a868-146">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="6a868-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6a868-147">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="6a868-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6a868-148">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6a868-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6a868-149">INPUTOBJECT <IDedicatedHsmIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="6a868-149">INPUTOBJECT <IDedicatedHsmIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6a868-150">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="6a868-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6a868-151">`[Name <String>]`: Name des dedizierten Hsm</span><span class="sxs-lookup"><span data-stu-id="6a868-151">`[Name <String>]`: Name of the dedicated Hsm</span></span>
  - <span data-ttu-id="6a868-152">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, zu der die Ressource gehört.</span><span class="sxs-lookup"><span data-stu-id="6a868-152">`[ResourceGroupName <String>]`: The name of the Resource Group to which the resource belongs.</span></span>
  - <span data-ttu-id="6a868-153">`[SubscriptionId <String>]`: Abonnementanmeldeinformationen, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="6a868-153">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="6a868-154">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="6a868-154">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="6a868-155">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="6a868-155">RELATED LINKS</span></span>

