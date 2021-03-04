---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/remove-azkustoattacheddatabaseconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoAttachedDatabaseConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoAttachedDatabaseConfiguration.md
ms.openlocfilehash: 065cb2177eec7bd94439d52f3a4157d9ef043779
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941144"
---
# <span data-ttu-id="ff988-101">Remove-AzKustoAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="ff988-101">Remove-AzKustoAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="ff988-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff988-102">SYNOPSIS</span></span>
<span data-ttu-id="ff988-103">Löscht die angefügte Datenbankkonfiguration mit dem angegebenen Namen.</span><span class="sxs-lookup"><span data-stu-id="ff988-103">Deletes the attached database configuration with the given name.</span></span>

## <span data-ttu-id="ff988-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ff988-104">SYNTAX</span></span>

### <span data-ttu-id="ff988-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="ff988-105">Delete (Default)</span></span>
```
Remove-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="ff988-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ff988-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoAttachedDatabaseConfiguration -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ff988-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ff988-107">DESCRIPTION</span></span>
<span data-ttu-id="ff988-108">Löscht die angefügte Datenbankkonfiguration mit dem angegebenen Namen.</span><span class="sxs-lookup"><span data-stu-id="ff988-108">Deletes the attached database configuration with the given name.</span></span>

## <span data-ttu-id="ff988-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ff988-109">EXAMPLES</span></span>

### <span data-ttu-id="ff988-110">Beispiel 1: Löschen einer vorhandenen AttachedDatabaseConfiguration nach Name</span><span class="sxs-lookup"><span data-stu-id="ff988-110">Example 1: Delete an existing AttachedDatabaseConfiguration by name</span></span>
```powershell
PS C:\> Remove-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf" -Name "myfollowerconfiguration"
```

<span data-ttu-id="ff988-111">Mit dem obigen Befehl wird die in der AttachedDatabaseConfiguration "myfollowerconfiguration" definierte Followerdatenbank aus dem Cluster "testnewkustoclusterf" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="ff988-111">The above command deletes the follower database defined in the AttachedDatabaseConfiguration "myfollowerconfiguration" from cluster "testnewkustoclusterf".</span></span>

## <span data-ttu-id="ff988-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ff988-112">PARAMETERS</span></span>

### <span data-ttu-id="ff988-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ff988-113">-AsJob</span></span>
<span data-ttu-id="ff988-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="ff988-114">Run the command as a job</span></span>

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

### <span data-ttu-id="ff988-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="ff988-115">-ClusterName</span></span>
<span data-ttu-id="ff988-116">Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="ff988-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="ff988-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff988-117">-DefaultProfile</span></span>
<span data-ttu-id="ff988-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ff988-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff988-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ff988-119">-InputObject</span></span>
<span data-ttu-id="ff988-120">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="ff988-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ff988-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ff988-121">-Name</span></span>
<span data-ttu-id="ff988-122">Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="ff988-122">The name of the attached database configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AttachedDatabaseConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff988-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ff988-123">-NoWait</span></span>
<span data-ttu-id="ff988-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="ff988-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ff988-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ff988-125">-PassThru</span></span>
<span data-ttu-id="ff988-126">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ff988-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ff988-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff988-127">-ResourceGroupName</span></span>
<span data-ttu-id="ff988-128">Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="ff988-128">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="ff988-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ff988-129">-SubscriptionId</span></span>
<span data-ttu-id="ff988-130">Ruft Abonnementanmeldeinformationen ab, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="ff988-130">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ff988-131">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="ff988-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ff988-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ff988-132">-Confirm</span></span>
<span data-ttu-id="ff988-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ff988-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff988-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff988-134">-WhatIf</span></span>
<span data-ttu-id="ff988-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ff988-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff988-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ff988-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff988-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff988-137">CommonParameters</span></span>
<span data-ttu-id="ff988-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff988-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff988-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ff988-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff988-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ff988-140">INPUTS</span></span>

### <span data-ttu-id="ff988-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="ff988-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="ff988-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ff988-142">OUTPUTS</span></span>

### <span data-ttu-id="ff988-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ff988-143">System.Boolean</span></span>

## <span data-ttu-id="ff988-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ff988-144">NOTES</span></span>

<span data-ttu-id="ff988-145">ALIASE</span><span class="sxs-lookup"><span data-stu-id="ff988-145">ALIASES</span></span>

<span data-ttu-id="ff988-146">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="ff988-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ff988-147">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="ff988-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ff988-148">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ff988-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ff988-149">INPUTOBJECT <IKustoIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="ff988-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ff988-150">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="ff988-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="ff988-151">`[ClusterName <String>]`: Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="ff988-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="ff988-152">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="ff988-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="ff988-153">`[DatabaseName <String>]`: Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="ff988-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="ff988-154">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="ff988-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ff988-155">`[Location <String>]`: Azure-Standort.</span><span class="sxs-lookup"><span data-stu-id="ff988-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="ff988-156">`[PrincipalAssignmentName <String>]`: Der Name der Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="ff988-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="ff988-157">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="ff988-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="ff988-158">`[SubscriptionId <String>]`: Ruft Abonnementanmeldeinformationen ab, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="ff988-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="ff988-159">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="ff988-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="ff988-160">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ff988-160">RELATED LINKS</span></span>

