---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/remove-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDataConnection.md
ms.openlocfilehash: ac2eac129231f33a2f74732923652d3851debbd0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930032"
---
# <span data-ttu-id="87113-101">Remove-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="87113-101">Remove-AzKustoDataConnection</span></span>

## <span data-ttu-id="87113-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87113-102">SYNOPSIS</span></span>
<span data-ttu-id="87113-103">Löscht die Datenverbindung mit dem angegebenen Namen.</span><span class="sxs-lookup"><span data-stu-id="87113-103">Deletes the data connection with the given name.</span></span>

## <span data-ttu-id="87113-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="87113-104">SYNTAX</span></span>

### <span data-ttu-id="87113-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="87113-105">Delete (Default)</span></span>
```
Remove-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="87113-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="87113-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoDataConnection -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="87113-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="87113-107">DESCRIPTION</span></span>
<span data-ttu-id="87113-108">Löscht die Datenverbindung mit dem angegebenen Namen.</span><span class="sxs-lookup"><span data-stu-id="87113-108">Deletes the data connection with the given name.</span></span>

## <span data-ttu-id="87113-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="87113-109">EXAMPLES</span></span>

### <span data-ttu-id="87113-110">Beispiel 1: Löschen einer vorhandenen Datenverbindung nach Name</span><span class="sxs-lookup"><span data-stu-id="87113-110">Example 1: Delete an existing data connection by name</span></span>
```powershell
PS C:\> Remove-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "mykustodataconnection"
```

<span data-ttu-id="87113-111">Mit dem obigen Befehl wird die Datenverbindung mit dem Namen "mykustodataconnection" in der Datenbank "mykustodatabase" des vorhandenen Clusters "testnewkustocluster" gelöscht, der in der Ressourcengruppe "testrg" gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="87113-111">The above command deletes the data connection named "mykustodataconnection" in database "mykustodatabase" of the existing cluster "testnewkustocluster" found in the resource group "testrg"</span></span>

## <span data-ttu-id="87113-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="87113-112">PARAMETERS</span></span>

### <span data-ttu-id="87113-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="87113-113">-AsJob</span></span>
<span data-ttu-id="87113-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="87113-114">Run the command as a job</span></span>

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

### <span data-ttu-id="87113-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="87113-115">-ClusterName</span></span>
<span data-ttu-id="87113-116">Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="87113-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="87113-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="87113-117">-DatabaseName</span></span>
<span data-ttu-id="87113-118">Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="87113-118">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="87113-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87113-119">-DefaultProfile</span></span>
<span data-ttu-id="87113-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="87113-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87113-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="87113-121">-InputObject</span></span>
<span data-ttu-id="87113-122">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="87113-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="87113-123">-Name</span><span class="sxs-lookup"><span data-stu-id="87113-123">-Name</span></span>
<span data-ttu-id="87113-124">Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="87113-124">The name of the data connection.</span></span>

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

### <span data-ttu-id="87113-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="87113-125">-NoWait</span></span>
<span data-ttu-id="87113-126">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="87113-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="87113-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="87113-127">-PassThru</span></span>
<span data-ttu-id="87113-128">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="87113-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="87113-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87113-129">-ResourceGroupName</span></span>
<span data-ttu-id="87113-130">Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="87113-130">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="87113-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="87113-131">-SubscriptionId</span></span>
<span data-ttu-id="87113-132">Ruft Abonnementanmeldeinformationen ab, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="87113-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="87113-133">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="87113-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="87113-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="87113-134">-Confirm</span></span>
<span data-ttu-id="87113-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="87113-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87113-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87113-136">-WhatIf</span></span>
<span data-ttu-id="87113-137">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="87113-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87113-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="87113-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87113-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87113-139">CommonParameters</span></span>
<span data-ttu-id="87113-140">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87113-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87113-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="87113-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87113-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="87113-142">INPUTS</span></span>

### <span data-ttu-id="87113-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="87113-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="87113-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="87113-144">OUTPUTS</span></span>

### <span data-ttu-id="87113-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="87113-145">System.Boolean</span></span>

## <span data-ttu-id="87113-146">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="87113-146">NOTES</span></span>

<span data-ttu-id="87113-147">ALIASE</span><span class="sxs-lookup"><span data-stu-id="87113-147">ALIASES</span></span>

<span data-ttu-id="87113-148">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="87113-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="87113-149">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="87113-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="87113-150">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="87113-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="87113-151">INPUTOBJECT <IKustoIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="87113-151">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="87113-152">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="87113-152">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="87113-153">`[ClusterName <String>]`: Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="87113-153">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="87113-154">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="87113-154">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="87113-155">`[DatabaseName <String>]`: Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="87113-155">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="87113-156">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="87113-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="87113-157">`[Location <String>]`: Azure-Standort.</span><span class="sxs-lookup"><span data-stu-id="87113-157">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="87113-158">`[PrincipalAssignmentName <String>]`: Der Name der Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="87113-158">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="87113-159">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="87113-159">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="87113-160">`[SubscriptionId <String>]`: Ruft Abonnementanmeldeinformationen ab, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="87113-160">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="87113-161">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="87113-161">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="87113-162">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="87113-162">RELATED LINKS</span></span>

