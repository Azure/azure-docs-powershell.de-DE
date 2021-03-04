---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/set-azsynapsesqlauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlAuditSetting.md
ms.openlocfilehash: 15d553800aa51bdf4752902dadd8d5b15fcdf2f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939232"
---
# <span data-ttu-id="a1779-101">Set-AzSynapseSqlAuditSetting</span><span class="sxs-lookup"><span data-stu-id="a1779-101">Set-AzSynapseSqlAuditSetting</span></span>

## <span data-ttu-id="a1779-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1779-102">SYNOPSIS</span></span>
<span data-ttu-id="a1779-103">Ändert die Überwachungseinstellungen eines Azure Synapse Analytics-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="a1779-103">Changes the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="a1779-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a1779-104">SYNTAX</span></span>

### <span data-ttu-id="a1779-105">SetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a1779-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzSynapseSqlAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-AuditActionGroup <AuditActionGroup[]>] [-PredicateExpression <String>] [-BlobStorageTargetState <String>]
 [-StorageAccountResourceId <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1779-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1779-106">SetByInputObjectParameterSet</span></span>
```
Set-AzSynapseSqlAuditSetting -InputObject <PSSynapseWorkspace> [-AuditActionGroup <AuditActionGroup[]>]
 [-PredicateExpression <String>] [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1779-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1779-107">SetByResourceIdParameterSet</span></span>
```
Set-AzSynapseSqlAuditSetting -ResourceId <String> [-AuditActionGroup <AuditActionGroup[]>]
 [-PredicateExpression <String>] [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1779-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a1779-108">DESCRIPTION</span></span>
<span data-ttu-id="a1779-109">Das **Cmdlet Set-AzSynapseSqlAuditSetting** ändert die Überwachungseinstellungen eines Azure Synapse Analytics Workspace.</span><span class="sxs-lookup"><span data-stu-id="a1779-109">The **Set-AzSynapseSqlAuditSetting** cmdlet changes the auditing settings of an Azure Synapse Analytics Workspace.</span></span>
<span data-ttu-id="a1779-110">Wenn blob storage ein Ziel für Überwachungsprotokolle ist, geben Sie den *Parameter StorageAccountResourceId* an, um das Speicherkonto für die Überwachungsprotokolle und den *Parameter StorageKeyType* zum Definieren der Speicherschlüssel zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="a1779-110">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="a1779-111">Sie können auch die Aufbewahrung für die Überwachungsprotokolle definieren, indem Sie den Wert des *Parameters RetentionInDays* festlegen, um den Zeitraum für die Überwachungsprotokolle zu definieren.</span><span class="sxs-lookup"><span data-stu-id="a1779-111">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

## <span data-ttu-id="a1779-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a1779-112">EXAMPLES</span></span>

### <span data-ttu-id="a1779-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a1779-113">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -StorageKeyType Primary
```

<span data-ttu-id="a1779-114">Aktivieren Sie die Blobspeicherüberwachungsrichtlinie eines Azure Synapse Analytics-Arbeitsbereichs mit dem Namen ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="a1779-114">Enable the blob storage auditing policy of an Azure Synapse Analytics Workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="a1779-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a1779-115">Example 2</span></span>
```powershell
PS C:\> Set-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace -BlobStorageTargetState Disabled
```

<span data-ttu-id="a1779-116">Deaktivieren Sie die Blobspeicherüberwachungsrichtlinie eines Azure Synapse Analytics-Arbeitsbereichs namens ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="a1779-116">Disable the blob storage auditing policy of an Azure Synapse Analytics Workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="a1779-117">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="a1779-117">Example 3</span></span>
```powershell
PS C:\> Set-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -StorageKeyType Primary -PredicateExpression "statement <> 'select 1'"
```

<span data-ttu-id="a1779-118">Aktivieren Sie die Blobspeicherüberwachungsrichtlinie eines Azure Synapse Analytics Workspace namens ContosoWorkspace mit erweiterter Filterung mithilfe eines T-SQL Prädikats.</span><span class="sxs-lookup"><span data-stu-id="a1779-118">Enable the blob storage auditing policy of an Azure Synapse Analytics Workspace named ContosoWorkspace with advanced filtering using a T-SQL predicate.</span></span>

### <span data-ttu-id="a1779-119">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="a1779-119">Example 4</span></span>
```powershell
PS C:\> Set-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace -PredicateExpression ""
```

<span data-ttu-id="a1779-120">Entfernen Sie die erweiterte Filtereinstellung aus der Überwachungsrichtlinie eines Azure Synapse Analytics-Arbeitsbereichs mit dem Namen ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="a1779-120">Remove the advanced filtering setting from the auditing policy of an Azure Synapse Analytics Workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="a1779-121">Beispiel 5</span><span class="sxs-lookup"><span data-stu-id="a1779-121">Example 5</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Set-AzSynapseSqlAuditSetting -BlobStorageTargetState Disabled
```

<span data-ttu-id="a1779-122">Deaktivieren Sie die Blobspeicherüberwachungsrichtlinie eines Azure Synapse Analytics-Arbeitsbereichs namens ContosoWorkspace über die Pipeline.</span><span class="sxs-lookup"><span data-stu-id="a1779-122">Disable the blob storage auditing policy of an Azure Synapse Analytics Workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="a1779-123">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a1779-123">PARAMETERS</span></span>

### <span data-ttu-id="a1779-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a1779-124">-AsJob</span></span>
<span data-ttu-id="a1779-125">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a1779-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a1779-126">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="a1779-126">-AuditActionGroup</span></span>
<span data-ttu-id="a1779-127">Die empfohlene Gruppe von Aktionsgruppen ist die folgende Kombination: Dadurch werden alle Abfragen und gespeicherten Prozeduren überwacht, die für die Datenbank ausgeführt werden, sowie erfolgreiche und fehlgeschlagene Anmeldungen:</span><span class="sxs-lookup"><span data-stu-id="a1779-127">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>



<span data-ttu-id="a1779-128">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="a1779-128">"BATCH_COMPLETED_GROUP",</span></span>

<span data-ttu-id="a1779-129">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="a1779-129">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>

<span data-ttu-id="a1779-130">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="a1779-130">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>

<span data-ttu-id="a1779-131">Diese obige Kombination ist auch der Satz, der standardmäßig konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="a1779-131">This above combination is also the set that is configured by default.</span></span>
<span data-ttu-id="a1779-132">Diese Gruppen decken alle SQL und gespeicherten Prozeduren ab, die für die Datenbank ausgeführt werden, und sollten nicht in Kombination mit anderen Gruppen verwendet werden, da dies zu doppelten Überwachungsprotokollen führt.</span><span class="sxs-lookup"><span data-stu-id="a1779-132">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>

<span data-ttu-id="a1779-133">Weitere Informationen finden Sie unter https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="a1779-133">For more information, see https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.AuditActionGroup[]
Parameter Sets: (All)
Aliases:
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1779-134">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="a1779-134">-BlobStorageTargetState</span></span>
<span data-ttu-id="a1779-135">Gibt an, ob blob storage ein Ziel für Überwachungsdatensätze ist.</span><span class="sxs-lookup"><span data-stu-id="a1779-135">Indicates whether blob storage is a destination for audit records.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1779-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1779-136">-DefaultProfile</span></span>
<span data-ttu-id="a1779-137">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a1779-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1779-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a1779-138">-InputObject</span></span>
<span data-ttu-id="a1779-139">Arbeitsbereichseingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="a1779-139">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1779-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a1779-140">-PassThru</span></span>
<span data-ttu-id="a1779-141">Dieses Cmdlet gibt standardmäßig kein -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="a1779-141">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="a1779-142">Wenn dieser Schalter angegeben ist, gibt er "true" zurück, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="a1779-142">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="a1779-143">-PrädikateExpression</span><span class="sxs-lookup"><span data-stu-id="a1779-143">-PredicateExpression</span></span>
<span data-ttu-id="a1779-144">Das T-SQL -Prädikat (WHERE-Klausel), das zum Filtern von Überwachungsprotokollen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a1779-144">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="a1779-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1779-145">-ResourceGroupName</span></span>
<span data-ttu-id="a1779-146">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a1779-146">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1779-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1779-147">-ResourceId</span></span>
<span data-ttu-id="a1779-148">Ressourcenbezeichner des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="a1779-148">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1779-149">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="a1779-149">-RetentionInDays</span></span>
<span data-ttu-id="a1779-150">Die Anzahl der Aufbewahrungstage für die Überwachungsprotokolle.</span><span class="sxs-lookup"><span data-stu-id="a1779-150">The number of retention days for the audit logs.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1779-151">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="a1779-151">-StorageAccountResourceId</span></span>
<span data-ttu-id="a1779-152">Ressourcen-ID des Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="a1779-152">The storage account resource id</span></span>

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

### <span data-ttu-id="a1779-153">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="a1779-153">-StorageKeyType</span></span>
<span data-ttu-id="a1779-154">Gibt an, welcher der Speicherzugriffsschlüssel verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a1779-154">Specifies which of the storage access keys to use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1779-155">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a1779-155">-WorkspaceName</span></span>
<span data-ttu-id="a1779-156">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="a1779-156">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1779-157">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a1779-157">-Confirm</span></span>
<span data-ttu-id="a1779-158">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a1779-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1779-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1779-159">-WhatIf</span></span>
<span data-ttu-id="a1779-160">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a1779-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1779-161">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a1779-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1779-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1779-162">CommonParameters</span></span>
<span data-ttu-id="a1779-163">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1779-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1779-164">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a1779-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1779-165">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a1779-165">INPUTS</span></span>

### <span data-ttu-id="a1779-166">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a1779-166">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="a1779-167">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a1779-167">OUTPUTS</span></span>

### <span data-ttu-id="a1779-168">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAuditModel</span><span class="sxs-lookup"><span data-stu-id="a1779-168">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAuditModel</span></span>

## <span data-ttu-id="a1779-169">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a1779-169">NOTES</span></span>

## <span data-ttu-id="a1779-170">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a1779-170">RELATED LINKS</span></span>
