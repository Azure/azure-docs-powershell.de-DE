---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratereplicationprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationProtectionContainerMapping.md
ms.openlocfilehash: b92d483689c94e6dd9f9af69e47f5b17ea1ab795
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178841"
---
# <span data-ttu-id="56adb-101">New-AzMigrateReplicationProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="56adb-101">New-AzMigrateReplicationProtectionContainerMapping</span></span>

## <span data-ttu-id="56adb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="56adb-102">SYNOPSIS</span></span>
<span data-ttu-id="56adb-103">Der Vorgang zum Erstellen einer Schutzcontainer Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="56adb-103">The operation to create a protection container mapping.</span></span>

## <span data-ttu-id="56adb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="56adb-104">SYNTAX</span></span>

```
New-AzMigrateReplicationProtectionContainerMapping -FabricName <String> -MappingName <String>
 -ProtectionContainerName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String>] [-PolicyId <String>]
 [-ProviderSpecificInput <IReplicationProviderSpecificContainerMappingInput>]
 [-TargetProtectionContainerId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="56adb-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="56adb-105">DESCRIPTION</span></span>
<span data-ttu-id="56adb-106">Der Vorgang zum Erstellen einer Schutzcontainer Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="56adb-106">The operation to create a protection container mapping.</span></span>

## <span data-ttu-id="56adb-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="56adb-107">EXAMPLES</span></span>

### <span data-ttu-id="56adb-108">Beispiel 1: Erstellen einer Zuordnung</span><span class="sxs-lookup"><span data-stu-id="56adb-108">Example 1: Create a mapping</span></span>
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

<span data-ttu-id="56adb-109">Erstellen einer Zuordnung</span><span class="sxs-lookup"><span data-stu-id="56adb-109">Create a mapping</span></span>

## <span data-ttu-id="56adb-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="56adb-110">PARAMETERS</span></span>

### <span data-ttu-id="56adb-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="56adb-111">-AsJob</span></span>
<span data-ttu-id="56adb-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="56adb-112">Run the command as a job</span></span>

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

### <span data-ttu-id="56adb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56adb-113">-DefaultProfile</span></span>
<span data-ttu-id="56adb-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="56adb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56adb-115">-Fabricname</span><span class="sxs-lookup"><span data-stu-id="56adb-115">-FabricName</span></span>
<span data-ttu-id="56adb-116">Name des Stoffs.</span><span class="sxs-lookup"><span data-stu-id="56adb-116">Fabric name.</span></span>

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

### <span data-ttu-id="56adb-117">-MappingName</span><span class="sxs-lookup"><span data-stu-id="56adb-117">-MappingName</span></span>
<span data-ttu-id="56adb-118">Name des Schutzcontainer-Mappings</span><span class="sxs-lookup"><span data-stu-id="56adb-118">Protection container mapping name.</span></span>

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

### <span data-ttu-id="56adb-119">-Nowait</span><span class="sxs-lookup"><span data-stu-id="56adb-119">-NoWait</span></span>
<span data-ttu-id="56adb-120">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="56adb-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="56adb-121">-Richtlinien-Nr</span><span class="sxs-lookup"><span data-stu-id="56adb-121">-PolicyId</span></span>
<span data-ttu-id="56adb-122">Anwendbare Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="56adb-122">Applicable policy.</span></span>

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

### <span data-ttu-id="56adb-123">-ProtectionContainerName</span><span class="sxs-lookup"><span data-stu-id="56adb-123">-ProtectionContainerName</span></span>
<span data-ttu-id="56adb-124">Name des Schutz Containers.</span><span class="sxs-lookup"><span data-stu-id="56adb-124">Protection container name.</span></span>

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

### <span data-ttu-id="56adb-125">-ProviderSpecificInput</span><span class="sxs-lookup"><span data-stu-id="56adb-125">-ProviderSpecificInput</span></span>
<span data-ttu-id="56adb-126">Anbieterspezifische Eingabe für Kopplung.</span><span class="sxs-lookup"><span data-stu-id="56adb-126">Provider specific input for pairing.</span></span>
<span data-ttu-id="56adb-127">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für PROVIDERSPECIFICINPUT-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="56adb-127">To construct, see NOTES section for PROVIDERSPECIFICINPUT properties and create a hash table.</span></span>

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

### <span data-ttu-id="56adb-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56adb-128">-ResourceGroupName</span></span>
<span data-ttu-id="56adb-129">Der Name der Ressourcengruppe, in der der Vault für Wiederherstellungsdienste vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="56adb-129">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="56adb-130">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="56adb-130">-ResourceName</span></span>
<span data-ttu-id="56adb-131">Der Name des Speichers für Wiederherstellungsdienste.</span><span class="sxs-lookup"><span data-stu-id="56adb-131">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="56adb-132">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="56adb-132">-SubscriptionId</span></span>
<span data-ttu-id="56adb-133">Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="56adb-133">The subscription Id.</span></span>

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

### <span data-ttu-id="56adb-134">-TargetProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="56adb-134">-TargetProtectionContainerId</span></span>
<span data-ttu-id="56adb-135">Der Name des eindeutigen Ziel Schutz Containers.</span><span class="sxs-lookup"><span data-stu-id="56adb-135">The target unique protection container name.</span></span>

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

### <span data-ttu-id="56adb-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="56adb-136">-Confirm</span></span>
<span data-ttu-id="56adb-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="56adb-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56adb-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56adb-138">-WhatIf</span></span>
<span data-ttu-id="56adb-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="56adb-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56adb-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="56adb-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56adb-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56adb-141">CommonParameters</span></span>
<span data-ttu-id="56adb-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56adb-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56adb-143">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="56adb-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56adb-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="56adb-144">INPUTS</span></span>

## <span data-ttu-id="56adb-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="56adb-145">OUTPUTS</span></span>

### <span data-ttu-id="56adb-146">Microsoft. Azure. PowerShell. Cmdlets. migrate. Models. Api20180110. IProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="56adb-146">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainerMapping</span></span>

## <span data-ttu-id="56adb-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="56adb-147">NOTES</span></span>

<span data-ttu-id="56adb-148">Aliase</span><span class="sxs-lookup"><span data-stu-id="56adb-148">ALIASES</span></span>

<span data-ttu-id="56adb-149">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="56adb-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="56adb-150">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="56adb-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="56adb-151">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="56adb-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="56adb-152">PROVIDERSPECIFICINPUT <IReplicationProviderSpecificContainerMappingInput> : anbieterspezifische Eingabe für die Kopplung.</span><span class="sxs-lookup"><span data-stu-id="56adb-152">PROVIDERSPECIFICINPUT <IReplicationProviderSpecificContainerMappingInput>: Provider specific input for pairing.</span></span>
  - <span data-ttu-id="56adb-153">`[InstanceType <String>]`: Der Klassentyp.</span><span class="sxs-lookup"><span data-stu-id="56adb-153">`[InstanceType <String>]`: The class type.</span></span>

## <span data-ttu-id="56adb-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="56adb-154">RELATED LINKS</span></span>

