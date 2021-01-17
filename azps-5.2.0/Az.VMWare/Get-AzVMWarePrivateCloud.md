---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWarePrivateCloud.md
ms.openlocfilehash: 31400d3b9b6e57190a852ae579fffcaa9fc60401
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364271"
---
# <span data-ttu-id="75c6e-101">Get-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="75c6e-101">Get-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="75c6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75c6e-102">SYNOPSIS</span></span>
<span data-ttu-id="75c6e-103">Erhalten einer privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="75c6e-103">Get a private cloud</span></span>

## <span data-ttu-id="75c6e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="75c6e-104">SYNTAX</span></span>

### <span data-ttu-id="75c6e-105">Liste1 (Standard)</span><span class="sxs-lookup"><span data-stu-id="75c6e-105">List1 (Default)</span></span>
```
Get-AzVMWarePrivateCloud [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="75c6e-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="75c6e-106">Get</span></span>
```
Get-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="75c6e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="75c6e-107">GetViaIdentity</span></span>
```
Get-AzVMWarePrivateCloud -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="75c6e-108">Liste</span><span class="sxs-lookup"><span data-stu-id="75c6e-108">List</span></span>
```
Get-AzVMWarePrivateCloud -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="75c6e-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="75c6e-109">DESCRIPTION</span></span>
<span data-ttu-id="75c6e-110">Erhalten einer privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="75c6e-110">Get a private cloud</span></span>

## <span data-ttu-id="75c6e-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="75c6e-111">EXAMPLES</span></span>

### <span data-ttu-id="75c6e-112">Beispiel 1: Auflisten der privaten Cloud im Abonnement</span><span class="sxs-lookup"><span data-stu-id="75c6e-112">Example 1: List private cloud under subscription</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="75c6e-113">Private Cloud unter Abonnement auflisten</span><span class="sxs-lookup"><span data-stu-id="75c6e-113">List private cloud under subscription</span></span>

### <span data-ttu-id="75c6e-114">Beispiel 2: Auflisten der privaten Cloud unter der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="75c6e-114">Example 2: List private cloud under resource group</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud -ResourceGroupName azps-test-group

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="75c6e-115">Auflisten der privaten Cloud unter der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="75c6e-115">List private cloud under resource group</span></span>

### <span data-ttu-id="75c6e-116">Beispiel 3: Private Cloud erhalten</span><span class="sxs-lookup"><span data-stu-id="75c6e-116">Example 3: Get private cloud</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="75c6e-117">Holen Sie sich die private Cloud</span><span class="sxs-lookup"><span data-stu-id="75c6e-117">Get private cloud</span></span>

## <span data-ttu-id="75c6e-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75c6e-118">PARAMETERS</span></span>

### <span data-ttu-id="75c6e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75c6e-119">-DefaultProfile</span></span>
<span data-ttu-id="75c6e-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="75c6e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75c6e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="75c6e-121">-InputObject</span></span>
<span data-ttu-id="75c6e-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="75c6e-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75c6e-123">-Name</span><span class="sxs-lookup"><span data-stu-id="75c6e-123">-Name</span></span>
<span data-ttu-id="75c6e-124">Name der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="75c6e-124">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: PrivateCloudName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75c6e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75c6e-125">-ResourceGroupName</span></span>
<span data-ttu-id="75c6e-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="75c6e-126">The name of the resource group.</span></span>
<span data-ttu-id="75c6e-127">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="75c6e-127">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75c6e-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="75c6e-128">-SubscriptionId</span></span>
<span data-ttu-id="75c6e-129">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="75c6e-129">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75c6e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75c6e-130">CommonParameters</span></span>
<span data-ttu-id="75c6e-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75c6e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75c6e-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="75c6e-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75c6e-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="75c6e-133">INPUTS</span></span>

### <span data-ttu-id="75c6e-134">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="75c6e-134">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="75c6e-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="75c6e-135">OUTPUTS</span></span>

### <span data-ttu-id="75c6e-136">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span><span class="sxs-lookup"><span data-stu-id="75c6e-136">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="75c6e-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="75c6e-137">NOTES</span></span>

<span data-ttu-id="75c6e-138">ALIASE</span><span class="sxs-lookup"><span data-stu-id="75c6e-138">ALIASES</span></span>

<span data-ttu-id="75c6e-139">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="75c6e-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="75c6e-140">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="75c6e-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="75c6e-141">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="75c6e-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="75c6e-142">INPUTOBJECT <IVMWareIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="75c6e-142">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="75c6e-143">`[AuthorizationName <String>]`: Name der ExpressRoute-Schaltkreisautorisierung in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="75c6e-143">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="75c6e-144">`[ClusterName <String>]`: Name des Clusters in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="75c6e-144">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="75c6e-145">`[HcxEnterpriseSiteName <String>]`: Name der HCX -Unternehmenswebsite in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="75c6e-145">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="75c6e-146">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="75c6e-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="75c6e-147">`[Location <String>]`: Region Azure</span><span class="sxs-lookup"><span data-stu-id="75c6e-147">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="75c6e-148">`[PrivateCloudName <String>]`: Name der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="75c6e-148">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="75c6e-149">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="75c6e-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="75c6e-150">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="75c6e-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="75c6e-151">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="75c6e-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="75c6e-152">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="75c6e-152">RELATED LINKS</span></span>

