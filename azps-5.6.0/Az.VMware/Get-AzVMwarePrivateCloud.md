---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/get-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwarePrivateCloud.md
ms.openlocfilehash: ae53ac56d60d61340e2592233901556a0e1d6b62
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937248"
---
# <span data-ttu-id="7eb20-101">Get-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="7eb20-101">Get-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="7eb20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7eb20-102">SYNOPSIS</span></span>
<span data-ttu-id="7eb20-103">Eine private Cloud erhalten</span><span class="sxs-lookup"><span data-stu-id="7eb20-103">Get a private cloud</span></span>

## <span data-ttu-id="7eb20-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7eb20-104">SYNTAX</span></span>

### <span data-ttu-id="7eb20-105">List1 (Standard)</span><span class="sxs-lookup"><span data-stu-id="7eb20-105">List1 (Default)</span></span>
```
Get-AzVMWarePrivateCloud [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7eb20-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="7eb20-106">Get</span></span>
```
Get-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7eb20-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7eb20-107">GetViaIdentity</span></span>
```
Get-AzVMWarePrivateCloud -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7eb20-108">Liste</span><span class="sxs-lookup"><span data-stu-id="7eb20-108">List</span></span>
```
Get-AzVMWarePrivateCloud -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="7eb20-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7eb20-109">DESCRIPTION</span></span>
<span data-ttu-id="7eb20-110">Eine private Cloud erhalten</span><span class="sxs-lookup"><span data-stu-id="7eb20-110">Get a private cloud</span></span>

## <span data-ttu-id="7eb20-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7eb20-111">EXAMPLES</span></span>

### <span data-ttu-id="7eb20-112">Beispiel 1: Auflisten der privaten Cloud unter Abonnement</span><span class="sxs-lookup"><span data-stu-id="7eb20-112">Example 1: List private cloud under subscription</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="7eb20-113">Private Cloud unter Abonnement auflisten</span><span class="sxs-lookup"><span data-stu-id="7eb20-113">List private cloud under subscription</span></span>

### <span data-ttu-id="7eb20-114">Beispiel 2: Auflisten der privaten Cloud unter Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="7eb20-114">Example 2: List private cloud under resource group</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud -ResourceGroupName azps-test-group

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="7eb20-115">Auflisten der privaten Cloud unter Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="7eb20-115">List private cloud under resource group</span></span>

### <span data-ttu-id="7eb20-116">Beispiel 3: Private Cloud erhalten</span><span class="sxs-lookup"><span data-stu-id="7eb20-116">Example 3: Get private cloud</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="7eb20-117">Private Cloud erhalten</span><span class="sxs-lookup"><span data-stu-id="7eb20-117">Get private cloud</span></span>

## <span data-ttu-id="7eb20-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="7eb20-118">PARAMETERS</span></span>

### <span data-ttu-id="7eb20-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7eb20-119">-DefaultProfile</span></span>
<span data-ttu-id="7eb20-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7eb20-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7eb20-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7eb20-121">-InputObject</span></span>
<span data-ttu-id="7eb20-122">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="7eb20-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7eb20-123">-Name</span><span class="sxs-lookup"><span data-stu-id="7eb20-123">-Name</span></span>
<span data-ttu-id="7eb20-124">Name der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="7eb20-124">Name of the private cloud</span></span>

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

### <span data-ttu-id="7eb20-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7eb20-125">-ResourceGroupName</span></span>
<span data-ttu-id="7eb20-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7eb20-126">The name of the resource group.</span></span>
<span data-ttu-id="7eb20-127">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="7eb20-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="7eb20-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7eb20-128">-SubscriptionId</span></span>
<span data-ttu-id="7eb20-129">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="7eb20-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="7eb20-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7eb20-130">CommonParameters</span></span>
<span data-ttu-id="7eb20-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7eb20-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7eb20-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7eb20-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7eb20-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7eb20-133">INPUTS</span></span>

### <span data-ttu-id="7eb20-134">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="7eb20-134">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="7eb20-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7eb20-135">OUTPUTS</span></span>

### <span data-ttu-id="7eb20-136">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span><span class="sxs-lookup"><span data-stu-id="7eb20-136">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="7eb20-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="7eb20-137">NOTES</span></span>

<span data-ttu-id="7eb20-138">ALIASE</span><span class="sxs-lookup"><span data-stu-id="7eb20-138">ALIASES</span></span>

<span data-ttu-id="7eb20-139">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="7eb20-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7eb20-140">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="7eb20-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7eb20-141">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7eb20-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7eb20-142">INPUTOBJECT <IVMWareIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="7eb20-142">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7eb20-143">`[AuthorizationName <String>]`: Name der ExpressRoute-Schaltkreisautorisierung in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="7eb20-143">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="7eb20-144">`[ClusterName <String>]`: Name des Clusters in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="7eb20-144">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="7eb20-145">`[HcxEnterpriseSiteName <String>]`: Name der HCX Enterprise-Website in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="7eb20-145">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="7eb20-146">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="7eb20-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7eb20-147">`[Location <String>]`: Azure Region</span><span class="sxs-lookup"><span data-stu-id="7eb20-147">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="7eb20-148">`[PrivateCloudName <String>]`: Name der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="7eb20-148">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="7eb20-149">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7eb20-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="7eb20-150">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="7eb20-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="7eb20-151">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="7eb20-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="7eb20-152">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="7eb20-152">RELATED LINKS</span></span>

