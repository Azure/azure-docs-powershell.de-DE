---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/get-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabase.md
ms.openlocfilehash: 714f971b32f9863ab2e5dc088d07859f2f5181a9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924832"
---
# <span data-ttu-id="92635-101">Get-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="92635-101">Get-AzKustoDatabase</span></span>

## <span data-ttu-id="92635-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92635-102">SYNOPSIS</span></span>
<span data-ttu-id="92635-103">Gibt eine Datenbank zurück.</span><span class="sxs-lookup"><span data-stu-id="92635-103">Returns a database.</span></span>

## <span data-ttu-id="92635-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="92635-104">SYNTAX</span></span>

### <span data-ttu-id="92635-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="92635-105">List (Default)</span></span>
```
Get-AzKustoDatabase -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="92635-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="92635-106">Get</span></span>
```
Get-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="92635-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="92635-107">GetViaIdentity</span></span>
```
Get-AzKustoDatabase -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="92635-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="92635-108">DESCRIPTION</span></span>
<span data-ttu-id="92635-109">Gibt eine Datenbank zurück.</span><span class="sxs-lookup"><span data-stu-id="92635-109">Returns a database.</span></span>

## <span data-ttu-id="92635-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="92635-110">EXAMPLES</span></span>

### <span data-ttu-id="92635-111">Beispiel 1: Auflisten aller Kusto-Datenbanken in einem Cluster nach Name</span><span class="sxs-lookup"><span data-stu-id="92635-111">Example 1: List all Kusto databases in a cluster by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster

Kind      Location Name                                 Type
----      -------- ----                                 ----
ReadWrite East US  testnewkustocluster/mykustodatabase  Microsoft.Kusto/Clusters/Databases
ReadWrite East US  testnewkustocluster/mykustodatabase2 Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="92635-112">Der obige Befehl gibt alle Kusto-Datenbanken im Cluster "testnewkustocluster" zurück, die in der Ressourcengruppe "testrg" gefunden wurden.</span><span class="sxs-lookup"><span data-stu-id="92635-112">The above command returns all Kusto databases in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="92635-113">Beispiel 2: Erhalten einer bestimmten Kusto-Datenbank nach Name</span><span class="sxs-lookup"><span data-stu-id="92635-113">Example 2: Get a specific Kusto database by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="92635-114">Der obige Befehl gibt die Kusto-Datenbank mit dem Namen "mykustodatabase" im Cluster "testnewkustocluster" zurück, der in der Ressourcengruppe "testrg" gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="92635-114">The above command returns the Kusto database named "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="92635-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="92635-115">PARAMETERS</span></span>

### <span data-ttu-id="92635-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="92635-116">-ClusterName</span></span>
<span data-ttu-id="92635-117">Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="92635-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="92635-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92635-118">-DefaultProfile</span></span>
<span data-ttu-id="92635-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="92635-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92635-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="92635-120">-InputObject</span></span>
<span data-ttu-id="92635-121">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="92635-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="92635-122">-Name</span><span class="sxs-lookup"><span data-stu-id="92635-122">-Name</span></span>
<span data-ttu-id="92635-123">Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="92635-123">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="92635-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92635-124">-ResourceGroupName</span></span>
<span data-ttu-id="92635-125">Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="92635-125">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="92635-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="92635-126">-SubscriptionId</span></span>
<span data-ttu-id="92635-127">Ruft Abonnementanmeldeinformationen ab, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="92635-127">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="92635-128">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="92635-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="92635-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92635-129">CommonParameters</span></span>
<span data-ttu-id="92635-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92635-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92635-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="92635-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92635-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="92635-132">INPUTS</span></span>

### <span data-ttu-id="92635-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="92635-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="92635-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="92635-134">OUTPUTS</span></span>

### <span data-ttu-id="92635-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabase</span><span class="sxs-lookup"><span data-stu-id="92635-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabase</span></span>

## <span data-ttu-id="92635-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="92635-136">NOTES</span></span>

<span data-ttu-id="92635-137">ALIASE</span><span class="sxs-lookup"><span data-stu-id="92635-137">ALIASES</span></span>

<span data-ttu-id="92635-138">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="92635-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="92635-139">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="92635-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="92635-140">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="92635-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="92635-141">INPUTOBJECT <IKustoIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="92635-141">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="92635-142">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="92635-142">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="92635-143">`[ClusterName <String>]`: Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="92635-143">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="92635-144">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="92635-144">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="92635-145">`[DatabaseName <String>]`: Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="92635-145">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="92635-146">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="92635-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="92635-147">`[Location <String>]`: Azure-Standort.</span><span class="sxs-lookup"><span data-stu-id="92635-147">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="92635-148">`[PrincipalAssignmentName <String>]`: Der Name der Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="92635-148">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="92635-149">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="92635-149">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="92635-150">`[SubscriptionId <String>]`: Ruft Abonnementanmeldeinformationen ab, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="92635-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="92635-151">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="92635-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="92635-152">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="92635-152">RELATED LINKS</span></span>

