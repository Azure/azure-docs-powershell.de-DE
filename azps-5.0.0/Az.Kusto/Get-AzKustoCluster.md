---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoCluster.md
ms.openlocfilehash: a95f8a00578ccf917a55cdfd9685dedf9a20734f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179228"
---
# <span data-ttu-id="eb39e-101">Get-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="eb39e-101">Get-AzKustoCluster</span></span>

## <span data-ttu-id="eb39e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="eb39e-102">SYNOPSIS</span></span>
<span data-ttu-id="eb39e-103">Ruft einen Kusto-Cluster ab.</span><span class="sxs-lookup"><span data-stu-id="eb39e-103">Gets a Kusto cluster.</span></span>

## <span data-ttu-id="eb39e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="eb39e-104">SYNTAX</span></span>

### <span data-ttu-id="eb39e-105">List1 (Standard)</span><span class="sxs-lookup"><span data-stu-id="eb39e-105">List1 (Default)</span></span>
```
Get-AzKustoCluster [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="eb39e-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="eb39e-106">Get</span></span>
```
Get-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="eb39e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="eb39e-107">GetViaIdentity</span></span>
```
Get-AzKustoCluster -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="eb39e-108">Liste</span><span class="sxs-lookup"><span data-stu-id="eb39e-108">List</span></span>
```
Get-AzKustoCluster -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="eb39e-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eb39e-109">DESCRIPTION</span></span>
<span data-ttu-id="eb39e-110">Ruft einen Kusto-Cluster ab.</span><span class="sxs-lookup"><span data-stu-id="eb39e-110">Gets a Kusto cluster.</span></span>

## <span data-ttu-id="eb39e-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="eb39e-111">EXAMPLES</span></span>

### <span data-ttu-id="eb39e-112">Beispiel 1: Auflisten aller Kusto-Cluster in einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="eb39e-112">Example 1: List all Kusto clusters in a resource group</span></span>
```powershell
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg

Location Name                 Type                     Zone
-------- ----                 ----                     ----
East US  testnewkustocluster  Microsoft.Kusto/Clusters
East US  testnewkustocluster2 Microsoft.Kusto/Clusters
```

<span data-ttu-id="eb39e-113">Der obige Befehl listet alle Kusto-Cluster in der Ressourcengruppe "testrg" auf.</span><span class="sxs-lookup"><span data-stu-id="eb39e-113">The above command lists all Kusto clusters in the resource group "testrg".</span></span>

### <span data-ttu-id="eb39e-114">Beispiel 2: Abrufen eines bestimmten Kusto-Clusters anhand des Namens</span><span class="sxs-lookup"><span data-stu-id="eb39e-114">Example 2: Get a specific Kusto cluster by name</span></span>
```powershell
PS C:\>  Get-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="eb39e-115">Der obige Befehl gibt den Kusto-Cluster mit dem Namen "testnewkustocluster" in der Ressourcengruppe "testrg" zurück.</span><span class="sxs-lookup"><span data-stu-id="eb39e-115">The above command returns the Kusto cluster named "testnewkustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="eb39e-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="eb39e-116">PARAMETERS</span></span>

### <span data-ttu-id="eb39e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb39e-117">-DefaultProfile</span></span>
<span data-ttu-id="eb39e-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="eb39e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb39e-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="eb39e-119">-InputObject</span></span>
<span data-ttu-id="eb39e-120">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="eb39e-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="eb39e-121">-Name</span><span class="sxs-lookup"><span data-stu-id="eb39e-121">-Name</span></span>
<span data-ttu-id="eb39e-122">Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="eb39e-122">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb39e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb39e-123">-ResourceGroupName</span></span>
<span data-ttu-id="eb39e-124">Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="eb39e-124">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="eb39e-125">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="eb39e-125">-SubscriptionId</span></span>
<span data-ttu-id="eb39e-126">Ruft Abonnement Anmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="eb39e-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="eb39e-127">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="eb39e-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb39e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb39e-128">CommonParameters</span></span>
<span data-ttu-id="eb39e-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb39e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb39e-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eb39e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb39e-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="eb39e-131">INPUTS</span></span>

### <span data-ttu-id="eb39e-132">Microsoft. Azure. PowerShell. Cmdlets. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="eb39e-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="eb39e-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="eb39e-133">OUTPUTS</span></span>

### <span data-ttu-id="eb39e-134">Microsoft. Azure. PowerShell. Cmdlets. Kusto. Models. Api20200614. ICluster</span><span class="sxs-lookup"><span data-stu-id="eb39e-134">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICluster</span></span>

## <span data-ttu-id="eb39e-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="eb39e-135">NOTES</span></span>

<span data-ttu-id="eb39e-136">Aliase</span><span class="sxs-lookup"><span data-stu-id="eb39e-136">ALIASES</span></span>

<span data-ttu-id="eb39e-137">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="eb39e-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="eb39e-138">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="eb39e-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="eb39e-139">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="eb39e-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="eb39e-140">Inputobject <IKustoIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="eb39e-140">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="eb39e-141">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="eb39e-141">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="eb39e-142">`[ClusterName <String>]`: Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="eb39e-142">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="eb39e-143">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="eb39e-143">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="eb39e-144">`[DatabaseName <String>]`: Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="eb39e-144">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="eb39e-145">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="eb39e-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="eb39e-146">`[Location <String>]`: Azure-Position.</span><span class="sxs-lookup"><span data-stu-id="eb39e-146">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="eb39e-147">`[PrincipalAssignmentName <String>]`: Der Name des Kusto-principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="eb39e-147">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="eb39e-148">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="eb39e-148">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="eb39e-149">`[SubscriptionId <String>]`: Ruft Abonnement Anmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="eb39e-149">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="eb39e-150">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="eb39e-150">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="eb39e-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="eb39e-151">RELATED LINKS</span></span>

