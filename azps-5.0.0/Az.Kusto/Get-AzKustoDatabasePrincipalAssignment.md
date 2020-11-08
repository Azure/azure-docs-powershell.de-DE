---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodatabaseprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipalAssignment.md
ms.openlocfilehash: 4becbb8285685c923fe6b0ec2174e7e84824a106
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179215"
---
# <span data-ttu-id="86d30-101">Get-AzKustoDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="86d30-101">Get-AzKustoDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="86d30-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="86d30-102">SYNOPSIS</span></span>
<span data-ttu-id="86d30-103">Ruft eine Kusto-Clusterdatenbank-principalAssignment ab.</span><span class="sxs-lookup"><span data-stu-id="86d30-103">Gets a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="86d30-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="86d30-104">SYNTAX</span></span>

### <span data-ttu-id="86d30-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="86d30-105">List (Default)</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="86d30-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="86d30-106">Get</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -PrincipalAssignmentName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="86d30-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="86d30-107">GetViaIdentity</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="86d30-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="86d30-108">DESCRIPTION</span></span>
<span data-ttu-id="86d30-109">Ruft eine Kusto-Clusterdatenbank-principalAssignment ab.</span><span class="sxs-lookup"><span data-stu-id="86d30-109">Gets a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="86d30-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="86d30-110">EXAMPLES</span></span>

### <span data-ttu-id="86d30-111">Beispiel 1: Auflisten aller PrincipalAssignment in einer Datenbank nach Name</span><span class="sxs-lookup"><span data-stu-id="86d30-111">Example 1: List all PrincipalAssignment in a database by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase

Name                                                                     Type
----                                                                     ----
testnewkustocluster/mykustodatabase/kustoprincipal1                      Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
testnewkustocluster/mykustodatabase/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
testnewkustocluster/mykustodatabase/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
```

<span data-ttu-id="86d30-112">Der obige Befehl gibt alle PrincipalAssignment in der Datenbank "mykustodatabase" zurück, die im Cluster "testnewkustocluster" gefunden wurden.</span><span class="sxs-lookup"><span data-stu-id="86d30-112">The above command returns all all PrincipalAssignment in the database "mykustodatabase" found in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="86d30-113">Beispiel 2: Abrufen eines bestimmten PrincipalAssignment in einer Datenbank nach Name</span><span class="sxs-lookup"><span data-stu-id="86d30-113">Example 2: Get a specific PrincipalAssignment in a database by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -PrincipalAssignmentName kustoprincipal1

Name                                                Type
----                                                ----
testnewkustocluster/mykustodatabase/kustoprincipal1 Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
```

<span data-ttu-id="86d30-114">Der obige Befehl gibt alle PrincipalAssignment namens "kustoprincipal1" in der Datenbank "mykustodatabase" zurück, die im Cluster "testnewkustocluster" gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="86d30-114">The above command returns all all PrincipalAssignment named "kustoprincipal1" in the database "mykustodatabase" found in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="86d30-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="86d30-115">PARAMETERS</span></span>

### <span data-ttu-id="86d30-116">-Clustername</span><span class="sxs-lookup"><span data-stu-id="86d30-116">-ClusterName</span></span>
<span data-ttu-id="86d30-117">Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="86d30-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="86d30-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="86d30-118">-DatabaseName</span></span>
<span data-ttu-id="86d30-119">Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="86d30-119">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="86d30-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86d30-120">-DefaultProfile</span></span>
<span data-ttu-id="86d30-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="86d30-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86d30-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="86d30-122">-InputObject</span></span>
<span data-ttu-id="86d30-123">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="86d30-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="86d30-124">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="86d30-124">-PrincipalAssignmentName</span></span>
<span data-ttu-id="86d30-125">Der Name des Kusto-principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="86d30-125">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="86d30-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86d30-126">-ResourceGroupName</span></span>
<span data-ttu-id="86d30-127">Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="86d30-127">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="86d30-128">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="86d30-128">-SubscriptionId</span></span>
<span data-ttu-id="86d30-129">Ruft Abonnement Anmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="86d30-129">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="86d30-130">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="86d30-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="86d30-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86d30-131">CommonParameters</span></span>
<span data-ttu-id="86d30-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86d30-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86d30-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="86d30-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86d30-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="86d30-134">INPUTS</span></span>

### <span data-ttu-id="86d30-135">Microsoft. Azure. PowerShell. Cmdlets. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="86d30-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="86d30-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="86d30-136">OUTPUTS</span></span>

### <span data-ttu-id="86d30-137">Microsoft. Azure. PowerShell. Cmdlets. Kusto. Models. Api20200614. IDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="86d30-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="86d30-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="86d30-138">NOTES</span></span>

<span data-ttu-id="86d30-139">Aliase</span><span class="sxs-lookup"><span data-stu-id="86d30-139">ALIASES</span></span>

<span data-ttu-id="86d30-140">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="86d30-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="86d30-141">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="86d30-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="86d30-142">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="86d30-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="86d30-143">Inputobject <IKustoIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="86d30-143">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="86d30-144">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="86d30-144">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="86d30-145">`[ClusterName <String>]`: Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="86d30-145">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="86d30-146">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="86d30-146">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="86d30-147">`[DatabaseName <String>]`: Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="86d30-147">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="86d30-148">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="86d30-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="86d30-149">`[Location <String>]`: Azure-Position.</span><span class="sxs-lookup"><span data-stu-id="86d30-149">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="86d30-150">`[PrincipalAssignmentName <String>]`: Der Name des Kusto-principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="86d30-150">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="86d30-151">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="86d30-151">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="86d30-152">`[SubscriptionId <String>]`: Ruft Abonnement Anmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="86d30-152">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="86d30-153">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="86d30-153">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="86d30-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="86d30-154">RELATED LINKS</span></span>

