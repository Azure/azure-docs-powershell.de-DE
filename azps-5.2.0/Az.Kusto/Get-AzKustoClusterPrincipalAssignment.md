---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclusterprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterPrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterPrincipalAssignment.md
ms.openlocfilehash: 0a6643a4909bb2125e419e28fe3d7a8494760d8d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98296561"
---
# <span data-ttu-id="e64d5-101">Get-AzKustoClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="e64d5-101">Get-AzKustoClusterPrincipalAssignment</span></span>

## <span data-ttu-id="e64d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e64d5-102">SYNOPSIS</span></span>
<span data-ttu-id="e64d5-103">Ruft eine PrincipalAssignment für den Kusto-Cluster ab.</span><span class="sxs-lookup"><span data-stu-id="e64d5-103">Gets a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="e64d5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e64d5-104">SYNTAX</span></span>

### <span data-ttu-id="e64d5-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="e64d5-105">List (Default)</span></span>
```
Get-AzKustoClusterPrincipalAssignment -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e64d5-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="e64d5-106">Get</span></span>
```
Get-AzKustoClusterPrincipalAssignment -ClusterName <String> -PrincipalAssignmentName <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e64d5-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e64d5-107">GetViaIdentity</span></span>
```
Get-AzKustoClusterPrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="e64d5-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e64d5-108">DESCRIPTION</span></span>
<span data-ttu-id="e64d5-109">Ruft eine PrincipalAssignment für den Kusto-Cluster ab.</span><span class="sxs-lookup"><span data-stu-id="e64d5-109">Gets a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="e64d5-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e64d5-110">EXAMPLES</span></span>

### <span data-ttu-id="e64d5-111">Beispiel 1: Auflisten aller PrincipalAssignment des Kusto-Clusters</span><span class="sxs-lookup"><span data-stu-id="e64d5-111">Example 1: List all Kusto cluster principalAssignment</span></span>
```powershell
PS C:\> Get-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="e64d5-112">Der oben aufgeführte Befehl listet alle PrincipalAssignment im Cluster "testnewkustocluster" auf.</span><span class="sxs-lookup"><span data-stu-id="e64d5-112">The above command lists all principalAssignment in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="e64d5-113">Beispiel 2: Ruft eine PrincipalAssignment für den Kusto-Cluster nach Name ab.</span><span class="sxs-lookup"><span data-stu-id="e64d5-113">Example 2: Gets a Kusto cluster principalAssignment by name</span></span>
```powershell
PS C:\> Get-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -PrincipalAssignmentName kustoprincipal1

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="e64d5-114">Der oben aufgeführte Befehl gibt das Kusto-Cluster-PrincipalAssignment namens "kustoprincipal1" im Cluster "testnewkustocluster" zurück.</span><span class="sxs-lookup"><span data-stu-id="e64d5-114">The above command returns the Kusto cluster principalAssignment named "kustoprincipal1" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="e64d5-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e64d5-115">PARAMETERS</span></span>

### <span data-ttu-id="e64d5-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="e64d5-116">-ClusterName</span></span>
<span data-ttu-id="e64d5-117">Der Name des Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="e64d5-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="e64d5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e64d5-118">-DefaultProfile</span></span>
<span data-ttu-id="e64d5-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e64d5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e64d5-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e64d5-120">-InputObject</span></span>
<span data-ttu-id="e64d5-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="e64d5-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e64d5-122">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="e64d5-122">-PrincipalAssignmentName</span></span>
<span data-ttu-id="e64d5-123">Der Name der Kusto PrincipalAssignment.</span><span class="sxs-lookup"><span data-stu-id="e64d5-123">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="e64d5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e64d5-124">-ResourceGroupName</span></span>
<span data-ttu-id="e64d5-125">Der Name der Ressourcengruppe, die den Cluster "Kusto" enthält.</span><span class="sxs-lookup"><span data-stu-id="e64d5-125">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="e64d5-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e64d5-126">-SubscriptionId</span></span>
<span data-ttu-id="e64d5-127">Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="e64d5-127">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e64d5-128">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="e64d5-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e64d5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e64d5-129">CommonParameters</span></span>
<span data-ttu-id="e64d5-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e64d5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e64d5-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e64d5-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e64d5-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e64d5-132">INPUTS</span></span>

### <span data-ttu-id="e64d5-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="e64d5-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="e64d5-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e64d5-134">OUTPUTS</span></span>

### <span data-ttu-id="e64d5-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="e64d5-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IClusterPrincipalAssignment</span></span>

## <span data-ttu-id="e64d5-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e64d5-136">NOTES</span></span>

<span data-ttu-id="e64d5-137">ALIASE</span><span class="sxs-lookup"><span data-stu-id="e64d5-137">ALIASES</span></span>

<span data-ttu-id="e64d5-138">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="e64d5-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e64d5-139">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e64d5-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e64d5-140">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e64d5-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e64d5-141">INPUTOBJECT <IKustoIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="e64d5-141">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e64d5-142">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="e64d5-142">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="e64d5-143">`[ClusterName <String>]`: Der Name des Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="e64d5-143">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="e64d5-144">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="e64d5-144">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="e64d5-145">`[DatabaseName <String>]`: Der Name der Datenbank im Cluster "Kusto".</span><span class="sxs-lookup"><span data-stu-id="e64d5-145">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="e64d5-146">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="e64d5-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e64d5-147">`[Location <String>]`: Azure-Standort.</span><span class="sxs-lookup"><span data-stu-id="e64d5-147">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="e64d5-148">`[PrincipalAssignmentName <String>]`: Der Name der Kusto PrincipalAssignment.</span><span class="sxs-lookup"><span data-stu-id="e64d5-148">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="e64d5-149">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Cluster "Kusto" enthält.</span><span class="sxs-lookup"><span data-stu-id="e64d5-149">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="e64d5-150">`[SubscriptionId <String>]`: Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="e64d5-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="e64d5-151">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="e64d5-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="e64d5-152">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e64d5-152">RELATED LINKS</span></span>

