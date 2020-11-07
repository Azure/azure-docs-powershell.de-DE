---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncGroup.md
ms.openlocfilehash: 512ed43ac1770a7a1a026c5a64d20a25016d547e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659077"
---
# <span data-ttu-id="5bd34-101">New-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="5bd34-101">New-AzSqlSyncGroup</span></span>

## <span data-ttu-id="5bd34-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5bd34-102">SYNOPSIS</span></span>
<span data-ttu-id="5bd34-103">Erstellt eine Azure SQL-Daten Bank Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="5bd34-103">Creates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="5bd34-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5bd34-104">SYNTAX</span></span>

```
New-AzSqlSyncGroup [-Name] <String> -SyncDatabaseName <String> -SyncDatabaseServerName <String>
 -SyncDatabaseResourceGroupName <String> [-IntervalInSeconds <Int32>] [-DatabaseCredential <PSCredential>]
 [-ConflictResolutionPolicy <String>] [-SchemaFile <String>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5bd34-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5bd34-105">DESCRIPTION</span></span>
<span data-ttu-id="5bd34-106">Das Cmdlet **New-AzSqlSyncGroup** erstellt eine Azure SQL-Daten Bank Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="5bd34-106">The **New-AzSqlSyncGroup** cmdlet creates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="5bd34-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5bd34-107">EXAMPLES</span></span>

### <span data-ttu-id="5bd34-108">Beispiel 1: Erstellen einer Synchronisierungsgruppe für eine Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="5bd34-108">Example 1: Create a sync group for an Azure SQL Database.</span></span>
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

<span data-ttu-id="5bd34-109">Mit diesem Befehl wird eine Synchronisierungsgruppe für eine Azure SQL-Datenbank erstellt.</span><span class="sxs-lookup"><span data-stu-id="5bd34-109">This command creates a sync group for an Azure SQL Database.</span></span> <span data-ttu-id="5bd34-110">"schema.jsein" ist eine Datei auf dem lokalen Datenträger.</span><span class="sxs-lookup"><span data-stu-id="5bd34-110">"schema.json" is a file in the local disk.</span></span> <span data-ttu-id="5bd34-111">Sie enthält die Shma-Nutzlast im JSON-Format.</span><span class="sxs-lookup"><span data-stu-id="5bd34-111">It contains the shema payload in json format.</span></span> <span data-ttu-id="5bd34-112">Ein Beispiel für das JSON-Schema ist: {"Tabellen": [{"Columns": [{"QUOTENAME": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column1"}, {"QUOTENAME": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column2"}]; "QUOTENAME": "MayQuotedTable1"}, {"Columns": [{"QUOTENAME": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column1"}, {"QUOTENAME": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column2"}], "QUOTENAME": "MayQuotedTable2"}], "MasterSyncMemberName": NULL}</span><span class="sxs-lookup"><span data-stu-id="5bd34-112">An example of the schema json is: {"Tables":  [{"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable1"}, {"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable2"}], "MasterSyncMemberName":  null }</span></span>

## <span data-ttu-id="5bd34-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="5bd34-113">PARAMETERS</span></span>

### <span data-ttu-id="5bd34-114">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="5bd34-114">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="5bd34-115">Die Richtlinie zum Auflösen von Konflikten zwischen Hub-und Mitgliedsdatenbank in der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="5bd34-115">The policy of resolving confliction between hub and member database in the sync group.</span></span>

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

### <span data-ttu-id="5bd34-116">-DatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="5bd34-116">-DatabaseCredential</span></span>
<span data-ttu-id="5bd34-117">Die SQL-Authentifizierungsanmeldeinformationen der Hub-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="5bd34-117">The SQL authentication credential of the hub database.</span></span>

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

### <span data-ttu-id="5bd34-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5bd34-118">-DatabaseName</span></span>
<span data-ttu-id="5bd34-119">Der Name der Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="5bd34-119">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="5bd34-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bd34-120">-DefaultProfile</span></span>
<span data-ttu-id="5bd34-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="5bd34-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5bd34-122">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="5bd34-122">-IntervalInSeconds</span></span>
<span data-ttu-id="5bd34-123">Die Häufigkeit (in Sekunden) der Datensynchronisierung.</span><span class="sxs-lookup"><span data-stu-id="5bd34-123">The frequency (in seconds) of doing data synchronization.</span></span>
<span data-ttu-id="5bd34-124">Der Standardwert ist-1, was bedeutet, dass die automatische Synchronisierung nicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="5bd34-124">Default is -1, which means the auto synchronization is not enabled.</span></span>

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

### <span data-ttu-id="5bd34-125">-Name</span><span class="sxs-lookup"><span data-stu-id="5bd34-125">-Name</span></span>
<span data-ttu-id="5bd34-126">Der Name der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="5bd34-126">The sync group name.</span></span>

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

### <span data-ttu-id="5bd34-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bd34-127">-ResourceGroupName</span></span>
<span data-ttu-id="5bd34-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5bd34-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="5bd34-129">-Schemadatei</span><span class="sxs-lookup"><span data-stu-id="5bd34-129">-SchemaFile</span></span>
<span data-ttu-id="5bd34-130">Der Pfad der Schemadatei.</span><span class="sxs-lookup"><span data-stu-id="5bd34-130">The path of the schema file.</span></span>

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

### <span data-ttu-id="5bd34-131">-Servername</span><span class="sxs-lookup"><span data-stu-id="5bd34-131">-ServerName</span></span>
<span data-ttu-id="5bd34-132">Der Name des Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5bd34-132">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="5bd34-133">-SyncDatabaseName</span><span class="sxs-lookup"><span data-stu-id="5bd34-133">-SyncDatabaseName</span></span>
<span data-ttu-id="5bd34-134">Die Datenbank, die zum Speichern von Synchronisierungs bezogenen Metadaten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5bd34-134">The database used to store sync related metadata.</span></span>

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

### <span data-ttu-id="5bd34-135">-SyncDatabaseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bd34-135">-SyncDatabaseResourceGroupName</span></span>
<span data-ttu-id="5bd34-136">Die Ressourcengruppe, zu der die Synchronisierungsmetadaten-Datenbank gehört.</span><span class="sxs-lookup"><span data-stu-id="5bd34-136">The resource group the sync metadata database belongs to.</span></span>

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

### <span data-ttu-id="5bd34-137">-SyncDatabaseServerName</span><span class="sxs-lookup"><span data-stu-id="5bd34-137">-SyncDatabaseServerName</span></span>
<span data-ttu-id="5bd34-138">Der Server, auf dem die Synchronisierungsmetadaten-Datenbank gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="5bd34-138">The server on which the sync metadata database is hosted.</span></span>

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

### <span data-ttu-id="5bd34-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5bd34-139">-Confirm</span></span>
<span data-ttu-id="5bd34-140">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5bd34-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5bd34-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bd34-141">-WhatIf</span></span>
<span data-ttu-id="5bd34-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5bd34-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5bd34-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5bd34-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5bd34-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bd34-144">CommonParameters</span></span>
<span data-ttu-id="5bd34-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bd34-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bd34-146">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5bd34-146">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bd34-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5bd34-147">INPUTS</span></span>

### <span data-ttu-id="5bd34-148">System. String</span><span class="sxs-lookup"><span data-stu-id="5bd34-148">System.String</span></span>

## <span data-ttu-id="5bd34-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5bd34-149">OUTPUTS</span></span>

### <span data-ttu-id="5bd34-150">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="5bd34-150">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="5bd34-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="5bd34-151">NOTES</span></span>

## <span data-ttu-id="5bd34-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5bd34-152">RELATED LINKS</span></span>

[<span data-ttu-id="5bd34-153">Satz-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="5bd34-153">Set-AzSqlSyncGroup</span></span>](./Set-AzSqlSyncGroup.md)

[<span data-ttu-id="5bd34-154">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="5bd34-154">Remove-AzSqlSyncGroup</span></span>](./Remove-AzSqlSyncGroup.md)

[<span data-ttu-id="5bd34-155">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="5bd34-155">Get-AzSqlSyncGroup</span></span>](./Get-AzSqlSyncGroup.md)

