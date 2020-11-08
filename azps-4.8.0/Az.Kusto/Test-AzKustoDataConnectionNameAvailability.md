---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustodataconnectionnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDataConnectionNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDataConnectionNameAvailability.md
ms.openlocfilehash: 556e0a7662a91c5c82bab7727bf676adf88d45d6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166555"
---
# <span data-ttu-id="7666e-101">Test-AzKustoDataConnectionNameAvailability</span><span class="sxs-lookup"><span data-stu-id="7666e-101">Test-AzKustoDataConnectionNameAvailability</span></span>

## <span data-ttu-id="7666e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7666e-102">SYNOPSIS</span></span>
<span data-ttu-id="7666e-103">Überprüft, ob der datenverbindungsname gültig ist und nicht bereits verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7666e-103">Checks that the data connection name is valid and is not already in use.</span></span>

## <span data-ttu-id="7666e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7666e-104">SYNTAX</span></span>

### <span data-ttu-id="7666e-105">CheckExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="7666e-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoDataConnectionNameAvailability -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -Name <String> -Type <Type> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7666e-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="7666e-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoDataConnectionNameAvailability -InputObject <IKustoIdentity> -Name <String> -Type <Type>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7666e-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7666e-107">DESCRIPTION</span></span>
<span data-ttu-id="7666e-108">Überprüft, ob der datenverbindungsname gültig ist und nicht bereits verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7666e-108">Checks that the data connection name is valid and is not already in use.</span></span>

## <span data-ttu-id="7666e-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7666e-109">EXAMPLES</span></span>

### <span data-ttu-id="7666e-110">Beispiel 1: Überprüfen der Verfügbarkeit eines Daten Verbindungsnamens, der verwendet wird</span><span class="sxs-lookup"><span data-stu-id="7666e-110">Example 1: Check the availability of a Data Connection name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoDataConnectionNameAvailability -ClusterName testnewkustocluster -DatabaseName mykustodatabase -ResourceGroupName testrg -Name mykustodataconnection -Type Microsoft.Kusto/Clusters/Databases/dataConnections

Message                                                                                                                                                          Name                  NameAvailable Reason
-------                                                                                                                                                          ----                  ------------- ------
Data Connection mykustodataconnection already exists in database mykustodatabase in cluster testnewkustocluster. Please select a different data connection name. mykustodataconnection False         AlreadyExists
```

<span data-ttu-id="7666e-111">Der obige Befehl gibt zurück, ob eine Datenverbindung mit dem Namen "mykustodataconnection" in der Datenbank "mykustodatabase" vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="7666e-111">The above command returns whether or not a Data Connection named "mykustodataconnection" exists in the "mykustodatabase" database.</span></span>

### <span data-ttu-id="7666e-112">Beispiel 2: Überprüfen der Verfügbarkeit eines Daten Verbindungsnamens, der nicht verwendet wird</span><span class="sxs-lookup"><span data-stu-id="7666e-112">Example 2: Check the availability of a Data Connection name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoDataConnectionNameAvailability -ClusterName testnewkustocluster -DatabaseName mykustodatabase -ResourceGroupName testrg -Name mydataconnection -Type Microsoft.Kusto/Clusters/Databases/dataConnections

Message Name             NameAvailable Reason
------- ----             ------------- ------
        mydataconnection True
```

<span data-ttu-id="7666e-113">Der obige Befehl gibt zurück, ob eine Datenverbindung mit dem Namen "mydataconnection" in der Datenbank "mykustodatabase" vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="7666e-113">The above command returns whether or not a Data Connection named "mydataconnection" exists in the "mykustodatabase" database.</span></span>

## <span data-ttu-id="7666e-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="7666e-114">PARAMETERS</span></span>

### <span data-ttu-id="7666e-115">-Clustername</span><span class="sxs-lookup"><span data-stu-id="7666e-115">-ClusterName</span></span>
<span data-ttu-id="7666e-116">Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="7666e-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="7666e-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7666e-117">-DatabaseName</span></span>
<span data-ttu-id="7666e-118">Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="7666e-118">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="7666e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7666e-119">-DefaultProfile</span></span>
<span data-ttu-id="7666e-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7666e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7666e-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7666e-121">-InputObject</span></span>
<span data-ttu-id="7666e-122">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="7666e-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7666e-123">-Name</span><span class="sxs-lookup"><span data-stu-id="7666e-123">-Name</span></span>
<span data-ttu-id="7666e-124">Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="7666e-124">Data Connection name.</span></span>

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

### <span data-ttu-id="7666e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7666e-125">-ResourceGroupName</span></span>
<span data-ttu-id="7666e-126">Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="7666e-126">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="7666e-127">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="7666e-127">-SubscriptionId</span></span>
<span data-ttu-id="7666e-128">Ruft Abonnement Anmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="7666e-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="7666e-129">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="7666e-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="7666e-130">-Typ</span><span class="sxs-lookup"><span data-stu-id="7666e-130">-Type</span></span>
<span data-ttu-id="7666e-131">Der Typ der Ressource, Microsoft. Kusto/Cluster/Datenbanken/Datenverbindungen.</span><span class="sxs-lookup"><span data-stu-id="7666e-131">The type of resource, Microsoft.Kusto/Clusters/Databases/dataConnections.</span></span>

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

### <span data-ttu-id="7666e-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7666e-132">-Confirm</span></span>
<span data-ttu-id="7666e-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7666e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7666e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7666e-134">-WhatIf</span></span>
<span data-ttu-id="7666e-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7666e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7666e-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7666e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7666e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7666e-137">CommonParameters</span></span>
<span data-ttu-id="7666e-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7666e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7666e-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7666e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7666e-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7666e-140">INPUTS</span></span>

### <span data-ttu-id="7666e-141">Microsoft. Azure. PowerShell. Cmdlets. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="7666e-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="7666e-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7666e-142">OUTPUTS</span></span>

### <span data-ttu-id="7666e-143">Microsoft. Azure. PowerShell. Cmdlets. Kusto. Models. Api20200614. ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="7666e-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICheckNameResult</span></span>

## <span data-ttu-id="7666e-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="7666e-144">NOTES</span></span>

<span data-ttu-id="7666e-145">Aliase</span><span class="sxs-lookup"><span data-stu-id="7666e-145">ALIASES</span></span>

<span data-ttu-id="7666e-146">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7666e-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7666e-147">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7666e-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7666e-148">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="7666e-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7666e-149">Inputobject <IKustoIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="7666e-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7666e-150">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="7666e-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="7666e-151">`[ClusterName <String>]`: Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="7666e-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="7666e-152">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="7666e-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="7666e-153">`[DatabaseName <String>]`: Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="7666e-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="7666e-154">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="7666e-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7666e-155">`[Location <String>]`: Azure-Position.</span><span class="sxs-lookup"><span data-stu-id="7666e-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="7666e-156">`[PrincipalAssignmentName <String>]`: Der Name des Kusto-principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="7666e-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="7666e-157">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="7666e-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="7666e-158">`[SubscriptionId <String>]`: Ruft Abonnement Anmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="7666e-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="7666e-159">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="7666e-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="7666e-160">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7666e-160">RELATED LINKS</span></span>

