---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/get-azkustoclusterprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterPrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterPrincipalAssignment.md
ms.openlocfilehash: b89327f80ec5f8e0f5faf9f66e943ee07601799e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924856"
---
# <span data-ttu-id="906d1-101">Get-AzKustoClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="906d1-101">Get-AzKustoClusterPrincipalAssignment</span></span>

## <span data-ttu-id="906d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="906d1-102">SYNOPSIS</span></span>
<span data-ttu-id="906d1-103">Ruft einen Kusto-ClusterprinzipalAssignment ab.</span><span class="sxs-lookup"><span data-stu-id="906d1-103">Gets a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="906d1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="906d1-104">SYNTAX</span></span>

### <span data-ttu-id="906d1-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="906d1-105">List (Default)</span></span>
```
Get-AzKustoClusterPrincipalAssignment -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="906d1-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="906d1-106">Get</span></span>
```
Get-AzKustoClusterPrincipalAssignment -ClusterName <String> -PrincipalAssignmentName <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="906d1-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="906d1-107">GetViaIdentity</span></span>
```
Get-AzKustoClusterPrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="906d1-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="906d1-108">DESCRIPTION</span></span>
<span data-ttu-id="906d1-109">Ruft einen Kusto-ClusterprinzipalAssignment ab.</span><span class="sxs-lookup"><span data-stu-id="906d1-109">Gets a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="906d1-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="906d1-110">EXAMPLES</span></span>

### <span data-ttu-id="906d1-111">Beispiel 1: Listen aller Kusto-Clusterprinzipalzuweisungen</span><span class="sxs-lookup"><span data-stu-id="906d1-111">Example 1: List all Kusto cluster principalAssignment</span></span>
```powershell
PS C:\> Get-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="906d1-112">Der obige Befehl listet alle PrincipalAssignment im Cluster "testnewkustocluster" auf.</span><span class="sxs-lookup"><span data-stu-id="906d1-112">The above command lists all principalAssignment in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="906d1-113">Beispiel 2: Ruft eine Kusto-Clusterprinzipalzuweisung nach Name ab.</span><span class="sxs-lookup"><span data-stu-id="906d1-113">Example 2: Gets a Kusto cluster principalAssignment by name</span></span>
```powershell
PS C:\> Get-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -PrincipalAssignmentName kustoprincipal1

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="906d1-114">Der obige Befehl gibt das Kusto-ClusterprinzipalAssignment mit dem Namen "kustoprincipal1" im Cluster "testnewkustocluster" zurück.</span><span class="sxs-lookup"><span data-stu-id="906d1-114">The above command returns the Kusto cluster principalAssignment named "kustoprincipal1" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="906d1-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="906d1-115">PARAMETERS</span></span>

### <span data-ttu-id="906d1-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="906d1-116">-ClusterName</span></span>
<span data-ttu-id="906d1-117">Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="906d1-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="906d1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="906d1-118">-DefaultProfile</span></span>
<span data-ttu-id="906d1-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="906d1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="906d1-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="906d1-120">-InputObject</span></span>
<span data-ttu-id="906d1-121">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="906d1-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="906d1-122">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="906d1-122">-PrincipalAssignmentName</span></span>
<span data-ttu-id="906d1-123">Der Name der Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="906d1-123">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="906d1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="906d1-124">-ResourceGroupName</span></span>
<span data-ttu-id="906d1-125">Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="906d1-125">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="906d1-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="906d1-126">-SubscriptionId</span></span>
<span data-ttu-id="906d1-127">Ruft Abonnementanmeldeinformationen ab, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="906d1-127">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="906d1-128">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="906d1-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="906d1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="906d1-129">CommonParameters</span></span>
<span data-ttu-id="906d1-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="906d1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="906d1-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="906d1-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="906d1-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="906d1-132">INPUTS</span></span>

### <span data-ttu-id="906d1-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="906d1-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="906d1-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="906d1-134">OUTPUTS</span></span>

### <span data-ttu-id="906d1-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="906d1-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IClusterPrincipalAssignment</span></span>

## <span data-ttu-id="906d1-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="906d1-136">NOTES</span></span>

<span data-ttu-id="906d1-137">ALIASE</span><span class="sxs-lookup"><span data-stu-id="906d1-137">ALIASES</span></span>

<span data-ttu-id="906d1-138">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="906d1-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="906d1-139">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="906d1-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="906d1-140">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="906d1-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="906d1-141">INPUTOBJECT <IKustoIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="906d1-141">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="906d1-142">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="906d1-142">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="906d1-143">`[ClusterName <String>]`: Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="906d1-143">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="906d1-144">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="906d1-144">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="906d1-145">`[DatabaseName <String>]`: Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="906d1-145">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="906d1-146">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="906d1-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="906d1-147">`[Location <String>]`: Azure-Standort.</span><span class="sxs-lookup"><span data-stu-id="906d1-147">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="906d1-148">`[PrincipalAssignmentName <String>]`: Der Name der Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="906d1-148">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="906d1-149">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="906d1-149">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="906d1-150">`[SubscriptionId <String>]`: Ruft Abonnementanmeldeinformationen ab, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="906d1-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="906d1-151">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="906d1-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="906d1-152">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="906d1-152">RELATED LINKS</span></span>

