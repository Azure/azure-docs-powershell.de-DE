---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/update-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncGroup.md
ms.openlocfilehash: 9c4a6572a5a2025bba23758160378519524b8ce7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98294190"
---
# <span data-ttu-id="09e71-101">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="09e71-101">Update-AzSqlSyncGroup</span></span>

## <span data-ttu-id="09e71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09e71-102">SYNOPSIS</span></span>
<span data-ttu-id="09e71-103">Aktualisiert eine Azure SQL-Datenbanksynchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="09e71-103">Updates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="09e71-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="09e71-104">SYNTAX</span></span>

```
Update-AzSqlSyncGroup [-Name] <String> [-IntervalInSeconds <Int32>] [-DatabaseCredential <PSCredential>]
 [-SchemaFile <String>] [-UsePrivateLinkConnection <Boolean>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="09e71-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="09e71-105">DESCRIPTION</span></span>
<span data-ttu-id="09e71-106">Das **Cmdlet "Update-AzSqlSyncGroup"** ändert die Eigenschaften einer Azure SQL-Datenbanksynchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="09e71-106">The **Update-AzSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="09e71-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="09e71-107">EXAMPLES</span></span>

### <span data-ttu-id="09e71-108">Beispiel 1: Aktualisieren einer Synchronisierungsgruppe für eine Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="09e71-108">Example 1: Update a sync group for an Azure SQL Database.</span></span>
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

<span data-ttu-id="09e71-109">Mit diesem Befehl wird eine Synchronisierungsgruppe für eine Azure SQL aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="09e71-109">This command updates a sync group for an Azure SQL Database.</span></span> <span data-ttu-id="09e71-110">"schema.jsein" ist eine Datei auf dem lokalen Datenträger.</span><span class="sxs-lookup"><span data-stu-id="09e71-110">"schema.json" is a file in the local disk.</span></span> <span data-ttu-id="09e71-111">Sie enthält die Schemanutzlast im json-Format.</span><span class="sxs-lookup"><span data-stu-id="09e71-111">It contains the schema payload in json format.</span></span> <span data-ttu-id="09e71-112">Beispiel für das Schema json: {"Tables": [{"Columns": [{"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable1"}, {"Columns": [{"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable2"}], "MasterSyncMemberName": null }</span><span class="sxs-lookup"><span data-stu-id="09e71-112">An example of the schema json is: {"Tables":  [{"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable1"}, {"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable2"}], "MasterSyncMemberName":  null }</span></span>

## <span data-ttu-id="09e71-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="09e71-113">PARAMETERS</span></span>

### <span data-ttu-id="09e71-114">-DatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="09e71-114">-DatabaseCredential</span></span>
<span data-ttu-id="09e71-115">Die SQL A0 der Hubdatenbank.</span><span class="sxs-lookup"><span data-stu-id="09e71-115">The SQL authentication credential of the hub database.</span></span>

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

### <span data-ttu-id="09e71-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="09e71-116">-DatabaseName</span></span>
<span data-ttu-id="09e71-117">SQL Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="09e71-117">SQL Database name.</span></span>

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

### <span data-ttu-id="09e71-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09e71-118">-DefaultProfile</span></span>
<span data-ttu-id="09e71-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="09e71-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="09e71-120">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="09e71-120">-IntervalInSeconds</span></span>
<span data-ttu-id="09e71-121">Die Häufigkeit (in Sekunden) der Datensynchronisierung.</span><span class="sxs-lookup"><span data-stu-id="09e71-121">The frequency (in seconds) of doing data synchronization.</span></span>
<span data-ttu-id="09e71-122">Der Standardwert ist -1, d. h., die automatische Synchronisierung ist nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="09e71-122">Default is -1, which means the auto synchronization is not enabled.</span></span>

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

### <span data-ttu-id="09e71-123">-Name</span><span class="sxs-lookup"><span data-stu-id="09e71-123">-Name</span></span>
<span data-ttu-id="09e71-124">Der Name der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="09e71-124">The sync group name.</span></span>

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

### <span data-ttu-id="09e71-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09e71-125">-ResourceGroupName</span></span>
<span data-ttu-id="09e71-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="09e71-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="09e71-127">-SchemaFile</span><span class="sxs-lookup"><span data-stu-id="09e71-127">-SchemaFile</span></span>
<span data-ttu-id="09e71-128">Der Pfad der Schemadatei.</span><span class="sxs-lookup"><span data-stu-id="09e71-128">The path of the schema file.</span></span>

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

### <span data-ttu-id="09e71-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="09e71-129">-ServerName</span></span>
<span data-ttu-id="09e71-130">Der Name des Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="09e71-130">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="09e71-131">-UsePrivateLinkConnection</span><span class="sxs-lookup"><span data-stu-id="09e71-131">-UsePrivateLinkConnection</span></span>
<span data-ttu-id="09e71-132">Gibt an, ob beim Herstellen einer Verbindung mit dem Hub dieser Synchronisierungsgruppe eine private Linkverbindung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="09e71-132">Whether to use a private link connection when connecting to the hub of this sync group.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09e71-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="09e71-133">-Confirm</span></span>
<span data-ttu-id="09e71-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="09e71-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09e71-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="09e71-135">-WhatIf</span></span>
<span data-ttu-id="09e71-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="09e71-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09e71-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="09e71-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09e71-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09e71-138">CommonParameters</span></span>
<span data-ttu-id="09e71-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09e71-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09e71-140">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="09e71-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09e71-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="09e71-141">INPUTS</span></span>

### <span data-ttu-id="09e71-142">System.String</span><span class="sxs-lookup"><span data-stu-id="09e71-142">System.String</span></span>

## <span data-ttu-id="09e71-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="09e71-143">OUTPUTS</span></span>

### <span data-ttu-id="09e71-144">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="09e71-144">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="09e71-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="09e71-145">NOTES</span></span>

## <span data-ttu-id="09e71-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="09e71-146">RELATED LINKS</span></span>

[<span data-ttu-id="09e71-147">New-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="09e71-147">New-AzSqlSyncGroup</span></span>](./New-AzSqlSyncGroup.md)

[<span data-ttu-id="09e71-148">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="09e71-148">Remove-AzSqlSyncGroup</span></span>](./Remove-AzSqlSyncGroup.md)

[<span data-ttu-id="09e71-149">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="09e71-149">Get-AzSqlSyncGroup</span></span>](./Get-AzSqlSyncGroup.md)

