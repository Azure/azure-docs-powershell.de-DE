---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratereplicationprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationProtectionContainerMapping.md
ms.openlocfilehash: b92d483689c94e6dd9f9af69e47f5b17ea1ab795
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469364"
---
# <span data-ttu-id="0d119-101">New-AzMigrateReplicationProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="0d119-101">New-AzMigrateReplicationProtectionContainerMapping</span></span>

## <span data-ttu-id="0d119-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d119-102">SYNOPSIS</span></span>
<span data-ttu-id="0d119-103">Der Vorgang zum Erstellen einer Schutzcontainerzuordnung.</span><span class="sxs-lookup"><span data-stu-id="0d119-103">The operation to create a protection container mapping.</span></span>

## <span data-ttu-id="0d119-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0d119-104">SYNTAX</span></span>

```
New-AzMigrateReplicationProtectionContainerMapping -FabricName <String> -MappingName <String>
 -ProtectionContainerName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String>] [-PolicyId <String>]
 [-ProviderSpecificInput <IReplicationProviderSpecificContainerMappingInput>]
 [-TargetProtectionContainerId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="0d119-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0d119-105">DESCRIPTION</span></span>
<span data-ttu-id="0d119-106">Der Vorgang zum Erstellen einer Schutzcontainerzuordnung.</span><span class="sxs-lookup"><span data-stu-id="0d119-106">The operation to create a protection container mapping.</span></span>

## <span data-ttu-id="0d119-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0d119-107">EXAMPLES</span></span>

### <span data-ttu-id="0d119-108">Beispiel 1: Erstellen einer Zuordnung</span><span class="sxs-lookup"><span data-stu-id="0d119-108">Example 1: Create a mapping</span></span>
```powershell
PS C:\> $providerSpecificInput = [Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.VMwareCbtContainerMappingInput]::new()
PS C:\> $providerSpecificInput.InstanceType = "VMwareCbt"
PS C:\> $providerSpecificInput.KeyVaultId = "/subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.KeyVault/vaults/migratekv846827101"
PS C:\> $providerSpecificInput.KeyVaultUri = "https://migratekv846827101.vault.azure.net"
PS C:\> $providerSpecificInput.ServiceBusConnectionStringSecretName = "ServiceBusConnectionString"
PS C:\> $providerSpecificInput.StorageAccountId = "/subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Storage/storageAccounts/migrategwsa846827101"
PS C:\> $providerSpecificInput.StorageAccountSasSecretName = "migrategwsa846827101-gwySas"
PS C:\> $providerSpecificInput.TargetLocation = "centraluseuap"

PS C:\> New-AzMigrateReplicationProtectionContainerMapping -FabricName "AzMigratePWSHTc8d1replicationfabric" -MappingName "containermapping" -ProtectionContainerName "AzMigratePWSHTc8d1replicationcontainer" -ResourceGroupName "azmigratepwshtestasr13072020" -ResourceName "AzMigrateTestProjectPWSH02aarsvault"  -PolicyId "/subscriptionsxxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationPolicies/migrateAzMigratePWSHTc8d1sitepolicy"  -ProviderSpecificInput $providerSpecificInput -TargetProtectionContainerId  "Microsoft Azure"

Location Name             Type
-------- ----             ----
         containermapping Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationProtectionContainerMappings
