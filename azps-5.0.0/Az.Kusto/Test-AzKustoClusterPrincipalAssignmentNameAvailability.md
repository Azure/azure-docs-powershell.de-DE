---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustoclusterprincipalassignmentnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterPrincipalAssignmentNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterPrincipalAssignmentNameAvailability.md
ms.openlocfilehash: cb4f375632626ee3c3428e6a990a228dacecd288
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180384"
---
# <span data-ttu-id="f8a35-101">Test-AzKustoClusterPrincipalAssignmentNameAvailability</span><span class="sxs-lookup"><span data-stu-id="f8a35-101">Test-AzKustoClusterPrincipalAssignmentNameAvailability</span></span>

## <span data-ttu-id="f8a35-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f8a35-102">SYNOPSIS</span></span>
<span data-ttu-id="f8a35-103">Überprüft, ob der Prinzipal Zuordnungsname gültig ist und nicht bereits verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f8a35-103">Checks that the principal assignment name is valid and is not already in use.</span></span>

## <span data-ttu-id="f8a35-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f8a35-104">SYNTAX</span></span>

### <span data-ttu-id="f8a35-105">CheckExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="f8a35-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoClusterPrincipalAssignmentNameAvailability -ClusterName <String> -ResourceGroupName <String>
 -Name <String> -Type <Type> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="f8a35-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="f8a35-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoClusterPrincipalAssignmentNameAvailability -InputObject <IKustoIdentity> -Name <String>
 -Type <Type> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f8a35-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f8a35-107">DESCRIPTION</span></span>
<span data-ttu-id="f8a35-108">Überprüft, ob der Prinzipal Zuordnungsname gültig ist und nicht bereits verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f8a35-108">Checks that the principal assignment name is valid and is not already in use.</span></span>

## <span data-ttu-id="f8a35-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f8a35-109">EXAMPLES</span></span>

### <span data-ttu-id="f8a35-110">Beispiel 1: Überprüfen der Verfügbarkeit eines Cluster-principalassignment-namens, der verwendet wird</span><span class="sxs-lookup"><span data-stu-id="f8a35-110">Example 1: Check the availability of a cluster principalassignment name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -Name "myprincipal" -Type "Microsoft.Kusto/clusters/principalAssignments" 

Message                                                                                                        Name            NameAvailable Reason
-------                                                                                                        ----            ------------- ------
PrincipalAssignment myprincipal already exists in cluster testnewkustocluster. Please select a different name. myprincipal   False
```

<span data-ttu-id="f8a35-111">Der obige Befehl gibt zurück, ob im Cluster "testnewkustocluster" ein PrincipalAssignment mit dem Namen "MyPrincipal" vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="f8a35-111">The above command returns whether or not a PrincipalAssignment named "myprincipal" exists in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="f8a35-112">Beispiel 2: Überprüfen der Verfügbarkeit eines Cluster-principalassignment-namens, der nicht verwendet wird</span><span class="sxs-lookup"><span data-stu-id="f8a35-112">Example 2: Check the availability of a cluster principalassignment name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -Name "newprincipal" -Type "Microsoft.Kusto/clusters/principalAssignments"

Message Name                  NameAvailable Reason
------- ----                  ------------- ------
        availablekustocluster True
```

<span data-ttu-id="f8a35-113">Der obige Befehl gibt zurück, ob ein PrincipalAssignment mit dem Namen "neuer Principal" im Cluster "testnewkustocluster" vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="f8a35-113">The above command returns whether or not a PrincipalAssignment named "newprincipal" exists in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="f8a35-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="f8a35-114">PARAMETERS</span></span>

### <span data-ttu-id="f8a35-115">-Clustername</span><span class="sxs-lookup"><span data-stu-id="f8a35-115">-ClusterName</span></span>
<span data-ttu-id="f8a35-116">Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="f8a35-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="f8a35-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8a35-117">-DefaultProfile</span></span>
<span data-ttu-id="f8a35-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f8a35-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8a35-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f8a35-119">-InputObject</span></span>
<span data-ttu-id="f8a35-120">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="f8a35-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f8a35-121">-Name</span><span class="sxs-lookup"><span data-stu-id="f8a35-121">-Name</span></span>
<span data-ttu-id="f8a35-122">Ressourcenname der Prinzipal Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="f8a35-122">Principal Assignment resource name.</span></span>

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

### <span data-ttu-id="f8a35-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8a35-123">-ResourceGroupName</span></span>
<span data-ttu-id="f8a35-124">Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="f8a35-124">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="f8a35-125">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="f8a35-125">-SubscriptionId</span></span>
<span data-ttu-id="f8a35-126">Ruft Abonnement Anmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="f8a35-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f8a35-127">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="f8a35-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f8a35-128">-Typ</span><span class="sxs-lookup"><span data-stu-id="f8a35-128">-Type</span></span>
<span data-ttu-id="f8a35-129">Der Typ der Ressource, Microsoft. Kusto/Clusters/principalAssignments.</span><span class="sxs-lookup"><span data-stu-id="f8a35-129">The type of resource, Microsoft.Kusto/Clusters/principalAssignments.</span></span>

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

### <span data-ttu-id="f8a35-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f8a35-130">-Confirm</span></span>
<span data-ttu-id="f8a35-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f8a35-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8a35-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8a35-132">-WhatIf</span></span>
<span data-ttu-id="f8a35-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f8a35-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8a35-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f8a35-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8a35-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8a35-135">CommonParameters</span></span>
<span data-ttu-id="f8a35-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8a35-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8a35-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f8a35-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8a35-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f8a35-138">INPUTS</span></span>

### <span data-ttu-id="f8a35-139">Microsoft. Azure. PowerShell. Cmdlets. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="f8a35-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="f8a35-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f8a35-140">OUTPUTS</span></span>

### <span data-ttu-id="f8a35-141">Microsoft. Azure. PowerShell. Cmdlets. Kusto. Models. Api20200614. ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="f8a35-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICheckNameResult</span></span>

## <span data-ttu-id="f8a35-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="f8a35-142">NOTES</span></span>

<span data-ttu-id="f8a35-143">Aliase</span><span class="sxs-lookup"><span data-stu-id="f8a35-143">ALIASES</span></span>

<span data-ttu-id="f8a35-144">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f8a35-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f8a35-145">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f8a35-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f8a35-146">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="f8a35-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f8a35-147">Inputobject <IKustoIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="f8a35-147">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f8a35-148">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="f8a35-148">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="f8a35-149">`[ClusterName <String>]`: Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="f8a35-149">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="f8a35-150">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="f8a35-150">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="f8a35-151">`[DatabaseName <String>]`: Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="f8a35-151">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="f8a35-152">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="f8a35-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f8a35-153">`[Location <String>]`: Azure-Position.</span><span class="sxs-lookup"><span data-stu-id="f8a35-153">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="f8a35-154">`[PrincipalAssignmentName <String>]`: Der Name des Kusto-principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="f8a35-154">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="f8a35-155">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="f8a35-155">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="f8a35-156">`[SubscriptionId <String>]`: Ruft Abonnement Anmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="f8a35-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f8a35-157">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="f8a35-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="f8a35-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f8a35-158">RELATED LINKS</span></span>

