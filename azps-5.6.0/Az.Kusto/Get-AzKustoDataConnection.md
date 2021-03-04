---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/get-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDataConnection.md
ms.openlocfilehash: 06c824c140f18c81ca3ce1547257e4765a2543b8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924835"
---
# <span data-ttu-id="11a8e-101">Get-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="11a8e-101">Get-AzKustoDataConnection</span></span>

## <span data-ttu-id="11a8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11a8e-102">SYNOPSIS</span></span>
<span data-ttu-id="11a8e-103">Gibt eine Datenverbindung zurück.</span><span class="sxs-lookup"><span data-stu-id="11a8e-103">Returns a data connection.</span></span>

## <span data-ttu-id="11a8e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="11a8e-104">SYNTAX</span></span>

### <span data-ttu-id="11a8e-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="11a8e-105">List (Default)</span></span>
```
Get-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="11a8e-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="11a8e-106">Get</span></span>
```
Get-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="11a8e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="11a8e-107">GetViaIdentity</span></span>
```
Get-AzKustoDataConnection -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="11a8e-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="11a8e-108">DESCRIPTION</span></span>
<span data-ttu-id="11a8e-109">Gibt eine Datenverbindung zurück.</span><span class="sxs-lookup"><span data-stu-id="11a8e-109">Returns a data connection.</span></span>

## <span data-ttu-id="11a8e-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="11a8e-110">EXAMPLES</span></span>

### <span data-ttu-id="11a8e-111">Beispiel 1: Auflisten aller Datenverbindungen in einer bestimmten Datenbank</span><span class="sxs-lookup"><span data-stu-id="11a8e-111">Example 1: List all data connections in a specific database</span></span>
```powershell
PS C:\> Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase"

Kind     Location Name                                               Type
----     -------- ----                                               ----
EventHub East US  testnewkustocluster/mykustodatabase/mykustodataconnection Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="11a8e-112">Der obige Befehl gibt alle Kusto-Datenbanken im Cluster "testnewkustocluster" zurück, die in der Ressourcengruppe "testrg" gefunden wurden.</span><span class="sxs-lookup"><span data-stu-id="11a8e-112">The above command returns all Kusto databases in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="11a8e-113">Beispiel 2: Erhalten einer bestimmten Datenverbindung nach Name</span><span class="sxs-lookup"><span data-stu-id="11a8e-113">Example 2: Get a specific data connection by name</span></span>
```powershell
PS C:\> Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "mykustodataconnection"

Kind     Location Name                                               Type
----     -------- ----                                               ----
EventHub East US  testnewkustocluster/mykustodatabase/mykustodataconnection Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="11a8e-114">Der obige Befehl gibt die Datenverbindung mit dem Namen "mykustodataconnection" in der Datenbank "mykustodatabase" des vorhandenen Clusters "testnewkustocluster" zurück, der in der Ressourcengruppe "testrg" gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="11a8e-114">The above command returns the data connection named "mykustodataconnection" in database "mykustodatabase" of the existing cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="11a8e-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="11a8e-115">PARAMETERS</span></span>

### <span data-ttu-id="11a8e-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="11a8e-116">-ClusterName</span></span>
<span data-ttu-id="11a8e-117">Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="11a8e-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="11a8e-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="11a8e-118">-DatabaseName</span></span>
<span data-ttu-id="11a8e-119">Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="11a8e-119">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="11a8e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11a8e-120">-DefaultProfile</span></span>
<span data-ttu-id="11a8e-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="11a8e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11a8e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11a8e-122">-InputObject</span></span>
<span data-ttu-id="11a8e-123">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="11a8e-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="11a8e-124">-Name</span><span class="sxs-lookup"><span data-stu-id="11a8e-124">-Name</span></span>
<span data-ttu-id="11a8e-125">Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="11a8e-125">The name of the data connection.</span></span>

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

### <span data-ttu-id="11a8e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11a8e-126">-ResourceGroupName</span></span>
<span data-ttu-id="11a8e-127">Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="11a8e-127">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="11a8e-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="11a8e-128">-SubscriptionId</span></span>
<span data-ttu-id="11a8e-129">Ruft Abonnementanmeldeinformationen ab, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="11a8e-129">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="11a8e-130">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="11a8e-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="11a8e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11a8e-131">CommonParameters</span></span>
<span data-ttu-id="11a8e-132">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11a8e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11a8e-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="11a8e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11a8e-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="11a8e-134">INPUTS</span></span>

### <span data-ttu-id="11a8e-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="11a8e-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="11a8e-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="11a8e-136">OUTPUTS</span></span>

### <span data-ttu-id="11a8e-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDataConnection</span><span class="sxs-lookup"><span data-stu-id="11a8e-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDataConnection</span></span>

## <span data-ttu-id="11a8e-138">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="11a8e-138">NOTES</span></span>

<span data-ttu-id="11a8e-139">ALIASE</span><span class="sxs-lookup"><span data-stu-id="11a8e-139">ALIASES</span></span>

<span data-ttu-id="11a8e-140">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="11a8e-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="11a8e-141">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="11a8e-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="11a8e-142">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="11a8e-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="11a8e-143">INPUTOBJECT <IKustoIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="11a8e-143">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="11a8e-144">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="11a8e-144">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="11a8e-145">`[ClusterName <String>]`: Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="11a8e-145">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="11a8e-146">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="11a8e-146">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="11a8e-147">`[DatabaseName <String>]`: Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="11a8e-147">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="11a8e-148">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="11a8e-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="11a8e-149">`[Location <String>]`: Azure-Standort.</span><span class="sxs-lookup"><span data-stu-id="11a8e-149">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="11a8e-150">`[PrincipalAssignmentName <String>]`: Der Name der Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="11a8e-150">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="11a8e-151">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="11a8e-151">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="11a8e-152">`[SubscriptionId <String>]`: Ruft Abonnementanmeldeinformationen ab, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="11a8e-152">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="11a8e-153">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="11a8e-153">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="11a8e-154">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="11a8e-154">RELATED LINKS</span></span>

