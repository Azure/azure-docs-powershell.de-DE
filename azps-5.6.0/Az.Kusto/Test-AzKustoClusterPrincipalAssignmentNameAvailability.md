---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/test-azkustoclusterprincipalassignmentnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterPrincipalAssignmentNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterPrincipalAssignmentNameAvailability.md
ms.openlocfilehash: f1c96909421dcc21d2b1f318a923ef7f9b804bf8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950179"
---
# <span data-ttu-id="87068-101">Test-AzKustoClusterPrincipalAssignmentNameAvailability</span><span class="sxs-lookup"><span data-stu-id="87068-101">Test-AzKustoClusterPrincipalAssignmentNameAvailability</span></span>

## <span data-ttu-id="87068-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87068-102">SYNOPSIS</span></span>
<span data-ttu-id="87068-103">Überprüft, ob der Name der Hauptzuordnung gültig und noch nicht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="87068-103">Checks that the principal assignment name is valid and is not already in use.</span></span>

## <span data-ttu-id="87068-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="87068-104">SYNTAX</span></span>

### <span data-ttu-id="87068-105">CheckExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="87068-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoClusterPrincipalAssignmentNameAvailability -ClusterName <String> -ResourceGroupName <String>
 -Name <String> -Type <Type> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="87068-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="87068-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoClusterPrincipalAssignmentNameAvailability -InputObject <IKustoIdentity> -Name <String>
 -Type <Type> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="87068-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="87068-107">DESCRIPTION</span></span>
<span data-ttu-id="87068-108">Überprüft, ob der Name der Hauptzuordnung gültig und noch nicht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="87068-108">Checks that the principal assignment name is valid and is not already in use.</span></span>

## <span data-ttu-id="87068-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="87068-109">EXAMPLES</span></span>

### <span data-ttu-id="87068-110">Beispiel 1: Überprüfen der Verfügbarkeit eines verwendeten Clusterprinzipalnamens</span><span class="sxs-lookup"><span data-stu-id="87068-110">Example 1: Check the availability of a cluster principalassignment name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -Name "myprincipal" -Type "Microsoft.Kusto/clusters/principalAssignments" 

Message                                                                                                        Name            NameAvailable Reason
-------                                                                                                        ----            ------------- ------
PrincipalAssignment myprincipal already exists in cluster testnewkustocluster. Please select a different name. myprincipal   False
```

<span data-ttu-id="87068-111">Der obige Befehl gibt zurück, ob im Cluster "testnewkustocluster" ein PrincipalAssignment mit dem Namen "myprincipal" vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="87068-111">The above command returns whether or not a PrincipalAssignment named "myprincipal" exists in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="87068-112">Beispiel 2: Überprüfen der Verfügbarkeit eines Clusterprinzipalnamens, der nicht verwendet wird</span><span class="sxs-lookup"><span data-stu-id="87068-112">Example 2: Check the availability of a cluster principalassignment name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -Name "newprincipal" -Type "Microsoft.Kusto/clusters/principalAssignments"

Message Name                  NameAvailable Reason
------- ----                  ------------- ------
        availablekustocluster True
```

<span data-ttu-id="87068-113">Der obige Befehl gibt zurück, ob im Cluster "testnewkustocluster" ein PrincipalAssignment mit dem Namen "newprincipal" vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="87068-113">The above command returns whether or not a PrincipalAssignment named "newprincipal" exists in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="87068-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="87068-114">PARAMETERS</span></span>

### <span data-ttu-id="87068-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="87068-115">-ClusterName</span></span>
<span data-ttu-id="87068-116">Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="87068-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="87068-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87068-117">-DefaultProfile</span></span>
<span data-ttu-id="87068-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="87068-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87068-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="87068-119">-InputObject</span></span>
<span data-ttu-id="87068-120">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="87068-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="87068-121">-Name</span><span class="sxs-lookup"><span data-stu-id="87068-121">-Name</span></span>
<span data-ttu-id="87068-122">Ressourcenname der Hauptzuordnung.</span><span class="sxs-lookup"><span data-stu-id="87068-122">Principal Assignment resource name.</span></span>

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

### <span data-ttu-id="87068-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87068-123">-ResourceGroupName</span></span>
<span data-ttu-id="87068-124">Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="87068-124">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="87068-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="87068-125">-SubscriptionId</span></span>
<span data-ttu-id="87068-126">Ruft Abonnementanmeldeinformationen ab, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="87068-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="87068-127">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="87068-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="87068-128">-Type</span><span class="sxs-lookup"><span data-stu-id="87068-128">-Type</span></span>
<span data-ttu-id="87068-129">Der Ressourcentyp Microsoft.Kusto/Clusters/principalAssignments.</span><span class="sxs-lookup"><span data-stu-id="87068-129">The type of resource, Microsoft.Kusto/Clusters/principalAssignments.</span></span>

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

### <span data-ttu-id="87068-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="87068-130">-Confirm</span></span>
<span data-ttu-id="87068-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="87068-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87068-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87068-132">-WhatIf</span></span>
<span data-ttu-id="87068-133">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="87068-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87068-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="87068-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87068-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87068-135">CommonParameters</span></span>
<span data-ttu-id="87068-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87068-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87068-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="87068-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87068-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="87068-138">INPUTS</span></span>

### <span data-ttu-id="87068-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="87068-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="87068-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="87068-140">OUTPUTS</span></span>

### <span data-ttu-id="87068-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="87068-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span></span>

## <span data-ttu-id="87068-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="87068-142">NOTES</span></span>

<span data-ttu-id="87068-143">ALIASE</span><span class="sxs-lookup"><span data-stu-id="87068-143">ALIASES</span></span>

<span data-ttu-id="87068-144">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="87068-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="87068-145">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="87068-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="87068-146">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="87068-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="87068-147">INPUTOBJECT <IKustoIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="87068-147">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="87068-148">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="87068-148">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="87068-149">`[ClusterName <String>]`: Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="87068-149">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="87068-150">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="87068-150">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="87068-151">`[DatabaseName <String>]`: Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="87068-151">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="87068-152">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="87068-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="87068-153">`[Location <String>]`: Azure-Standort.</span><span class="sxs-lookup"><span data-stu-id="87068-153">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="87068-154">`[PrincipalAssignmentName <String>]`: Der Name der Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="87068-154">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="87068-155">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="87068-155">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="87068-156">`[SubscriptionId <String>]`: Ruft Abonnementanmeldeinformationen ab, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="87068-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="87068-157">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="87068-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="87068-158">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="87068-158">RELATED LINKS</span></span>

