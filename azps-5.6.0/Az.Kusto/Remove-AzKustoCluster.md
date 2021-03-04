---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/remove-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoCluster.md
ms.openlocfilehash: 90d080f3c45db107c3f7f86ed8c32c3efe0b066c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921160"
---
# <span data-ttu-id="3c1be-101">Remove-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="3c1be-101">Remove-AzKustoCluster</span></span>

## <span data-ttu-id="3c1be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c1be-102">SYNOPSIS</span></span>
<span data-ttu-id="3c1be-103">Löscht einen Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="3c1be-103">Deletes a Kusto cluster.</span></span>

## <span data-ttu-id="3c1be-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3c1be-104">SYNTAX</span></span>

### <span data-ttu-id="3c1be-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="3c1be-105">Delete (Default)</span></span>
```
Remove-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3c1be-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3c1be-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoCluster -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3c1be-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3c1be-107">DESCRIPTION</span></span>
<span data-ttu-id="3c1be-108">Löscht einen Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="3c1be-108">Deletes a Kusto cluster.</span></span>

## <span data-ttu-id="3c1be-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3c1be-109">EXAMPLES</span></span>

### <span data-ttu-id="3c1be-110">Beispiel 1: Löschen eines vorhandenen Kusto-Clusters nach Name</span><span class="sxs-lookup"><span data-stu-id="3c1be-110">Example 1: Delete an existing Kusto cluster by name</span></span>
```powershell
PS C:\> Remove-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster
```

<span data-ttu-id="3c1be-111">Mit dem obigen Befehl wird der Kusto-Cluster mit dem Namen "testnewkustocluster" in der Ressourcengruppe "testrg" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="3c1be-111">The above command deletes the Kusto cluster named "testnewkustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="3c1be-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3c1be-112">PARAMETERS</span></span>

### <span data-ttu-id="3c1be-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3c1be-113">-AsJob</span></span>
<span data-ttu-id="3c1be-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="3c1be-114">Run the command as a job</span></span>

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

### <span data-ttu-id="3c1be-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c1be-115">-DefaultProfile</span></span>
<span data-ttu-id="3c1be-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3c1be-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c1be-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3c1be-117">-InputObject</span></span>
<span data-ttu-id="3c1be-118">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="3c1be-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3c1be-119">-Name</span><span class="sxs-lookup"><span data-stu-id="3c1be-119">-Name</span></span>
<span data-ttu-id="3c1be-120">Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="3c1be-120">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="3c1be-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3c1be-121">-NoWait</span></span>
<span data-ttu-id="3c1be-122">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="3c1be-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3c1be-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3c1be-123">-PassThru</span></span>
<span data-ttu-id="3c1be-124">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3c1be-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="3c1be-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c1be-125">-ResourceGroupName</span></span>
<span data-ttu-id="3c1be-126">Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="3c1be-126">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="3c1be-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3c1be-127">-SubscriptionId</span></span>
<span data-ttu-id="3c1be-128">Ruft Abonnementanmeldeinformationen ab, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="3c1be-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="3c1be-129">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="3c1be-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3c1be-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3c1be-130">-Confirm</span></span>
<span data-ttu-id="3c1be-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3c1be-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c1be-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c1be-132">-WhatIf</span></span>
<span data-ttu-id="3c1be-133">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3c1be-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c1be-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3c1be-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c1be-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c1be-135">CommonParameters</span></span>
<span data-ttu-id="3c1be-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c1be-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c1be-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3c1be-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c1be-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3c1be-138">INPUTS</span></span>

### <span data-ttu-id="3c1be-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="3c1be-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="3c1be-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3c1be-140">OUTPUTS</span></span>

### <span data-ttu-id="3c1be-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3c1be-141">System.Boolean</span></span>

## <span data-ttu-id="3c1be-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="3c1be-142">NOTES</span></span>

<span data-ttu-id="3c1be-143">ALIASE</span><span class="sxs-lookup"><span data-stu-id="3c1be-143">ALIASES</span></span>

<span data-ttu-id="3c1be-144">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="3c1be-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3c1be-145">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="3c1be-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3c1be-146">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3c1be-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3c1be-147">INPUTOBJECT <IKustoIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="3c1be-147">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3c1be-148">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="3c1be-148">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="3c1be-149">`[ClusterName <String>]`: Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="3c1be-149">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="3c1be-150">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="3c1be-150">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="3c1be-151">`[DatabaseName <String>]`: Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="3c1be-151">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="3c1be-152">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="3c1be-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3c1be-153">`[Location <String>]`: Azure-Standort.</span><span class="sxs-lookup"><span data-stu-id="3c1be-153">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="3c1be-154">`[PrincipalAssignmentName <String>]`: Der Name der Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="3c1be-154">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="3c1be-155">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="3c1be-155">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="3c1be-156">`[SubscriptionId <String>]`: Ruft Abonnementanmeldeinformationen ab, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="3c1be-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="3c1be-157">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="3c1be-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="3c1be-158">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="3c1be-158">RELATED LINKS</span></span>

