---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/get-azkustodatabaseprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipalAssignment.md
ms.openlocfilehash: 038db26826c4f3f37dcba42e1ccd435512ecd88b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936192"
---
# <span data-ttu-id="a763a-101">Get-AzKustoDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="a763a-101">Get-AzKustoDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="a763a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a763a-102">SYNOPSIS</span></span>
<span data-ttu-id="a763a-103">Ruft einen Kusto-ClusterdatenbankprinzipalAssignment ab.</span><span class="sxs-lookup"><span data-stu-id="a763a-103">Gets a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="a763a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a763a-104">SYNTAX</span></span>

### <span data-ttu-id="a763a-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="a763a-105">List (Default)</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a763a-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="a763a-106">Get</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -PrincipalAssignmentName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a763a-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a763a-107">GetViaIdentity</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="a763a-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a763a-108">DESCRIPTION</span></span>
<span data-ttu-id="a763a-109">Ruft einen Kusto-ClusterdatenbankprinzipalAssignment ab.</span><span class="sxs-lookup"><span data-stu-id="a763a-109">Gets a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="a763a-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a763a-110">EXAMPLES</span></span>

### <span data-ttu-id="a763a-111">Beispiel 1: Auflisten aller PrincipalAssignment in einer Datenbank nach Namen</span><span class="sxs-lookup"><span data-stu-id="a763a-111">Example 1: List all PrincipalAssignment in a database by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase

Name                                                                     Type
----                                                                     ----
testnewkustocluster/mykustodatabase/kustoprincipal1                      Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
testnewkustocluster/mykustodatabase/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
testnewkustocluster/mykustodatabase/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
```

<span data-ttu-id="a763a-112">Der obige Befehl gibt alle PrincipalAssignment in der Datenbank "mykustodatabase" zurück, die im Cluster "testnewkustocluster" gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="a763a-112">The above command returns all all PrincipalAssignment in the database "mykustodatabase" found in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="a763a-113">Beispiel 2: Erhalten einer bestimmten PrincipalAssignment in einer Datenbank nach Name</span><span class="sxs-lookup"><span data-stu-id="a763a-113">Example 2: Get a specific PrincipalAssignment in a database by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -PrincipalAssignmentName kustoprincipal1

Name                                                Type
----                                                ----
testnewkustocluster/mykustodatabase/kustoprincipal1 Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
```

<span data-ttu-id="a763a-114">Der obige Befehl gibt alle PrincipalAssignment mit dem Namen "kustoprincipal1" in der Datenbank "mykustodatabase" zurück, die im Cluster "testnewkustocluster" gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="a763a-114">The above command returns all all PrincipalAssignment named "kustoprincipal1" in the database "mykustodatabase" found in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="a763a-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a763a-115">PARAMETERS</span></span>

### <span data-ttu-id="a763a-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="a763a-116">-ClusterName</span></span>
<span data-ttu-id="a763a-117">Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="a763a-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="a763a-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a763a-118">-DatabaseName</span></span>
<span data-ttu-id="a763a-119">Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="a763a-119">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="a763a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a763a-120">-DefaultProfile</span></span>
<span data-ttu-id="a763a-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a763a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a763a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a763a-122">-InputObject</span></span>
<span data-ttu-id="a763a-123">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="a763a-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a763a-124">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="a763a-124">-PrincipalAssignmentName</span></span>
<span data-ttu-id="a763a-125">Der Name der Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="a763a-125">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="a763a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a763a-126">-ResourceGroupName</span></span>
<span data-ttu-id="a763a-127">Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="a763a-127">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="a763a-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a763a-128">-SubscriptionId</span></span>
<span data-ttu-id="a763a-129">Ruft Abonnementanmeldeinformationen ab, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="a763a-129">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a763a-130">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="a763a-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a763a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a763a-131">CommonParameters</span></span>
<span data-ttu-id="a763a-132">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a763a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a763a-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a763a-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a763a-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a763a-134">INPUTS</span></span>

### <span data-ttu-id="a763a-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="a763a-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="a763a-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a763a-136">OUTPUTS</span></span>

### <span data-ttu-id="a763a-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="a763a-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="a763a-138">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a763a-138">NOTES</span></span>

<span data-ttu-id="a763a-139">ALIASE</span><span class="sxs-lookup"><span data-stu-id="a763a-139">ALIASES</span></span>

<span data-ttu-id="a763a-140">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="a763a-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a763a-141">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="a763a-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a763a-142">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a763a-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a763a-143">INPUTOBJECT <IKustoIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="a763a-143">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a763a-144">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="a763a-144">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="a763a-145">`[ClusterName <String>]`: Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="a763a-145">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="a763a-146">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="a763a-146">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="a763a-147">`[DatabaseName <String>]`: Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="a763a-147">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="a763a-148">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="a763a-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a763a-149">`[Location <String>]`: Azure-Standort.</span><span class="sxs-lookup"><span data-stu-id="a763a-149">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="a763a-150">`[PrincipalAssignmentName <String>]`: Der Name der Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="a763a-150">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="a763a-151">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="a763a-151">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="a763a-152">`[SubscriptionId <String>]`: Ruft Abonnementanmeldeinformationen ab, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="a763a-152">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="a763a-153">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="a763a-153">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="a763a-154">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a763a-154">RELATED LINKS</span></span>

