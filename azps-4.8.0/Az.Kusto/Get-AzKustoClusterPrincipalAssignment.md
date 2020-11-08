---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclusterprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterPrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterPrincipalAssignment.md
ms.openlocfilehash: 0a6643a4909bb2125e419e28fe3d7a8494760d8d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010174"
---
# <span data-ttu-id="f0559-101">Get-AzKustoClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="f0559-101">Get-AzKustoClusterPrincipalAssignment</span></span>

## <span data-ttu-id="f0559-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f0559-102">SYNOPSIS</span></span>
<span data-ttu-id="f0559-103">Ruft einen Kusto-Cluster-principalAssignment ab.</span><span class="sxs-lookup"><span data-stu-id="f0559-103">Gets a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="f0559-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f0559-104">SYNTAX</span></span>

### <span data-ttu-id="f0559-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="f0559-105">List (Default)</span></span>
```
Get-AzKustoClusterPrincipalAssignment -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f0559-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="f0559-106">Get</span></span>
```
Get-AzKustoClusterPrincipalAssignment -ClusterName <String> -PrincipalAssignmentName <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f0559-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f0559-107">GetViaIdentity</span></span>
```
Get-AzKustoClusterPrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="f0559-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f0559-108">DESCRIPTION</span></span>
<span data-ttu-id="f0559-109">Ruft einen Kusto-Cluster-principalAssignment ab.</span><span class="sxs-lookup"><span data-stu-id="f0559-109">Gets a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="f0559-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f0559-110">EXAMPLES</span></span>

### <span data-ttu-id="f0559-111">Beispiel 1: Auflisten aller Kusto-Cluster principalAssignment</span><span class="sxs-lookup"><span data-stu-id="f0559-111">Example 1: List all Kusto cluster principalAssignment</span></span>
```powershell
PS C:\> Get-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="f0559-112">Der obige Befehl listet alle principalAssignment im Cluster "testnewkustocluster" auf.</span><span class="sxs-lookup"><span data-stu-id="f0559-112">The above command lists all principalAssignment in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="f0559-113">Beispiel 2: Ruft einen Kusto-Cluster principalAssignment nach Name ab.</span><span class="sxs-lookup"><span data-stu-id="f0559-113">Example 2: Gets a Kusto cluster principalAssignment by name</span></span>
```powershell
PS C:\> Get-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -PrincipalAssignmentName kustoprincipal1

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="f0559-114">Der obige Befehl gibt den Kusto-Cluster principalAssignment mit dem Namen "kustoprincipal1" im Cluster "testnewkustocluster" zurück.</span><span class="sxs-lookup"><span data-stu-id="f0559-114">The above command returns the Kusto cluster principalAssignment named "kustoprincipal1" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="f0559-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="f0559-115">PARAMETERS</span></span>

### <span data-ttu-id="f0559-116">-Clustername</span><span class="sxs-lookup"><span data-stu-id="f0559-116">-ClusterName</span></span>
<span data-ttu-id="f0559-117">Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="f0559-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="f0559-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0559-118">-DefaultProfile</span></span>
<span data-ttu-id="f0559-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f0559-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0559-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f0559-120">-InputObject</span></span>
<span data-ttu-id="f0559-121">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="f0559-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f0559-122">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="f0559-122">-PrincipalAssignmentName</span></span>
<span data-ttu-id="f0559-123">Der Name des Kusto-principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="f0559-123">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="f0559-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0559-124">-ResourceGroupName</span></span>
<span data-ttu-id="f0559-125">Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="f0559-125">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="f0559-126">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="f0559-126">-SubscriptionId</span></span>
<span data-ttu-id="f0559-127">Ruft Abonnement Anmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="f0559-127">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f0559-128">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="f0559-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f0559-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0559-129">CommonParameters</span></span>
<span data-ttu-id="f0559-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0559-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0559-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f0559-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0559-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f0559-132">INPUTS</span></span>

### <span data-ttu-id="f0559-133">Microsoft. Azure. PowerShell. Cmdlets. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="f0559-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="f0559-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f0559-134">OUTPUTS</span></span>

### <span data-ttu-id="f0559-135">Microsoft. Azure. PowerShell. Cmdlets. Kusto. Models. Api20200614. IClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="f0559-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IClusterPrincipalAssignment</span></span>

## <span data-ttu-id="f0559-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="f0559-136">NOTES</span></span>

<span data-ttu-id="f0559-137">Aliase</span><span class="sxs-lookup"><span data-stu-id="f0559-137">ALIASES</span></span>

<span data-ttu-id="f0559-138">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f0559-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f0559-139">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f0559-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f0559-140">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="f0559-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f0559-141">Inputobject <IKustoIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="f0559-141">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f0559-142">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="f0559-142">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="f0559-143">`[ClusterName <String>]`: Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="f0559-143">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="f0559-144">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="f0559-144">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="f0559-145">`[DatabaseName <String>]`: Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="f0559-145">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="f0559-146">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="f0559-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f0559-147">`[Location <String>]`: Azure-Position.</span><span class="sxs-lookup"><span data-stu-id="f0559-147">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="f0559-148">`[PrincipalAssignmentName <String>]`: Der Name des Kusto-principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="f0559-148">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="f0559-149">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="f0559-149">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="f0559-150">`[SubscriptionId <String>]`: Ruft Abonnement Anmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="f0559-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f0559-151">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="f0559-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="f0559-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f0559-152">RELATED LINKS</span></span>

