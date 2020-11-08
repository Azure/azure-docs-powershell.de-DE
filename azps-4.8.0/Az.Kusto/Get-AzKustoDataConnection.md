---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDataConnection.md
ms.openlocfilehash: 6cfc5cdae87512245a573ed5c7ff9c746036c815
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010173"
---
# <span data-ttu-id="1f90f-101">Get-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="1f90f-101">Get-AzKustoDataConnection</span></span>

## <span data-ttu-id="1f90f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1f90f-102">SYNOPSIS</span></span>
<span data-ttu-id="1f90f-103">Gibt eine Datenverbindung zurück.</span><span class="sxs-lookup"><span data-stu-id="1f90f-103">Returns a data connection.</span></span>

## <span data-ttu-id="1f90f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1f90f-104">SYNTAX</span></span>

### <span data-ttu-id="1f90f-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="1f90f-105">List (Default)</span></span>
```
Get-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1f90f-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="1f90f-106">Get</span></span>
```
Get-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1f90f-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1f90f-107">GetViaIdentity</span></span>
```
Get-AzKustoDataConnection -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="1f90f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1f90f-108">DESCRIPTION</span></span>
<span data-ttu-id="1f90f-109">Gibt eine Datenverbindung zurück.</span><span class="sxs-lookup"><span data-stu-id="1f90f-109">Returns a data connection.</span></span>

## <span data-ttu-id="1f90f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1f90f-110">EXAMPLES</span></span>

### <span data-ttu-id="1f90f-111">Beispiel 1: Auflisten aller Datenverbindungen in einer bestimmten Datenbank</span><span class="sxs-lookup"><span data-stu-id="1f90f-111">Example 1: List all data connections in a specific database</span></span>
```powershell
PS C:\> Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase"

Kind     Location Name                                               Type
----     -------- ----                                               ----
EventHub East US  testnewkustocluster/mykustodatabase/mykustodataconnection Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="1f90f-112">Der obige Befehl gibt alle Kusto-Datenbanken im Cluster "testnewkustocluster" zurück, die in der Ressourcengruppe "testrg" gefunden wurden.</span><span class="sxs-lookup"><span data-stu-id="1f90f-112">The above command returns all Kusto databases in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="1f90f-113">Beispiel 2: Abrufen einer bestimmten Datenverbindung nach Namen</span><span class="sxs-lookup"><span data-stu-id="1f90f-113">Example 2: Get a specific data connection by name</span></span>
```powershell
PS C:\> Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "mykustodataconnection"

Kind     Location Name                                               Type
----     -------- ----                                               ----
EventHub East US  testnewkustocluster/mykustodatabase/mykustodataconnection Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="1f90f-114">Der obige Befehl gibt die Datenverbindung mit dem Namen "mykustodataconnection" in der Datenbank "mykustodatabase" des vorhandenen Clusters "testnewkustocluster" zurück, der in der Ressourcengruppe "testrg" gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="1f90f-114">The above command returns the data connection named "mykustodataconnection" in database "mykustodatabase" of the existing cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="1f90f-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="1f90f-115">PARAMETERS</span></span>

### <span data-ttu-id="1f90f-116">-Clustername</span><span class="sxs-lookup"><span data-stu-id="1f90f-116">-ClusterName</span></span>
<span data-ttu-id="1f90f-117">Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="1f90f-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="1f90f-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1f90f-118">-DatabaseName</span></span>
<span data-ttu-id="1f90f-119">Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="1f90f-119">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="1f90f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f90f-120">-DefaultProfile</span></span>
<span data-ttu-id="1f90f-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1f90f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f90f-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1f90f-122">-InputObject</span></span>
<span data-ttu-id="1f90f-123">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="1f90f-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1f90f-124">-Name</span><span class="sxs-lookup"><span data-stu-id="1f90f-124">-Name</span></span>
<span data-ttu-id="1f90f-125">Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="1f90f-125">The name of the data connection.</span></span>

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

### <span data-ttu-id="1f90f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f90f-126">-ResourceGroupName</span></span>
<span data-ttu-id="1f90f-127">Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="1f90f-127">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="1f90f-128">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="1f90f-128">-SubscriptionId</span></span>
<span data-ttu-id="1f90f-129">Ruft Abonnement Anmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="1f90f-129">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="1f90f-130">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="1f90f-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="1f90f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f90f-131">CommonParameters</span></span>
<span data-ttu-id="1f90f-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f90f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f90f-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1f90f-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f90f-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1f90f-134">INPUTS</span></span>

### <span data-ttu-id="1f90f-135">Microsoft. Azure. PowerShell. Cmdlets. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="1f90f-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="1f90f-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1f90f-136">OUTPUTS</span></span>

### <span data-ttu-id="1f90f-137">Microsoft. Azure. PowerShell. Cmdlets. Kusto. Models. Api20200614. IDataConnection</span><span class="sxs-lookup"><span data-stu-id="1f90f-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDataConnection</span></span>

## <span data-ttu-id="1f90f-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="1f90f-138">NOTES</span></span>

<span data-ttu-id="1f90f-139">Aliase</span><span class="sxs-lookup"><span data-stu-id="1f90f-139">ALIASES</span></span>

<span data-ttu-id="1f90f-140">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1f90f-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1f90f-141">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1f90f-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1f90f-142">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="1f90f-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1f90f-143">Inputobject <IKustoIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="1f90f-143">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1f90f-144">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="1f90f-144">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="1f90f-145">`[ClusterName <String>]`: Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="1f90f-145">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="1f90f-146">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="1f90f-146">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="1f90f-147">`[DatabaseName <String>]`: Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="1f90f-147">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="1f90f-148">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="1f90f-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1f90f-149">`[Location <String>]`: Azure-Position.</span><span class="sxs-lookup"><span data-stu-id="1f90f-149">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="1f90f-150">`[PrincipalAssignmentName <String>]`: Der Name des Kusto-principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="1f90f-150">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="1f90f-151">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="1f90f-151">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="1f90f-152">`[SubscriptionId <String>]`: Ruft Abonnement Anmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="1f90f-152">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="1f90f-153">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="1f90f-153">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="1f90f-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1f90f-154">RELATED LINKS</span></span>

