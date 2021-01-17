---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoCluster.md
ms.openlocfilehash: e9bdea3820b8b8121e0e250c99283c0ca656ca61
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470477"
---
# <span data-ttu-id="4e306-101">Remove-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="4e306-101">Remove-AzKustoCluster</span></span>

## <span data-ttu-id="4e306-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e306-102">SYNOPSIS</span></span>
<span data-ttu-id="4e306-103">Löscht einen Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="4e306-103">Deletes a Kusto cluster.</span></span>

## <span data-ttu-id="4e306-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4e306-104">SYNTAX</span></span>

### <span data-ttu-id="4e306-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="4e306-105">Delete (Default)</span></span>
```
Remove-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4e306-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4e306-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoCluster -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4e306-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4e306-107">DESCRIPTION</span></span>
<span data-ttu-id="4e306-108">Löscht einen Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="4e306-108">Deletes a Kusto cluster.</span></span>

## <span data-ttu-id="4e306-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4e306-109">EXAMPLES</span></span>

### <span data-ttu-id="4e306-110">Beispiel 1: Löschen eines vorhandenen Kusto-Clusters nach Name</span><span class="sxs-lookup"><span data-stu-id="4e306-110">Example 1: Delete an existing Kusto cluster by name</span></span>
```powershell
PS C:\> Remove-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster
```

<span data-ttu-id="4e306-111">Mit dem oben angegebenen Befehl wird der Cluster "Kusto" mit dem Namen "testnewkustocluster" in der Ressourcengruppe "testrg" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="4e306-111">The above command deletes the Kusto cluster named "testnewkustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="4e306-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4e306-112">PARAMETERS</span></span>

### <span data-ttu-id="4e306-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4e306-113">-AsJob</span></span>
<span data-ttu-id="4e306-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="4e306-114">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e306-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e306-115">-DefaultProfile</span></span>
<span data-ttu-id="4e306-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4e306-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e306-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4e306-117">-InputObject</span></span>
<span data-ttu-id="4e306-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="4e306-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e306-119">-Name</span><span class="sxs-lookup"><span data-stu-id="4e306-119">-Name</span></span>
<span data-ttu-id="4e306-120">Der Name des Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="4e306-120">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e306-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="4e306-121">-NoWait</span></span>
<span data-ttu-id="4e306-122">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="4e306-122">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e306-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4e306-123">-PassThru</span></span>
<span data-ttu-id="4e306-124">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="4e306-124">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e306-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e306-125">-ResourceGroupName</span></span>
<span data-ttu-id="4e306-126">Der Name der Ressourcengruppe, die den Cluster "Kusto" enthält.</span><span class="sxs-lookup"><span data-stu-id="4e306-126">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e306-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4e306-127">-SubscriptionId</span></span>
<span data-ttu-id="4e306-128">Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="4e306-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="4e306-129">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="4e306-129">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e306-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4e306-130">-Confirm</span></span>
<span data-ttu-id="4e306-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4e306-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e306-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4e306-132">-WhatIf</span></span>
<span data-ttu-id="4e306-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4e306-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e306-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4e306-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e306-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e306-135">CommonParameters</span></span>
<span data-ttu-id="4e306-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e306-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e306-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4e306-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e306-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4e306-138">INPUTS</span></span>

### <span data-ttu-id="4e306-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="4e306-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="4e306-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4e306-140">OUTPUTS</span></span>

### <span data-ttu-id="4e306-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4e306-141">System.Boolean</span></span>

## <span data-ttu-id="4e306-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4e306-142">NOTES</span></span>

<span data-ttu-id="4e306-143">ALIASE</span><span class="sxs-lookup"><span data-stu-id="4e306-143">ALIASES</span></span>

<span data-ttu-id="4e306-144">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="4e306-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4e306-145">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4e306-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4e306-146">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4e306-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4e306-147">INPUTOBJECT <IKustoIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="4e306-147">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4e306-148">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="4e306-148">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="4e306-149">`[ClusterName <String>]`: Der Name des Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="4e306-149">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="4e306-150">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="4e306-150">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="4e306-151">`[DatabaseName <String>]`: Der Name der Datenbank im Cluster "Kusto".</span><span class="sxs-lookup"><span data-stu-id="4e306-151">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="4e306-152">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="4e306-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4e306-153">`[Location <String>]`: Azure-Standort.</span><span class="sxs-lookup"><span data-stu-id="4e306-153">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="4e306-154">`[PrincipalAssignmentName <String>]`: Der Name der Kusto PrincipalAssignment.</span><span class="sxs-lookup"><span data-stu-id="4e306-154">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="4e306-155">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Cluster "Kusto" enthält.</span><span class="sxs-lookup"><span data-stu-id="4e306-155">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="4e306-156">`[SubscriptionId <String>]`: Ruft Abonnementanmeldeinformationen ab, mit denen Das Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="4e306-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="4e306-157">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="4e306-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="4e306-158">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4e306-158">RELATED LINKS</span></span>

