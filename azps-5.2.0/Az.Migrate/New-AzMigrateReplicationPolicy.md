---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratereplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationPolicy.md
ms.openlocfilehash: 5978c247f14507934662f5a5d1846a02180cd812
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356780"
---
# <span data-ttu-id="e1ec1-101">New-AzMigrateReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="e1ec1-101">New-AzMigrateReplicationPolicy</span></span>

## <span data-ttu-id="e1ec1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1ec1-102">SYNOPSIS</span></span>
<span data-ttu-id="e1ec1-103">Der Vorgang zum Erstellen einer Replikationsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="e1ec1-103">The operation to create a replication policy</span></span>

## <span data-ttu-id="e1ec1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e1ec1-104">SYNTAX</span></span>

```
New-AzMigrateReplicationPolicy -PolicyName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String>] [-ProviderSpecificInput <IPolicyProviderSpecificInput>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e1ec1-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e1ec1-105">DESCRIPTION</span></span>
<span data-ttu-id="e1ec1-106">Der Vorgang zum Erstellen einer Replikationsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="e1ec1-106">The operation to create a replication policy</span></span>

## <span data-ttu-id="e1ec1-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e1ec1-107">EXAMPLES</span></span>

### <span data-ttu-id="e1ec1-108">Beispiel 1: Erstellen einer Replikationsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="e1ec1-108">Example 1: Create a replication policy</span></span>
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

<span data-ttu-id="e1ec1-109">Erstellt eine Richtlinie für VmWare Cbt.</span><span class="sxs-lookup"><span data-stu-id="e1ec1-109">Creates a policy for VmWare Cbt</span></span>

## <span data-ttu-id="e1ec1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1ec1-110">PARAMETERS</span></span>

### <span data-ttu-id="e1ec1-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e1ec1-111">-AsJob</span></span>
<span data-ttu-id="e1ec1-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="e1ec1-112">Run the command as a job</span></span>

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

### <span data-ttu-id="e1ec1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1ec1-113">-DefaultProfile</span></span>
<span data-ttu-id="e1ec1-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e1ec1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1ec1-115">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e1ec1-115">-NoWait</span></span>
<span data-ttu-id="e1ec1-116">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="e1ec1-116">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e1ec1-117">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="e1ec1-117">-PolicyName</span></span>
<span data-ttu-id="e1ec1-118">Name der Replikationsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="e1ec1-118">Replication policy name</span></span>

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

### <span data-ttu-id="e1ec1-119">-ProviderSpecificInput</span><span class="sxs-lookup"><span data-stu-id="e1ec1-119">-ProviderSpecificInput</span></span>
<span data-ttu-id="e1ec1-120">Die ReplicationProviderSettings.</span><span class="sxs-lookup"><span data-stu-id="e1ec1-120">The ReplicationProviderSettings.</span></span>
<span data-ttu-id="e1ec1-121">Informationen zum Erstellen finden Sie im Abschnitt NOTES zu DEN PROVIDERSPECIFICINPUT-Eigenschaften und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="e1ec1-121">To construct, see NOTES section for PROVIDERSPECIFICINPUT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e1ec1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1ec1-122">-ResourceGroupName</span></span>
<span data-ttu-id="e1ec1-123">Der Name der Ressourcengruppe, in der sich der Tresor der Wiederherstellungsdienste befindet.</span><span class="sxs-lookup"><span data-stu-id="e1ec1-123">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="e1ec1-124">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="e1ec1-124">-ResourceName</span></span>
<span data-ttu-id="e1ec1-125">Der Name des Tresors der Wiederherstellungsdienste.</span><span class="sxs-lookup"><span data-stu-id="e1ec1-125">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="e1ec1-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e1ec1-126">-SubscriptionId</span></span>
<span data-ttu-id="e1ec1-127">Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="e1ec1-127">The subscription Id.</span></span>

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

### <span data-ttu-id="e1ec1-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e1ec1-128">-Confirm</span></span>
<span data-ttu-id="e1ec1-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e1ec1-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1ec1-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="e1ec1-130">-WhatIf</span></span>
<span data-ttu-id="e1ec1-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e1ec1-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1ec1-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e1ec1-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1ec1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1ec1-133">CommonParameters</span></span>
<span data-ttu-id="e1ec1-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1ec1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1ec1-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e1ec1-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1ec1-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e1ec1-136">INPUTS</span></span>

## <span data-ttu-id="e1ec1-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e1ec1-137">OUTPUTS</span></span>

### <span data-ttu-id="e1ec1-138">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicy</span><span class="sxs-lookup"><span data-stu-id="e1ec1-138">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicy</span></span>

## <span data-ttu-id="e1ec1-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e1ec1-139">NOTES</span></span>

<span data-ttu-id="e1ec1-140">ALIASE</span><span class="sxs-lookup"><span data-stu-id="e1ec1-140">ALIASES</span></span>

<span data-ttu-id="e1ec1-141">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="e1ec1-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e1ec1-142">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e1ec1-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e1ec1-143">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e1ec1-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e1ec1-144">PROVIDERSPECIFICINPUT <IPolicyProviderSpecificInput> :The ReplicationProviderSettings.</span><span class="sxs-lookup"><span data-stu-id="e1ec1-144">PROVIDERSPECIFICINPUT <IPolicyProviderSpecificInput>: The ReplicationProviderSettings.</span></span>
  - <span data-ttu-id="e1ec1-145">`[InstanceType <String>]`: Der Klassentyp.</span><span class="sxs-lookup"><span data-stu-id="e1ec1-145">`[InstanceType <String>]`: The class type.</span></span>

## <span data-ttu-id="e1ec1-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e1ec1-146">RELATED LINKS</span></span>

