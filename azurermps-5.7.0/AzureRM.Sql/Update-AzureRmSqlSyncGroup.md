---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/update-azurermsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncGroup.md
ms.openlocfilehash: 198dee21b2674f3c10d0679cbb57fdee6e1f6ba0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498682"
---
# <span data-ttu-id="dc78e-101">Update-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="dc78e-101">Update-AzureRmSqlSyncGroup</span></span>

## <span data-ttu-id="dc78e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dc78e-102">SYNOPSIS</span></span>
<span data-ttu-id="dc78e-103">Aktualisiert eine Azure SQL-Daten Bank Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="dc78e-103">Updates an Azure SQL Database Sync Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc78e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc78e-104">SYNTAX</span></span>

```
Update-AzureRmSqlSyncGroup [-Name] <String> [-IntervalInSeconds <Int32>] [-DatabaseCredential <PSCredential>]
 [-SchemaFile <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc78e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dc78e-105">DESCRIPTION</span></span>
<span data-ttu-id="dc78e-106">Das Cmdlet **Update-AzureRmSqlSyncGroup** ändert die Eigenschaften einer Azure SQL-Daten Bank Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="dc78e-106">The **Update-AzureRmSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="dc78e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dc78e-107">EXAMPLES</span></span>

### <span data-ttu-id="dc78e-108">Beispiel 1: Aktualisieren einer Synchronisierungsgruppe für eine Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="dc78e-108">Example 1: Update a sync group for an Azure SQL Database.</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> Update-AzureRmSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup01"
-DatabaseCredential $credential -IntervalInSeconds 100 -Schema ".\schema.json" | Format-List
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

<span data-ttu-id="dc78e-109">Dieser Befehl aktualisiert eine Synchronisierungsgruppe für eine Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="dc78e-109">This command updates a sync group for an Azure SQL Database.</span></span> <span data-ttu-id="dc78e-110">"schema.jsein" ist eine Datei auf dem lokalen Datenträger.</span><span class="sxs-lookup"><span data-stu-id="dc78e-110">"schema.json" is a file in the local disk.</span></span> <span data-ttu-id="dc78e-111">Sie enthält die Shma-Nutzlast im JSON-Format.</span><span class="sxs-lookup"><span data-stu-id="dc78e-111">It contains the shema payload in json format.</span></span> <span data-ttu-id="dc78e-112">Ein Beispiel für das JSON-Schema ist: {"Tabellen": [{"Columns": [{"QUOTENAME": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column1"}, {"QUOTENAME": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column2"}]; "QUOTENAME": "MayQuotedTable1"}, {"Columns": [{"QUOTENAME": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column1"}, {"QUOTENAME": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column2"}], "QUOTENAME": "MayQuotedTable2"}], "MasterSyncMemberName": NULL}</span><span class="sxs-lookup"><span data-stu-id="dc78e-112">An example of the schema json is: {"Tables":  [{"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable1"}, {"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable2"}], "MasterSyncMemberName":  null }</span></span>

## <span data-ttu-id="dc78e-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="dc78e-113">PARAMETERS</span></span>

### <span data-ttu-id="dc78e-114">-DatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="dc78e-114">-DatabaseCredential</span></span>
<span data-ttu-id="dc78e-115">Die SQL-Authentifizierungsanmeldeinformationen der Hub-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="dc78e-115">The SQL authentication credential of the hub database.</span></span>

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

### <span data-ttu-id="dc78e-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="dc78e-116">-DatabaseName</span></span>
<span data-ttu-id="dc78e-117">SQL-Datenbankname</span><span class="sxs-lookup"><span data-stu-id="dc78e-117">SQL Database name.</span></span>

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

### <span data-ttu-id="dc78e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc78e-118">-DefaultProfile</span></span>
<span data-ttu-id="dc78e-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="dc78e-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dc78e-120">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="dc78e-120">-IntervalInSeconds</span></span>
<span data-ttu-id="dc78e-121">Die Häufigkeit (in Sekunden) der Datensynchronisierung.</span><span class="sxs-lookup"><span data-stu-id="dc78e-121">The frequency (in seconds) of doing data synchronization.</span></span>
<span data-ttu-id="dc78e-122">Der Standardwert ist-1, was bedeutet, dass die automatische Synchronisierung nicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="dc78e-122">Default is -1, which means the auto synchronization is not enabled.</span></span>

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

### <span data-ttu-id="dc78e-123">-Name</span><span class="sxs-lookup"><span data-stu-id="dc78e-123">-Name</span></span>
<span data-ttu-id="dc78e-124">Der Name der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="dc78e-124">The sync group name.</span></span>

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

### <span data-ttu-id="dc78e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc78e-125">-ResourceGroupName</span></span>
<span data-ttu-id="dc78e-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="dc78e-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="dc78e-127">-Schemadatei</span><span class="sxs-lookup"><span data-stu-id="dc78e-127">-SchemaFile</span></span>
<span data-ttu-id="dc78e-128">Der Pfad der Schemadatei.</span><span class="sxs-lookup"><span data-stu-id="dc78e-128">The path of the schema file.</span></span>

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

### <span data-ttu-id="dc78e-129">-Servername</span><span class="sxs-lookup"><span data-stu-id="dc78e-129">-ServerName</span></span>
<span data-ttu-id="dc78e-130">Der Name des Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="dc78e-130">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="dc78e-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dc78e-131">-Confirm</span></span>
<span data-ttu-id="dc78e-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dc78e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc78e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc78e-133">-WhatIf</span></span>
<span data-ttu-id="dc78e-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dc78e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc78e-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dc78e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc78e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc78e-136">CommonParameters</span></span>
<span data-ttu-id="dc78e-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc78e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc78e-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc78e-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc78e-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dc78e-139">INPUTS</span></span>

### <span data-ttu-id="dc78e-140">Keine</span><span class="sxs-lookup"><span data-stu-id="dc78e-140">None</span></span>
<span data-ttu-id="dc78e-141">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="dc78e-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dc78e-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dc78e-142">OUTPUTS</span></span>

### <span data-ttu-id="dc78e-143">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="dc78e-143">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="dc78e-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="dc78e-144">NOTES</span></span>

## <span data-ttu-id="dc78e-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dc78e-145">RELATED LINKS</span></span>

[<span data-ttu-id="dc78e-146">Neu – AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="dc78e-146">New-AzureRmSqlSyncGroup</span></span>](./New-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="dc78e-147">Remove-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="dc78e-147">Remove-AzureRmSqlSyncGroup</span></span>](./Remove-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="dc78e-148">Get-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="dc78e-148">Get-AzureRmSqlSyncGroup</span></span>](./Get-AzureRmSqlSyncGroup.md)

