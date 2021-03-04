---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/set-azsynapsesqlpoolauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolAuditSetting.md
ms.openlocfilehash: 102d8f9e33a90d97cadb984a671797a89d6f3833
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939224"
---
# <span data-ttu-id="8e8af-101">Set-AzSynapseSqlPoolAuditSetting</span><span class="sxs-lookup"><span data-stu-id="8e8af-101">Set-AzSynapseSqlPoolAuditSetting</span></span>

## <span data-ttu-id="8e8af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e8af-102">SYNOPSIS</span></span>
<span data-ttu-id="8e8af-103">Ändert die Überwachungseinstellungen für einen Azure Synapse Analytics SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="8e8af-103">Changes the auditing settings for an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="8e8af-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8e8af-104">SYNTAX</span></span>

### <span data-ttu-id="8e8af-105">SetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="8e8af-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzSynapseSqlPoolAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-AuditActionGroup <AuditActionGroup[]>] [-AuditAction <String[]>] [-PredicateExpression <String>]
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e8af-106">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e8af-106">SetByParentObjectParameterSet</span></span>
```
Set-AzSynapseSqlPoolAuditSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-AuditActionGroup <AuditActionGroup[]>] [-AuditAction <String[]>] [-PredicateExpression <String>]
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e8af-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e8af-107">SetByInputObjectParameterSet</span></span>
```
Set-AzSynapseSqlPoolAuditSetting -InputObject <PSSynapseSqlPool> [-AuditActionGroup <AuditActionGroup[]>]
 [-AuditAction <String[]>] [-PredicateExpression <String>] [-BlobStorageTargetState <String>]
 [-StorageAccountResourceId <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e8af-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e8af-108">SetByResourceIdParameterSet</span></span>
```
Set-AzSynapseSqlPoolAuditSetting -ResourceId <String> [-AuditActionGroup <AuditActionGroup[]>]
 [-AuditAction <String[]>] [-PredicateExpression <String>] [-BlobStorageTargetState <String>]
 [-StorageAccountResourceId <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e8af-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8e8af-109">DESCRIPTION</span></span>
<span data-ttu-id="8e8af-110">Das **Cmdlet Set-AzSynapseSqlPoolAuditSetting** ändert die Überwachungseinstellungen eines Azure Synapse Analytics SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="8e8af-110">The **Set-AzSynapseSqlPoolAuditSetting** cmdlet changes the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>
<span data-ttu-id="8e8af-111">Wenn blob storage ein Ziel für Überwachungsprotokolle ist, geben Sie den *Parameter StorageAccountResourceId* an, um das Speicherkonto für die Überwachungsprotokolle und den *Parameter StorageKeyType* zum Definieren der Speicherschlüssel zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="8e8af-111">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="8e8af-112">Sie können auch die Aufbewahrung für die Überwachungsprotokolle definieren, indem Sie den Wert des *Parameters RetentionInDays* festlegen, um den Zeitraum für die Überwachungsprotokolle zu definieren.</span><span class="sxs-lookup"><span data-stu-id="8e8af-112">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

## <span data-ttu-id="8e8af-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8e8af-113">EXAMPLES</span></span>

### <span data-ttu-id="8e8af-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8e8af-114">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -StorageKeyType Primary
```

<span data-ttu-id="8e8af-115">Aktivieren Sie die Blobspeicherüberwachungsrichtlinie eines Azure Synapse Analytics SQL ContosoSqlPool.</span><span class="sxs-lookup"><span data-stu-id="8e8af-115">Enable the blob storage auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool.</span></span>

### <span data-ttu-id="8e8af-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="8e8af-116">Example 2</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BlobStorageTargetState Disabled
```

<span data-ttu-id="8e8af-117">Deaktivieren Sie die Blobspeicherüberwachungsrichtlinie eines Azure Synapse Analytics SQL ContosoSqlPool.</span><span class="sxs-lookup"><span data-stu-id="8e8af-117">Disable the blob storage auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool.</span></span>

### <span data-ttu-id="8e8af-118">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="8e8af-118">Example 3</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -StorageKeyType Primary -PredicateExpression "statement <> 'select 1'"
```

<span data-ttu-id="8e8af-119">Aktivieren Sie die Blobspeicherüberwachungsrichtlinie eines Azure Synapse Analytics SQL ContosoSqlPool mit erweiterter Filterung mithilfe eines T-SQL Prädikats.</span><span class="sxs-lookup"><span data-stu-id="8e8af-119">Enable the blob storage auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool with advanced filtering using a T-SQL predicate.</span></span>

### <span data-ttu-id="8e8af-120">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="8e8af-120">Example 4</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PredicateExpression ""
```

<span data-ttu-id="8e8af-121">Entfernen Sie die erweiterte Filtereinstellung aus der Überwachungsrichtlinie eines Azure Synapse Analytics SQL ContosoSqlPool.</span><span class="sxs-lookup"><span data-stu-id="8e8af-121">Remove the advanced filtering setting from the auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool.</span></span>

### <span data-ttu-id="8e8af-122">Beispiel 5</span><span class="sxs-lookup"><span data-stu-id="8e8af-122">Example 5</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Set-AzSynapseSqlPoolAuditSetting -BlobStorageTargetState Disabled
```

<span data-ttu-id="8e8af-123">Deaktivieren Sie die Blobspeicherüberwachungsrichtlinie eines Azure Synapse Analytics SQL ContosoSqlPool über die Pipeline.</span><span class="sxs-lookup"><span data-stu-id="8e8af-123">Disable the blob storage auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool through pipeline.</span></span>

## <span data-ttu-id="8e8af-124">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8e8af-124">PARAMETERS</span></span>

### <span data-ttu-id="8e8af-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8e8af-125">-AsJob</span></span>
<span data-ttu-id="8e8af-126">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="8e8af-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8e8af-127">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="8e8af-127">-AuditAction</span></span>
<span data-ttu-id="8e8af-128">Die Gruppe der Überwachungsaktionen.</span><span class="sxs-lookup"><span data-stu-id="8e8af-128">The set of audit actions.</span></span>

<span data-ttu-id="8e8af-129">Die unterstützten Aktionen zur Überwachung sind:</span><span class="sxs-lookup"><span data-stu-id="8e8af-129">The supported actions to audit are:</span></span>

<span data-ttu-id="8e8af-130">SELECT</span><span class="sxs-lookup"><span data-stu-id="8e8af-130">SELECT</span></span>

<span data-ttu-id="8e8af-131">UPDATE</span><span class="sxs-lookup"><span data-stu-id="8e8af-131">UPDATE</span></span>

<span data-ttu-id="8e8af-132">EINFÜGEN</span><span class="sxs-lookup"><span data-stu-id="8e8af-132">INSERT</span></span>

<span data-ttu-id="8e8af-133">LÖSCHEN</span><span class="sxs-lookup"><span data-stu-id="8e8af-133">DELETE</span></span>

<span data-ttu-id="8e8af-134">EXECUTE</span><span class="sxs-lookup"><span data-stu-id="8e8af-134">EXECUTE</span></span>

<span data-ttu-id="8e8af-135">RECEIVE</span><span class="sxs-lookup"><span data-stu-id="8e8af-135">RECEIVE</span></span>

<span data-ttu-id="8e8af-136">VERWEISE</span><span class="sxs-lookup"><span data-stu-id="8e8af-136">REFERENCES</span></span>

<span data-ttu-id="8e8af-137">Das allgemeine Formular zum Definieren einer zu überwachenden Aktion ist:</span><span class="sxs-lookup"><span data-stu-id="8e8af-137">The general form for defining an action to be audited is:</span></span>

<span data-ttu-id="8e8af-138">\[Aktion \] \[ ON-Objekt-BY-Prinzipal \] \[\]</span><span class="sxs-lookup"><span data-stu-id="8e8af-138">\[action\] ON \[object\] BY \[principal\]</span></span>

<span data-ttu-id="8e8af-139">Beachten Sie, dass sich ein Objekt im oben angegebenen Format auf ein Objekt wie eine Tabelle, eine Ansicht oder eine gespeicherte Prozedur oder eine \[ gesamte Datenbank oder ein \] gesamtes Schema beziehen kann.</span><span class="sxs-lookup"><span data-stu-id="8e8af-139">Note that \[object\] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span>
<span data-ttu-id="8e8af-140">In letzteren Fällen werden die Formulare DATABASE:: \[ dbname \] und SCHEMA:: \[ schemaname \] verwendet.</span><span class="sxs-lookup"><span data-stu-id="8e8af-140">For the latter cases, the forms DATABASE::\[dbname\] and SCHEMA::\[schemaname\] are used, respectively.</span></span>

<span data-ttu-id="8e8af-141">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="8e8af-141">For example:</span></span>

<span data-ttu-id="8e8af-142">SELECT on dbo.myTable by public</span><span class="sxs-lookup"><span data-stu-id="8e8af-142">SELECT on dbo.myTable by public</span></span>

<span data-ttu-id="8e8af-143">SELECT on DATABASE::myDatabase by public</span><span class="sxs-lookup"><span data-stu-id="8e8af-143">SELECT on DATABASE::myDatabase by public</span></span>

<span data-ttu-id="8e8af-144">SELECT on SCHEMA::mySchema by public</span><span class="sxs-lookup"><span data-stu-id="8e8af-144">SELECT on SCHEMA::mySchema by public</span></span>

<span data-ttu-id="8e8af-145">Weitere Informationen finden Sie unter https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions .</span><span class="sxs-lookup"><span data-stu-id="8e8af-145">For more information, see https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e8af-146">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="8e8af-146">-AuditActionGroup</span></span>
<span data-ttu-id="8e8af-147">Die empfohlene Gruppe von Aktionsgruppen ist die folgende Kombination: Dadurch werden alle Abfragen und gespeicherten Prozeduren überwacht, die für die Datenbank ausgeführt werden, sowie erfolgreiche und fehlgeschlagene Anmeldungen:</span><span class="sxs-lookup"><span data-stu-id="8e8af-147">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>



<span data-ttu-id="8e8af-148">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="8e8af-148">"BATCH_COMPLETED_GROUP",</span></span>

<span data-ttu-id="8e8af-149">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="8e8af-149">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>

<span data-ttu-id="8e8af-150">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="8e8af-150">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>

<span data-ttu-id="8e8af-151">Diese obige Kombination ist auch der Satz, der standardmäßig konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="8e8af-151">This above combination is also the set that is configured by default.</span></span>
<span data-ttu-id="8e8af-152">Diese Gruppen decken alle SQL und gespeicherten Prozeduren ab, die für die Datenbank ausgeführt werden, und sollten nicht in Kombination mit anderen Gruppen verwendet werden, da dies zu doppelten Überwachungsprotokollen führt.</span><span class="sxs-lookup"><span data-stu-id="8e8af-152">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>

<span data-ttu-id="8e8af-153">Weitere Informationen finden Sie unter https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="8e8af-153">For more information, see https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="8e8af-154">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="8e8af-154">-BlobStorageTargetState</span></span>
<span data-ttu-id="8e8af-155">Gibt an, ob blob storage ein Ziel für Überwachungsdatensätze ist.</span><span class="sxs-lookup"><span data-stu-id="8e8af-155">Indicates whether blob storage is a destination for audit records.</span></span>

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

### <span data-ttu-id="8e8af-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e8af-156">-DefaultProfile</span></span>
<span data-ttu-id="8e8af-157">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8e8af-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e8af-158">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8e8af-158">-InputObject</span></span>
<span data-ttu-id="8e8af-159">SQL -Pooleingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="8e8af-159">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e8af-160">-Name</span><span class="sxs-lookup"><span data-stu-id="8e8af-160">-Name</span></span>
<span data-ttu-id="8e8af-161">Name des Synapse SQL Pools.</span><span class="sxs-lookup"><span data-stu-id="8e8af-161">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet, SetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e8af-162">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8e8af-162">-PassThru</span></span>
<span data-ttu-id="8e8af-163">Dieses Cmdlet gibt standardmäßig kein -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="8e8af-163">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="8e8af-164">Wenn dieser Schalter angegeben ist, gibt er "true" zurück, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="8e8af-164">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="8e8af-165">-PrädikateExpression</span><span class="sxs-lookup"><span data-stu-id="8e8af-165">-PredicateExpression</span></span>
<span data-ttu-id="8e8af-166">Das T-SQL -Prädikat (WHERE-Klausel), das zum Filtern von Überwachungsprotokollen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8e8af-166">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="8e8af-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e8af-167">-ResourceGroupName</span></span>
<span data-ttu-id="8e8af-168">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8e8af-168">Resource group name.</span></span>

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

### <span data-ttu-id="8e8af-169">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e8af-169">-ResourceId</span></span>
<span data-ttu-id="8e8af-170">Ressourcenbezeichner von Synapse SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="8e8af-170">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="8e8af-171">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="8e8af-171">-RetentionInDays</span></span>
<span data-ttu-id="8e8af-172">Die Anzahl der Aufbewahrungstage für die Überwachungsprotokolle.</span><span class="sxs-lookup"><span data-stu-id="8e8af-172">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="8e8af-173">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="8e8af-173">-StorageAccountResourceId</span></span>
<span data-ttu-id="8e8af-174">Ressourcen-ID des Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="8e8af-174">The storage account resource id</span></span>

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

### <span data-ttu-id="8e8af-175">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="8e8af-175">-StorageKeyType</span></span>
<span data-ttu-id="8e8af-176">Gibt an, welcher der Speicherzugriffsschlüssel verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8e8af-176">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="8e8af-177">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8e8af-177">-WorkspaceName</span></span>
<span data-ttu-id="8e8af-178">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="8e8af-178">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="8e8af-179">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="8e8af-179">-WorkspaceObject</span></span>
<span data-ttu-id="8e8af-180">Arbeitsbereichseingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="8e8af-180">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e8af-181">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8e8af-181">-Confirm</span></span>
<span data-ttu-id="8e8af-182">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8e8af-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e8af-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e8af-183">-WhatIf</span></span>
<span data-ttu-id="8e8af-184">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8e8af-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e8af-185">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8e8af-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e8af-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e8af-186">CommonParameters</span></span>
<span data-ttu-id="8e8af-187">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e8af-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e8af-188">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8e8af-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e8af-189">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8e8af-189">INPUTS</span></span>

### <span data-ttu-id="8e8af-190">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="8e8af-190">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="8e8af-191">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="8e8af-191">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="8e8af-192">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8e8af-192">OUTPUTS</span></span>

### <span data-ttu-id="8e8af-193">Microsoft.Azure.Commands.Synapse.Models.SqlPoolAuditModel</span><span class="sxs-lookup"><span data-stu-id="8e8af-193">Microsoft.Azure.Commands.Synapse.Models.SqlPoolAuditModel</span></span>

## <span data-ttu-id="8e8af-194">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8e8af-194">NOTES</span></span>

## <span data-ttu-id="8e8af-195">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8e8af-195">RELATED LINKS</span></span>
