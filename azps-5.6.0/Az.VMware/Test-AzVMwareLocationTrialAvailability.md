---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/test-azvmwarelocationtrialavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Test-AzVMwareLocationTrialAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Test-AzVMwareLocationTrialAvailability.md
ms.openlocfilehash: 133dc4dd259025556ab5f8dd3b848ae70a5101c7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937232"
---
# <span data-ttu-id="cde14-101">Test-AzVMWareLocationTrialAvailability</span><span class="sxs-lookup"><span data-stu-id="cde14-101">Test-AzVMWareLocationTrialAvailability</span></span>

## <span data-ttu-id="cde14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cde14-102">SYNOPSIS</span></span>
<span data-ttu-id="cde14-103">Rückgabeversuchsstatus für Abonnement nach Region</span><span class="sxs-lookup"><span data-stu-id="cde14-103">Return trial status for subscription by region</span></span>

## <span data-ttu-id="cde14-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cde14-104">SYNTAX</span></span>

### <span data-ttu-id="cde14-105">Überprüfen (Standard)</span><span class="sxs-lookup"><span data-stu-id="cde14-105">Check (Default)</span></span>
```
Test-AzVMWareLocationTrialAvailability -Location <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cde14-106">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cde14-106">CheckViaIdentity</span></span>
```
Test-AzVMWareLocationTrialAvailability -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cde14-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cde14-107">DESCRIPTION</span></span>
<span data-ttu-id="cde14-108">Rückgabeversuchsstatus für Abonnement nach Region</span><span class="sxs-lookup"><span data-stu-id="cde14-108">Return trial status for subscription by region</span></span>

## <span data-ttu-id="cde14-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cde14-109">EXAMPLES</span></span>

### <span data-ttu-id="cde14-110">Beispiel 1: Überprüfen der Verfügbarkeit von Testversionen</span><span class="sxs-lookup"><span data-stu-id="cde14-110">Example 1: Check trial availability</span></span>
```powershell
PS C:\> Test-AzVMWareLocationTrialAvailability -Location australiaeast

AvailableHost Status
------------- ------
0             TrialDisabled
```

<span data-ttu-id="cde14-111">Überprüfen der Verfügbarkeit von Testversionen</span><span class="sxs-lookup"><span data-stu-id="cde14-111">Check trial availability</span></span>

## <span data-ttu-id="cde14-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="cde14-112">PARAMETERS</span></span>

### <span data-ttu-id="cde14-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cde14-113">-DefaultProfile</span></span>
<span data-ttu-id="cde14-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cde14-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cde14-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cde14-115">-InputObject</span></span>
<span data-ttu-id="cde14-116">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="cde14-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="cde14-117">-Location</span><span class="sxs-lookup"><span data-stu-id="cde14-117">-Location</span></span>
<span data-ttu-id="cde14-118">Azure-Region</span><span class="sxs-lookup"><span data-stu-id="cde14-118">Azure region</span></span>

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

### <span data-ttu-id="cde14-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cde14-119">-SubscriptionId</span></span>
<span data-ttu-id="cde14-120">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="cde14-120">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="cde14-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cde14-121">-Confirm</span></span>
<span data-ttu-id="cde14-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cde14-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cde14-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cde14-123">-WhatIf</span></span>
<span data-ttu-id="cde14-124">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cde14-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cde14-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cde14-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cde14-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cde14-126">CommonParameters</span></span>
<span data-ttu-id="cde14-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cde14-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cde14-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cde14-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cde14-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cde14-129">INPUTS</span></span>

### <span data-ttu-id="cde14-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="cde14-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="cde14-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cde14-131">OUTPUTS</span></span>

### <span data-ttu-id="cde14-132">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ITrial</span><span class="sxs-lookup"><span data-stu-id="cde14-132">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ITrial</span></span>

## <span data-ttu-id="cde14-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="cde14-133">NOTES</span></span>

<span data-ttu-id="cde14-134">ALIASE</span><span class="sxs-lookup"><span data-stu-id="cde14-134">ALIASES</span></span>

<span data-ttu-id="cde14-135">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="cde14-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cde14-136">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="cde14-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cde14-137">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cde14-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cde14-138">INPUTOBJECT <IVMWareIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="cde14-138">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cde14-139">`[AuthorizationName <String>]`: Name der ExpressRoute-Schaltkreisautorisierung in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="cde14-139">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="cde14-140">`[ClusterName <String>]`: Name des Clusters in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="cde14-140">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="cde14-141">`[HcxEnterpriseSiteName <String>]`: Name der HCX Enterprise-Website in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="cde14-141">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="cde14-142">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="cde14-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cde14-143">`[Location <String>]`: Azure Region</span><span class="sxs-lookup"><span data-stu-id="cde14-143">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="cde14-144">`[PrivateCloudName <String>]`: Name der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="cde14-144">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="cde14-145">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="cde14-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="cde14-146">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="cde14-146">The name is case insensitive.</span></span>
  - <span data-ttu-id="cde14-147">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="cde14-147">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="cde14-148">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="cde14-148">RELATED LINKS</span></span>

