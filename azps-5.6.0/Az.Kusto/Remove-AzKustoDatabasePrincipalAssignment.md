---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/remove-azkustodatabaseprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipalAssignment.md
ms.openlocfilehash: 66a5a844255f5a44000638877abf6a3ed5f908c1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922376"
---
# <span data-ttu-id="d8e72-101">Remove-AzKustoDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="d8e72-101">Remove-AzKustoDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="d8e72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8e72-102">SYNOPSIS</span></span>
<span data-ttu-id="d8e72-103">Löscht eine Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="d8e72-103">Deletes a Kusto principalAssignment.</span></span>

## <span data-ttu-id="d8e72-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d8e72-104">SYNTAX</span></span>

### <span data-ttu-id="d8e72-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="d8e72-105">Delete (Default)</span></span>
```
Remove-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -PrincipalAssignmentName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d8e72-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d8e72-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoDatabasePrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d8e72-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d8e72-107">DESCRIPTION</span></span>
<span data-ttu-id="d8e72-108">Löscht eine Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="d8e72-108">Deletes a Kusto principalAssignment.</span></span>

## <span data-ttu-id="d8e72-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d8e72-109">EXAMPLES</span></span>

### <span data-ttu-id="d8e72-110">Beispiel 1: Löschen einer vorhandenen Kusto-Datenbank PrincipalAssignment nach Name</span><span class="sxs-lookup"><span data-stu-id="d8e72-110">Example 1: Delete an existing Kusto database PrincipalAssignment by name</span></span>
```powershell
PS C:\> Remove-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -PrincipalAssignmentName kustoprincipal1
```

<span data-ttu-id="d8e72-111">Mit dem obigen Befehl wird das PrincipalAssignment mit dem Namen "kustoprincipal1" in der Kusto-Datenbank "mykustodatabase" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="d8e72-111">The above command deletes the PrincipalAssignment named "kustoprincipal1" in the Kusto database  "mykustodatabase".</span></span>

## <span data-ttu-id="d8e72-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d8e72-112">PARAMETERS</span></span>

### <span data-ttu-id="d8e72-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d8e72-113">-AsJob</span></span>
<span data-ttu-id="d8e72-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="d8e72-114">Run the command as a job</span></span>

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

### <span data-ttu-id="d8e72-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="d8e72-115">-ClusterName</span></span>
<span data-ttu-id="d8e72-116">Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="d8e72-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="d8e72-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d8e72-117">-DatabaseName</span></span>
<span data-ttu-id="d8e72-118">Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="d8e72-118">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="d8e72-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8e72-119">-DefaultProfile</span></span>
<span data-ttu-id="d8e72-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d8e72-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8e72-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8e72-121">-InputObject</span></span>
<span data-ttu-id="d8e72-122">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="d8e72-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d8e72-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d8e72-123">-NoWait</span></span>
<span data-ttu-id="d8e72-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="d8e72-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d8e72-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d8e72-125">-PassThru</span></span>
<span data-ttu-id="d8e72-126">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d8e72-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d8e72-127">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="d8e72-127">-PrincipalAssignmentName</span></span>
<span data-ttu-id="d8e72-128">Der Name der Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="d8e72-128">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="d8e72-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8e72-129">-ResourceGroupName</span></span>
<span data-ttu-id="d8e72-130">Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="d8e72-130">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="d8e72-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d8e72-131">-SubscriptionId</span></span>
<span data-ttu-id="d8e72-132">Ruft Abonnementanmeldeinformationen ab, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="d8e72-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d8e72-133">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="d8e72-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d8e72-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d8e72-134">-Confirm</span></span>
<span data-ttu-id="d8e72-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d8e72-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8e72-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8e72-136">-WhatIf</span></span>
<span data-ttu-id="d8e72-137">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d8e72-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8e72-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d8e72-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8e72-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8e72-139">CommonParameters</span></span>
<span data-ttu-id="d8e72-140">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8e72-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8e72-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d8e72-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8e72-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d8e72-142">INPUTS</span></span>

### <span data-ttu-id="d8e72-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="d8e72-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="d8e72-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d8e72-144">OUTPUTS</span></span>

### <span data-ttu-id="d8e72-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d8e72-145">System.Boolean</span></span>

## <span data-ttu-id="d8e72-146">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d8e72-146">NOTES</span></span>

<span data-ttu-id="d8e72-147">ALIASE</span><span class="sxs-lookup"><span data-stu-id="d8e72-147">ALIASES</span></span>

<span data-ttu-id="d8e72-148">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="d8e72-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d8e72-149">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="d8e72-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d8e72-150">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d8e72-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d8e72-151">INPUTOBJECT <IKustoIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="d8e72-151">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d8e72-152">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="d8e72-152">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="d8e72-153">`[ClusterName <String>]`: Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="d8e72-153">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="d8e72-154">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="d8e72-154">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="d8e72-155">`[DatabaseName <String>]`: Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="d8e72-155">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="d8e72-156">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="d8e72-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d8e72-157">`[Location <String>]`: Azure-Standort.</span><span class="sxs-lookup"><span data-stu-id="d8e72-157">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="d8e72-158">`[PrincipalAssignmentName <String>]`: Der Name der Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="d8e72-158">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="d8e72-159">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="d8e72-159">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="d8e72-160">`[SubscriptionId <String>]`: Ruft Abonnementanmeldeinformationen ab, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="d8e72-160">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="d8e72-161">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="d8e72-161">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="d8e72-162">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d8e72-162">RELATED LINKS</span></span>

