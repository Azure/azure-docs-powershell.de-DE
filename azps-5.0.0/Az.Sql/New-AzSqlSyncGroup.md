---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncGroup.md
ms.openlocfilehash: d6964f076dd1e6882a8031f19101f55d19b9e4d4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176857"
---
# <span data-ttu-id="640af-101">New-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="640af-101">New-AzSqlSyncGroup</span></span>

## <span data-ttu-id="640af-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="640af-102">SYNOPSIS</span></span>
<span data-ttu-id="640af-103">Erstellt eine Azure SQL-Daten Bank Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="640af-103">Creates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="640af-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="640af-104">SYNTAX</span></span>

```
New-AzSqlSyncGroup [-Name] <String> -SyncDatabaseName <String> -SyncDatabaseServerName <String>
 -SyncDatabaseResourceGroupName <String> [-IntervalInSeconds <Int32>] [-DatabaseCredential <PSCredential>]
 [-ConflictResolutionPolicy <String>] [-SchemaFile <String>] [-UsePrivateLinkConnection] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="640af-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="640af-105">DESCRIPTION</span></span>
<span data-ttu-id="640af-106">Das Cmdlet **New-AzSqlSyncGroup** erstellt eine Azure SQL-Daten Bank Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="640af-106">The **New-AzSqlSyncGroup** cmdlet creates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="640af-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="640af-107">EXAMPLES</span></span>

### <span data-ttu-id="640af-108">Beispiel 1: Erstellen einer Synchronisierungsgruppe für eine Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="640af-108">Example 1: Create a sync group for an Azure SQL Database.</span></span>
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

<span data-ttu-id="640af-109">Mit diesem Befehl wird eine Synchronisierungsgruppe für eine Azure SQL-Datenbank erstellt.</span><span class="sxs-lookup"><span data-stu-id="640af-109">This command creates a sync group for an Azure SQL Database.</span></span> <span data-ttu-id="640af-110">"schema.jsein" ist eine Datei auf dem lokalen Datenträger.</span><span class="sxs-lookup"><span data-stu-id="640af-110">"schema.json" is a file in the local disk.</span></span> <span data-ttu-id="640af-111">Sie enthält die Schema Nutzlast im JSON-Format.</span><span class="sxs-lookup"><span data-stu-id="640af-111">It contains the schema payload in json format.</span></span> <span data-ttu-id="640af-112">Ein Beispiel für das JSON-Schema ist: {"Tabellen": [{"Columns": [{"QUOTENAME": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column1"}, {"QUOTENAME": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column2"}]; "QUOTENAME": "MayQuotedTable1"}, {"Columns": [{"QUOTENAME": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column1"}, {"QUOTENAME": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column2"}], "QUOTENAME": "MayQuotedTable2"}], "MasterSyncMemberName": NULL}</span><span class="sxs-lookup"><span data-stu-id="640af-112">An example of the schema json is: {"Tables":  [{"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable1"}, {"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable2"}], "MasterSyncMemberName":  null }</span></span>

## <span data-ttu-id="640af-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="640af-113">PARAMETERS</span></span>

### <span data-ttu-id="640af-114">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="640af-114">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="640af-115">Die Richtlinie zum Beheben von Konflikten zwischen Hub-und Mitgliedsdatenbank in der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="640af-115">The policy of resolving conflicts between hub and member database in the sync group.</span></span>

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

### <span data-ttu-id="640af-116">-DatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="640af-116">-DatabaseCredential</span></span>
<span data-ttu-id="640af-117">Die SQL-Authentifizierungsanmeldeinformationen der Hub-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="640af-117">The SQL authentication credential of the hub database.</span></span>

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

### <span data-ttu-id="640af-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="640af-118">-DatabaseName</span></span>
<span data-ttu-id="640af-119">Der Name der Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="640af-119">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="640af-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="640af-120">-DefaultProfile</span></span>
<span data-ttu-id="640af-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="640af-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="640af-122">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="640af-122">-IntervalInSeconds</span></span>
<span data-ttu-id="640af-123">Die Häufigkeit (in Sekunden) der Datensynchronisierung.</span><span class="sxs-lookup"><span data-stu-id="640af-123">The frequency (in seconds) of doing data synchronization.</span></span>
<span data-ttu-id="640af-124">Der Standardwert ist-1, was bedeutet, dass die automatische Synchronisierung nicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="640af-124">Default is -1, which means the auto synchronization is not enabled.</span></span>

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

### <span data-ttu-id="640af-125">-Name</span><span class="sxs-lookup"><span data-stu-id="640af-125">-Name</span></span>
<span data-ttu-id="640af-126">Der Name der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="640af-126">The sync group name.</span></span>

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

### <span data-ttu-id="640af-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="640af-127">-ResourceGroupName</span></span>
<span data-ttu-id="640af-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="640af-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="640af-129">-Schemadatei</span><span class="sxs-lookup"><span data-stu-id="640af-129">-SchemaFile</span></span>
<span data-ttu-id="640af-130">Der Pfad der Schemadatei.</span><span class="sxs-lookup"><span data-stu-id="640af-130">The path of the schema file.</span></span>

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

### <span data-ttu-id="640af-131">-Servername</span><span class="sxs-lookup"><span data-stu-id="640af-131">-ServerName</span></span>
<span data-ttu-id="640af-132">Der Name des Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="640af-132">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="640af-133">-SyncDatabaseName</span><span class="sxs-lookup"><span data-stu-id="640af-133">-SyncDatabaseName</span></span>
<span data-ttu-id="640af-134">Die Datenbank, die zum Speichern von Synchronisierungs bezogenen Metadaten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="640af-134">The database used to store sync related metadata.</span></span>

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

### <span data-ttu-id="640af-135">-SyncDatabaseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="640af-135">-SyncDatabaseResourceGroupName</span></span>
<span data-ttu-id="640af-136">Die Ressourcengruppe, zu der die Synchronisierungsmetadaten-Datenbank gehört.</span><span class="sxs-lookup"><span data-stu-id="640af-136">The resource group the sync metadata database belongs to.</span></span>

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

### <span data-ttu-id="640af-137">-SyncDatabaseServerName</span><span class="sxs-lookup"><span data-stu-id="640af-137">-SyncDatabaseServerName</span></span>
<span data-ttu-id="640af-138">Der Server, auf dem die Synchronisierungsmetadaten-Datenbank gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="640af-138">The server on which the sync metadata database is hosted.</span></span>

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

### <span data-ttu-id="640af-139">-UsePrivateLinkConnection</span><span class="sxs-lookup"><span data-stu-id="640af-139">-UsePrivateLinkConnection</span></span>
<span data-ttu-id="640af-140">Verwenden Sie eine private Link Verbindung beim Herstellen einer Verbindung mit dem Hub dieser Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="640af-140">Use a private link connection when connecting to the hub of this sync group.</span></span>

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

### <span data-ttu-id="640af-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="640af-141">-Confirm</span></span>
<span data-ttu-id="640af-142">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="640af-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="640af-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="640af-143">-WhatIf</span></span>
<span data-ttu-id="640af-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="640af-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="640af-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="640af-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="640af-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="640af-146">CommonParameters</span></span>
<span data-ttu-id="640af-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="640af-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="640af-148">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="640af-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="640af-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="640af-149">INPUTS</span></span>

### <span data-ttu-id="640af-150">System. String</span><span class="sxs-lookup"><span data-stu-id="640af-150">System.String</span></span>

## <span data-ttu-id="640af-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="640af-151">OUTPUTS</span></span>

### <span data-ttu-id="640af-152">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="640af-152">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="640af-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="640af-153">NOTES</span></span>

## <span data-ttu-id="640af-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="640af-154">RELATED LINKS</span></span>

[<span data-ttu-id="640af-155">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="640af-155">Update-AzSqlSyncGroup</span></span>](./Update-AzSqlSyncGroup.md)

[<span data-ttu-id="640af-156">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="640af-156">Remove-AzSqlSyncGroup</span></span>](./Remove-AzSqlSyncGroup.md)

[<span data-ttu-id="640af-157">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="640af-157">Get-AzSqlSyncGroup</span></span>](./Get-AzSqlSyncGroup.md)

