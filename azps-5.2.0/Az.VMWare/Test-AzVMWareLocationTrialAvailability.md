---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/test-azvmwarelocationtrialavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Test-AzVMWareLocationTrialAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Test-AzVMWareLocationTrialAvailability.md
ms.openlocfilehash: 942ac0b4a8bca964e88c7dfd327fe460f249a915
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98308672"
---
# <span data-ttu-id="897a2-101">Test-AzVMWareLocationTrialAvailability</span><span class="sxs-lookup"><span data-stu-id="897a2-101">Test-AzVMWareLocationTrialAvailability</span></span>

## <span data-ttu-id="897a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="897a2-102">SYNOPSIS</span></span>
<span data-ttu-id="897a2-103">Status der Rückgabe des Testabonnements nach Region</span><span class="sxs-lookup"><span data-stu-id="897a2-103">Return trial status for subscription by region</span></span>

## <span data-ttu-id="897a2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="897a2-104">SYNTAX</span></span>

### <span data-ttu-id="897a2-105">Überprüfen (Standard)</span><span class="sxs-lookup"><span data-stu-id="897a2-105">Check (Default)</span></span>
```
Test-AzVMWareLocationTrialAvailability -Location <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="897a2-106">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="897a2-106">CheckViaIdentity</span></span>
```
Test-AzVMWareLocationTrialAvailability -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="897a2-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="897a2-107">DESCRIPTION</span></span>
<span data-ttu-id="897a2-108">Status der Rückgabe des Testabonnements nach Region</span><span class="sxs-lookup"><span data-stu-id="897a2-108">Return trial status for subscription by region</span></span>

## <span data-ttu-id="897a2-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="897a2-109">EXAMPLES</span></span>

### <span data-ttu-id="897a2-110">Beispiel 1: Überprüfen der Verfügbarkeit von Testversionen</span><span class="sxs-lookup"><span data-stu-id="897a2-110">Example 1: Check trial availability</span></span>
```powershell
PS C:\> Test-AzVMWareLocationTrialAvailability -Location australiaeast

AvailableHost Status
------------- ------
0             TrialDisabled
```

<span data-ttu-id="897a2-111">Prüfen der Verfügbarkeit von Testversionen</span><span class="sxs-lookup"><span data-stu-id="897a2-111">Check trial availability</span></span>

## <span data-ttu-id="897a2-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="897a2-112">PARAMETERS</span></span>

### <span data-ttu-id="897a2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="897a2-113">-DefaultProfile</span></span>
<span data-ttu-id="897a2-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="897a2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="897a2-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="897a2-115">-InputObject</span></span>
<span data-ttu-id="897a2-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="897a2-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: CheckViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="897a2-117">-Location</span><span class="sxs-lookup"><span data-stu-id="897a2-117">-Location</span></span>
<span data-ttu-id="897a2-118">Azure Region</span><span class="sxs-lookup"><span data-stu-id="897a2-118">Azure region</span></span>

```yaml
Type: System.String
Parameter Sets: Check
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="897a2-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="897a2-119">-SubscriptionId</span></span>
<span data-ttu-id="897a2-120">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="897a2-120">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Check
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="897a2-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="897a2-121">-Confirm</span></span>
<span data-ttu-id="897a2-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="897a2-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="897a2-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="897a2-123">-WhatIf</span></span>
<span data-ttu-id="897a2-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="897a2-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="897a2-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="897a2-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="897a2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="897a2-126">CommonParameters</span></span>
<span data-ttu-id="897a2-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="897a2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="897a2-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="897a2-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="897a2-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="897a2-129">INPUTS</span></span>

### <span data-ttu-id="897a2-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="897a2-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="897a2-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="897a2-131">OUTPUTS</span></span>

### <span data-ttu-id="897a2-132">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ITrial</span><span class="sxs-lookup"><span data-stu-id="897a2-132">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ITrial</span></span>

## <span data-ttu-id="897a2-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="897a2-133">NOTES</span></span>

<span data-ttu-id="897a2-134">ALIASE</span><span class="sxs-lookup"><span data-stu-id="897a2-134">ALIASES</span></span>

<span data-ttu-id="897a2-135">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="897a2-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="897a2-136">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="897a2-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="897a2-137">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="897a2-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="897a2-138">INPUTOBJECT <IVMWareIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="897a2-138">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="897a2-139">`[AuthorizationName <String>]`: Name der ExpressRoute-Schaltkreisautorisierung in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="897a2-139">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="897a2-140">`[ClusterName <String>]`: Name des Clusters in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="897a2-140">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="897a2-141">`[HcxEnterpriseSiteName <String>]`: Name der HCX -Unternehmenswebsite in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="897a2-141">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="897a2-142">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="897a2-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="897a2-143">`[Location <String>]`: Region Azure</span><span class="sxs-lookup"><span data-stu-id="897a2-143">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="897a2-144">`[PrivateCloudName <String>]`: Name der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="897a2-144">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="897a2-145">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="897a2-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="897a2-146">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="897a2-146">The name is case insensitive.</span></span>
  - <span data-ttu-id="897a2-147">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="897a2-147">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="897a2-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="897a2-148">RELATED LINKS</span></span>

