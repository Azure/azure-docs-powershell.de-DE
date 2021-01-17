---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDataConnection.md
ms.openlocfilehash: c04cbc2a92e6fa80c718cb32d95cc4059e4e3a6d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369367"
---
# <span data-ttu-id="72641-101">Remove-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="72641-101">Remove-AzKustoDataConnection</span></span>

## <span data-ttu-id="72641-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72641-102">SYNOPSIS</span></span>
<span data-ttu-id="72641-103">Löscht die Datenverbindung mit dem angegebenen Namen.</span><span class="sxs-lookup"><span data-stu-id="72641-103">Deletes the data connection with the given name.</span></span>

## <span data-ttu-id="72641-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="72641-104">SYNTAX</span></span>

### <span data-ttu-id="72641-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="72641-105">Delete (Default)</span></span>
```
Remove-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="72641-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="72641-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoDataConnection -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="72641-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="72641-107">DESCRIPTION</span></span>
<span data-ttu-id="72641-108">Löscht die Datenverbindung mit dem angegebenen Namen.</span><span class="sxs-lookup"><span data-stu-id="72641-108">Deletes the data connection with the given name.</span></span>

## <span data-ttu-id="72641-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="72641-109">EXAMPLES</span></span>

### <span data-ttu-id="72641-110">Beispiel 1: Löschen einer vorhandenen Datenverbindung nach Name</span><span class="sxs-lookup"><span data-stu-id="72641-110">Example 1: Delete an existing data connection by name</span></span>
```powershell
PS C:\> Remove-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "mykustodataconnection"
```

<span data-ttu-id="72641-111">Der obige Befehl löscht die Datenverbindung mit dem Namen "mykustodataconnection" in der Datenbank "mykustodatabase" des vorhandenen Cluster "testnewkustocluster", der in der Ressourcengruppe "testrg" gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="72641-111">The above command deletes the data connection named "mykustodataconnection" in database "mykustodatabase" of the existing cluster "testnewkustocluster" found in the resource group "testrg"</span></span>

## <span data-ttu-id="72641-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="72641-112">PARAMETERS</span></span>

### <span data-ttu-id="72641-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="72641-113">-AsJob</span></span>
<span data-ttu-id="72641-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="72641-114">Run the command as a job</span></span>

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

### <span data-ttu-id="72641-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="72641-115">-ClusterName</span></span>
<span data-ttu-id="72641-116">Der Name des Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="72641-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="72641-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="72641-117">-DatabaseName</span></span>
<span data-ttu-id="72641-118">Der Name der Datenbank im Cluster "Kusto".</span><span class="sxs-lookup"><span data-stu-id="72641-118">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="72641-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72641-119">-DefaultProfile</span></span>
<span data-ttu-id="72641-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="72641-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72641-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="72641-121">-InputObject</span></span>
<span data-ttu-id="72641-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="72641-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="72641-123">-Name</span><span class="sxs-lookup"><span data-stu-id="72641-123">-Name</span></span>
<span data-ttu-id="72641-124">Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="72641-124">The name of the data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DataConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72641-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="72641-125">-NoWait</span></span>
<span data-ttu-id="72641-126">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="72641-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="72641-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="72641-127">-PassThru</span></span>
<span data-ttu-id="72641-128">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="72641-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="72641-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72641-129">-ResourceGroupName</span></span>
<span data-ttu-id="72641-130">Der Name der Ressourcengruppe, die den Cluster "Kusto" enthält.</span><span class="sxs-lookup"><span data-stu-id="72641-130">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="72641-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="72641-131">-SubscriptionId</span></span>
<span data-ttu-id="72641-132">Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="72641-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="72641-133">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="72641-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="72641-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="72641-134">-Confirm</span></span>
<span data-ttu-id="72641-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="72641-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72641-136">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="72641-136">-WhatIf</span></span>
<span data-ttu-id="72641-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="72641-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72641-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="72641-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72641-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72641-139">CommonParameters</span></span>
<span data-ttu-id="72641-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72641-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72641-141">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="72641-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72641-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="72641-142">INPUTS</span></span>

### <span data-ttu-id="72641-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="72641-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="72641-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="72641-144">OUTPUTS</span></span>

### <span data-ttu-id="72641-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="72641-145">System.Boolean</span></span>

## <span data-ttu-id="72641-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="72641-146">NOTES</span></span>

<span data-ttu-id="72641-147">ALIASE</span><span class="sxs-lookup"><span data-stu-id="72641-147">ALIASES</span></span>

<span data-ttu-id="72641-148">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="72641-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="72641-149">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="72641-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="72641-150">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="72641-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="72641-151">INPUTOBJECT <IKustoIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="72641-151">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="72641-152">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="72641-152">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="72641-153">`[ClusterName <String>]`: Der Name des Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="72641-153">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="72641-154">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="72641-154">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="72641-155">`[DatabaseName <String>]`: Der Name der Datenbank im Cluster "Kusto".</span><span class="sxs-lookup"><span data-stu-id="72641-155">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="72641-156">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="72641-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="72641-157">`[Location <String>]`: Azure-Standort.</span><span class="sxs-lookup"><span data-stu-id="72641-157">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="72641-158">`[PrincipalAssignmentName <String>]`: Der Name der Kusto PrincipalAssignment.</span><span class="sxs-lookup"><span data-stu-id="72641-158">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="72641-159">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Cluster "Kusto" enthält.</span><span class="sxs-lookup"><span data-stu-id="72641-159">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="72641-160">`[SubscriptionId <String>]`: Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="72641-160">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="72641-161">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="72641-161">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="72641-162">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="72641-162">RELATED LINKS</span></span>

