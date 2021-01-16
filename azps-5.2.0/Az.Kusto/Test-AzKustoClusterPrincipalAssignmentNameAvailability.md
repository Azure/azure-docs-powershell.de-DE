---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustoclusterprincipalassignmentnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterPrincipalAssignmentNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterPrincipalAssignmentNameAvailability.md
ms.openlocfilehash: cb4f375632626ee3c3428e6a990a228dacecd288
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98305051"
---
# <span data-ttu-id="39c3f-101">Test-AzKustoClusterPrincipalAssignmentNameAvailability</span><span class="sxs-lookup"><span data-stu-id="39c3f-101">Test-AzKustoClusterPrincipalAssignmentNameAvailability</span></span>

## <span data-ttu-id="39c3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39c3f-102">SYNOPSIS</span></span>
<span data-ttu-id="39c3f-103">Überprüft, ob der Name der Hauptzuordnung gültig und noch nicht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="39c3f-103">Checks that the principal assignment name is valid and is not already in use.</span></span>

## <span data-ttu-id="39c3f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="39c3f-104">SYNTAX</span></span>

### <span data-ttu-id="39c3f-105">CheckExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="39c3f-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoClusterPrincipalAssignmentNameAvailability -ClusterName <String> -ResourceGroupName <String>
 -Name <String> -Type <Type> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="39c3f-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="39c3f-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoClusterPrincipalAssignmentNameAvailability -InputObject <IKustoIdentity> -Name <String>
 -Type <Type> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="39c3f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="39c3f-107">DESCRIPTION</span></span>
<span data-ttu-id="39c3f-108">Überprüft, ob der Name der Hauptzuordnung gültig und noch nicht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="39c3f-108">Checks that the principal assignment name is valid and is not already in use.</span></span>

## <span data-ttu-id="39c3f-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="39c3f-109">EXAMPLES</span></span>

### <span data-ttu-id="39c3f-110">Beispiel 1: Überprüfen der Verfügbarkeit eines Clusterprinzipalnamens, der verwendet wird</span><span class="sxs-lookup"><span data-stu-id="39c3f-110">Example 1: Check the availability of a cluster principalassignment name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -Name "myprincipal" -Type "Microsoft.Kusto/clusters/principalAssignments" 

Message                                                                                                        Name            NameAvailable Reason
-------                                                                                                        ----            ------------- ------
PrincipalAssignment myprincipal already exists in cluster testnewkustocluster. Please select a different name. myprincipal   False
```

<span data-ttu-id="39c3f-111">Der oben aufgeführte Befehl gibt zurück, ob ein PrincipalAssignment namens "myprincipal" im Cluster "testnewkustocluster" vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="39c3f-111">The above command returns whether or not a PrincipalAssignment named "myprincipal" exists in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="39c3f-112">Beispiel 2: Überprüfen der Verfügbarkeit eines Clusterprinzipalnamens, der nicht verwendet wird</span><span class="sxs-lookup"><span data-stu-id="39c3f-112">Example 2: Check the availability of a cluster principalassignment name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -Name "newprincipal" -Type "Microsoft.Kusto/clusters/principalAssignments"

Message Name                  NameAvailable Reason
------- ----                  ------------- ------
        availablekustocluster True
```

<span data-ttu-id="39c3f-113">Der oben aufgeführte Befehl gibt zurück, ob ein PrincipalAssignment namens "newprincipal" im Cluster "testnewkustocluster" vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="39c3f-113">The above command returns whether or not a PrincipalAssignment named "newprincipal" exists in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="39c3f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39c3f-114">PARAMETERS</span></span>

### <span data-ttu-id="39c3f-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="39c3f-115">-ClusterName</span></span>
<span data-ttu-id="39c3f-116">Der Name des Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="39c3f-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="39c3f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39c3f-117">-DefaultProfile</span></span>
<span data-ttu-id="39c3f-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="39c3f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39c3f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="39c3f-119">-InputObject</span></span>
<span data-ttu-id="39c3f-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="39c3f-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="39c3f-121">-Name</span><span class="sxs-lookup"><span data-stu-id="39c3f-121">-Name</span></span>
<span data-ttu-id="39c3f-122">Ressourcenname der Hauptzuordnung.</span><span class="sxs-lookup"><span data-stu-id="39c3f-122">Principal Assignment resource name.</span></span>

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

### <span data-ttu-id="39c3f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39c3f-123">-ResourceGroupName</span></span>
<span data-ttu-id="39c3f-124">Der Name der Ressourcengruppe, die den Cluster "Kusto" enthält.</span><span class="sxs-lookup"><span data-stu-id="39c3f-124">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="39c3f-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="39c3f-125">-SubscriptionId</span></span>
<span data-ttu-id="39c3f-126">Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="39c3f-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="39c3f-127">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="39c3f-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="39c3f-128">-Type</span><span class="sxs-lookup"><span data-stu-id="39c3f-128">-Type</span></span>
<span data-ttu-id="39c3f-129">Der Ressourcentyp "Microsoft.Kusto/Cluster/principalAssignments".</span><span class="sxs-lookup"><span data-stu-id="39c3f-129">The type of resource, Microsoft.Kusto/Clusters/principalAssignments.</span></span>

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

### <span data-ttu-id="39c3f-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="39c3f-130">-Confirm</span></span>
<span data-ttu-id="39c3f-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="39c3f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39c3f-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="39c3f-132">-WhatIf</span></span>
<span data-ttu-id="39c3f-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="39c3f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39c3f-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="39c3f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39c3f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39c3f-135">CommonParameters</span></span>
<span data-ttu-id="39c3f-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39c3f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39c3f-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="39c3f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39c3f-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="39c3f-138">INPUTS</span></span>

### <span data-ttu-id="39c3f-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="39c3f-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="39c3f-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="39c3f-140">OUTPUTS</span></span>

### <span data-ttu-id="39c3f-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="39c3f-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICheckNameResult</span></span>

## <span data-ttu-id="39c3f-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="39c3f-142">NOTES</span></span>

<span data-ttu-id="39c3f-143">ALIASE</span><span class="sxs-lookup"><span data-stu-id="39c3f-143">ALIASES</span></span>

<span data-ttu-id="39c3f-144">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="39c3f-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="39c3f-145">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="39c3f-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="39c3f-146">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="39c3f-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="39c3f-147">INPUTOBJECT <IKustoIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="39c3f-147">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="39c3f-148">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="39c3f-148">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="39c3f-149">`[ClusterName <String>]`: Der Name des Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="39c3f-149">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="39c3f-150">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="39c3f-150">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="39c3f-151">`[DatabaseName <String>]`: Der Name der Datenbank im Cluster "Kusto".</span><span class="sxs-lookup"><span data-stu-id="39c3f-151">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="39c3f-152">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="39c3f-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="39c3f-153">`[Location <String>]`: Azure-Standort.</span><span class="sxs-lookup"><span data-stu-id="39c3f-153">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="39c3f-154">`[PrincipalAssignmentName <String>]`: Der Name der Kusto PrincipalAssignment.</span><span class="sxs-lookup"><span data-stu-id="39c3f-154">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="39c3f-155">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Cluster "Kusto" enthält.</span><span class="sxs-lookup"><span data-stu-id="39c3f-155">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="39c3f-156">`[SubscriptionId <String>]`: Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="39c3f-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="39c3f-157">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="39c3f-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="39c3f-158">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="39c3f-158">RELATED LINKS</span></span>

