---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/stop-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Stop-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Stop-AzKustoCluster.md
ms.openlocfilehash: 1dd67a5a3557ba38267f570c77b5117466e4260b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100159577"
---
# <span data-ttu-id="19ae5-101">Stop-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="19ae5-101">Stop-AzKustoCluster</span></span>

## <span data-ttu-id="19ae5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19ae5-102">SYNOPSIS</span></span>
<span data-ttu-id="19ae5-103">Beendet einen Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="19ae5-103">Stops a Kusto cluster.</span></span>

## <span data-ttu-id="19ae5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="19ae5-104">SYNTAX</span></span>

### <span data-ttu-id="19ae5-105">Stopp (Standard)</span><span class="sxs-lookup"><span data-stu-id="19ae5-105">Stop (Default)</span></span>
```
Stop-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="19ae5-106">StopViaIdentity</span><span class="sxs-lookup"><span data-stu-id="19ae5-106">StopViaIdentity</span></span>
```
Stop-AzKustoCluster -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="19ae5-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="19ae5-107">DESCRIPTION</span></span>
<span data-ttu-id="19ae5-108">Beendet einen Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="19ae5-108">Stops a Kusto cluster.</span></span>

## <span data-ttu-id="19ae5-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="19ae5-109">EXAMPLES</span></span>

### <span data-ttu-id="19ae5-110">Beispiel 1: Beenden eines Cluster "Kusto"</span><span class="sxs-lookup"><span data-stu-id="19ae5-110">Example 1: Stop a Kusto cluster</span></span>
```powershell
PS C:\> Stop-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster
```

<span data-ttu-id="19ae5-111">Der oben aufgeführte Befehl stoppt einen Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="19ae5-111">The above command stops a Kusto cluster</span></span>

## <span data-ttu-id="19ae5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="19ae5-112">PARAMETERS</span></span>

### <span data-ttu-id="19ae5-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="19ae5-113">-AsJob</span></span>
<span data-ttu-id="19ae5-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="19ae5-114">Run the command as a job</span></span>

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

### <span data-ttu-id="19ae5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19ae5-115">-DefaultProfile</span></span>
<span data-ttu-id="19ae5-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="19ae5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19ae5-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="19ae5-117">-InputObject</span></span>
<span data-ttu-id="19ae5-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="19ae5-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: StopViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19ae5-119">-Name</span><span class="sxs-lookup"><span data-stu-id="19ae5-119">-Name</span></span>
<span data-ttu-id="19ae5-120">Der Name des Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="19ae5-120">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19ae5-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="19ae5-121">-NoWait</span></span>
<span data-ttu-id="19ae5-122">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="19ae5-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="19ae5-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="19ae5-123">-PassThru</span></span>
<span data-ttu-id="19ae5-124">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="19ae5-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="19ae5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19ae5-125">-ResourceGroupName</span></span>
<span data-ttu-id="19ae5-126">Der Name der Ressourcengruppe, die den Cluster "Kusto" enthält.</span><span class="sxs-lookup"><span data-stu-id="19ae5-126">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19ae5-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="19ae5-127">-SubscriptionId</span></span>
<span data-ttu-id="19ae5-128">Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="19ae5-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="19ae5-129">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="19ae5-129">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19ae5-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="19ae5-130">-Confirm</span></span>
<span data-ttu-id="19ae5-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="19ae5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19ae5-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="19ae5-132">-WhatIf</span></span>
<span data-ttu-id="19ae5-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="19ae5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19ae5-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="19ae5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19ae5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19ae5-135">CommonParameters</span></span>
<span data-ttu-id="19ae5-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19ae5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19ae5-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="19ae5-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19ae5-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="19ae5-138">INPUTS</span></span>

### <span data-ttu-id="19ae5-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="19ae5-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="19ae5-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="19ae5-140">OUTPUTS</span></span>

### <span data-ttu-id="19ae5-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="19ae5-141">System.Boolean</span></span>

## <span data-ttu-id="19ae5-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="19ae5-142">NOTES</span></span>

<span data-ttu-id="19ae5-143">ALIASE</span><span class="sxs-lookup"><span data-stu-id="19ae5-143">ALIASES</span></span>

<span data-ttu-id="19ae5-144">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="19ae5-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="19ae5-145">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="19ae5-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="19ae5-146">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="19ae5-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="19ae5-147">INPUTOBJECT <IKustoIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="19ae5-147">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="19ae5-148">`[AttachedDatabaseConfigurationName <String>]`: Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="19ae5-148">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="19ae5-149">`[ClusterName <String>]`: Der Name des Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="19ae5-149">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="19ae5-150">`[DataConnectionName <String>]`: Der Name der Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="19ae5-150">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="19ae5-151">`[DatabaseName <String>]`: Der Name der Datenbank im Cluster "Kusto".</span><span class="sxs-lookup"><span data-stu-id="19ae5-151">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="19ae5-152">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="19ae5-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="19ae5-153">`[Location <String>]`: Azure-Standort.</span><span class="sxs-lookup"><span data-stu-id="19ae5-153">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="19ae5-154">`[PrincipalAssignmentName <String>]`: Der Name der Kusto PrincipalAssignment.</span><span class="sxs-lookup"><span data-stu-id="19ae5-154">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="19ae5-155">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Cluster "Kusto" enthält.</span><span class="sxs-lookup"><span data-stu-id="19ae5-155">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="19ae5-156">`[SubscriptionId <String>]`: Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="19ae5-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="19ae5-157">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="19ae5-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="19ae5-158">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="19ae5-158">RELATED LINKS</span></span>

