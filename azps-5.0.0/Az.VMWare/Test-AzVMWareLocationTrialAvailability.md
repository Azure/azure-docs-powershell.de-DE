---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/test-azvmwarelocationtrialavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Test-AzVMWareLocationTrialAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Test-AzVMWareLocationTrialAvailability.md
ms.openlocfilehash: 942ac0b4a8bca964e88c7dfd327fe460f249a915
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303255"
---
# <span data-ttu-id="56217-101">Test-AzVMWareLocationTrialAvailability</span><span class="sxs-lookup"><span data-stu-id="56217-101">Test-AzVMWareLocationTrialAvailability</span></span>

## <span data-ttu-id="56217-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="56217-102">SYNOPSIS</span></span>
<span data-ttu-id="56217-103">Teststatus für Abonnement nach Region zurückgeben</span><span class="sxs-lookup"><span data-stu-id="56217-103">Return trial status for subscription by region</span></span>

## <span data-ttu-id="56217-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="56217-104">SYNTAX</span></span>

### <span data-ttu-id="56217-105">Überprüfen (Standard)</span><span class="sxs-lookup"><span data-stu-id="56217-105">Check (Default)</span></span>
```
Test-AzVMWareLocationTrialAvailability -Location <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="56217-106">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="56217-106">CheckViaIdentity</span></span>
```
Test-AzVMWareLocationTrialAvailability -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="56217-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="56217-107">DESCRIPTION</span></span>
<span data-ttu-id="56217-108">Teststatus für Abonnement nach Region zurückgeben</span><span class="sxs-lookup"><span data-stu-id="56217-108">Return trial status for subscription by region</span></span>

## <span data-ttu-id="56217-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="56217-109">EXAMPLES</span></span>

### <span data-ttu-id="56217-110">Beispiel 1: Prüfen der Verfügbarkeit von Testversionen</span><span class="sxs-lookup"><span data-stu-id="56217-110">Example 1: Check trial availability</span></span>
```powershell
PS C:\> Test-AzVMWareLocationTrialAvailability -Location australiaeast

AvailableHost Status
------------- ------
0             TrialDisabled
```

<span data-ttu-id="56217-111">Prüfen der Verfügbarkeit von Testversionen</span><span class="sxs-lookup"><span data-stu-id="56217-111">Check trial availability</span></span>

## <span data-ttu-id="56217-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="56217-112">PARAMETERS</span></span>

### <span data-ttu-id="56217-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56217-113">-DefaultProfile</span></span>
<span data-ttu-id="56217-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="56217-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56217-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="56217-115">-InputObject</span></span>
<span data-ttu-id="56217-116">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="56217-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="56217-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="56217-117">-Location</span></span>
<span data-ttu-id="56217-118">Azure-Bereich</span><span class="sxs-lookup"><span data-stu-id="56217-118">Azure region</span></span>

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

### <span data-ttu-id="56217-119">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="56217-119">-SubscriptionId</span></span>
<span data-ttu-id="56217-120">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="56217-120">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="56217-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="56217-121">-Confirm</span></span>
<span data-ttu-id="56217-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="56217-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56217-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56217-123">-WhatIf</span></span>
<span data-ttu-id="56217-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="56217-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56217-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="56217-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56217-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56217-126">CommonParameters</span></span>
<span data-ttu-id="56217-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56217-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56217-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="56217-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56217-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="56217-129">INPUTS</span></span>

### <span data-ttu-id="56217-130">Microsoft. Azure. PowerShell. Cmdlets. VMware. Models. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="56217-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="56217-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="56217-131">OUTPUTS</span></span>

### <span data-ttu-id="56217-132">Microsoft. Azure. PowerShell. Cmdlets. VMware. Models. Api20200320. ITrial</span><span class="sxs-lookup"><span data-stu-id="56217-132">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ITrial</span></span>

## <span data-ttu-id="56217-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="56217-133">NOTES</span></span>

<span data-ttu-id="56217-134">Aliase</span><span class="sxs-lookup"><span data-stu-id="56217-134">ALIASES</span></span>

<span data-ttu-id="56217-135">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="56217-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="56217-136">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="56217-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="56217-137">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="56217-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="56217-138">Inputobject <IVMWareIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="56217-138">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="56217-139">`[AuthorizationName <String>]`: Name der Express Route-Schaltkreis Autorisierung in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="56217-139">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="56217-140">`[ClusterName <String>]`: Name des Clusters in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="56217-140">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="56217-141">`[HcxEnterpriseSiteName <String>]`: Name der HCx Enterprise-Website in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="56217-141">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="56217-142">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="56217-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="56217-143">`[Location <String>]`: Azure-Bereich</span><span class="sxs-lookup"><span data-stu-id="56217-143">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="56217-144">`[PrivateCloudName <String>]`: Name der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="56217-144">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="56217-145">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="56217-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="56217-146">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="56217-146">The name is case insensitive.</span></span>
  - <span data-ttu-id="56217-147">`[SubscriptionId <String>]`: Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="56217-147">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="56217-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="56217-148">RELATED LINKS</span></span>

