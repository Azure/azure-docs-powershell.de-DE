---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncGroup.md
ms.openlocfilehash: d6964f076dd1e6882a8031f19101f55d19b9e4d4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145596"
---
# <span data-ttu-id="90950-101">New-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="90950-101">New-AzSqlSyncGroup</span></span>

## <span data-ttu-id="90950-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90950-102">SYNOPSIS</span></span>
<span data-ttu-id="90950-103">Erstellt eine Azure SQL-Datenbanksynchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="90950-103">Creates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="90950-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="90950-104">SYNTAX</span></span>

```
New-AzSqlSyncGroup [-Name] <String> -SyncDatabaseName <String> -SyncDatabaseServerName <String>
 -SyncDatabaseResourceGroupName <String> [-IntervalInSeconds <Int32>] [-DatabaseCredential <PSCredential>]
 [-ConflictResolutionPolicy <String>] [-SchemaFile <String>] [-UsePrivateLinkConnection] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90950-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="90950-105">DESCRIPTION</span></span>
<span data-ttu-id="90950-106">Das **Cmdlet "New-AzSqlSyncGroup"** erstellt eine Azure SQL Database Sync Group.</span><span class="sxs-lookup"><span data-stu-id="90950-106">The **New-AzSqlSyncGroup** cmdlet creates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="90950-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="90950-107">EXAMPLES</span></span>

### <span data-ttu-id="90950-108">Beispiel 1: Erstellen einer Synchronisierungsgruppe für eine Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="90950-108">Example 1: Create a sync group for an Azure SQL Database.</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> New-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup01" -ConflictResolutionPolicy "HubWin"
-DatabaseCredential $credential -IntervalInSeconds 100 -SyncDatabaseServerName "syncDatabaseServer01" -SyncDatabaseName "syncDatabaseName01"
-SyncDatabaseResourceGroupName "syncDatabaseResourceGroup01" -Schema ".\schema.json" | Format-List
ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
IntervalInSeconds           : 100
ConflictResolutionPolicy:   : HubWin
HubDatabaseUserName         : myAccount
HubDatabasePassword         : 
SyncState                   : NotReady
LastSyncTime                : 1/1/0001 12:00:00 AM
Schema                      :
```

