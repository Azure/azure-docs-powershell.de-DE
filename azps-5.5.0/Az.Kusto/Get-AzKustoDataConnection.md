---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDataConnection.md
ms.openlocfilehash: e1fee17e7f7bf58785c96c28bc6e1f3f66136bb6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100152476"
---
# <span data-ttu-id="dd8b2-101">Get-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="dd8b2-101">Get-AzKustoDataConnection</span></span>

## <span data-ttu-id="dd8b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd8b2-102">SYNOPSIS</span></span>
<span data-ttu-id="dd8b2-103">Gibt eine Datenverbindung zurück.</span><span class="sxs-lookup"><span data-stu-id="dd8b2-103">Returns a data connection.</span></span>

## <span data-ttu-id="dd8b2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dd8b2-104">SYNTAX</span></span>

### <span data-ttu-id="dd8b2-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="dd8b2-105">List (Default)</span></span>
```
Get-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="dd8b2-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="dd8b2-106">Get</span></span>
```
Get-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="dd8b2-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="dd8b2-107">GetViaIdentity</span></span>
```
Get-AzKustoDataConnection -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="dd8b2-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dd8b2-108">DESCRIPTION</span></span>
<span data-ttu-id="dd8b2-109">Gibt eine Datenverbindung zurück.</span><span class="sxs-lookup"><span data-stu-id="dd8b2-109">Returns a data connection.</span></span>

## <span data-ttu-id="dd8b2-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="dd8b2-110">EXAMPLES</span></span>

### <span data-ttu-id="dd8b2-111">Beispiel 1: Auflisten aller Datenverbindungen in einer bestimmten Datenbank</span><span class="sxs-lookup"><span data-stu-id="dd8b2-111">Example 1: List all data connections in a specific database</span></span>
```powershell
PS C:\> Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase"

Kind     Location Name                                               Type
----     -------- ----                                               ----
EventHub East US  testnewkustocluster/mykustodatabase/mykustodataconnection Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="dd8b2-112">Der oben aufgeführte Befehl gibt alle In-Kusto-Datenbanken im Cluster "testnewkustocluster" zurück, die in der Ressourcengruppe "testrg" gefunden wurden.</span><span class="sxs-lookup"><span data-stu-id="dd8b2-112">The above command returns all Kusto databases in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="dd8b2-113">Beispiel 2: Herstellen einer bestimmten Datenverbindung nach Name</span><span class="sxs-lookup"><span data-stu-id="dd8b2-113">Example 2: Get a specific data connection by name</span></span>
```powershell
PS C:\> Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "mykustodataconnection"

Kind     Location Name                                               Type
----     -------- ----                                               ----
EventHub East US  testnewkustocluster/mykustodatabase/mykustodataconnection Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="dd8b2-114">Der oben aufgeführte Befehl gibt die Datenverbindung namens "mykustodataconnection" in der Datenbank "mykustodatabase" des vorhandenen Cluster "testnewkustocluster" zurück, der in der Ressourcengruppe "testrg" gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="dd8b2-114">The above command returns the data connection named "mykustodataconnection" in database "mykustodatabase" of the existing cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="dd8b2-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dd8b2-115">PARAMETERS</span></span>

### <span data-ttu-id="dd8b2-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="dd8b2-116">-ClusterName</span></span>
<span data-ttu-id="dd8b2-117">Der Name des Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="dd8b2-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="dd8b2-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="dd8b2-118">-DatabaseName</span></span>
<span data-ttu-id="dd8b2-119">Der Name der Datenbank im Cluster "Kusto".</span><span class="sxs-lookup"><span data-stu-id="dd8b2-119">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="dd8b2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd8b2-120">-DefaultProfile</span></span>
<span data-ttu-id="dd8b2-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dd8b2-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd8b2-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd8b2-122">-InputObject</span></span>
<span data-ttu-id="dd8b2-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="dd8b2-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="dd8b2-124">-Name</span><span class="sxs-lookup"><span data-stu-id="dd8b2-124">-Name</span></span>
<span data-ttu-id="dd8b2-125">Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="dd8b2-125">The name of the data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DataConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd8b2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd8b2-126">-ResourceGroupName</span></span>
<span data-ttu-id="dd8b2-127">Der Name der Ressourcengruppe, die den Cluster "Kusto" enthält.</span><span class="sxs-lookup"><span data-stu-id="dd8b2-127">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="dd8b2-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dd8b2-128">-SubscriptionId</span></span>
<span data-ttu-id="dd8b2-129">Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="dd8b2-129">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="dd8b2-130">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="dd8b2-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="dd8b2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd8b2-131">CommonParameters</span></span>
<span data-ttu-id="dd8b2-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd8b2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd8b2-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dd8b2-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd8b2-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="dd8b2-134">INPUTS</span></span>

### <span data-ttu-id="dd8b2-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="dd8b2-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="dd8b2-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="dd8b2-136">OUTPUTS</span></span>

### <span data-ttu-id="dd8b2-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDataConnection</span><span class="sxs-lookup"><span data-stu-id="dd8b2-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDataConnection</span></span>

## <span data-ttu-id="dd8b2-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="dd8b2-138">NOTES</span></span>

<span data-ttu-id="dd8b2-139">ALIASE</span><span class="sxs-lookup"><span data-stu-id="dd8b2-139">ALIASES</span></span>

<span data-ttu-id="dd8b2-140">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="dd8b2-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="dd8b2-141">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="dd8b2-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dd8b2-142">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="dd8b2-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="dd8b2-143">INPUTOBJECT <IKustoIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="dd8b2-143">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="dd8b2-144">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="dd8b2-144">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="dd8b2-145">`[ClusterName <String>]`: Der Name des Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="dd8b2-145">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="dd8b2-146">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="dd8b2-146">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="dd8b2-147">`[DatabaseName <String>]`: Der Name der Datenbank im Cluster "Kusto".</span><span class="sxs-lookup"><span data-stu-id="dd8b2-147">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="dd8b2-148">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="dd8b2-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dd8b2-149">`[Location <String>]`: Azure-Standort.</span><span class="sxs-lookup"><span data-stu-id="dd8b2-149">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="dd8b2-150">`[PrincipalAssignmentName <String>]`: Der Name der Kusto PrincipalAssignment.</span><span class="sxs-lookup"><span data-stu-id="dd8b2-150">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="dd8b2-151">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Cluster "Kusto" enthält.</span><span class="sxs-lookup"><span data-stu-id="dd8b2-151">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="dd8b2-152">`[SubscriptionId <String>]`: Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="dd8b2-152">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="dd8b2-153">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="dd8b2-153">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="dd8b2-154">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="dd8b2-154">RELATED LINKS</span></span>

