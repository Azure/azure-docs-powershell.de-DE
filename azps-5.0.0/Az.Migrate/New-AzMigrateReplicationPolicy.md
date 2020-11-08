---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratereplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationPolicy.md
ms.openlocfilehash: 5978c247f14507934662f5a5d1846a02180cd812
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177521"
---
# <span data-ttu-id="ba21e-101">New-AzMigrateReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="ba21e-101">New-AzMigrateReplicationPolicy</span></span>

## <span data-ttu-id="ba21e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ba21e-102">SYNOPSIS</span></span>
<span data-ttu-id="ba21e-103">Der Vorgang zum Erstellen einer Replikationsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="ba21e-103">The operation to create a replication policy</span></span>

## <span data-ttu-id="ba21e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba21e-104">SYNTAX</span></span>

```
New-AzMigrateReplicationPolicy -PolicyName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String>] [-ProviderSpecificInput <IPolicyProviderSpecificInput>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ba21e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ba21e-105">DESCRIPTION</span></span>
<span data-ttu-id="ba21e-106">Der Vorgang zum Erstellen einer Replikationsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="ba21e-106">The operation to create a replication policy</span></span>

## <span data-ttu-id="ba21e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ba21e-107">EXAMPLES</span></span>

### <span data-ttu-id="ba21e-108">Beispiel 1: Erstellen einer Replikationsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="ba21e-108">Example 1: Create a replication policy</span></span>
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

<span data-ttu-id="ba21e-109">Erstellt eine Richtlinie für VMware CBT</span><span class="sxs-lookup"><span data-stu-id="ba21e-109">Creates a policy for VmWare Cbt</span></span>

## <span data-ttu-id="ba21e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ba21e-110">PARAMETERS</span></span>

### <span data-ttu-id="ba21e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ba21e-111">-AsJob</span></span>
<span data-ttu-id="ba21e-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="ba21e-112">Run the command as a job</span></span>

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

### <span data-ttu-id="ba21e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba21e-113">-DefaultProfile</span></span>
<span data-ttu-id="ba21e-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ba21e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba21e-115">-Nowait</span><span class="sxs-lookup"><span data-stu-id="ba21e-115">-NoWait</span></span>
<span data-ttu-id="ba21e-116">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="ba21e-116">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ba21e-117">-Richtlinienname</span><span class="sxs-lookup"><span data-stu-id="ba21e-117">-PolicyName</span></span>
<span data-ttu-id="ba21e-118">Name der Replikationsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="ba21e-118">Replication policy name</span></span>

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

### <span data-ttu-id="ba21e-119">-ProviderSpecificInput</span><span class="sxs-lookup"><span data-stu-id="ba21e-119">-ProviderSpecificInput</span></span>
<span data-ttu-id="ba21e-120">Die ReplicationProviderSettings.</span><span class="sxs-lookup"><span data-stu-id="ba21e-120">The ReplicationProviderSettings.</span></span>
<span data-ttu-id="ba21e-121">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für PROVIDERSPECIFICINPUT-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="ba21e-121">To construct, see NOTES section for PROVIDERSPECIFICINPUT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ba21e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba21e-122">-ResourceGroupName</span></span>
<span data-ttu-id="ba21e-123">Der Name der Ressourcengruppe, in der der Vault für Wiederherstellungsdienste vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="ba21e-123">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="ba21e-124">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="ba21e-124">-ResourceName</span></span>
<span data-ttu-id="ba21e-125">Der Name des Speichers für Wiederherstellungsdienste.</span><span class="sxs-lookup"><span data-stu-id="ba21e-125">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="ba21e-126">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="ba21e-126">-SubscriptionId</span></span>
<span data-ttu-id="ba21e-127">Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="ba21e-127">The subscription Id.</span></span>

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

### <span data-ttu-id="ba21e-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ba21e-128">-Confirm</span></span>
<span data-ttu-id="ba21e-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ba21e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba21e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba21e-130">-WhatIf</span></span>
<span data-ttu-id="ba21e-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ba21e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba21e-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ba21e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba21e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba21e-133">CommonParameters</span></span>
<span data-ttu-id="ba21e-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba21e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba21e-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ba21e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba21e-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ba21e-136">INPUTS</span></span>

## <span data-ttu-id="ba21e-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ba21e-137">OUTPUTS</span></span>

### <span data-ttu-id="ba21e-138">Microsoft. Azure. PowerShell. Cmdlets. migrate. Models. Api20180110. iPolicy</span><span class="sxs-lookup"><span data-stu-id="ba21e-138">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicy</span></span>

## <span data-ttu-id="ba21e-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="ba21e-139">NOTES</span></span>

<span data-ttu-id="ba21e-140">Aliase</span><span class="sxs-lookup"><span data-stu-id="ba21e-140">ALIASES</span></span>

<span data-ttu-id="ba21e-141">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ba21e-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ba21e-142">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ba21e-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ba21e-143">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="ba21e-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ba21e-144">PROVIDERSPECIFICINPUT <IPolicyProviderSpecificInput> : ReplicationProviderSettings.</span><span class="sxs-lookup"><span data-stu-id="ba21e-144">PROVIDERSPECIFICINPUT <IPolicyProviderSpecificInput>: The ReplicationProviderSettings.</span></span>
  - <span data-ttu-id="ba21e-145">`[InstanceType <String>]`: Der Klassentyp.</span><span class="sxs-lookup"><span data-stu-id="ba21e-145">`[InstanceType <String>]`: The class type.</span></span>

## <span data-ttu-id="ba21e-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ba21e-146">RELATED LINKS</span></span>

