---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncGroup.md
ms.openlocfilehash: 65ac7bb4a63fa8519bd8f0b0c006209d5f171833
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498714"
---
# <span data-ttu-id="0b4d8-101">New-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="0b4d8-101">New-AzureRmSqlSyncGroup</span></span>

## <span data-ttu-id="0b4d8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0b4d8-102">SYNOPSIS</span></span>
<span data-ttu-id="0b4d8-103">Erstellt eine Azure SQL-Daten Bank Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="0b4d8-103">Creates an Azure SQL Database Sync Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b4d8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b4d8-104">SYNTAX</span></span>

```
New-AzureRmSqlSyncGroup [-Name] <String> -SyncDatabaseName <String> -SyncDatabaseServerName <String>
 -SyncDatabaseResourceGroupName <String> [-IntervalInSeconds <Int32>] [-DatabaseCredential <PSCredential>]
 [-ConflictResolutionPolicy <String>] [-SchemaFile <String>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0b4d8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0b4d8-105">DESCRIPTION</span></span>
<span data-ttu-id="0b4d8-106">Das Cmdlet **New-AzureRmSqlSyncGroup** erstellt eine Azure SQL-Daten Bank Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="0b4d8-106">The **New-AzureRmSqlSyncGroup** cmdlet creates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="0b4d8-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0b4d8-107">EXAMPLES</span></span>

### <span data-ttu-id="0b4d8-108">Beispiel 1: Erstellen einer Synchronisierungsgruppe für eine Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="0b4d8-108">Example 1: Create a sync group for an Azure SQL Database.</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> New-AzureRmSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup01" -ConflictResolutionPolicy "HubWin"
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

<span data-ttu-id="0b4d8-109">Mit diesem Befehl wird eine Synchronisierungsgruppe für eine Azure SQL-Datenbank erstellt.</span><span class="sxs-lookup"><span data-stu-id="0b4d8-109">This command creates a sync group for an Azure SQL Database.</span></span> <span data-ttu-id="0b4d8-110">"schema.jsein" ist eine Datei auf dem lokalen Datenträger.</span><span class="sxs-lookup"><span data-stu-id="0b4d8-110">"schema.json" is a file in the local disk.</span></span> <span data-ttu-id="0b4d8-111">Sie enthält die Shma-Nutzlast im JSON-Format.</span><span class="sxs-lookup"><span data-stu-id="0b4d8-111">It contains the shema payload in json format.</span></span> <span data-ttu-id="0b4d8-112">Ein Beispiel für das JSON-Schema ist: {"Tabellen": [{"Columns": [{"QUOTENAME": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column1"}, {"QUOTENAME": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column2"}]; "QUOTENAME": "MayQuotedTable1"}, {"Columns": [{"QUOTENAME": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column1"}, {"QUOTENAME": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column2"}], "QUOTENAME": "MayQuotedTable2"}], "MasterSyncMemberName": NULL}</span><span class="sxs-lookup"><span data-stu-id="0b4d8-112">An example of the schema json is: {"Tables":  [{"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable1"}, {"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable2"}], "MasterSyncMemberName":  null }</span></span>

## <span data-ttu-id="0b4d8-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b4d8-113">PARAMETERS</span></span>

### <span data-ttu-id="0b4d8-114">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="0b4d8-114">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="0b4d8-115">Die Richtlinie zum Auflösen von Konflikten zwischen Hub-und Mitgliedsdatenbank in der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="0b4d8-115">The policy of resolving confliction between hub and member database in the sync group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: HubWin, MemberWin

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b4d8-116">-DatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="0b4d8-116">-DatabaseCredential</span></span>
<span data-ttu-id="0b4d8-117">Die SQL-Authentifizierungsanmeldeinformationen der Hub-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="0b4d8-117">The SQL authentication credential of the hub database.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b4d8-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0b4d8-118">-DatabaseName</span></span>
<span data-ttu-id="0b4d8-119">Der Name der Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="0b4d8-119">The name of the Azure SQL Database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b4d8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b4d8-120">-DefaultProfile</span></span>
<span data-ttu-id="0b4d8-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="0b4d8-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b4d8-122">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="0b4d8-122">-IntervalInSeconds</span></span>
<span data-ttu-id="0b4d8-123">Die Häufigkeit (in Sekunden) der Datensynchronisierung.</span><span class="sxs-lookup"><span data-stu-id="0b4d8-123">The frequency (in seconds) of doing data synchronization.</span></span>
<span data-ttu-id="0b4d8-124">Der Standardwert ist-1, was bedeutet, dass die automatische Synchronisierung nicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="0b4d8-124">Default is -1, which means the auto synchronization is not enabled.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b4d8-125">-Name</span><span class="sxs-lookup"><span data-stu-id="0b4d8-125">-Name</span></span>
<span data-ttu-id="0b4d8-126">Der Name der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="0b4d8-126">The sync group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b4d8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b4d8-127">-ResourceGroupName</span></span>
<span data-ttu-id="0b4d8-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0b4d8-128">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b4d8-129">-Schemadatei</span><span class="sxs-lookup"><span data-stu-id="0b4d8-129">-SchemaFile</span></span>
<span data-ttu-id="0b4d8-130">Der Pfad der Schemadatei.</span><span class="sxs-lookup"><span data-stu-id="0b4d8-130">The path of the schema file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b4d8-131">-Servername</span><span class="sxs-lookup"><span data-stu-id="0b4d8-131">-ServerName</span></span>
<span data-ttu-id="0b4d8-132">Der Name des Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="0b4d8-132">The name of the Azure SQL Server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b4d8-133">-SyncDatabaseName</span><span class="sxs-lookup"><span data-stu-id="0b4d8-133">-SyncDatabaseName</span></span>
<span data-ttu-id="0b4d8-134">Die Datenbank, die zum Speichern von Synchronisierungs bezogenen Metadaten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0b4d8-134">The database used to store sync related metadata.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b4d8-135">-SyncDatabaseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b4d8-135">-SyncDatabaseResourceGroupName</span></span>
<span data-ttu-id="0b4d8-136">Die Ressourcengruppe, zu der die Synchronisierungsmetadaten-Datenbank gehört.</span><span class="sxs-lookup"><span data-stu-id="0b4d8-136">The resource group the sync metadata database belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b4d8-137">-SyncDatabaseServerName</span><span class="sxs-lookup"><span data-stu-id="0b4d8-137">-SyncDatabaseServerName</span></span>
<span data-ttu-id="0b4d8-138">Der Server, auf dem die Synchronisierungsmetadaten-Datenbank gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="0b4d8-138">The server on which the sync metadata database is hosted.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b4d8-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0b4d8-139">-Confirm</span></span>
<span data-ttu-id="0b4d8-140">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0b4d8-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b4d8-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b4d8-141">-WhatIf</span></span>
<span data-ttu-id="0b4d8-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0b4d8-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b4d8-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0b4d8-143">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b4d8-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b4d8-144">CommonParameters</span></span>
<span data-ttu-id="0b4d8-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b4d8-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b4d8-146">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b4d8-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b4d8-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0b4d8-147">INPUTS</span></span>

### <span data-ttu-id="0b4d8-148">Keine</span><span class="sxs-lookup"><span data-stu-id="0b4d8-148">None</span></span>
<span data-ttu-id="0b4d8-149">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="0b4d8-149">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0b4d8-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0b4d8-150">OUTPUTS</span></span>

### <span data-ttu-id="0b4d8-151">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="0b4d8-151">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="0b4d8-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="0b4d8-152">NOTES</span></span>

## <span data-ttu-id="0b4d8-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0b4d8-153">RELATED LINKS</span></span>

[<span data-ttu-id="0b4d8-154">Satz-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="0b4d8-154">Set-AzureRmSqlSyncGroup</span></span>](./Set-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="0b4d8-155">Remove-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="0b4d8-155">Remove-AzureRmSqlSyncGroup</span></span>](./Remove-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="0b4d8-156">Get-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="0b4d8-156">Get-AzureRmSqlSyncGroup</span></span>](./Get-AzureRmSqlSyncGroup.md)

