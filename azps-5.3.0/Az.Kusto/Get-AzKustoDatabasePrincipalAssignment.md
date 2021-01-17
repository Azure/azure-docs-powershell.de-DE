---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodatabaseprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipalAssignment.md
ms.openlocfilehash: 533e247ed2a0b9682e2fe87699d0a77b51ed06ee
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459112"
---
# <span data-ttu-id="5b9e4-101">Get-AzKustoDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="5b9e4-101">Get-AzKustoDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="5b9e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b9e4-102">SYNOPSIS</span></span>
<span data-ttu-id="5b9e4-103">Ruft eine PrincipalAssignment für die Kusto-Clusterdatenbank ab.</span><span class="sxs-lookup"><span data-stu-id="5b9e4-103">Gets a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="5b9e4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5b9e4-104">SYNTAX</span></span>

### <span data-ttu-id="5b9e4-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="5b9e4-105">List (Default)</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5b9e4-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="5b9e4-106">Get</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -PrincipalAssignmentName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5b9e4-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5b9e4-107">GetViaIdentity</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="5b9e4-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5b9e4-108">DESCRIPTION</span></span>
<span data-ttu-id="5b9e4-109">Ruft eine PrincipalAssignment für die Kusto-Clusterdatenbank ab.</span><span class="sxs-lookup"><span data-stu-id="5b9e4-109">Gets a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="5b9e4-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5b9e4-110">EXAMPLES</span></span>

### <span data-ttu-id="5b9e4-111">Beispiel 1: Auflisten aller PrincipalAssignment in einer Datenbank nach Name</span><span class="sxs-lookup"><span data-stu-id="5b9e4-111">Example 1: List all PrincipalAssignment in a database by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase

Name                                                                     Type
----                                                                     ----
testnewkustocluster/mykustodatabase/kustoprincipal1                      Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
testnewkustocluster/mykustodatabase/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
testnewkustocluster/mykustodatabase/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
```

<span data-ttu-id="5b9e4-112">Der oben aufgeführte Befehl gibt alle PrincipalAssignment-Werte in der Datenbank "mykustodatabase" zurück, die im Cluster "testnewkustocluster" gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="5b9e4-112">The above command returns all all PrincipalAssignment in the database "mykustodatabase" found in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="5b9e4-113">Beispiel 2: Erhalten einer bestimmten PrincipalAssignment in einer Datenbank nach Name</span><span class="sxs-lookup"><span data-stu-id="5b9e4-113">Example 2: Get a specific PrincipalAssignment in a database by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -PrincipalAssignmentName kustoprincipal1

Name                                                Type
----                                                ----
testnewkustocluster/mykustodatabase/kustoprincipal1 Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
```

<span data-ttu-id="5b9e4-114">Der oben aufgeführte Befehl gibt alle PrincipalAssignment namens "kustoprincipal1" in der Datenbank "mykustodatabase" zurück, die im Cluster "testnewkustocluster" gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="5b9e4-114">The above command returns all all PrincipalAssignment named "kustoprincipal1" in the database "mykustodatabase" found in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="5b9e4-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5b9e4-115">PARAMETERS</span></span>

### <span data-ttu-id="5b9e4-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="5b9e4-116">-ClusterName</span></span>
<span data-ttu-id="5b9e4-117">Der Name des Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="5b9e4-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="5b9e4-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5b9e4-118">-DatabaseName</span></span>
<span data-ttu-id="5b9e4-119">Der Name der Datenbank im Cluster "Kusto".</span><span class="sxs-lookup"><span data-stu-id="5b9e4-119">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="5b9e4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b9e4-120">-DefaultProfile</span></span>
<span data-ttu-id="5b9e4-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5b9e4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b9e4-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5b9e4-122">-InputObject</span></span>
<span data-ttu-id="5b9e4-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="5b9e4-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5b9e4-124">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="5b9e4-124">-PrincipalAssignmentName</span></span>
<span data-ttu-id="5b9e4-125">Der Name der Kusto PrincipalAssignment.</span><span class="sxs-lookup"><span data-stu-id="5b9e4-125">The name of the Kusto principalAssignment.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b9e4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b9e4-126">-ResourceGroupName</span></span>
<span data-ttu-id="5b9e4-127">Der Name der Ressourcengruppe, die den Cluster "Kusto" enthält.</span><span class="sxs-lookup"><span data-stu-id="5b9e4-127">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="5b9e4-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5b9e4-128">-SubscriptionId</span></span>
<span data-ttu-id="5b9e4-129">Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="5b9e4-129">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="5b9e4-130">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="5b9e4-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="5b9e4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b9e4-131">CommonParameters</span></span>
<span data-ttu-id="5b9e4-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b9e4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b9e4-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5b9e4-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b9e4-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5b9e4-134">INPUTS</span></span>

### <span data-ttu-id="5b9e4-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="5b9e4-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="5b9e4-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5b9e4-136">OUTPUTS</span></span>

### <span data-ttu-id="5b9e4-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="5b9e4-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="5b9e4-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5b9e4-138">NOTES</span></span>

<span data-ttu-id="5b9e4-139">ALIASE</span><span class="sxs-lookup"><span data-stu-id="5b9e4-139">ALIASES</span></span>

<span data-ttu-id="5b9e4-140">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="5b9e4-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5b9e4-141">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5b9e4-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5b9e4-142">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5b9e4-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5b9e4-143">INPUTOBJECT <IKustoIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="5b9e4-143">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5b9e4-144">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="5b9e4-144">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="5b9e4-145">`[ClusterName <String>]`: Der Name des Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="5b9e4-145">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="5b9e4-146">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="5b9e4-146">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="5b9e4-147">`[DatabaseName <String>]`: Der Name der Datenbank im Cluster "Kusto".</span><span class="sxs-lookup"><span data-stu-id="5b9e4-147">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="5b9e4-148">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="5b9e4-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5b9e4-149">`[Location <String>]`: Azure-Standort.</span><span class="sxs-lookup"><span data-stu-id="5b9e4-149">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="5b9e4-150">`[PrincipalAssignmentName <String>]`: Der Name der Kusto PrincipalAssignment.</span><span class="sxs-lookup"><span data-stu-id="5b9e4-150">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="5b9e4-151">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Cluster "Kusto" enthält.</span><span class="sxs-lookup"><span data-stu-id="5b9e4-151">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="5b9e4-152">`[SubscriptionId <String>]`: Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="5b9e4-152">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="5b9e4-153">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="5b9e4-153">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="5b9e4-154">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5b9e4-154">RELATED LINKS</span></span>

