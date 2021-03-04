---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/remove-azkustoclusterprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoClusterPrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoClusterPrincipalAssignment.md
ms.openlocfilehash: b2dd7c125fbf2529e7dc214efdc9ef5fdef1ace0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944057"
---
# <span data-ttu-id="c56aa-101">Remove-AzKustoClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="c56aa-101">Remove-AzKustoClusterPrincipalAssignment</span></span>

## <span data-ttu-id="c56aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c56aa-102">SYNOPSIS</span></span>
<span data-ttu-id="c56aa-103">Löscht einen Kusto-ClusterprinzipalAssignment.</span><span class="sxs-lookup"><span data-stu-id="c56aa-103">Deletes a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="c56aa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c56aa-104">SYNTAX</span></span>

### <span data-ttu-id="c56aa-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="c56aa-105">Delete (Default)</span></span>
```
Remove-AzKustoClusterPrincipalAssignment -ClusterName <String> -PrincipalAssignmentName <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c56aa-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c56aa-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoClusterPrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c56aa-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c56aa-107">DESCRIPTION</span></span>
<span data-ttu-id="c56aa-108">Löscht einen Kusto-ClusterprinzipalAssignment.</span><span class="sxs-lookup"><span data-stu-id="c56aa-108">Deletes a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="c56aa-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c56aa-109">EXAMPLES</span></span>

### <span data-ttu-id="c56aa-110">Beispiel 1: Löschen eines vorhandenen Kusto-Cluster principalAssignment nach Name</span><span class="sxs-lookup"><span data-stu-id="c56aa-110">Example 1: Delete an existing Kusto cluster PrincipalAssignment by name</span></span>
```powershell
PS C:\> Remove-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -PrincipalAssignmentName kustoprincipal1
```

<span data-ttu-id="c56aa-111">Mit dem obigen Befehl wird das PrincipalAssignment mit dem Namen "kustoprincipal1" im Kusto-Cluster "testnewkustocluster" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="c56aa-111">The above command deletes the PrincipalAssignment named "kustoprincipal1" in the Kusto cluster  "testnewkustocluster".</span></span>

## <span data-ttu-id="c56aa-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c56aa-112">PARAMETERS</span></span>

### <span data-ttu-id="c56aa-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c56aa-113">-AsJob</span></span>
<span data-ttu-id="c56aa-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="c56aa-114">Run the command as a job</span></span>

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

### <span data-ttu-id="c56aa-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="c56aa-115">-ClusterName</span></span>
<span data-ttu-id="c56aa-116">Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="c56aa-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="c56aa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c56aa-117">-DefaultProfile</span></span>
<span data-ttu-id="c56aa-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c56aa-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c56aa-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c56aa-119">-InputObject</span></span>
<span data-ttu-id="c56aa-120">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="c56aa-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c56aa-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c56aa-121">-NoWait</span></span>
<span data-ttu-id="c56aa-122">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="c56aa-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c56aa-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c56aa-123">-PassThru</span></span>
<span data-ttu-id="c56aa-124">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c56aa-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c56aa-125">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="c56aa-125">-PrincipalAssignmentName</span></span>
<span data-ttu-id="c56aa-126">Der Name der Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="c56aa-126">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="c56aa-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c56aa-127">-ResourceGroupName</span></span>
<span data-ttu-id="c56aa-128">Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="c56aa-128">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="c56aa-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c56aa-129">-SubscriptionId</span></span>
<span data-ttu-id="c56aa-130">Ruft Abonnementanmeldeinformationen ab, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="c56aa-130">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c56aa-131">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="c56aa-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c56aa-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c56aa-132">-Confirm</span></span>
<span data-ttu-id="c56aa-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c56aa-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c56aa-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c56aa-134">-WhatIf</span></span>
<span data-ttu-id="c56aa-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c56aa-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c56aa-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c56aa-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c56aa-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c56aa-137">CommonParameters</span></span>
<span data-ttu-id="c56aa-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c56aa-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c56aa-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c56aa-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c56aa-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c56aa-140">INPUTS</span></span>

### <span data-ttu-id="c56aa-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="c56aa-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="c56aa-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c56aa-142">OUTPUTS</span></span>

### <span data-ttu-id="c56aa-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c56aa-143">System.Boolean</span></span>

## <span data-ttu-id="c56aa-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c56aa-144">NOTES</span></span>

<span data-ttu-id="c56aa-145">ALIASE</span><span class="sxs-lookup"><span data-stu-id="c56aa-145">ALIASES</span></span>

<span data-ttu-id="c56aa-146">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="c56aa-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c56aa-147">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="c56aa-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c56aa-148">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c56aa-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c56aa-149">INPUTOBJECT <IKustoIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="c56aa-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c56aa-150">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="c56aa-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="c56aa-151">`[ClusterName <String>]`: Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="c56aa-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="c56aa-152">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="c56aa-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="c56aa-153">`[DatabaseName <String>]`: Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="c56aa-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="c56aa-154">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="c56aa-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c56aa-155">`[Location <String>]`: Azure-Standort.</span><span class="sxs-lookup"><span data-stu-id="c56aa-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="c56aa-156">`[PrincipalAssignmentName <String>]`: Der Name der Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="c56aa-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="c56aa-157">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="c56aa-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="c56aa-158">`[SubscriptionId <String>]`: Ruft Abonnementanmeldeinformationen ab, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="c56aa-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="c56aa-159">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="c56aa-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="c56aa-160">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c56aa-160">RELATED LINKS</span></span>

