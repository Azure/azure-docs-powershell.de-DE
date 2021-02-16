---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustodatabaseprincipalassignmentnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDatabasePrincipalAssignmentNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDatabasePrincipalAssignmentNameAvailability.md
ms.openlocfilehash: b4a670046403aafb4b40740c34f27d7c81bcf8e0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100170412"
---
# <span data-ttu-id="ae704-101">Test-AzKustoDatabasePrincipalAssignmentNameAvailability</span><span class="sxs-lookup"><span data-stu-id="ae704-101">Test-AzKustoDatabasePrincipalAssignmentNameAvailability</span></span>

## <span data-ttu-id="ae704-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae704-102">SYNOPSIS</span></span>
<span data-ttu-id="ae704-103">Überprüft, ob die Datenbankprinzipalzuordnung gültig und noch nicht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ae704-103">Checks that the database principal assignment is valid and is not already in use.</span></span>

## <span data-ttu-id="ae704-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ae704-104">SYNTAX</span></span>

### <span data-ttu-id="ae704-105">CheckExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="ae704-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoDatabasePrincipalAssignmentNameAvailability -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -Name <String> -Type <Type> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ae704-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="ae704-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoDatabasePrincipalAssignmentNameAvailability -InputObject <IKustoIdentity> -Name <String>
 -Type <Type> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ae704-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ae704-107">DESCRIPTION</span></span>
<span data-ttu-id="ae704-108">Überprüft, ob die Datenbankprinzipalzuordnung gültig und noch nicht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ae704-108">Checks that the database principal assignment is valid and is not already in use.</span></span>

## <span data-ttu-id="ae704-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ae704-109">EXAMPLES</span></span>

### <span data-ttu-id="ae704-110">Beispiel 1: Überprüfen der Verfügbarkeit eines Datenbankprinzipalnamens, der verwendet wird</span><span class="sxs-lookup"><span data-stu-id="ae704-110">Example 1: Check the availability of a database principalassignment name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -Name "myprincipal" -Type "Microsoft.Kusto/Clusters/Database/principalAssignments" 

Message                                                                                                                                   Name            NameAvailable Reason
-------                                                                                                                                    ----            ------------- ------
Database principal assignment myprincipal already exists in database mykustodatabase. Please select a different principal assignment name. myprincipal   False
```

<span data-ttu-id="ae704-111">Der oben aufgeführte Befehl gibt zurück, ob ein PrincipalAssignment namens "myprincipal" in der Datenbank "mykustodatabase" aus dem Cluster "testnewkustocluster" vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="ae704-111">The above command returns whether or not a PrincipalAssignment named "myprincipal" exists in the database "mykustodatabase" from cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="ae704-112">Beispiel 2: Überprüfen der Verfügbarkeit eines Namen für die Prinzipalzuweisung, der nicht verwendet wird</span><span class="sxs-lookup"><span data-stu-id="ae704-112">Example 2: Check the availability of a database principalassignment name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -Name "newprincipal" -Type "Microsoft.Kusto/Clusters/Database/principalAssignments"

Message Name                  NameAvailable Reason
------- ----                  ------------- ------
        availablekustocluster True
```

<span data-ttu-id="ae704-113">Der oben aufgeführte Befehl gibt zurück, ob ein PrincipalAssignment namens "myprincipal" in der Datenbank "mykustodatabase" aus dem Cluster "testnewkustocluster" vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="ae704-113">The above command returns whether or not a PrincipalAssignment named "myprincipal" exists in the database "mykustodatabase" from cluster "testnewkustocluster" .</span></span>

## <span data-ttu-id="ae704-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ae704-114">PARAMETERS</span></span>

### <span data-ttu-id="ae704-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="ae704-115">-ClusterName</span></span>
<span data-ttu-id="ae704-116">Der Name des Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="ae704-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="ae704-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ae704-117">-DatabaseName</span></span>
<span data-ttu-id="ae704-118">Der Name der Datenbank im Cluster "Kusto".</span><span class="sxs-lookup"><span data-stu-id="ae704-118">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="ae704-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae704-119">-DefaultProfile</span></span>
<span data-ttu-id="ae704-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ae704-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae704-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ae704-121">-InputObject</span></span>
<span data-ttu-id="ae704-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="ae704-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ae704-123">-Name</span><span class="sxs-lookup"><span data-stu-id="ae704-123">-Name</span></span>
<span data-ttu-id="ae704-124">Ressourcenname der Hauptzuordnung.</span><span class="sxs-lookup"><span data-stu-id="ae704-124">Principal Assignment resource name.</span></span>

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

### <span data-ttu-id="ae704-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae704-125">-ResourceGroupName</span></span>
<span data-ttu-id="ae704-126">Der Name der Ressourcengruppe, die den Cluster "Kusto" enthält.</span><span class="sxs-lookup"><span data-stu-id="ae704-126">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="ae704-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ae704-127">-SubscriptionId</span></span>
<span data-ttu-id="ae704-128">Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="ae704-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ae704-129">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="ae704-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ae704-130">-Type</span><span class="sxs-lookup"><span data-stu-id="ae704-130">-Type</span></span>
<span data-ttu-id="ae704-131">Der Ressourcentyp "Microsoft.Kusto/Cluster/Databases/principalAssignments".</span><span class="sxs-lookup"><span data-stu-id="ae704-131">The type of resource, Microsoft.Kusto/Clusters/Databases/principalAssignments.</span></span>

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

### <span data-ttu-id="ae704-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ae704-132">-Confirm</span></span>
<span data-ttu-id="ae704-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ae704-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae704-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ae704-134">-WhatIf</span></span>
<span data-ttu-id="ae704-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ae704-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae704-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ae704-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae704-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae704-137">CommonParameters</span></span>
<span data-ttu-id="ae704-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae704-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae704-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ae704-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae704-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ae704-140">INPUTS</span></span>

### <span data-ttu-id="ae704-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="ae704-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="ae704-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ae704-142">OUTPUTS</span></span>

### <span data-ttu-id="ae704-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="ae704-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span></span>

## <span data-ttu-id="ae704-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ae704-144">NOTES</span></span>

<span data-ttu-id="ae704-145">ALIASE</span><span class="sxs-lookup"><span data-stu-id="ae704-145">ALIASES</span></span>

<span data-ttu-id="ae704-146">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="ae704-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ae704-147">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ae704-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ae704-148">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ae704-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ae704-149">INPUTOBJECT <IKustoIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="ae704-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ae704-150">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="ae704-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="ae704-151">`[ClusterName <String>]`: Der Name des Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="ae704-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="ae704-152">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="ae704-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="ae704-153">`[DatabaseName <String>]`: Der Name der Datenbank im Cluster "Kusto".</span><span class="sxs-lookup"><span data-stu-id="ae704-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="ae704-154">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="ae704-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ae704-155">`[Location <String>]`: Azure-Standort.</span><span class="sxs-lookup"><span data-stu-id="ae704-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="ae704-156">`[PrincipalAssignmentName <String>]`: Der Name der Kusto PrincipalAssignment.</span><span class="sxs-lookup"><span data-stu-id="ae704-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="ae704-157">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Cluster "Kusto" enthält.</span><span class="sxs-lookup"><span data-stu-id="ae704-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="ae704-158">`[SubscriptionId <String>]`: Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="ae704-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="ae704-159">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="ae704-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="ae704-160">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ae704-160">RELATED LINKS</span></span>

