---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustodatabasenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDatabaseNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDatabaseNameAvailability.md
ms.openlocfilehash: ab15d7a9da10e7e7a024d3af332f449cd011a290
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371047"
---
# <span data-ttu-id="56977-101">Test-AzKustoDatabaseNameAvailability</span><span class="sxs-lookup"><span data-stu-id="56977-101">Test-AzKustoDatabaseNameAvailability</span></span>

## <span data-ttu-id="56977-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56977-102">SYNOPSIS</span></span>
<span data-ttu-id="56977-103">Überprüft, ob der Datenbankname gültig und noch nicht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="56977-103">Checks that the database name is valid and is not already in use.</span></span>

## <span data-ttu-id="56977-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="56977-104">SYNTAX</span></span>

### <span data-ttu-id="56977-105">CheckExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="56977-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoDatabaseNameAvailability -ClusterName <String> -ResourceGroupName <String> -Name <String>
 -Type <Type> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="56977-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="56977-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoDatabaseNameAvailability -InputObject <IKustoIdentity> -Name <String> -Type <Type>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="56977-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="56977-107">DESCRIPTION</span></span>
<span data-ttu-id="56977-108">Überprüft, ob der Datenbankname gültig und noch nicht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="56977-108">Checks that the database name is valid and is not already in use.</span></span>

## <span data-ttu-id="56977-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="56977-109">EXAMPLES</span></span>

### <span data-ttu-id="56977-110">Beispiel 1: Überprüfen der Verfügbarkeit eines verwendeten Namen einer Kusto-Datenbank</span><span class="sxs-lookup"><span data-stu-id="56977-110">Example 1: Check the availability of a Kusto database name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoDatabaseNameAvailability -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase -Type Microsoft.Kusto/Clusters/Databases

Message                                                                                                          Name            NameAvailable Reason
-------                                                                                                          ----            ------------- ------
Database mykustodatabase already exists in cluster testnewkustocluster. Please select a different database name. mykustodatabase False
```

<span data-ttu-id="56977-111">Der oben aufgeführte Befehl gibt zurück, ob im Cluster "testnewkustocluster" eine "mykustodatabase"-Datenbank namens "mykustodatacluster" vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="56977-111">The above command returns whether or not a Kusto database named "mykustodatabase" exists in the "testnewkustocluster" cluster.</span></span>

### <span data-ttu-id="56977-112">Beispiel 2: Überprüfen der Verfügbarkeit eines nicht verwendeten Namen einer Kusto-Datenbank</span><span class="sxs-lookup"><span data-stu-id="56977-112">Example 2: Check the availability of a Kusto database name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoDatabaseNameAvailability -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase2 -Type Microsoft.Kusto/Clusters/Databases

Message Name             NameAvailable Reason
------- ----             ------------- ------
        mykustodatabase2 True
```

<span data-ttu-id="56977-113">Der oben aufgeführte Befehl gibt zurück, ob eine "mykustodatabase2"-Datenbank namens "mykustodatabase2" im Cluster "testnewkustocluster" vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="56977-113">The above command returns whether or not a Kusto database named "mykustodatabase2" exists in the "testnewkustocluster" cluster.</span></span>

## <span data-ttu-id="56977-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="56977-114">PARAMETERS</span></span>

### <span data-ttu-id="56977-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="56977-115">-ClusterName</span></span>
<span data-ttu-id="56977-116">Der Name des Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="56977-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="56977-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56977-117">-DefaultProfile</span></span>
<span data-ttu-id="56977-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="56977-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56977-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="56977-119">-InputObject</span></span>
<span data-ttu-id="56977-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="56977-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="56977-121">-Name</span><span class="sxs-lookup"><span data-stu-id="56977-121">-Name</span></span>
<span data-ttu-id="56977-122">Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="56977-122">Resource name.</span></span>

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

### <span data-ttu-id="56977-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56977-123">-ResourceGroupName</span></span>
<span data-ttu-id="56977-124">Der Name der Ressourcengruppe, die den Cluster "Kusto" enthält.</span><span class="sxs-lookup"><span data-stu-id="56977-124">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="56977-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="56977-125">-SubscriptionId</span></span>
<span data-ttu-id="56977-126">Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="56977-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="56977-127">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="56977-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="56977-128">-Type</span><span class="sxs-lookup"><span data-stu-id="56977-128">-Type</span></span>
<span data-ttu-id="56977-129">Der Ressourcentyp, z. B. "Microsoft.Kusto/Cluster/databases".</span><span class="sxs-lookup"><span data-stu-id="56977-129">The type of resource, for instance Microsoft.Kusto/Clusters/databases.</span></span>

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

### <span data-ttu-id="56977-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="56977-130">-Confirm</span></span>
<span data-ttu-id="56977-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="56977-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56977-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="56977-132">-WhatIf</span></span>
<span data-ttu-id="56977-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="56977-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56977-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="56977-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56977-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56977-135">CommonParameters</span></span>
<span data-ttu-id="56977-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56977-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56977-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="56977-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56977-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="56977-138">INPUTS</span></span>

### <span data-ttu-id="56977-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="56977-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="56977-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="56977-140">OUTPUTS</span></span>

### <span data-ttu-id="56977-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="56977-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICheckNameResult</span></span>

## <span data-ttu-id="56977-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="56977-142">NOTES</span></span>

<span data-ttu-id="56977-143">ALIASE</span><span class="sxs-lookup"><span data-stu-id="56977-143">ALIASES</span></span>

<span data-ttu-id="56977-144">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="56977-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="56977-145">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="56977-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="56977-146">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="56977-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="56977-147">INPUTOBJECT <IKustoIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="56977-147">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="56977-148">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="56977-148">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="56977-149">`[ClusterName <String>]`: Der Name des Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="56977-149">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="56977-150">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="56977-150">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="56977-151">`[DatabaseName <String>]`: Der Name der Datenbank im Cluster "Kusto".</span><span class="sxs-lookup"><span data-stu-id="56977-151">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="56977-152">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="56977-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="56977-153">`[Location <String>]`: Azure-Standort.</span><span class="sxs-lookup"><span data-stu-id="56977-153">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="56977-154">`[PrincipalAssignmentName <String>]`: Der Name der Kusto PrincipalAssignment.</span><span class="sxs-lookup"><span data-stu-id="56977-154">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="56977-155">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Cluster "Kusto" enthält.</span><span class="sxs-lookup"><span data-stu-id="56977-155">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="56977-156">`[SubscriptionId <String>]`: Ruft Abonnementanmeldeinformationen ab, mit denen Das Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="56977-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="56977-157">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="56977-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="56977-158">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="56977-158">RELATED LINKS</span></span>

