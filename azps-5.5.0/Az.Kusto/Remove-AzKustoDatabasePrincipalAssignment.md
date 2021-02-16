---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodatabaseprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipalAssignment.md
ms.openlocfilehash: cd29af9ac8569683e6447a51f4d4f6784139f735
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100170424"
---
# <span data-ttu-id="389a3-101">Remove-AzKustoDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="389a3-101">Remove-AzKustoDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="389a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="389a3-102">SYNOPSIS</span></span>
<span data-ttu-id="389a3-103">Löscht eine Kusto PrincipalAssignment.</span><span class="sxs-lookup"><span data-stu-id="389a3-103">Deletes a Kusto principalAssignment.</span></span>

## <span data-ttu-id="389a3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="389a3-104">SYNTAX</span></span>

### <span data-ttu-id="389a3-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="389a3-105">Delete (Default)</span></span>
```
Remove-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -PrincipalAssignmentName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="389a3-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="389a3-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoDatabasePrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="389a3-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="389a3-107">DESCRIPTION</span></span>
<span data-ttu-id="389a3-108">Löscht eine Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="389a3-108">Deletes a Kusto principalAssignment.</span></span>

## <span data-ttu-id="389a3-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="389a3-109">EXAMPLES</span></span>

### <span data-ttu-id="389a3-110">Beispiel 1: Löschen einer vorhandenen PrincipalAssignment für eine Kusto-Datenbank nach Name</span><span class="sxs-lookup"><span data-stu-id="389a3-110">Example 1: Delete an existing Kusto database PrincipalAssignment by name</span></span>
```powershell
PS C:\> Remove-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -PrincipalAssignmentName kustoprincipal1
```

<span data-ttu-id="389a3-111">Der obige Befehl löscht das PrincipalAssignment namens "kustoprincipal1" in der "mykustodatabase" der Kusto-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="389a3-111">The above command deletes the PrincipalAssignment named "kustoprincipal1" in the Kusto database  "mykustodatabase".</span></span>

## <span data-ttu-id="389a3-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="389a3-112">PARAMETERS</span></span>

### <span data-ttu-id="389a3-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="389a3-113">-AsJob</span></span>
<span data-ttu-id="389a3-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="389a3-114">Run the command as a job</span></span>

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

### <span data-ttu-id="389a3-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="389a3-115">-ClusterName</span></span>
<span data-ttu-id="389a3-116">Der Name des Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="389a3-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="389a3-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="389a3-117">-DatabaseName</span></span>
<span data-ttu-id="389a3-118">Der Name der Datenbank im Cluster "Kusto".</span><span class="sxs-lookup"><span data-stu-id="389a3-118">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="389a3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="389a3-119">-DefaultProfile</span></span>
<span data-ttu-id="389a3-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="389a3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="389a3-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="389a3-121">-InputObject</span></span>
<span data-ttu-id="389a3-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="389a3-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="389a3-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="389a3-123">-NoWait</span></span>
<span data-ttu-id="389a3-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="389a3-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="389a3-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="389a3-125">-PassThru</span></span>
<span data-ttu-id="389a3-126">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="389a3-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="389a3-127">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="389a3-127">-PrincipalAssignmentName</span></span>
<span data-ttu-id="389a3-128">Der Name der Kusto PrincipalAssignment.</span><span class="sxs-lookup"><span data-stu-id="389a3-128">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="389a3-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="389a3-129">-ResourceGroupName</span></span>
<span data-ttu-id="389a3-130">Der Name der Ressourcengruppe, die den Cluster "Kusto" enthält.</span><span class="sxs-lookup"><span data-stu-id="389a3-130">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="389a3-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="389a3-131">-SubscriptionId</span></span>
<span data-ttu-id="389a3-132">Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="389a3-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="389a3-133">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="389a3-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="389a3-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="389a3-134">-Confirm</span></span>
<span data-ttu-id="389a3-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="389a3-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="389a3-136">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="389a3-136">-WhatIf</span></span>
<span data-ttu-id="389a3-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="389a3-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="389a3-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="389a3-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="389a3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="389a3-139">CommonParameters</span></span>
<span data-ttu-id="389a3-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="389a3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="389a3-141">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="389a3-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="389a3-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="389a3-142">INPUTS</span></span>

### <span data-ttu-id="389a3-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="389a3-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="389a3-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="389a3-144">OUTPUTS</span></span>

### <span data-ttu-id="389a3-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="389a3-145">System.Boolean</span></span>

## <span data-ttu-id="389a3-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="389a3-146">NOTES</span></span>

<span data-ttu-id="389a3-147">ALIASE</span><span class="sxs-lookup"><span data-stu-id="389a3-147">ALIASES</span></span>

<span data-ttu-id="389a3-148">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="389a3-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="389a3-149">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="389a3-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="389a3-150">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="389a3-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="389a3-151">INPUTOBJECT <IKustoIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="389a3-151">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="389a3-152">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="389a3-152">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="389a3-153">`[ClusterName <String>]`: Der Name des Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="389a3-153">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="389a3-154">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="389a3-154">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="389a3-155">`[DatabaseName <String>]`: Der Name der Datenbank im Cluster "Kusto".</span><span class="sxs-lookup"><span data-stu-id="389a3-155">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="389a3-156">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="389a3-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="389a3-157">`[Location <String>]`: Azure-Standort.</span><span class="sxs-lookup"><span data-stu-id="389a3-157">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="389a3-158">`[PrincipalAssignmentName <String>]`: Der Name der Kusto PrincipalAssignment.</span><span class="sxs-lookup"><span data-stu-id="389a3-158">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="389a3-159">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Cluster "Kusto" enthält.</span><span class="sxs-lookup"><span data-stu-id="389a3-159">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="389a3-160">`[SubscriptionId <String>]`: Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="389a3-160">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="389a3-161">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="389a3-161">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="389a3-162">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="389a3-162">RELATED LINKS</span></span>

