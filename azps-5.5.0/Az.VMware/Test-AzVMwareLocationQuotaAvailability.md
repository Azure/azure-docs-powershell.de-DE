---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/test-azvmwarelocationquotaavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Test-AzVMwareLocationQuotaAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Test-AzVMwareLocationQuotaAvailability.md
ms.openlocfilehash: 93ede93fc47d5afcabeda8a38a4d8c5fc57c30c4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149769"
---
# <span data-ttu-id="8e24b-101">Test-AzVMwareLocationQuotaAvailability</span><span class="sxs-lookup"><span data-stu-id="8e24b-101">Test-AzVMwareLocationQuotaAvailability</span></span>

## <span data-ttu-id="8e24b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e24b-102">SYNOPSIS</span></span>
<span data-ttu-id="8e24b-103">Rückgabekontingent für Abonnement nach Region</span><span class="sxs-lookup"><span data-stu-id="8e24b-103">Return quota for subscription by region</span></span>

## <span data-ttu-id="8e24b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8e24b-104">SYNTAX</span></span>

### <span data-ttu-id="8e24b-105">Überprüfen (Standard)</span><span class="sxs-lookup"><span data-stu-id="8e24b-105">Check (Default)</span></span>
```
Test-AzVMwareLocationQuotaAvailability -Location <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8e24b-106">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8e24b-106">CheckViaIdentity</span></span>
```
Test-AzVMwareLocationQuotaAvailability -InputObject <IVMwareIdentity> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8e24b-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8e24b-107">DESCRIPTION</span></span>
<span data-ttu-id="8e24b-108">Rückgabekontingent für Abonnement nach Region</span><span class="sxs-lookup"><span data-stu-id="8e24b-108">Return quota for subscription by region</span></span>

## <span data-ttu-id="8e24b-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8e24b-109">EXAMPLES</span></span>

### <span data-ttu-id="8e24b-110">Beispiel 1: Überprüfen der Verfügbarkeit des Kontingents</span><span class="sxs-lookup"><span data-stu-id="8e24b-110">Example 1: Check quota availability</span></span>
```powershell
PS C:\> Test-AzVMwareLocationQuotaAvailability -Location eastus

Enabled
-------
Disabled
```

<span data-ttu-id="8e24b-111">Überprüfen der Verfügbarkeit des Kontingents</span><span class="sxs-lookup"><span data-stu-id="8e24b-111">Check quota availability</span></span>

## <span data-ttu-id="8e24b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e24b-112">PARAMETERS</span></span>

### <span data-ttu-id="8e24b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e24b-113">-DefaultProfile</span></span>
<span data-ttu-id="8e24b-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8e24b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e24b-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8e24b-115">-InputObject</span></span>
<span data-ttu-id="8e24b-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="8e24b-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity
Parameter Sets: CheckViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e24b-117">-Location</span><span class="sxs-lookup"><span data-stu-id="8e24b-117">-Location</span></span>
<span data-ttu-id="8e24b-118">Azure Region</span><span class="sxs-lookup"><span data-stu-id="8e24b-118">Azure region</span></span>

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

### <span data-ttu-id="8e24b-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8e24b-119">-SubscriptionId</span></span>
<span data-ttu-id="8e24b-120">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="8e24b-120">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="8e24b-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8e24b-121">-Confirm</span></span>
<span data-ttu-id="8e24b-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8e24b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e24b-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="8e24b-123">-WhatIf</span></span>
<span data-ttu-id="8e24b-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8e24b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e24b-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8e24b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e24b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e24b-126">CommonParameters</span></span>
<span data-ttu-id="8e24b-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e24b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e24b-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8e24b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e24b-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8e24b-129">INPUTS</span></span>

### <span data-ttu-id="8e24b-130">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span><span class="sxs-lookup"><span data-stu-id="8e24b-130">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span></span>

## <span data-ttu-id="8e24b-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8e24b-131">OUTPUTS</span></span>

### <span data-ttu-id="8e24b-132">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.IQuota</span><span class="sxs-lookup"><span data-stu-id="8e24b-132">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.IQuota</span></span>

## <span data-ttu-id="8e24b-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8e24b-133">NOTES</span></span>

<span data-ttu-id="8e24b-134">ALIASE</span><span class="sxs-lookup"><span data-stu-id="8e24b-134">ALIASES</span></span>

<span data-ttu-id="8e24b-135">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="8e24b-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8e24b-136">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8e24b-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8e24b-137">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8e24b-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8e24b-138">INPUTOBJECT <IVMwareIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="8e24b-138">INPUTOBJECT <IVMwareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8e24b-139">`[AuthorizationName <String>]`: Name der ExpressRoute-Schaltkreisautorisierung in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="8e24b-139">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="8e24b-140">`[ClusterName <String>]`: Name des Clusters in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="8e24b-140">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="8e24b-141">`[HcxEnterpriseSiteName <String>]`: Name der HCX -Unternehmenswebsite in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="8e24b-141">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="8e24b-142">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="8e24b-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8e24b-143">`[Location <String>]`: Region Azure</span><span class="sxs-lookup"><span data-stu-id="8e24b-143">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="8e24b-144">`[PrivateCloudName <String>]`: Name der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="8e24b-144">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="8e24b-145">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8e24b-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="8e24b-146">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="8e24b-146">The name is case insensitive.</span></span>
  - <span data-ttu-id="8e24b-147">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="8e24b-147">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="8e24b-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8e24b-148">RELATED LINKS</span></span>

