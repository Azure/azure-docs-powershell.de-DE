---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabase.md
ms.openlocfilehash: cfb5eb3c65434f0f62af03bcca57174010041e58
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470471"
---
# <span data-ttu-id="f1e1f-101">Remove-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="f1e1f-101">Remove-AzKustoDatabase</span></span>

## <span data-ttu-id="f1e1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1e1f-102">SYNOPSIS</span></span>
<span data-ttu-id="f1e1f-103">Löscht die Datenbank mit dem angegebenen Namen.</span><span class="sxs-lookup"><span data-stu-id="f1e1f-103">Deletes the database with the given name.</span></span>

## <span data-ttu-id="f1e1f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f1e1f-104">SYNTAX</span></span>

### <span data-ttu-id="f1e1f-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="f1e1f-105">Delete (Default)</span></span>
```
Remove-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="f1e1f-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f1e1f-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoDatabase -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f1e1f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f1e1f-107">DESCRIPTION</span></span>
<span data-ttu-id="f1e1f-108">Löscht die Datenbank mit dem angegebenen Namen.</span><span class="sxs-lookup"><span data-stu-id="f1e1f-108">Deletes the database with the given name.</span></span>

## <span data-ttu-id="f1e1f-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f1e1f-109">EXAMPLES</span></span>

### <span data-ttu-id="f1e1f-110">Beispiel 1: Löschen einer vorhandenen Datenbank in Kusto nach Name</span><span class="sxs-lookup"><span data-stu-id="f1e1f-110">Example 1: Delete an existing Kusto database by name</span></span>
```powershell
PS C:\> Remove-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase
```

<span data-ttu-id="f1e1f-111">Mit dem oben angegebenen Befehl wird die Datenbank "Kusto" mit dem Namen "mykustodatabase" im Cluster "testnewkustocluster" gelöscht, der in der Ressourcengruppe "testrg" gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="f1e1f-111">The above command deletes the Kusto database named "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="f1e1f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f1e1f-112">PARAMETERS</span></span>

### <span data-ttu-id="f1e1f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f1e1f-113">-AsJob</span></span>
<span data-ttu-id="f1e1f-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="f1e1f-114">Run the command as a job</span></span>

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

### <span data-ttu-id="f1e1f-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="f1e1f-115">-ClusterName</span></span>
<span data-ttu-id="f1e1f-116">Der Name des Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="f1e1f-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="f1e1f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1e1f-117">-DefaultProfile</span></span>
<span data-ttu-id="f1e1f-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f1e1f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1e1f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f1e1f-119">-InputObject</span></span>
<span data-ttu-id="f1e1f-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="f1e1f-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f1e1f-121">-Name</span><span class="sxs-lookup"><span data-stu-id="f1e1f-121">-Name</span></span>
<span data-ttu-id="f1e1f-122">Der Name der Datenbank im Cluster "Kusto".</span><span class="sxs-lookup"><span data-stu-id="f1e1f-122">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1e1f-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f1e1f-123">-NoWait</span></span>
<span data-ttu-id="f1e1f-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="f1e1f-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f1e1f-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f1e1f-125">-PassThru</span></span>
<span data-ttu-id="f1e1f-126">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="f1e1f-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f1e1f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1e1f-127">-ResourceGroupName</span></span>
<span data-ttu-id="f1e1f-128">Der Name der Ressourcengruppe, die den Cluster "Kusto" enthält.</span><span class="sxs-lookup"><span data-stu-id="f1e1f-128">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="f1e1f-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f1e1f-129">-SubscriptionId</span></span>
<span data-ttu-id="f1e1f-130">Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="f1e1f-130">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f1e1f-131">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="f1e1f-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f1e1f-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f1e1f-132">-Confirm</span></span>
<span data-ttu-id="f1e1f-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f1e1f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1e1f-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f1e1f-134">-WhatIf</span></span>
<span data-ttu-id="f1e1f-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f1e1f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1e1f-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f1e1f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1e1f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1e1f-137">CommonParameters</span></span>
<span data-ttu-id="f1e1f-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1e1f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1e1f-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f1e1f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1e1f-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f1e1f-140">INPUTS</span></span>

### <span data-ttu-id="f1e1f-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="f1e1f-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="f1e1f-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f1e1f-142">OUTPUTS</span></span>

### <span data-ttu-id="f1e1f-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f1e1f-143">System.Boolean</span></span>

## <span data-ttu-id="f1e1f-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f1e1f-144">NOTES</span></span>

<span data-ttu-id="f1e1f-145">ALIASE</span><span class="sxs-lookup"><span data-stu-id="f1e1f-145">ALIASES</span></span>

<span data-ttu-id="f1e1f-146">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="f1e1f-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f1e1f-147">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f1e1f-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f1e1f-148">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f1e1f-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f1e1f-149">INPUTOBJECT <IKustoIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="f1e1f-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f1e1f-150">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="f1e1f-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="f1e1f-151">`[ClusterName <String>]`: Der Name des Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="f1e1f-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="f1e1f-152">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="f1e1f-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="f1e1f-153">`[DatabaseName <String>]`: Der Name der Datenbank im Cluster "Kusto".</span><span class="sxs-lookup"><span data-stu-id="f1e1f-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="f1e1f-154">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="f1e1f-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f1e1f-155">`[Location <String>]`: Azure-Standort.</span><span class="sxs-lookup"><span data-stu-id="f1e1f-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="f1e1f-156">`[PrincipalAssignmentName <String>]`: Der Name der Kusto PrincipalAssignment.</span><span class="sxs-lookup"><span data-stu-id="f1e1f-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="f1e1f-157">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Cluster "Kusto" enthält.</span><span class="sxs-lookup"><span data-stu-id="f1e1f-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="f1e1f-158">`[SubscriptionId <String>]`: Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="f1e1f-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f1e1f-159">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="f1e1f-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="f1e1f-160">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f1e1f-160">RELATED LINKS</span></span>

