---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratereplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationPolicy.md
ms.openlocfilehash: 5978c247f14507934662f5a5d1846a02180cd812
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458291"
---
# <span data-ttu-id="afccb-101">New-AzMigrateReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="afccb-101">New-AzMigrateReplicationPolicy</span></span>

## <span data-ttu-id="afccb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="afccb-102">SYNOPSIS</span></span>
<span data-ttu-id="afccb-103">Der Vorgang zum Erstellen einer Replikationsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="afccb-103">The operation to create a replication policy</span></span>

## <span data-ttu-id="afccb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="afccb-104">SYNTAX</span></span>

```
New-AzMigrateReplicationPolicy -PolicyName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String>] [-ProviderSpecificInput <IPolicyProviderSpecificInput>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="afccb-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="afccb-105">DESCRIPTION</span></span>
<span data-ttu-id="afccb-106">Der Vorgang zum Erstellen einer Replikationsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="afccb-106">The operation to create a replication policy</span></span>

## <span data-ttu-id="afccb-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="afccb-107">EXAMPLES</span></span>

### <span data-ttu-id="afccb-108">Beispiel 1: Erstellen einer Replikationsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="afccb-108">Example 1: Create a replication policy</span></span>
```powershell
PS C:\> $providerSpecificPolicy = [Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.VMwareCbtPolicyCreationInput]::new()
PS C:\> $providerSpecificPolicy.AppConsistentFrequencyInMinute = 240
PS C:\> $providerSpecificPolicy.InstanceType = "VMwareCbt"
PS C:\> $providerSpecificPolicy.RecoveryPointHistoryInMinute = 4320
PS C:\> $providerSpecificPolicy.CrashConsistentFrequencyInMinute = 60
PS C:\> New-AzMigrateReplicationPolicy -PolicyName TestPolicy -ResourceGroupName ResourceGroup -ResourceName VaultName -SubscriptionId SubscriptionId -ProviderSpecificInput $providerSpecificPolicy

Location Name       Type
-------- ----       ----
         TestPolicy Microsoft.RecoveryServices/vaults/replicationPolicies
         
```

<span data-ttu-id="afccb-109">Erstellt eine Richtlinie für VmWare Cbt.</span><span class="sxs-lookup"><span data-stu-id="afccb-109">Creates a policy for VmWare Cbt</span></span>

## <span data-ttu-id="afccb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="afccb-110">PARAMETERS</span></span>

### <span data-ttu-id="afccb-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="afccb-111">-AsJob</span></span>
<span data-ttu-id="afccb-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="afccb-112">Run the command as a job</span></span>

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

### <span data-ttu-id="afccb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afccb-113">-DefaultProfile</span></span>
<span data-ttu-id="afccb-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="afccb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afccb-115">-NoWait</span><span class="sxs-lookup"><span data-stu-id="afccb-115">-NoWait</span></span>
<span data-ttu-id="afccb-116">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="afccb-116">Run the command asynchronously</span></span>

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

### <span data-ttu-id="afccb-117">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="afccb-117">-PolicyName</span></span>
<span data-ttu-id="afccb-118">Name der Replikationsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="afccb-118">Replication policy name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afccb-119">-ProviderSpecificInput</span><span class="sxs-lookup"><span data-stu-id="afccb-119">-ProviderSpecificInput</span></span>
<span data-ttu-id="afccb-120">Die ReplicationProviderSettings.</span><span class="sxs-lookup"><span data-stu-id="afccb-120">The ReplicationProviderSettings.</span></span>
<span data-ttu-id="afccb-121">Informationen zum Erstellen finden Sie im Abschnitt NOTES zu DEN PROVIDERSPECIFICINPUT-Eigenschaften und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="afccb-121">To construct, see NOTES section for PROVIDERSPECIFICINPUT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicyProviderSpecificInput
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afccb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afccb-122">-ResourceGroupName</span></span>
<span data-ttu-id="afccb-123">Der Name der Ressourcengruppe, in der sich der Tresor der Wiederherstellungsdienste befindet.</span><span class="sxs-lookup"><span data-stu-id="afccb-123">The name of the resource group where the recovery services vault is present.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afccb-124">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="afccb-124">-ResourceName</span></span>
<span data-ttu-id="afccb-125">Der Name des Tresors der Wiederherstellungsdienste.</span><span class="sxs-lookup"><span data-stu-id="afccb-125">The name of the recovery services vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afccb-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="afccb-126">-SubscriptionId</span></span>
<span data-ttu-id="afccb-127">Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="afccb-127">The subscription Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afccb-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="afccb-128">-Confirm</span></span>
<span data-ttu-id="afccb-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="afccb-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afccb-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="afccb-130">-WhatIf</span></span>
<span data-ttu-id="afccb-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="afccb-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afccb-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="afccb-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afccb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afccb-133">CommonParameters</span></span>
<span data-ttu-id="afccb-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afccb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afccb-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="afccb-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afccb-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="afccb-136">INPUTS</span></span>

## <span data-ttu-id="afccb-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="afccb-137">OUTPUTS</span></span>

### <span data-ttu-id="afccb-138">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicy</span><span class="sxs-lookup"><span data-stu-id="afccb-138">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicy</span></span>

## <span data-ttu-id="afccb-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="afccb-139">NOTES</span></span>

<span data-ttu-id="afccb-140">ALIASE</span><span class="sxs-lookup"><span data-stu-id="afccb-140">ALIASES</span></span>

<span data-ttu-id="afccb-141">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="afccb-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="afccb-142">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="afccb-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="afccb-143">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="afccb-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="afccb-144">PROVIDERSPECIFICINPUT <IPolicyProviderSpecificInput> :The ReplicationProviderSettings.</span><span class="sxs-lookup"><span data-stu-id="afccb-144">PROVIDERSPECIFICINPUT <IPolicyProviderSpecificInput>: The ReplicationProviderSettings.</span></span>
  - <span data-ttu-id="afccb-145">`[InstanceType <String>]`: Der Klassentyp.</span><span class="sxs-lookup"><span data-stu-id="afccb-145">`[InstanceType <String>]`: The class type.</span></span>

## <span data-ttu-id="afccb-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="afccb-146">RELATED LINKS</span></span>

