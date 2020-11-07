---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/update-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncGroup.md
ms.openlocfilehash: cef62c85f42c2c9f0e6fbda776c58d6818659474
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846440"
---
# <span data-ttu-id="eb6a5-101">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="eb6a5-101">Update-AzSqlSyncGroup</span></span>

## <span data-ttu-id="eb6a5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="eb6a5-102">SYNOPSIS</span></span>
<span data-ttu-id="eb6a5-103">Aktualisiert eine Azure SQL-Daten Bank Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="eb6a5-103">Updates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="eb6a5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="eb6a5-104">SYNTAX</span></span>

```
Update-AzSqlSyncGroup [-Name] <String> [-IntervalInSeconds <Int32>] [-DatabaseCredential <PSCredential>]
 [-SchemaFile <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb6a5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eb6a5-105">DESCRIPTION</span></span>
<span data-ttu-id="eb6a5-106">Das Cmdlet **Update-AzSqlSyncGroup** ändert die Eigenschaften einer Azure SQL-Daten Bank Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="eb6a5-106">The **Update-AzSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="eb6a5-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="eb6a5-107">EXAMPLES</span></span>

### <span data-ttu-id="eb6a5-108">Beispiel 1: Aktualisieren einer Synchronisierungsgruppe für eine Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="eb6a5-108">Example 1: Update a sync group for an Azure SQL Database.</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> Update-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup01"
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

<span data-ttu-id="eb6a5-109">Dieser Befehl aktualisiert eine Synchronisierungsgruppe für eine Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="eb6a5-109">This command updates a sync group for an Azure SQL Database.</span></span> <span data-ttu-id="eb6a5-110">"schema.jsein" ist eine Datei auf dem lokalen Datenträger.</span><span class="sxs-lookup"><span data-stu-id="eb6a5-110">"schema.json" is a file in the local disk.</span></span> <span data-ttu-id="eb6a5-111">Sie enthält die Schema Nutzlast im JSON-Format.</span><span class="sxs-lookup"><span data-stu-id="eb6a5-111">It contains the schema payload in json format.</span></span> <span data-ttu-id="eb6a5-112">Ein Beispiel für das JSON-Schema ist: {"Tabellen": [{"Columns": [{"QUOTENAME": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column1"}, {"QUOTENAME": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column2"}]; "QUOTENAME": "MayQuotedTable1"}, {"Columns": [{"QUOTENAME": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column1"}, {"QUOTENAME": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column2"}], "QUOTENAME": "MayQuotedTable2"}], "MasterSyncMemberName": NULL}</span><span class="sxs-lookup"><span data-stu-id="eb6a5-112">An example of the schema json is: {"Tables":  [{"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable1"}, {"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable2"}], "MasterSyncMemberName":  null }</span></span>

## <span data-ttu-id="eb6a5-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="eb6a5-113">PARAMETERS</span></span>

### <span data-ttu-id="eb6a5-114">-DatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="eb6a5-114">-DatabaseCredential</span></span>
<span data-ttu-id="eb6a5-115">Die SQL-Authentifizierungsanmeldeinformationen der Hub-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="eb6a5-115">The SQL authentication credential of the hub database.</span></span>

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

### <span data-ttu-id="eb6a5-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="eb6a5-116">-DatabaseName</span></span>
<span data-ttu-id="eb6a5-117">SQL-Datenbankname</span><span class="sxs-lookup"><span data-stu-id="eb6a5-117">SQL Database name.</span></span>

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

### <span data-ttu-id="eb6a5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb6a5-118">-DefaultProfile</span></span>
<span data-ttu-id="eb6a5-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="eb6a5-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eb6a5-120">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="eb6a5-120">-IntervalInSeconds</span></span>
<span data-ttu-id="eb6a5-121">Die Häufigkeit (in Sekunden) der Datensynchronisierung.</span><span class="sxs-lookup"><span data-stu-id="eb6a5-121">The frequency (in seconds) of doing data synchronization.</span></span>
<span data-ttu-id="eb6a5-122">Der Standardwert ist-1, was bedeutet, dass die automatische Synchronisierung nicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="eb6a5-122">Default is -1, which means the auto synchronization is not enabled.</span></span>

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

### <span data-ttu-id="eb6a5-123">-Name</span><span class="sxs-lookup"><span data-stu-id="eb6a5-123">-Name</span></span>
<span data-ttu-id="eb6a5-124">Der Name der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="eb6a5-124">The sync group name.</span></span>

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

### <span data-ttu-id="eb6a5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb6a5-125">-ResourceGroupName</span></span>
<span data-ttu-id="eb6a5-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="eb6a5-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="eb6a5-127">-Schemadatei</span><span class="sxs-lookup"><span data-stu-id="eb6a5-127">-SchemaFile</span></span>
<span data-ttu-id="eb6a5-128">Der Pfad der Schemadatei.</span><span class="sxs-lookup"><span data-stu-id="eb6a5-128">The path of the schema file.</span></span>

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

### <span data-ttu-id="eb6a5-129">-Servername</span><span class="sxs-lookup"><span data-stu-id="eb6a5-129">-ServerName</span></span>
<span data-ttu-id="eb6a5-130">Der Name des Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="eb6a5-130">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="eb6a5-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="eb6a5-131">-Confirm</span></span>
<span data-ttu-id="eb6a5-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="eb6a5-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb6a5-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb6a5-133">-WhatIf</span></span>
<span data-ttu-id="eb6a5-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="eb6a5-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb6a5-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="eb6a5-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb6a5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb6a5-136">CommonParameters</span></span>
<span data-ttu-id="eb6a5-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb6a5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb6a5-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eb6a5-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb6a5-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="eb6a5-139">INPUTS</span></span>

### <span data-ttu-id="eb6a5-140">System. String</span><span class="sxs-lookup"><span data-stu-id="eb6a5-140">System.String</span></span>

## <span data-ttu-id="eb6a5-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="eb6a5-141">OUTPUTS</span></span>

### <span data-ttu-id="eb6a5-142">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="eb6a5-142">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="eb6a5-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="eb6a5-143">NOTES</span></span>

## <span data-ttu-id="eb6a5-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="eb6a5-144">RELATED LINKS</span></span>

[<span data-ttu-id="eb6a5-145">Neu – AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="eb6a5-145">New-AzSqlSyncGroup</span></span>](./New-AzSqlSyncGroup.md)

[<span data-ttu-id="eb6a5-146">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="eb6a5-146">Remove-AzSqlSyncGroup</span></span>](./Remove-AzSqlSyncGroup.md)

[<span data-ttu-id="eb6a5-147">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="eb6a5-147">Get-AzSqlSyncGroup</span></span>](./Get-AzSqlSyncGroup.md)

