---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustoclusternameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterNameAvailability.md
ms.openlocfilehash: d7dc3a154049e486490edddd5fbda52a552d32c5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470457"
---
# <span data-ttu-id="e23bb-101">Test-AzKustoClusterNameAvailability</span><span class="sxs-lookup"><span data-stu-id="e23bb-101">Test-AzKustoClusterNameAvailability</span></span>

## <span data-ttu-id="e23bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e23bb-102">SYNOPSIS</span></span>
<span data-ttu-id="e23bb-103">Überprüft, ob der Clustername gültig und noch nicht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e23bb-103">Checks that the cluster name is valid and is not already in use.</span></span>

## <span data-ttu-id="e23bb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e23bb-104">SYNTAX</span></span>

### <span data-ttu-id="e23bb-105">CheckExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="e23bb-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoClusterNameAvailability -Location <String> -Name <String> -Type <Type> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e23bb-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="e23bb-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoClusterNameAvailability -InputObject <IKustoIdentity> -Name <String> -Type <Type>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e23bb-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e23bb-107">DESCRIPTION</span></span>
<span data-ttu-id="e23bb-108">Überprüft, ob der Clustername gültig und noch nicht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e23bb-108">Checks that the cluster name is valid and is not already in use.</span></span>

## <span data-ttu-id="e23bb-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e23bb-109">EXAMPLES</span></span>

### <span data-ttu-id="e23bb-110">Beispiel 1: Überprüfen der Verfügbarkeit eines verwendeten Namens eines Kusto-Clusters</span><span class="sxs-lookup"><span data-stu-id="e23bb-110">Example 1: Check the availability of a Kusto cluster name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterNameAvailability -Name testnewkustocluster -Location 'East US' -Type Microsoft.Kusto/clusters

Message                                                                                       Name                NameAvailable Reason
-------                                                                                       ----                ------------- ------
Name 'testnewkustocluster' with type Engine is already taken. Please specify a different name testnewkustocluster False
```

<span data-ttu-id="e23bb-111">Der oben aufgeführte Befehl gibt zurück, ob ein Kusto-Cluster mit dem Namen "testnewkustocluster" in der Region "Ost US" vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="e23bb-111">The above command returns whether or not a Kusto cluster named "testnewkustocluster" exists in the "East US" region.</span></span>

### <span data-ttu-id="e23bb-112">Beispiel 2: Überprüfen der Verfügbarkeit eines nicht verwendeten Namens eines Kusto-Clusters</span><span class="sxs-lookup"><span data-stu-id="e23bb-112">Example 2: Check the availability of a Kusto cluster name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterNameAvailability -Name availablekustocluster -Location 'East US' -Type Microsoft.Kusto/clusters

Message Name                  NameAvailable Reason
------- ----                  ------------- ------
        availablekustocluster True
```

<span data-ttu-id="e23bb-113">Der oben aufgeführte Befehl gibt zurück, ob ein Kusto-Cluster namens "availablekustocluster" in der Region "Ost US" vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="e23bb-113">The above command returns whether or not a Kusto cluster named "availablekustocluster" exists in the "East US" region.</span></span>

## <span data-ttu-id="e23bb-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e23bb-114">PARAMETERS</span></span>

### <span data-ttu-id="e23bb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e23bb-115">-DefaultProfile</span></span>
<span data-ttu-id="e23bb-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e23bb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e23bb-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e23bb-117">-InputObject</span></span>
<span data-ttu-id="e23bb-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="e23bb-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: CheckViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e23bb-119">-Location</span><span class="sxs-lookup"><span data-stu-id="e23bb-119">-Location</span></span>
<span data-ttu-id="e23bb-120">Azure-Standort.</span><span class="sxs-lookup"><span data-stu-id="e23bb-120">Azure location.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e23bb-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e23bb-121">-Name</span></span>
<span data-ttu-id="e23bb-122">Clustername.</span><span class="sxs-lookup"><span data-stu-id="e23bb-122">Cluster name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e23bb-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e23bb-123">-SubscriptionId</span></span>
<span data-ttu-id="e23bb-124">Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="e23bb-124">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e23bb-125">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="e23bb-125">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e23bb-126">-Type</span><span class="sxs-lookup"><span data-stu-id="e23bb-126">-Type</span></span>
<span data-ttu-id="e23bb-127">Der Ressourcentyp "Microsoft.Kusto/cluster".</span><span class="sxs-lookup"><span data-stu-id="e23bb-127">The type of resource, Microsoft.Kusto/clusters.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Type
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e23bb-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e23bb-128">-Confirm</span></span>
<span data-ttu-id="e23bb-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e23bb-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e23bb-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="e23bb-130">-WhatIf</span></span>
<span data-ttu-id="e23bb-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e23bb-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e23bb-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e23bb-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e23bb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e23bb-133">CommonParameters</span></span>
<span data-ttu-id="e23bb-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e23bb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e23bb-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e23bb-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e23bb-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e23bb-136">INPUTS</span></span>

### <span data-ttu-id="e23bb-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="e23bb-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="e23bb-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e23bb-138">OUTPUTS</span></span>

### <span data-ttu-id="e23bb-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="e23bb-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span></span>

## <span data-ttu-id="e23bb-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e23bb-140">NOTES</span></span>

<span data-ttu-id="e23bb-141">ALIASE</span><span class="sxs-lookup"><span data-stu-id="e23bb-141">ALIASES</span></span>

<span data-ttu-id="e23bb-142">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="e23bb-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e23bb-143">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e23bb-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e23bb-144">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e23bb-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e23bb-145">INPUTOBJECT <IKustoIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="e23bb-145">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e23bb-146">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="e23bb-146">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="e23bb-147">`[ClusterName <String>]`: Der Name des Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="e23bb-147">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="e23bb-148">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="e23bb-148">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="e23bb-149">`[DatabaseName <String>]`: Der Name der Datenbank im Cluster "Kusto".</span><span class="sxs-lookup"><span data-stu-id="e23bb-149">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="e23bb-150">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="e23bb-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e23bb-151">`[Location <String>]`: Azure-Standort.</span><span class="sxs-lookup"><span data-stu-id="e23bb-151">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="e23bb-152">`[PrincipalAssignmentName <String>]`: Der Name der Kusto PrincipalAssignment.</span><span class="sxs-lookup"><span data-stu-id="e23bb-152">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="e23bb-153">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Cluster "Kusto" enthält.</span><span class="sxs-lookup"><span data-stu-id="e23bb-153">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="e23bb-154">`[SubscriptionId <String>]`: Ruft Abonnementanmeldeinformationen ab, mit denen Das Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="e23bb-154">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="e23bb-155">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="e23bb-155">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="e23bb-156">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e23bb-156">RELATED LINKS</span></span>

