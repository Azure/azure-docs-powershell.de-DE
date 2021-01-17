---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoCluster.md
ms.openlocfilehash: 99afad24d33cfd6a614100b5bc53406f04965ba9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472459"
---
# <span data-ttu-id="e277d-101">Get-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="e277d-101">Get-AzKustoCluster</span></span>

## <span data-ttu-id="e277d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e277d-102">SYNOPSIS</span></span>
<span data-ttu-id="e277d-103">Ruft einen "Kusto"-Cluster ab.</span><span class="sxs-lookup"><span data-stu-id="e277d-103">Gets a Kusto cluster.</span></span>

## <span data-ttu-id="e277d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e277d-104">SYNTAX</span></span>

### <span data-ttu-id="e277d-105">Liste1 (Standard)</span><span class="sxs-lookup"><span data-stu-id="e277d-105">List1 (Default)</span></span>
```
Get-AzKustoCluster [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e277d-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="e277d-106">Get</span></span>
```
Get-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e277d-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e277d-107">GetViaIdentity</span></span>
```
Get-AzKustoCluster -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e277d-108">Liste</span><span class="sxs-lookup"><span data-stu-id="e277d-108">List</span></span>
```
Get-AzKustoCluster -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="e277d-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e277d-109">DESCRIPTION</span></span>
<span data-ttu-id="e277d-110">Ruft einen "Kusto"-Cluster ab.</span><span class="sxs-lookup"><span data-stu-id="e277d-110">Gets a Kusto cluster.</span></span>

## <span data-ttu-id="e277d-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e277d-111">EXAMPLES</span></span>

### <span data-ttu-id="e277d-112">Beispiel 1: Auflisten aller Kusto-Cluster in einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="e277d-112">Example 1: List all Kusto clusters in a resource group</span></span>
```powershell
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg

Location Name                 Type                     Zone
-------- ----                 ----                     ----
East US  testnewkustocluster  Microsoft.Kusto/Clusters
East US  testnewkustocluster2 Microsoft.Kusto/Clusters
```

<span data-ttu-id="e277d-113">Der oben aufgeführte Befehl listet alle Kusto-Cluster in der Ressourcengruppe "testrg" auf.</span><span class="sxs-lookup"><span data-stu-id="e277d-113">The above command lists all Kusto clusters in the resource group "testrg".</span></span>

### <span data-ttu-id="e277d-114">Beispiel 2: Erhalten eines bestimmten Kusto-Cluster nach Name</span><span class="sxs-lookup"><span data-stu-id="e277d-114">Example 2: Get a specific Kusto cluster by name</span></span>
```powershell
PS C:\>  Get-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="e277d-115">Der oben aufgeführte Befehl gibt den Cluster "Kusto" mit dem Namen "testnewkustocluster" in der Ressourcengruppe "testrg" zurück.</span><span class="sxs-lookup"><span data-stu-id="e277d-115">The above command returns the Kusto cluster named "testnewkustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="e277d-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e277d-116">PARAMETERS</span></span>

### <span data-ttu-id="e277d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e277d-117">-DefaultProfile</span></span>
<span data-ttu-id="e277d-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e277d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e277d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e277d-119">-InputObject</span></span>
<span data-ttu-id="e277d-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="e277d-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e277d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e277d-121">-Name</span></span>
<span data-ttu-id="e277d-122">Der Name des Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="e277d-122">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="e277d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e277d-123">-ResourceGroupName</span></span>
<span data-ttu-id="e277d-124">Der Name der Ressourcengruppe, die den Cluster "Kusto" enthält.</span><span class="sxs-lookup"><span data-stu-id="e277d-124">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="e277d-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e277d-125">-SubscriptionId</span></span>
<span data-ttu-id="e277d-126">Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="e277d-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e277d-127">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="e277d-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e277d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e277d-128">CommonParameters</span></span>
<span data-ttu-id="e277d-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e277d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e277d-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e277d-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e277d-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e277d-131">INPUTS</span></span>

### <span data-ttu-id="e277d-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="e277d-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="e277d-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e277d-133">OUTPUTS</span></span>

### <span data-ttu-id="e277d-134">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICluster</span><span class="sxs-lookup"><span data-stu-id="e277d-134">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICluster</span></span>

## <span data-ttu-id="e277d-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e277d-135">NOTES</span></span>

<span data-ttu-id="e277d-136">ALIASE</span><span class="sxs-lookup"><span data-stu-id="e277d-136">ALIASES</span></span>

<span data-ttu-id="e277d-137">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="e277d-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e277d-138">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e277d-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e277d-139">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e277d-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e277d-140">INPUTOBJECT <IKustoIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="e277d-140">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e277d-141">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="e277d-141">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="e277d-142">`[ClusterName <String>]`: Der Name des Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="e277d-142">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="e277d-143">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="e277d-143">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="e277d-144">`[DatabaseName <String>]`: Der Name der Datenbank im Cluster "Kusto".</span><span class="sxs-lookup"><span data-stu-id="e277d-144">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="e277d-145">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="e277d-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e277d-146">`[Location <String>]`: Azure-Standort.</span><span class="sxs-lookup"><span data-stu-id="e277d-146">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="e277d-147">`[PrincipalAssignmentName <String>]`: Der Name der Kusto PrincipalAssignment.</span><span class="sxs-lookup"><span data-stu-id="e277d-147">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="e277d-148">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Cluster "Kusto" enthält.</span><span class="sxs-lookup"><span data-stu-id="e277d-148">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="e277d-149">`[SubscriptionId <String>]`: Ruft Abonnementanmeldeinformationen ab, mit denen Das Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="e277d-149">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="e277d-150">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="e277d-150">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="e277d-151">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e277d-151">RELATED LINKS</span></span>

