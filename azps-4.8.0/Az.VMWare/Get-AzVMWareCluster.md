---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWareCluster.md
ms.openlocfilehash: bf763e152c482c4a3fda4951715b01008a730533
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94007647"
---
# <span data-ttu-id="12b4f-101">Get-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="12b4f-101">Get-AzVMWareCluster</span></span>

## <span data-ttu-id="12b4f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="12b4f-102">SYNOPSIS</span></span>
<span data-ttu-id="12b4f-103">Abrufen eines Clusters anhand des Namens in einer privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="12b4f-103">Get a cluster by name in a private cloud</span></span>

## <span data-ttu-id="12b4f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="12b4f-104">SYNTAX</span></span>

### <span data-ttu-id="12b4f-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="12b4f-105">List (Default)</span></span>
```
Get-AzVMWareCluster -PrivateCloudName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="12b4f-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="12b4f-106">Get</span></span>
```
Get-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="12b4f-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="12b4f-107">GetViaIdentity</span></span>
```
Get-AzVMWareCluster -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="12b4f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="12b4f-108">DESCRIPTION</span></span>
<span data-ttu-id="12b4f-109">Abrufen eines Clusters anhand des Namens in einer privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="12b4f-109">Get a cluster by name in a private cloud</span></span>

## <span data-ttu-id="12b4f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="12b4f-110">EXAMPLES</span></span>

### <span data-ttu-id="12b4f-111">Beispiel 1: Abrufen von Cluster</span><span class="sxs-lookup"><span data-stu-id="12b4f-111">Example 1: Get cluster</span></span>
```powershell
PS C:\> Get-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="12b4f-112">Cluster abrufen</span><span class="sxs-lookup"><span data-stu-id="12b4f-112">Get cluster</span></span>

### <span data-ttu-id="12b4f-113">Beispiel 2: Auflisten von Clustern</span><span class="sxs-lookup"><span data-stu-id="12b4f-113">Example 2: List clusters</span></span>
```powershell
PS C:\> Get-AzVMWareCluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="12b4f-114">Listen Cluster</span><span class="sxs-lookup"><span data-stu-id="12b4f-114">List clusters</span></span>

## <span data-ttu-id="12b4f-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="12b4f-115">PARAMETERS</span></span>

### <span data-ttu-id="12b4f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12b4f-116">-DefaultProfile</span></span>
<span data-ttu-id="12b4f-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="12b4f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12b4f-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="12b4f-118">-InputObject</span></span>
<span data-ttu-id="12b4f-119">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="12b4f-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="12b4f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="12b4f-120">-Name</span></span>
<span data-ttu-id="12b4f-121">Name des Clusters in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="12b4f-121">Name of the cluster in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12b4f-122">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="12b4f-122">-PrivateCloudName</span></span>
<span data-ttu-id="12b4f-123">Name der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="12b4f-123">Name of the private cloud</span></span>

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

### <span data-ttu-id="12b4f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12b4f-124">-ResourceGroupName</span></span>
<span data-ttu-id="12b4f-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="12b4f-125">The name of the resource group.</span></span>
<span data-ttu-id="12b4f-126">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="12b4f-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="12b4f-127">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="12b4f-127">-SubscriptionId</span></span>
<span data-ttu-id="12b4f-128">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="12b4f-128">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12b4f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12b4f-129">CommonParameters</span></span>
<span data-ttu-id="12b4f-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12b4f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12b4f-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="12b4f-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12b4f-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="12b4f-132">INPUTS</span></span>

### <span data-ttu-id="12b4f-133">Microsoft. Azure. PowerShell. Cmdlets. VMware. Models. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="12b4f-133">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="12b4f-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="12b4f-134">OUTPUTS</span></span>

### <span data-ttu-id="12b4f-135">Microsoft. Azure. PowerShell. Cmdlets. VMware. Models. Api20200320. ICluster</span><span class="sxs-lookup"><span data-stu-id="12b4f-135">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="12b4f-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="12b4f-136">NOTES</span></span>

<span data-ttu-id="12b4f-137">Aliase</span><span class="sxs-lookup"><span data-stu-id="12b4f-137">ALIASES</span></span>

<span data-ttu-id="12b4f-138">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="12b4f-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="12b4f-139">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="12b4f-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="12b4f-140">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="12b4f-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="12b4f-141">Inputobject <IVMWareIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="12b4f-141">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="12b4f-142">`[AuthorizationName <String>]`: Name der Express Route-Schaltkreis Autorisierung in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="12b4f-142">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="12b4f-143">`[ClusterName <String>]`: Name des Clusters in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="12b4f-143">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="12b4f-144">`[HcxEnterpriseSiteName <String>]`: Name der HCx Enterprise-Website in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="12b4f-144">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="12b4f-145">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="12b4f-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="12b4f-146">`[Location <String>]`: Azure-Bereich</span><span class="sxs-lookup"><span data-stu-id="12b4f-146">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="12b4f-147">`[PrivateCloudName <String>]`: Name der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="12b4f-147">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="12b4f-148">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="12b4f-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="12b4f-149">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="12b4f-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="12b4f-150">`[SubscriptionId <String>]`: Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="12b4f-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="12b4f-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="12b4f-151">RELATED LINKS</span></span>

