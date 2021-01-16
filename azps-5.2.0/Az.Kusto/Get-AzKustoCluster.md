---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoCluster.md
ms.openlocfilehash: a95f8a00578ccf917a55cdfd9685dedf9a20734f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98293393"
---
# <span data-ttu-id="49364-101">Get-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="49364-101">Get-AzKustoCluster</span></span>

## <span data-ttu-id="49364-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49364-102">SYNOPSIS</span></span>
<span data-ttu-id="49364-103">Ruft einen "Kusto"-Cluster ab.</span><span class="sxs-lookup"><span data-stu-id="49364-103">Gets a Kusto cluster.</span></span>

## <span data-ttu-id="49364-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="49364-104">SYNTAX</span></span>

### <span data-ttu-id="49364-105">Liste1 (Standard)</span><span class="sxs-lookup"><span data-stu-id="49364-105">List1 (Default)</span></span>
```
Get-AzKustoCluster [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="49364-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="49364-106">Get</span></span>
```
Get-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="49364-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="49364-107">GetViaIdentity</span></span>
```
Get-AzKustoCluster -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="49364-108">Liste</span><span class="sxs-lookup"><span data-stu-id="49364-108">List</span></span>
```
Get-AzKustoCluster -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="49364-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="49364-109">DESCRIPTION</span></span>
<span data-ttu-id="49364-110">Ruft einen "Kusto"-Cluster ab.</span><span class="sxs-lookup"><span data-stu-id="49364-110">Gets a Kusto cluster.</span></span>

## <span data-ttu-id="49364-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="49364-111">EXAMPLES</span></span>

### <span data-ttu-id="49364-112">Beispiel 1: Auflisten aller Kusto-Cluster in einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="49364-112">Example 1: List all Kusto clusters in a resource group</span></span>
```powershell
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg

Location Name                 Type                     Zone
-------- ----                 ----                     ----
East US  testnewkustocluster  Microsoft.Kusto/Clusters
East US  testnewkustocluster2 Microsoft.Kusto/Clusters
```

<span data-ttu-id="49364-113">Der oben aufgeführte Befehl listet alle Kusto-Cluster in der Ressourcengruppe "testrg" auf.</span><span class="sxs-lookup"><span data-stu-id="49364-113">The above command lists all Kusto clusters in the resource group "testrg".</span></span>

### <span data-ttu-id="49364-114">Beispiel 2: Erhalten eines bestimmten Kusto-Cluster nach Name</span><span class="sxs-lookup"><span data-stu-id="49364-114">Example 2: Get a specific Kusto cluster by name</span></span>
```powershell
PS C:\>  Get-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="49364-115">Der oben aufgeführte Befehl gibt den Cluster "Kusto" mit dem Namen "testnewkustocluster" in der Ressourcengruppe "testrg" zurück.</span><span class="sxs-lookup"><span data-stu-id="49364-115">The above command returns the Kusto cluster named "testnewkustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="49364-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49364-116">PARAMETERS</span></span>

### <span data-ttu-id="49364-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49364-117">-DefaultProfile</span></span>
<span data-ttu-id="49364-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="49364-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49364-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="49364-119">-InputObject</span></span>
<span data-ttu-id="49364-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="49364-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="49364-121">-Name</span><span class="sxs-lookup"><span data-stu-id="49364-121">-Name</span></span>
<span data-ttu-id="49364-122">Der Name des Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="49364-122">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="49364-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49364-123">-ResourceGroupName</span></span>
<span data-ttu-id="49364-124">Der Name der Ressourcengruppe, die den Cluster "Kusto" enthält.</span><span class="sxs-lookup"><span data-stu-id="49364-124">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="49364-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="49364-125">-SubscriptionId</span></span>
<span data-ttu-id="49364-126">Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="49364-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="49364-127">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="49364-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="49364-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49364-128">CommonParameters</span></span>
<span data-ttu-id="49364-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49364-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49364-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="49364-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49364-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="49364-131">INPUTS</span></span>

### <span data-ttu-id="49364-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="49364-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="49364-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="49364-133">OUTPUTS</span></span>

### <span data-ttu-id="49364-134">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICluster</span><span class="sxs-lookup"><span data-stu-id="49364-134">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICluster</span></span>

## <span data-ttu-id="49364-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="49364-135">NOTES</span></span>

<span data-ttu-id="49364-136">ALIASE</span><span class="sxs-lookup"><span data-stu-id="49364-136">ALIASES</span></span>

<span data-ttu-id="49364-137">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="49364-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="49364-138">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="49364-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="49364-139">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="49364-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="49364-140">INPUTOBJECT <IKustoIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="49364-140">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="49364-141">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="49364-141">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="49364-142">`[ClusterName <String>]`: Der Name des Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="49364-142">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="49364-143">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="49364-143">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="49364-144">`[DatabaseName <String>]`: Der Name der Datenbank im Cluster "Kusto".</span><span class="sxs-lookup"><span data-stu-id="49364-144">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="49364-145">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="49364-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="49364-146">`[Location <String>]`: Azure-Standort.</span><span class="sxs-lookup"><span data-stu-id="49364-146">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="49364-147">`[PrincipalAssignmentName <String>]`: Der Name der Kusto PrincipalAssignment.</span><span class="sxs-lookup"><span data-stu-id="49364-147">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="49364-148">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Cluster "Kusto" enthält.</span><span class="sxs-lookup"><span data-stu-id="49364-148">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="49364-149">`[SubscriptionId <String>]`: Ruft Abonnementanmeldeinformationen ab, mit denen Das Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="49364-149">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="49364-150">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="49364-150">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="49364-151">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="49364-151">RELATED LINKS</span></span>

