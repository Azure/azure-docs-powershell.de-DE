---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabase.md
ms.openlocfilehash: cdcba65473974da6ba8d526247ca947daa97a55c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98303995"
---
# <span data-ttu-id="7fd8e-101">Get-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="7fd8e-101">Get-AzKustoDatabase</span></span>

## <span data-ttu-id="7fd8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7fd8e-102">SYNOPSIS</span></span>
<span data-ttu-id="7fd8e-103">Gibt eine Datenbank zurück.</span><span class="sxs-lookup"><span data-stu-id="7fd8e-103">Returns a database.</span></span>

## <span data-ttu-id="7fd8e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7fd8e-104">SYNTAX</span></span>

### <span data-ttu-id="7fd8e-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="7fd8e-105">List (Default)</span></span>
```
Get-AzKustoDatabase -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7fd8e-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="7fd8e-106">Get</span></span>
```
Get-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7fd8e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7fd8e-107">GetViaIdentity</span></span>
```
Get-AzKustoDatabase -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="7fd8e-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7fd8e-108">DESCRIPTION</span></span>
<span data-ttu-id="7fd8e-109">Gibt eine Datenbank zurück.</span><span class="sxs-lookup"><span data-stu-id="7fd8e-109">Returns a database.</span></span>

## <span data-ttu-id="7fd8e-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7fd8e-110">EXAMPLES</span></span>

### <span data-ttu-id="7fd8e-111">Beispiel 1: Auflisten aller Datenbanken in einem Cluster nach Namen</span><span class="sxs-lookup"><span data-stu-id="7fd8e-111">Example 1: List all Kusto databases in a cluster by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster

Kind      Location Name                                 Type
----      -------- ----                                 ----
ReadWrite East US  testnewkustocluster/mykustodatabase  Microsoft.Kusto/Clusters/Databases
ReadWrite East US  testnewkustocluster/mykustodatabase2 Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="7fd8e-112">Der oben aufgeführte Befehl gibt alle In-Kusto-Datenbanken im Cluster "testnewkustocluster" zurück, die in der Ressourcengruppe "testrg" gefunden wurden.</span><span class="sxs-lookup"><span data-stu-id="7fd8e-112">The above command returns all Kusto databases in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="7fd8e-113">Beispiel 2: Erhalten einer bestimmten "Kusto"-Datenbank nach Name</span><span class="sxs-lookup"><span data-stu-id="7fd8e-113">Example 2: Get a specific Kusto database by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="7fd8e-114">Der oben aufgeführte Befehl gibt die "mykustodatabase"-Datenbank mit dem Namen "mykustodatabase" im Cluster "testnewkustocluster" zurück, der in der Ressourcengruppe "testrg" gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="7fd8e-114">The above command returns the Kusto database named "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="7fd8e-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7fd8e-115">PARAMETERS</span></span>

### <span data-ttu-id="7fd8e-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="7fd8e-116">-ClusterName</span></span>
<span data-ttu-id="7fd8e-117">Der Name des Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="7fd8e-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="7fd8e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fd8e-118">-DefaultProfile</span></span>
<span data-ttu-id="7fd8e-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7fd8e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7fd8e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7fd8e-120">-InputObject</span></span>
<span data-ttu-id="7fd8e-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="7fd8e-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7fd8e-122">-Name</span><span class="sxs-lookup"><span data-stu-id="7fd8e-122">-Name</span></span>
<span data-ttu-id="7fd8e-123">Der Name der Datenbank im Cluster "Kusto".</span><span class="sxs-lookup"><span data-stu-id="7fd8e-123">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fd8e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fd8e-124">-ResourceGroupName</span></span>
<span data-ttu-id="7fd8e-125">Der Name der Ressourcengruppe, die den Cluster "Kusto" enthält.</span><span class="sxs-lookup"><span data-stu-id="7fd8e-125">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="7fd8e-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7fd8e-126">-SubscriptionId</span></span>
<span data-ttu-id="7fd8e-127">Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="7fd8e-127">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="7fd8e-128">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="7fd8e-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="7fd8e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fd8e-129">CommonParameters</span></span>
<span data-ttu-id="7fd8e-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fd8e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fd8e-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7fd8e-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fd8e-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7fd8e-132">INPUTS</span></span>

### <span data-ttu-id="7fd8e-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="7fd8e-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="7fd8e-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7fd8e-134">OUTPUTS</span></span>

### <span data-ttu-id="7fd8e-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabase</span><span class="sxs-lookup"><span data-stu-id="7fd8e-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabase</span></span>

## <span data-ttu-id="7fd8e-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7fd8e-136">NOTES</span></span>

<span data-ttu-id="7fd8e-137">ALIASE</span><span class="sxs-lookup"><span data-stu-id="7fd8e-137">ALIASES</span></span>

<span data-ttu-id="7fd8e-138">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="7fd8e-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7fd8e-139">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7fd8e-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7fd8e-140">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7fd8e-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7fd8e-141">INPUTOBJECT <IKustoIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="7fd8e-141">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7fd8e-142">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="7fd8e-142">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="7fd8e-143">`[ClusterName <String>]`: Der Name des Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="7fd8e-143">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="7fd8e-144">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="7fd8e-144">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="7fd8e-145">`[DatabaseName <String>]`: Der Name der Datenbank im Cluster "Kusto".</span><span class="sxs-lookup"><span data-stu-id="7fd8e-145">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="7fd8e-146">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="7fd8e-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7fd8e-147">`[Location <String>]`: Azure-Standort.</span><span class="sxs-lookup"><span data-stu-id="7fd8e-147">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="7fd8e-148">`[PrincipalAssignmentName <String>]`: Der Name der Kusto PrincipalAssignment.</span><span class="sxs-lookup"><span data-stu-id="7fd8e-148">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="7fd8e-149">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Cluster "Kusto" enthält.</span><span class="sxs-lookup"><span data-stu-id="7fd8e-149">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="7fd8e-150">`[SubscriptionId <String>]`: Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="7fd8e-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="7fd8e-151">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="7fd8e-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="7fd8e-152">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7fd8e-152">RELATED LINKS</span></span>

