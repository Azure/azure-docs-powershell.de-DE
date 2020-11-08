---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustodatabaseprincipalassignmentnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDatabasePrincipalAssignmentNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDatabasePrincipalAssignmentNameAvailability.md
ms.openlocfilehash: f61bbfc57017f16f9fee0c05f57aa51bd21d364d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166389"
---
# <span data-ttu-id="2f4ae-101">Test-AzKustoDatabasePrincipalAssignmentNameAvailability</span><span class="sxs-lookup"><span data-stu-id="2f4ae-101">Test-AzKustoDatabasePrincipalAssignmentNameAvailability</span></span>

## <span data-ttu-id="2f4ae-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2f4ae-102">SYNOPSIS</span></span>
<span data-ttu-id="2f4ae-103">Überprüft, ob die Datenbankprinzipal Zuordnung gültig ist und nicht bereits verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2f4ae-103">Checks that the database principal assignment is valid and is not already in use.</span></span>

## <span data-ttu-id="2f4ae-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f4ae-104">SYNTAX</span></span>

### <span data-ttu-id="2f4ae-105">CheckExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="2f4ae-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoDatabasePrincipalAssignmentNameAvailability -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -Name <String> -Type <Type> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2f4ae-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="2f4ae-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoDatabasePrincipalAssignmentNameAvailability -InputObject <IKustoIdentity> -Name <String>
 -Type <Type> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2f4ae-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2f4ae-107">DESCRIPTION</span></span>
<span data-ttu-id="2f4ae-108">Überprüft, ob die Datenbankprinzipal Zuordnung gültig ist und nicht bereits verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2f4ae-108">Checks that the database principal assignment is valid and is not already in use.</span></span>

## <span data-ttu-id="2f4ae-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2f4ae-109">EXAMPLES</span></span>

### <span data-ttu-id="2f4ae-110">Beispiel 1: Überprüfen der Verfügbarkeit eines in Verwendung begriffenen Datenbank-principalassignment</span><span class="sxs-lookup"><span data-stu-id="2f4ae-110">Example 1: Check the availability of a database principalassignment name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -Name "myprincipal" -Type "Microsoft.Kusto/Clusters/Database/principalAssignments" 

Message                                                                                                                                   Name            NameAvailable Reason
-------                                                                                                                                    ----            ------------- ------
Database principal assignment myprincipal already exists in database mykustodatabase. Please select a different principal assignment name. myprincipal   False
```

<span data-ttu-id="2f4ae-111">Der obige Befehl gibt zurück, ob ein PrincipalAssignment mit dem Namen "MyPrincipal" in der Datenbank "mykustodatabase" aus dem Cluster "testnewkustocluster" vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="2f4ae-111">The above command returns whether or not a PrincipalAssignment named "myprincipal" exists in the database "mykustodatabase" from cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="2f4ae-112">Beispiel 2: Überprüfen der Verfügbarkeit eines Datenbank-principalassignment-namens, der nicht verwendet wird</span><span class="sxs-lookup"><span data-stu-id="2f4ae-112">Example 2: Check the availability of a database principalassignment name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -Name "newprincipal" -Type "Microsoft.Kusto/Clusters/Database/principalAssignments"

Message Name                  NameAvailable Reason
------- ----                  ------------- ------
        availablekustocluster True
```

<span data-ttu-id="2f4ae-113">Der obige Befehl gibt zurück, ob ein PrincipalAssignment mit dem Namen "MyPrincipal" in der Datenbank "mykustodatabase" aus dem Cluster "testnewkustocluster" vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="2f4ae-113">The above command returns whether or not a PrincipalAssignment named "myprincipal" exists in the database "mykustodatabase" from cluster "testnewkustocluster" .</span></span>

## <span data-ttu-id="2f4ae-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="2f4ae-114">PARAMETERS</span></span>

