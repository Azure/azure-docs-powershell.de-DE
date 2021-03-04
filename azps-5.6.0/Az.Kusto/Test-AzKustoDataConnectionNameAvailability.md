---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/test-azkustodataconnectionnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDataConnectionNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDataConnectionNameAvailability.md
ms.openlocfilehash: b33f496845cf03a31a90203d5a4d10076d156e59
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946531"
---
# <span data-ttu-id="96bd2-101">Test-AzKustoDataConnectionNameAvailability</span><span class="sxs-lookup"><span data-stu-id="96bd2-101">Test-AzKustoDataConnectionNameAvailability</span></span>

## <span data-ttu-id="96bd2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96bd2-102">SYNOPSIS</span></span>
<span data-ttu-id="96bd2-103">Überprüft, ob der Name der Datenverbindung gültig und noch nicht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="96bd2-103">Checks that the data connection name is valid and is not already in use.</span></span>

## <span data-ttu-id="96bd2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="96bd2-104">SYNTAX</span></span>

### <span data-ttu-id="96bd2-105">CheckExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="96bd2-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoDataConnectionNameAvailability -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -Name <String> -Type <Type> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="96bd2-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="96bd2-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoDataConnectionNameAvailability -InputObject <IKustoIdentity> -Name <String> -Type <Type>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="96bd2-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="96bd2-107">DESCRIPTION</span></span>
<span data-ttu-id="96bd2-108">Überprüft, ob der Name der Datenverbindung gültig und noch nicht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="96bd2-108">Checks that the data connection name is valid and is not already in use.</span></span>

## <span data-ttu-id="96bd2-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="96bd2-109">EXAMPLES</span></span>

### <span data-ttu-id="96bd2-110">Beispiel 1: Überprüfen der Verfügbarkeit eines verwendeten Datenverbindungsnamens</span><span class="sxs-lookup"><span data-stu-id="96bd2-110">Example 1: Check the availability of a Data Connection name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoDataConnectionNameAvailability -ClusterName testnewkustocluster -DatabaseName mykustodatabase -ResourceGroupName testrg -Name mykustodataconnection -Type Microsoft.Kusto/Clusters/Databases/dataConnections

Message                                                                                                                                                          Name                  NameAvailable Reason
-------                                                                                                                                                          ----                  ------------- ------
Data Connection mykustodataconnection already exists in database mykustodatabase in cluster testnewkustocluster. Please select a different data connection name. mykustodataconnection False         AlreadyExists
```

<span data-ttu-id="96bd2-111">Der obige Befehl gibt zurück, ob eine Datenverbindung mit dem Namen "mykustodataconnection" in der Datenbank "mykustodatabase" vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="96bd2-111">The above command returns whether or not a Data Connection named "mykustodataconnection" exists in the "mykustodatabase" database.</span></span>

### <span data-ttu-id="96bd2-112">Beispiel 2: Überprüfen der Verfügbarkeit eines Nicht verwendeten Datenverbindungsnamens</span><span class="sxs-lookup"><span data-stu-id="96bd2-112">Example 2: Check the availability of a Data Connection name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoDataConnectionNameAvailability -ClusterName testnewkustocluster -DatabaseName mykustodatabase -ResourceGroupName testrg -Name mydataconnection -Type Microsoft.Kusto/Clusters/Databases/dataConnections

Message Name             NameAvailable Reason
------- ----             ------------- ------
        mydataconnection True
```

<span data-ttu-id="96bd2-113">Der obige Befehl gibt zurück, ob eine Datenverbindung mit dem Namen "mydataconnection" in der Datenbank "mykustodatabase" vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="96bd2-113">The above command returns whether or not a Data Connection named "mydataconnection" exists in the "mykustodatabase" database.</span></span>

## <span data-ttu-id="96bd2-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="96bd2-114">PARAMETERS</span></span>

### <span data-ttu-id="96bd2-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="96bd2-115">-ClusterName</span></span>
<span data-ttu-id="96bd2-116">Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="96bd2-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="96bd2-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="96bd2-117">-DatabaseName</span></span>
<span data-ttu-id="96bd2-118">Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="96bd2-118">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="96bd2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96bd2-119">-DefaultProfile</span></span>
<span data-ttu-id="96bd2-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="96bd2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96bd2-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="96bd2-121">-InputObject</span></span>
<span data-ttu-id="96bd2-122">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="96bd2-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="96bd2-123">-Name</span><span class="sxs-lookup"><span data-stu-id="96bd2-123">-Name</span></span>
<span data-ttu-id="96bd2-124">Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="96bd2-124">Data Connection name.</span></span>

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

### <span data-ttu-id="96bd2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96bd2-125">-ResourceGroupName</span></span>
<span data-ttu-id="96bd2-126">Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="96bd2-126">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="96bd2-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="96bd2-127">-SubscriptionId</span></span>
<span data-ttu-id="96bd2-128">Ruft Abonnementanmeldeinformationen ab, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="96bd2-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="96bd2-129">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="96bd2-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="96bd2-130">-Type</span><span class="sxs-lookup"><span data-stu-id="96bd2-130">-Type</span></span>
<span data-ttu-id="96bd2-131">Der Ressourcentyp Microsoft.Kusto/Clusters/Databases/dataConnections.</span><span class="sxs-lookup"><span data-stu-id="96bd2-131">The type of resource, Microsoft.Kusto/Clusters/Databases/dataConnections.</span></span>

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

### <span data-ttu-id="96bd2-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="96bd2-132">-Confirm</span></span>
<span data-ttu-id="96bd2-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="96bd2-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96bd2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96bd2-134">-WhatIf</span></span>
<span data-ttu-id="96bd2-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="96bd2-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96bd2-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="96bd2-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96bd2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96bd2-137">CommonParameters</span></span>
<span data-ttu-id="96bd2-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96bd2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96bd2-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="96bd2-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96bd2-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="96bd2-140">INPUTS</span></span>

### <span data-ttu-id="96bd2-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="96bd2-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="96bd2-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="96bd2-142">OUTPUTS</span></span>

### <span data-ttu-id="96bd2-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="96bd2-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span></span>

## <span data-ttu-id="96bd2-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="96bd2-144">NOTES</span></span>

<span data-ttu-id="96bd2-145">ALIASE</span><span class="sxs-lookup"><span data-stu-id="96bd2-145">ALIASES</span></span>

<span data-ttu-id="96bd2-146">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="96bd2-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="96bd2-147">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="96bd2-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="96bd2-148">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="96bd2-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="96bd2-149">INPUTOBJECT <IKustoIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="96bd2-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="96bd2-150">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="96bd2-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="96bd2-151">`[ClusterName <String>]`: Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="96bd2-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="96bd2-152">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="96bd2-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="96bd2-153">`[DatabaseName <String>]`: Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="96bd2-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="96bd2-154">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="96bd2-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="96bd2-155">`[Location <String>]`: Azure-Standort.</span><span class="sxs-lookup"><span data-stu-id="96bd2-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="96bd2-156">`[PrincipalAssignmentName <String>]`: Der Name der Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="96bd2-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="96bd2-157">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="96bd2-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="96bd2-158">`[SubscriptionId <String>]`: Ruft Abonnementanmeldeinformationen ab, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="96bd2-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="96bd2-159">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="96bd2-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="96bd2-160">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="96bd2-160">RELATED LINKS</span></span>