<span data-ttu-id="90950-109">Mit diesem Befehl wird eine Synchronisierungsgruppe für eine Azure SQL erstellt.</span><span class="sxs-lookup"><span data-stu-id="90950-109">This command creates a sync group for an Azure SQL Database.</span></span> <span data-ttu-id="90950-110">"schema.jsein" ist eine Datei auf dem lokalen Datenträger.</span><span class="sxs-lookup"><span data-stu-id="90950-110">"schema.json" is a file in the local disk.</span></span> <span data-ttu-id="90950-111">Sie enthält die Schemanutzlast im json-Format.</span><span class="sxs-lookup"><span data-stu-id="90950-111">It contains the schema payload in json format.</span></span> <span data-ttu-id="90950-112">Beispiel für das Schema json: {"Tables": [{"Columns": [{"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable1"}, {"Columns": [{"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable2"}], "MasterSyncMemberName": null }</span><span class="sxs-lookup"><span data-stu-id="90950-112">An example of the schema json is: {"Tables":  [{"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable1"}, {"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable2"}], "MasterSyncMemberName":  null }</span></span>

## <span data-ttu-id="90950-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="90950-113">PARAMETERS</span></span>

### <span data-ttu-id="90950-114">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="90950-114">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="90950-115">Die Richtlinie zum Auflösen von Konflikten zwischen Hub- und Mitgliederdatenbank in der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="90950-115">The policy of resolving conflicts between hub and member database in the sync group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: HubWin, MemberWin

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90950-116">-DatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="90950-116">-DatabaseCredential</span></span>
<span data-ttu-id="90950-117">Die SQL A0 der Hubdatenbank.</span><span class="sxs-lookup"><span data-stu-id="90950-117">The SQL authentication credential of the hub database.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90950-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="90950-118">-DatabaseName</span></span>
<span data-ttu-id="90950-119">Der Name der Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="90950-119">The name of the Azure SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90950-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90950-120">-DefaultProfile</span></span>
<span data-ttu-id="90950-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="90950-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="90950-122">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="90950-122">-IntervalInSeconds</span></span>
<span data-ttu-id="90950-123">Die Häufigkeit (in Sekunden) der Datensynchronisierung.</span><span class="sxs-lookup"><span data-stu-id="90950-123">The frequency (in seconds) of doing data synchronization.</span></span>
<span data-ttu-id="90950-124">Der Standardwert ist -1, d. h., die automatische Synchronisierung ist nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="90950-124">Default is -1, which means the auto synchronization is not enabled.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90950-125">-Name</span><span class="sxs-lookup"><span data-stu-id="90950-125">-Name</span></span>
<span data-ttu-id="90950-126">Der Name der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="90950-126">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90950-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90950-127">-ResourceGroupName</span></span>
<span data-ttu-id="90950-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="90950-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90950-129">-SchemaFile</span><span class="sxs-lookup"><span data-stu-id="90950-129">-SchemaFile</span></span>
<span data-ttu-id="90950-130">Der Pfad der Schemadatei.</span><span class="sxs-lookup"><span data-stu-id="90950-130">The path of the schema file.</span></span>

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

### <span data-ttu-id="90950-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="90950-131">-ServerName</span></span>
<span data-ttu-id="90950-132">Der Name des Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="90950-132">The name of the Azure SQL Server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90950-133">-SyncDatabaseName</span><span class="sxs-lookup"><span data-stu-id="90950-133">-SyncDatabaseName</span></span>
<span data-ttu-id="90950-134">Die Datenbank, die zum Speichern von Synchronisierungsmetadaten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="90950-134">The database used to store sync related metadata.</span></span>

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

### <span data-ttu-id="90950-135">-SyncDatabaseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90950-135">-SyncDatabaseResourceGroupName</span></span>
<span data-ttu-id="90950-136">Die Ressourcengruppe, zu der die Synchronisierungsmetadatendatenbank gehört.</span><span class="sxs-lookup"><span data-stu-id="90950-136">The resource group the sync metadata database belongs to.</span></span>

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

### <span data-ttu-id="90950-137">-SyncDatabaseServerName</span><span class="sxs-lookup"><span data-stu-id="90950-137">-SyncDatabaseServerName</span></span>
<span data-ttu-id="90950-138">Der Server, auf dem die Synchronisierungsmetadatendatenbank gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="90950-138">The server on which the sync metadata database is hosted.</span></span>

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

### <span data-ttu-id="90950-139">-UsePrivateLinkConnection</span><span class="sxs-lookup"><span data-stu-id="90950-139">-UsePrivateLinkConnection</span></span>
<span data-ttu-id="90950-140">Verwenden Sie eine private Linkverbindung, wenn Sie eine Verbindung mit dem Hub dieser Synchronisierungsgruppe herstellen.</span><span class="sxs-lookup"><span data-stu-id="90950-140">Use a private link connection when connecting to the hub of this sync group.</span></span>

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

### <span data-ttu-id="90950-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="90950-141">-Confirm</span></span>
<span data-ttu-id="90950-142">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="90950-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90950-143">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="90950-143">-WhatIf</span></span>
<span data-ttu-id="90950-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="90950-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90950-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="90950-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90950-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90950-146">CommonParameters</span></span>
<span data-ttu-id="90950-147">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90950-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90950-148">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="90950-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90950-149">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="90950-149">INPUTS</span></span>

### <span data-ttu-id="90950-150">System.String</span><span class="sxs-lookup"><span data-stu-id="90950-150">System.String</span></span>

## <span data-ttu-id="90950-151">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="90950-151">OUTPUTS</span></span>

### <span data-ttu-id="90950-152">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="90950-152">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="90950-153">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="90950-153">NOTES</span></span>

## <span data-ttu-id="90950-154">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="90950-154">RELATED LINKS</span></span>

[<span data-ttu-id="90950-155">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="90950-155">Update-AzSqlSyncGroup</span></span>](./Update-AzSqlSyncGroup.md)

[<span data-ttu-id="90950-156">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="90950-156">Remove-AzSqlSyncGroup</span></span>](./Remove-AzSqlSyncGroup.md)

[<span data-ttu-id="90950-157">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="90950-157">Get-AzSqlSyncGroup</span></span>](./Get-AzSqlSyncGroup.md)

