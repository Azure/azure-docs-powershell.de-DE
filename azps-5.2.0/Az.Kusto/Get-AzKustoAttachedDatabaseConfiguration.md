---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoattacheddatabaseconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoAttachedDatabaseConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoAttachedDatabaseConfiguration.md
ms.openlocfilehash: fd735b1d343c046f9ca2f0528bff4bf7ce8a403d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361596"
---
# <span data-ttu-id="fd529-101">Get-AzKustoAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="fd529-101">Get-AzKustoAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="fd529-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd529-102">SYNOPSIS</span></span>
<span data-ttu-id="fd529-103">Gibt eine angefügte Datenbankkonfiguration zurück.</span><span class="sxs-lookup"><span data-stu-id="fd529-103">Returns an attached database configuration.</span></span>

## <span data-ttu-id="fd529-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fd529-104">SYNTAX</span></span>

### <span data-ttu-id="fd529-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="fd529-105">List (Default)</span></span>
```
Get-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="fd529-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="fd529-106">Get</span></span>
```
Get-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="fd529-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="fd529-107">GetViaIdentity</span></span>
```
Get-AzKustoAttachedDatabaseConfiguration -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="fd529-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fd529-108">DESCRIPTION</span></span>
<span data-ttu-id="fd529-109">Gibt eine angefügte Datenbankkonfiguration zurück.</span><span class="sxs-lookup"><span data-stu-id="fd529-109">Returns an attached database configuration.</span></span>

## <span data-ttu-id="fd529-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fd529-110">EXAMPLES</span></span>

### <span data-ttu-id="fd529-111">Beispiel 1: Auflisten aller AttachedDatabaseConfigurations in einem Cluster</span><span class="sxs-lookup"><span data-stu-id="fd529-111">Example 1: List all the AttachedDatabaseConfigurations in a cluster</span></span>
```powershell
PS C:\> Get-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf"

Name                                 Type                                                    Location
----                                 ----                                                    --------
testnewkustoclusterf/myfollowerconfiguration Microsoft.Kusto/Clusters/AttachedDatabaseConfigurations East US
```

<span data-ttu-id="fd529-112">Der oben aufgeführte Befehl listet alle AttachedDatabaseConfigurations im Cluster "testnewkustoclusterf" auf.</span><span class="sxs-lookup"><span data-stu-id="fd529-112">The above command lists all the AttachedDatabaseConfigurations in the cluster "testnewkustoclusterf".</span></span>

### <span data-ttu-id="fd529-113">Beispiel 2: Erhalten einer bestimmten AttachedDatabaseConfiguration in einem Cluster</span><span class="sxs-lookup"><span data-stu-id="fd529-113">Example 2: Get a specific AttachedDatabaseConfiguration in a cluster</span></span>
```powershell
PS C:\>  Get-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf" -Name "myfollowerconfiguration" 

Name                                 Type                                                    Location
----                                 ----                                                    --------
testnewkustoclusterf/myfollowerconfiguration Microsoft.Kusto/Clusters/AttachedDatabaseConfigurations East US
```

<span data-ttu-id="fd529-114">Der oben aufgeführte Befehl gibt die AttachedDatabaseConfigurations namens "myfollowerconfiguration" im Cluster "testnewkustoclusterf" zurück.</span><span class="sxs-lookup"><span data-stu-id="fd529-114">The above command returns the AttachedDatabaseConfigurations named "myfollowerconfiguration" in the cluster "testnewkustoclusterf".</span></span>

## <span data-ttu-id="fd529-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd529-115">PARAMETERS</span></span>

### <span data-ttu-id="fd529-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="fd529-116">-ClusterName</span></span>
<span data-ttu-id="fd529-117">Der Name des Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="fd529-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="fd529-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd529-118">-DefaultProfile</span></span>
<span data-ttu-id="fd529-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fd529-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd529-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd529-120">-InputObject</span></span>
<span data-ttu-id="fd529-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="fd529-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="fd529-122">-Name</span><span class="sxs-lookup"><span data-stu-id="fd529-122">-Name</span></span>
<span data-ttu-id="fd529-123">Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="fd529-123">The name of the attached database configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AttachedDatabaseConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd529-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd529-124">-ResourceGroupName</span></span>
<span data-ttu-id="fd529-125">Der Name der Ressourcengruppe, die den Cluster "Kusto" enthält.</span><span class="sxs-lookup"><span data-stu-id="fd529-125">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="fd529-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fd529-126">-SubscriptionId</span></span>
<span data-ttu-id="fd529-127">Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="fd529-127">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="fd529-128">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="fd529-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="fd529-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd529-129">CommonParameters</span></span>
<span data-ttu-id="fd529-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd529-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd529-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fd529-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd529-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fd529-132">INPUTS</span></span>

### <span data-ttu-id="fd529-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="fd529-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="fd529-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fd529-134">OUTPUTS</span></span>

### <span data-ttu-id="fd529-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="fd529-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="fd529-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fd529-136">NOTES</span></span>

<span data-ttu-id="fd529-137">ALIASE</span><span class="sxs-lookup"><span data-stu-id="fd529-137">ALIASES</span></span>

<span data-ttu-id="fd529-138">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="fd529-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fd529-139">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fd529-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fd529-140">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fd529-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fd529-141">INPUTOBJECT <IKustoIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="fd529-141">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fd529-142">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="fd529-142">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="fd529-143">`[ClusterName <String>]`: Der Name des Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="fd529-143">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="fd529-144">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="fd529-144">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="fd529-145">`[DatabaseName <String>]`: Der Name der Datenbank im Cluster "Kusto".</span><span class="sxs-lookup"><span data-stu-id="fd529-145">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="fd529-146">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="fd529-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fd529-147">`[Location <String>]`: Azure-Standort.</span><span class="sxs-lookup"><span data-stu-id="fd529-147">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="fd529-148">`[PrincipalAssignmentName <String>]`: Der Name der Kusto PrincipalAssignment.</span><span class="sxs-lookup"><span data-stu-id="fd529-148">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="fd529-149">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Cluster "Kusto" enthält.</span><span class="sxs-lookup"><span data-stu-id="fd529-149">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="fd529-150">`[SubscriptionId <String>]`: Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="fd529-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="fd529-151">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="fd529-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="fd529-152">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fd529-152">RELATED LINKS</span></span>

