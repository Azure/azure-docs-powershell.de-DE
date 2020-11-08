---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustodatabasenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDatabaseNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDatabaseNameAvailability.md
ms.openlocfilehash: ab15d7a9da10e7e7a024d3af332f449cd011a290
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177928"
---
# <span data-ttu-id="782b0-101">Test-AzKustoDatabaseNameAvailability</span><span class="sxs-lookup"><span data-stu-id="782b0-101">Test-AzKustoDatabaseNameAvailability</span></span>

## <span data-ttu-id="782b0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="782b0-102">SYNOPSIS</span></span>
<span data-ttu-id="782b0-103">Überprüft, ob der Datenbankname gültig ist und nicht bereits verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="782b0-103">Checks that the database name is valid and is not already in use.</span></span>

## <span data-ttu-id="782b0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="782b0-104">SYNTAX</span></span>

### <span data-ttu-id="782b0-105">CheckExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="782b0-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoDatabaseNameAvailability -ClusterName <String> -ResourceGroupName <String> -Name <String>
 -Type <Type> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="782b0-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="782b0-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoDatabaseNameAvailability -InputObject <IKustoIdentity> -Name <String> -Type <Type>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="782b0-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="782b0-107">DESCRIPTION</span></span>
<span data-ttu-id="782b0-108">Überprüft, ob der Datenbankname gültig ist und nicht bereits verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="782b0-108">Checks that the database name is valid and is not already in use.</span></span>

## <span data-ttu-id="782b0-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="782b0-109">EXAMPLES</span></span>

### <span data-ttu-id="782b0-110">Beispiel 1: Überprüfen der Verfügbarkeit eines Kusto-Datenbanknamens, der verwendet wird</span><span class="sxs-lookup"><span data-stu-id="782b0-110">Example 1: Check the availability of a Kusto database name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoDatabaseNameAvailability -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase -Type Microsoft.Kusto/Clusters/Databases

Message                                                                                                          Name            NameAvailable Reason
-------                                                                                                          ----            ------------- ------
Database mykustodatabase already exists in cluster testnewkustocluster. Please select a different database name. mykustodatabase False
```

<span data-ttu-id="782b0-111">Der obige Befehl gibt zurück, ob im Cluster "testnewkustocluster" eine Kusto-Datenbank mit dem Namen "mykustodatabase" vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="782b0-111">The above command returns whether or not a Kusto database named "mykustodatabase" exists in the "testnewkustocluster" cluster.</span></span>

### <span data-ttu-id="782b0-112">Beispiel 2: Überprüfen der Verfügbarkeit eines nicht verwendeten Kusto-Datenbanknamens</span><span class="sxs-lookup"><span data-stu-id="782b0-112">Example 2: Check the availability of a Kusto database name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoDatabaseNameAvailability -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase2 -Type Microsoft.Kusto/Clusters/Databases

Message Name             NameAvailable Reason
------- ----             ------------- ------
        mykustodatabase2 True
```

<span data-ttu-id="782b0-113">Der obige Befehl gibt zurück, ob im Cluster "testnewkustocluster" eine Kusto-Datenbank mit dem Namen "mykustodatabase2" vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="782b0-113">The above command returns whether or not a Kusto database named "mykustodatabase2" exists in the "testnewkustocluster" cluster.</span></span>

## <span data-ttu-id="782b0-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="782b0-114">PARAMETERS</span></span>

### <span data-ttu-id="782b0-115">-Clustername</span><span class="sxs-lookup"><span data-stu-id="782b0-115">-ClusterName</span></span>
<span data-ttu-id="782b0-116">Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="782b0-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="782b0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="782b0-117">-DefaultProfile</span></span>
<span data-ttu-id="782b0-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="782b0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="782b0-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="782b0-119">-InputObject</span></span>
<span data-ttu-id="782b0-120">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="782b0-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="782b0-121">-Name</span><span class="sxs-lookup"><span data-stu-id="782b0-121">-Name</span></span>
<span data-ttu-id="782b0-122">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="782b0-122">Resource name.</span></span>

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

### <span data-ttu-id="782b0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="782b0-123">-ResourceGroupName</span></span>
<span data-ttu-id="782b0-124">Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="782b0-124">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="782b0-125">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="782b0-125">-SubscriptionId</span></span>
<span data-ttu-id="782b0-126">Ruft Abonnement Anmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="782b0-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="782b0-127">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="782b0-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="782b0-128">-Typ</span><span class="sxs-lookup"><span data-stu-id="782b0-128">-Type</span></span>
<span data-ttu-id="782b0-129">Der Typ der Ressource, beispielsweise Microsoft. Kusto/-Cluster/-Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="782b0-129">The type of resource, for instance Microsoft.Kusto/Clusters/databases.</span></span>

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

### <span data-ttu-id="782b0-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="782b0-130">-Confirm</span></span>
<span data-ttu-id="782b0-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="782b0-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="782b0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="782b0-132">-WhatIf</span></span>
<span data-ttu-id="782b0-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="782b0-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="782b0-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="782b0-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="782b0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="782b0-135">CommonParameters</span></span>
<span data-ttu-id="782b0-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="782b0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="782b0-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="782b0-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="782b0-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="782b0-138">INPUTS</span></span>

### <span data-ttu-id="782b0-139">Microsoft. Azure. PowerShell. Cmdlets. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="782b0-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="782b0-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="782b0-140">OUTPUTS</span></span>

### <span data-ttu-id="782b0-141">Microsoft. Azure. PowerShell. Cmdlets. Kusto. Models. Api20200614. ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="782b0-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICheckNameResult</span></span>

## <span data-ttu-id="782b0-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="782b0-142">NOTES</span></span>

<span data-ttu-id="782b0-143">Aliase</span><span class="sxs-lookup"><span data-stu-id="782b0-143">ALIASES</span></span>

<span data-ttu-id="782b0-144">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="782b0-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="782b0-145">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="782b0-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="782b0-146">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="782b0-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="782b0-147">Inputobject <IKustoIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="782b0-147">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="782b0-148">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="782b0-148">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="782b0-149">`[ClusterName <String>]`: Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="782b0-149">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="782b0-150">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="782b0-150">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="782b0-151">`[DatabaseName <String>]`: Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="782b0-151">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="782b0-152">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="782b0-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="782b0-153">`[Location <String>]`: Azure-Position.</span><span class="sxs-lookup"><span data-stu-id="782b0-153">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="782b0-154">`[PrincipalAssignmentName <String>]`: Der Name des Kusto-principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="782b0-154">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="782b0-155">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="782b0-155">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="782b0-156">`[SubscriptionId <String>]`: Ruft Abonnement Anmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="782b0-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="782b0-157">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="782b0-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="782b0-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="782b0-158">RELATED LINKS</span></span>

