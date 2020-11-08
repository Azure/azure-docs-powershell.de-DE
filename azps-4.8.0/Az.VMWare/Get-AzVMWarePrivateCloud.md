---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWarePrivateCloud.md
ms.openlocfilehash: 31400d3b9b6e57190a852ae579fffcaa9fc60401
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173645"
---
# <span data-ttu-id="5d0b3-101">Get-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="5d0b3-101">Get-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="5d0b3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5d0b3-102">SYNOPSIS</span></span>
<span data-ttu-id="5d0b3-103">Besorgen Sie sich eine Private Cloud</span><span class="sxs-lookup"><span data-stu-id="5d0b3-103">Get a private cloud</span></span>

## <span data-ttu-id="5d0b3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5d0b3-104">SYNTAX</span></span>

### <span data-ttu-id="5d0b3-105">List1 (Standard)</span><span class="sxs-lookup"><span data-stu-id="5d0b3-105">List1 (Default)</span></span>
```
Get-AzVMWarePrivateCloud [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5d0b3-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="5d0b3-106">Get</span></span>
```
Get-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5d0b3-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5d0b3-107">GetViaIdentity</span></span>
```
Get-AzVMWarePrivateCloud -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5d0b3-108">Liste</span><span class="sxs-lookup"><span data-stu-id="5d0b3-108">List</span></span>
```
Get-AzVMWarePrivateCloud -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="5d0b3-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5d0b3-109">DESCRIPTION</span></span>
<span data-ttu-id="5d0b3-110">Besorgen Sie sich eine Private Cloud</span><span class="sxs-lookup"><span data-stu-id="5d0b3-110">Get a private cloud</span></span>

## <span data-ttu-id="5d0b3-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5d0b3-111">EXAMPLES</span></span>

### <span data-ttu-id="5d0b3-112">Beispiel 1: Auflisten der privaten Cloud unter "Abonnement"</span><span class="sxs-lookup"><span data-stu-id="5d0b3-112">Example 1: List private cloud under subscription</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="5d0b3-113">Private Cloud-Liste unter Abonnement</span><span class="sxs-lookup"><span data-stu-id="5d0b3-113">List private cloud under subscription</span></span>

### <span data-ttu-id="5d0b3-114">Beispiel 2: Auflisten der privaten Cloud unter Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="5d0b3-114">Example 2: List private cloud under resource group</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud -ResourceGroupName azps-test-group

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="5d0b3-115">Private Cloud auflisten unter Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="5d0b3-115">List private cloud under resource group</span></span>

### <span data-ttu-id="5d0b3-116">Beispiel 3: Abrufen der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="5d0b3-116">Example 3: Get private cloud</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="5d0b3-117">Private Cloud abrufen</span><span class="sxs-lookup"><span data-stu-id="5d0b3-117">Get private cloud</span></span>

## <span data-ttu-id="5d0b3-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="5d0b3-118">PARAMETERS</span></span>

### <span data-ttu-id="5d0b3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d0b3-119">-DefaultProfile</span></span>
<span data-ttu-id="5d0b3-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5d0b3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d0b3-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5d0b3-121">-InputObject</span></span>
<span data-ttu-id="5d0b3-122">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="5d0b3-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5d0b3-123">-Name</span><span class="sxs-lookup"><span data-stu-id="5d0b3-123">-Name</span></span>
<span data-ttu-id="5d0b3-124">Name der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="5d0b3-124">Name of the private cloud</span></span>

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

### <span data-ttu-id="5d0b3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d0b3-125">-ResourceGroupName</span></span>
<span data-ttu-id="5d0b3-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5d0b3-126">The name of the resource group.</span></span>
<span data-ttu-id="5d0b3-127">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="5d0b3-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="5d0b3-128">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="5d0b3-128">-SubscriptionId</span></span>
<span data-ttu-id="5d0b3-129">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="5d0b3-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="5d0b3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d0b3-130">CommonParameters</span></span>
<span data-ttu-id="5d0b3-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d0b3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d0b3-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5d0b3-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d0b3-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5d0b3-133">INPUTS</span></span>

### <span data-ttu-id="5d0b3-134">Microsoft. Azure. PowerShell. Cmdlets. VMware. Models. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="5d0b3-134">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="5d0b3-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5d0b3-135">OUTPUTS</span></span>

### <span data-ttu-id="5d0b3-136">Microsoft. Azure. PowerShell. Cmdlets. VMware. Models. Api20200320. IPrivateCloud</span><span class="sxs-lookup"><span data-stu-id="5d0b3-136">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="5d0b3-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="5d0b3-137">NOTES</span></span>

<span data-ttu-id="5d0b3-138">Aliase</span><span class="sxs-lookup"><span data-stu-id="5d0b3-138">ALIASES</span></span>

<span data-ttu-id="5d0b3-139">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5d0b3-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5d0b3-140">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5d0b3-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5d0b3-141">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="5d0b3-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5d0b3-142">Inputobject <IVMWareIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="5d0b3-142">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5d0b3-143">`[AuthorizationName <String>]`: Name der Express Route-Schaltkreis Autorisierung in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="5d0b3-143">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="5d0b3-144">`[ClusterName <String>]`: Name des Clusters in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="5d0b3-144">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="5d0b3-145">`[HcxEnterpriseSiteName <String>]`: Name der HCx Enterprise-Website in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="5d0b3-145">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="5d0b3-146">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="5d0b3-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5d0b3-147">`[Location <String>]`: Azure-Bereich</span><span class="sxs-lookup"><span data-stu-id="5d0b3-147">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="5d0b3-148">`[PrivateCloudName <String>]`: Name der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="5d0b3-148">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="5d0b3-149">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5d0b3-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="5d0b3-150">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="5d0b3-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="5d0b3-151">`[SubscriptionId <String>]`: Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="5d0b3-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="5d0b3-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5d0b3-152">RELATED LINKS</span></span>

