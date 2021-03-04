---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/test-azkustodatabaseprincipalassignmentnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDatabasePrincipalAssignmentNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDatabasePrincipalAssignmentNameAvailability.md
ms.openlocfilehash: 6a151119552ab4b0e42d247641248dd110af4994
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929024"
---
# <span data-ttu-id="b8391-101">Test-AzKustoDatabasePrincipalAssignmentNameAvailability</span><span class="sxs-lookup"><span data-stu-id="b8391-101">Test-AzKustoDatabasePrincipalAssignmentNameAvailability</span></span>

## <span data-ttu-id="b8391-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8391-102">SYNOPSIS</span></span>
<span data-ttu-id="b8391-103">Überprüft, ob die Datenbankprinzipalzuordnung gültig und noch nicht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b8391-103">Checks that the database principal assignment is valid and is not already in use.</span></span>

## <span data-ttu-id="b8391-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b8391-104">SYNTAX</span></span>

### <span data-ttu-id="b8391-105">CheckExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="b8391-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoDatabasePrincipalAssignmentNameAvailability -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -Name <String> -Type <Type> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b8391-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="b8391-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoDatabasePrincipalAssignmentNameAvailability -InputObject <IKustoIdentity> -Name <String>
 -Type <Type> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b8391-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b8391-107">DESCRIPTION</span></span>
<span data-ttu-id="b8391-108">Überprüft, ob die Datenbankprinzipalzuordnung gültig und noch nicht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b8391-108">Checks that the database principal assignment is valid and is not already in use.</span></span>

## <span data-ttu-id="b8391-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b8391-109">EXAMPLES</span></span>

### <span data-ttu-id="b8391-110">Beispiel 1: Überprüfen der Verfügbarkeit eines Datenbankprinzipalnamens, der verwendet wird</span><span class="sxs-lookup"><span data-stu-id="b8391-110">Example 1: Check the availability of a database principalassignment name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -Name "myprincipal" -Type "Microsoft.Kusto/Clusters/Database/principalAssignments" 

Message                                                                                                                                   Name            NameAvailable Reason
-------                                                                                                                                    ----            ------------- ------
Database principal assignment myprincipal already exists in database mykustodatabase. Please select a different principal assignment name. myprincipal   False
```

<span data-ttu-id="b8391-111">Der obige Befehl gibt zurück, ob ein PrincipalAssignment namens "myprincipal" in der Datenbank "mykustodatabase" aus dem Cluster "testnewkustocluster" vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="b8391-111">The above command returns whether or not a PrincipalAssignment named "myprincipal" exists in the database "mykustodatabase" from cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="b8391-112">Beispiel 2: Überprüfen der Verfügbarkeit eines Datenbankprinzipalnamens, der nicht verwendet wird</span><span class="sxs-lookup"><span data-stu-id="b8391-112">Example 2: Check the availability of a database principalassignment name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -Name "newprincipal" -Type "Microsoft.Kusto/Clusters/Database/principalAssignments"

Message Name                  NameAvailable Reason
------- ----                  ------------- ------
        availablekustocluster True
```

<span data-ttu-id="b8391-113">Der obige Befehl gibt zurück, ob ein PrincipalAssignment namens "myprincipal" in der Datenbank "mykustodatabase" aus dem Cluster "testnewkustocluster" vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="b8391-113">The above command returns whether or not a PrincipalAssignment named "myprincipal" exists in the database "mykustodatabase" from cluster "testnewkustocluster" .</span></span>

## <span data-ttu-id="b8391-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b8391-114">PARAMETERS</span></span>

### <span data-ttu-id="b8391-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="b8391-115">-ClusterName</span></span>
<span data-ttu-id="b8391-116">Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="b8391-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="b8391-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b8391-117">-DatabaseName</span></span>
<span data-ttu-id="b8391-118">Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="b8391-118">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="b8391-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8391-119">-DefaultProfile</span></span>
<span data-ttu-id="b8391-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b8391-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8391-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b8391-121">-InputObject</span></span>
<span data-ttu-id="b8391-122">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="b8391-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b8391-123">-Name</span><span class="sxs-lookup"><span data-stu-id="b8391-123">-Name</span></span>
<span data-ttu-id="b8391-124">Ressourcenname der Hauptzuordnung.</span><span class="sxs-lookup"><span data-stu-id="b8391-124">Principal Assignment resource name.</span></span>

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

### <span data-ttu-id="b8391-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8391-125">-ResourceGroupName</span></span>
<span data-ttu-id="b8391-126">Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="b8391-126">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="b8391-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b8391-127">-SubscriptionId</span></span>
<span data-ttu-id="b8391-128">Ruft Abonnementanmeldeinformationen ab, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="b8391-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b8391-129">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="b8391-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b8391-130">-Type</span><span class="sxs-lookup"><span data-stu-id="b8391-130">-Type</span></span>
<span data-ttu-id="b8391-131">Der Ressourcentyp Microsoft.Kusto/Clusters/Databases/principalAssignments.</span><span class="sxs-lookup"><span data-stu-id="b8391-131">The type of resource, Microsoft.Kusto/Clusters/Databases/principalAssignments.</span></span>

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

### <span data-ttu-id="b8391-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b8391-132">-Confirm</span></span>
<span data-ttu-id="b8391-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b8391-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8391-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8391-134">-WhatIf</span></span>
<span data-ttu-id="b8391-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b8391-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8391-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b8391-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8391-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8391-137">CommonParameters</span></span>
<span data-ttu-id="b8391-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8391-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8391-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b8391-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8391-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b8391-140">INPUTS</span></span>

### <span data-ttu-id="b8391-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="b8391-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="b8391-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b8391-142">OUTPUTS</span></span>

### <span data-ttu-id="b8391-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="b8391-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span></span>

## <span data-ttu-id="b8391-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b8391-144">NOTES</span></span>

<span data-ttu-id="b8391-145">ALIASE</span><span class="sxs-lookup"><span data-stu-id="b8391-145">ALIASES</span></span>

<span data-ttu-id="b8391-146">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="b8391-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b8391-147">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="b8391-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b8391-148">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b8391-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b8391-149">INPUTOBJECT <IKustoIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="b8391-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b8391-150">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="b8391-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="b8391-151">`[ClusterName <String>]`: Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="b8391-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="b8391-152">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="b8391-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="b8391-153">`[DatabaseName <String>]`: Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="b8391-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="b8391-154">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="b8391-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b8391-155">`[Location <String>]`: Azure-Standort.</span><span class="sxs-lookup"><span data-stu-id="b8391-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="b8391-156">`[PrincipalAssignmentName <String>]`: Der Name der Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="b8391-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="b8391-157">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="b8391-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="b8391-158">`[SubscriptionId <String>]`: Ruft Abonnementanmeldeinformationen ab, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="b8391-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="b8391-159">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="b8391-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="b8391-160">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b8391-160">RELATED LINKS</span></span>