### <span data-ttu-id="2f4ae-115">-Clustername</span><span class="sxs-lookup"><span data-stu-id="2f4ae-115">-ClusterName</span></span>
<span data-ttu-id="2f4ae-116">Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="2f4ae-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="2f4ae-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2f4ae-117">-DatabaseName</span></span>
<span data-ttu-id="2f4ae-118">Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="2f4ae-118">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="2f4ae-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f4ae-119">-DefaultProfile</span></span>
<span data-ttu-id="2f4ae-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2f4ae-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f4ae-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2f4ae-121">-InputObject</span></span>
<span data-ttu-id="2f4ae-122">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="2f4ae-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2f4ae-123">-Name</span><span class="sxs-lookup"><span data-stu-id="2f4ae-123">-Name</span></span>
<span data-ttu-id="2f4ae-124">Ressourcenname der Prinzipal Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="2f4ae-124">Principal Assignment resource name.</span></span>

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

### <span data-ttu-id="2f4ae-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f4ae-125">-ResourceGroupName</span></span>
<span data-ttu-id="2f4ae-126">Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="2f4ae-126">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="2f4ae-127">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="2f4ae-127">-SubscriptionId</span></span>
<span data-ttu-id="2f4ae-128">Ruft Abonnement Anmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="2f4ae-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="2f4ae-129">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="2f4ae-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="2f4ae-130">-Typ</span><span class="sxs-lookup"><span data-stu-id="2f4ae-130">-Type</span></span>
<span data-ttu-id="2f4ae-131">Der Typ der Ressource, Microsoft. Kusto/Clusters/Databases/principalAssignments.</span><span class="sxs-lookup"><span data-stu-id="2f4ae-131">The type of resource, Microsoft.Kusto/Clusters/Databases/principalAssignments.</span></span>

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

### <span data-ttu-id="2f4ae-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2f4ae-132">-Confirm</span></span>
<span data-ttu-id="2f4ae-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2f4ae-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f4ae-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f4ae-134">-WhatIf</span></span>
<span data-ttu-id="2f4ae-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2f4ae-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f4ae-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2f4ae-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f4ae-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f4ae-137">CommonParameters</span></span>
<span data-ttu-id="2f4ae-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f4ae-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f4ae-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2f4ae-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f4ae-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2f4ae-140">INPUTS</span></span>

### <span data-ttu-id="2f4ae-141">Microsoft. Azure. PowerShell. Cmdlets. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="2f4ae-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="2f4ae-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2f4ae-142">OUTPUTS</span></span>

### <span data-ttu-id="2f4ae-143">Microsoft. Azure. PowerShell. Cmdlets. Kusto. Models. Api20200614. ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="2f4ae-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICheckNameResult</span></span>

## <span data-ttu-id="2f4ae-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="2f4ae-144">NOTES</span></span>

<span data-ttu-id="2f4ae-145">Aliase</span><span class="sxs-lookup"><span data-stu-id="2f4ae-145">ALIASES</span></span>

<span data-ttu-id="2f4ae-146">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2f4ae-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2f4ae-147">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2f4ae-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2f4ae-148">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="2f4ae-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2f4ae-149">Inputobject <IKustoIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="2f4ae-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2f4ae-150">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="2f4ae-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="2f4ae-151">`[ClusterName <String>]`: Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="2f4ae-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="2f4ae-152">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="2f4ae-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="2f4ae-153">`[DatabaseName <String>]`: Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="2f4ae-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="2f4ae-154">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="2f4ae-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2f4ae-155">`[Location <String>]`: Azure-Position.</span><span class="sxs-lookup"><span data-stu-id="2f4ae-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="2f4ae-156">`[PrincipalAssignmentName <String>]`: Der Name des Kusto-principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="2f4ae-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="2f4ae-157">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="2f4ae-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="2f4ae-158">`[SubscriptionId <String>]`: Ruft Abonnement Anmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="2f4ae-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="2f4ae-159">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="2f4ae-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="2f4ae-160">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2f4ae-160">RELATED LINKS</span></span>

