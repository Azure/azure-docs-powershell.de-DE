---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncGroup.md
ms.openlocfilehash: bcae25cba6eae5f883bffb7248cbca6f5516bcfd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496810"
---
# <span data-ttu-id="78ac6-101">New-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="78ac6-101">New-AzureRmSqlSyncGroup</span></span>

## <span data-ttu-id="78ac6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="78ac6-102">SYNOPSIS</span></span>
<span data-ttu-id="78ac6-103">Erstellt eine Azure SQL-Daten Bank Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="78ac6-103">Creates an Azure SQL Database Sync Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78ac6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="78ac6-104">SYNTAX</span></span>

```
New-AzureRmSqlSyncGroup [-Name] <String> -SyncDatabaseName <String> -SyncDatabaseServerName <String>
 -SyncDatabaseResourceGroupName <String> [-IntervalInSeconds <Int32>] [-DatabaseCredential <PSCredential>]
 [-ConflictResolutionPolicy <String>] [-SchemaFile <String>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="78ac6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="78ac6-105">DESCRIPTION</span></span>
<span data-ttu-id="78ac6-106">Das Cmdlet **New-AzureRmSqlSyncGroup** erstellt eine Azure SQL-Daten Bank Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="78ac6-106">The **New-AzureRmSqlSyncGroup** cmdlet creates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="78ac6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="78ac6-107">EXAMPLES</span></span>

### <span data-ttu-id="78ac6-108">Beispiel 1: Erstellen einer Synchronisierungsgruppe für eine Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="78ac6-108">Example 1: Create a sync group for an Azure SQL Database.</span></span>
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

<span data-ttu-id="78ac6-109">Mit diesem Befehl wird eine Synchronisierungsgruppe für eine Azure SQL-Datenbank erstellt.</span><span class="sxs-lookup"><span data-stu-id="78ac6-109">This command creates a sync group for an Azure SQL Database.</span></span> <span data-ttu-id="78ac6-110">"schema.jsein" ist eine Datei auf dem lokalen Datenträger.</span><span class="sxs-lookup"><span data-stu-id="78ac6-110">"schema.json" is a file in the local disk.</span></span> <span data-ttu-id="78ac6-111">Sie enthält die Shma-Nutzlast im JSON-Format.</span><span class="sxs-lookup"><span data-stu-id="78ac6-111">It contains the shema payload in json format.</span></span> <span data-ttu-id="78ac6-112">Ein Beispiel für das JSON-Schema ist: {"Tabellen": [{"Columns": [{"QUOTENAME": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column1"}, {"QUOTENAME": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column2"}]; "QUOTENAME": "MayQuotedTable1"}, {"Columns": [{"QUOTENAME": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column1"}, {"QUOTENAME": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column2"}], "QUOTENAME": "MayQuotedTable2"}], "MasterSyncMemberName": NULL}</span><span class="sxs-lookup"><span data-stu-id="78ac6-112">An example of the schema json is: {"Tables":  [{"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable1"}, {"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable2"}], "MasterSyncMemberName":  null }</span></span>

## <span data-ttu-id="78ac6-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="78ac6-113">PARAMETERS</span></span>

### <span data-ttu-id="78ac6-114">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="78ac6-114">-Confirm</span></span>
<span data-ttu-id="78ac6-115">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="78ac6-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78ac6-116">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="78ac6-116">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="78ac6-117">Die Richtlinie zum Auflösen von Konflikten zwischen Hub-und Mitgliedsdatenbank in der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="78ac6-117">The policy of resolving confliction between hub and member database in the sync group.</span></span>

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

### <span data-ttu-id="78ac6-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="78ac6-118">-DatabaseName</span></span>
<span data-ttu-id="78ac6-119">Der Name der Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="78ac6-119">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="78ac6-120">-DatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="78ac6-120">-DatabaseCredential</span></span>
<span data-ttu-id="78ac6-121">Die SQL-Authentifizierungsanmeldeinformationen der Hub-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="78ac6-121">The SQL authentication credential of the hub database.</span></span>

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

### <span data-ttu-id="78ac6-122">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="78ac6-122">-IntervalInSeconds</span></span>
<span data-ttu-id="78ac6-123">Die Häufigkeit (in Sekunden) der Datensynchronisierung.</span><span class="sxs-lookup"><span data-stu-id="78ac6-123">The frequency (in seconds) of doing data synchronization.</span></span>
<span data-ttu-id="78ac6-124">Der Standardwert ist-1, was bedeutet, dass die automatische Synchronisierung nicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="78ac6-124">Default is -1, which means the auto synchronization is not enabled.</span></span>

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

### <span data-ttu-id="78ac6-125">-Name</span><span class="sxs-lookup"><span data-stu-id="78ac6-125">-Name</span></span>
<span data-ttu-id="78ac6-126">Der Name der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="78ac6-126">The sync group name.</span></span>

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

### <span data-ttu-id="78ac6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78ac6-127">-ResourceGroupName</span></span>
<span data-ttu-id="78ac6-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="78ac6-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="78ac6-129">-Schemadatei</span><span class="sxs-lookup"><span data-stu-id="78ac6-129">-SchemaFile</span></span>
<span data-ttu-id="78ac6-130">Der Pfad der Schemadatei.</span><span class="sxs-lookup"><span data-stu-id="78ac6-130">The path of the schema file.</span></span>

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

### <span data-ttu-id="78ac6-131">-Servername</span><span class="sxs-lookup"><span data-stu-id="78ac6-131">-ServerName</span></span>
<span data-ttu-id="78ac6-132">Der Name des Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="78ac6-132">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="78ac6-133">-SyncDatabaseName</span><span class="sxs-lookup"><span data-stu-id="78ac6-133">-SyncDatabaseName</span></span>
<span data-ttu-id="78ac6-134">Die Datenbank, die zum Speichern von Synchronisierungs bezogenen Metadaten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="78ac6-134">The database used to store sync related metadata.</span></span>

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

### <span data-ttu-id="78ac6-135">-SyncDatabaseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78ac6-135">-SyncDatabaseResourceGroupName</span></span>
<span data-ttu-id="78ac6-136">Die Ressourcengruppe, zu der die Synchronisierungsmetadaten-Datenbank gehört.</span><span class="sxs-lookup"><span data-stu-id="78ac6-136">The resource group the sync metadata database belongs to.</span></span>

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

### <span data-ttu-id="78ac6-137">-SyncDatabaseServerName</span><span class="sxs-lookup"><span data-stu-id="78ac6-137">-SyncDatabaseServerName</span></span>
<span data-ttu-id="78ac6-138">Der Server, auf dem die Synchronisierungsmetadaten-Datenbank gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="78ac6-138">The server on which the sync metadata database is hosted.</span></span>

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

### <span data-ttu-id="78ac6-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78ac6-139">-WhatIf</span></span>
<span data-ttu-id="78ac6-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="78ac6-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78ac6-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="78ac6-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78ac6-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78ac6-142">-DefaultProfile</span></span>
<span data-ttu-id="78ac6-143">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="78ac6-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78ac6-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78ac6-144">CommonParameters</span></span>
<span data-ttu-id="78ac6-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78ac6-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78ac6-146">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78ac6-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78ac6-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="78ac6-147">INPUTS</span></span>

## <span data-ttu-id="78ac6-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="78ac6-148">OUTPUTS</span></span>

### <span data-ttu-id="78ac6-149">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="78ac6-149">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="78ac6-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="78ac6-150">NOTES</span></span>

## <span data-ttu-id="78ac6-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="78ac6-151">RELATED LINKS</span></span>

[<span data-ttu-id="78ac6-152">Satz-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="78ac6-152">Set-AzureRmSqlSyncGroup</span></span>](./Set-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="78ac6-153">Remove-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="78ac6-153">Remove-AzureRmSqlSyncGroup</span></span>](./Remove-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="78ac6-154">Get-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="78ac6-154">Get-AzureRmSqlSyncGroup</span></span>](./Get-AzureRmSqlSyncGroup.md)