```

<span data-ttu-id="0d119-109">Erstellen einer Zuordnung</span><span class="sxs-lookup"><span data-stu-id="0d119-109">Create a mapping</span></span>

## <span data-ttu-id="0d119-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0d119-110">PARAMETERS</span></span>

### <span data-ttu-id="0d119-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0d119-111">-AsJob</span></span>
<span data-ttu-id="0d119-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="0d119-112">Run the command as a job</span></span>

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

### <span data-ttu-id="0d119-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d119-113">-DefaultProfile</span></span>
<span data-ttu-id="0d119-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0d119-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d119-115">-FabricName</span><span class="sxs-lookup"><span data-stu-id="0d119-115">-FabricName</span></span>
<span data-ttu-id="0d119-116">Fabric name.</span><span class="sxs-lookup"><span data-stu-id="0d119-116">Fabric name.</span></span>

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

### <span data-ttu-id="0d119-117">-MappingName</span><span class="sxs-lookup"><span data-stu-id="0d119-117">-MappingName</span></span>
<span data-ttu-id="0d119-118">Name der Schutzcontainerzuordnung.</span><span class="sxs-lookup"><span data-stu-id="0d119-118">Protection container mapping name.</span></span>

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

### <span data-ttu-id="0d119-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="0d119-119">-NoWait</span></span>
<span data-ttu-id="0d119-120">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="0d119-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0d119-121">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="0d119-121">-PolicyId</span></span>
<span data-ttu-id="0d119-122">Anwendbare Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="0d119-122">Applicable policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d119-123">-ProtectionContainerName</span><span class="sxs-lookup"><span data-stu-id="0d119-123">-ProtectionContainerName</span></span>
<span data-ttu-id="0d119-124">Name des Schutzcontainers.</span><span class="sxs-lookup"><span data-stu-id="0d119-124">Protection container name.</span></span>

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

### <span data-ttu-id="0d119-125">-ProviderSpecificInput</span><span class="sxs-lookup"><span data-stu-id="0d119-125">-ProviderSpecificInput</span></span>
<span data-ttu-id="0d119-126">Anbieterspezifische Eingabe für die Kopplung.</span><span class="sxs-lookup"><span data-stu-id="0d119-126">Provider specific input for pairing.</span></span>
<span data-ttu-id="0d119-127">Informationen zum Erstellen finden Sie im Abschnitt NOTES zu DEN PROVIDERSPECIFICINPUT-Eigenschaften und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="0d119-127">To construct, see NOTES section for PROVIDERSPECIFICINPUT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IReplicationProviderSpecificContainerMappingInput
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d119-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d119-128">-ResourceGroupName</span></span>
<span data-ttu-id="0d119-129">Der Name der Ressourcengruppe, in der sich der Tresor der Wiederherstellungsdienste befindet.</span><span class="sxs-lookup"><span data-stu-id="0d119-129">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="0d119-130">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="0d119-130">-ResourceName</span></span>
<span data-ttu-id="0d119-131">Der Name des Tresors der Wiederherstellungsdienste.</span><span class="sxs-lookup"><span data-stu-id="0d119-131">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="0d119-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0d119-132">-SubscriptionId</span></span>
<span data-ttu-id="0d119-133">Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="0d119-133">The subscription Id.</span></span>

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

### <span data-ttu-id="0d119-134">-TargetProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="0d119-134">-TargetProtectionContainerId</span></span>
<span data-ttu-id="0d119-135">Der Name des eindeutigen Zielschutzescontainers.</span><span class="sxs-lookup"><span data-stu-id="0d119-135">The target unique protection container name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d119-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0d119-136">-Confirm</span></span>
<span data-ttu-id="0d119-137">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0d119-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d119-138">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="0d119-138">-WhatIf</span></span>
<span data-ttu-id="0d119-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0d119-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d119-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0d119-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d119-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d119-141">CommonParameters</span></span>
<span data-ttu-id="0d119-142">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d119-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d119-143">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0d119-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d119-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0d119-144">INPUTS</span></span>

## <span data-ttu-id="0d119-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0d119-145">OUTPUTS</span></span>

### <span data-ttu-id="0d119-146">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="0d119-146">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainerMapping</span></span>

## <span data-ttu-id="0d119-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0d119-147">NOTES</span></span>

<span data-ttu-id="0d119-148">ALIASE</span><span class="sxs-lookup"><span data-stu-id="0d119-148">ALIASES</span></span>

<span data-ttu-id="0d119-149">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="0d119-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0d119-150">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0d119-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0d119-151">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0d119-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0d119-152">PROVIDERSPECIFICINPUT <IReplicationProviderSpecificContainerMappingInput> : Anbieterspezifische Eingabe für die Kopplung.</span><span class="sxs-lookup"><span data-stu-id="0d119-152">PROVIDERSPECIFICINPUT <IReplicationProviderSpecificContainerMappingInput>: Provider specific input for pairing.</span></span>
  - <span data-ttu-id="0d119-153">`[InstanceType <String>]`: Der Klassentyp.</span><span class="sxs-lookup"><span data-stu-id="0d119-153">`[InstanceType <String>]`: The class type.</span></span>

## <span data-ttu-id="0d119-154">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0d119-154">RELATED LINKS</span></span>

