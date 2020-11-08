---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgent.md
ms.openlocfilehash: 4a4ce99eb30aaa959eabdc9c1385b567aef2b0fc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174116"
---
# <span data-ttu-id="f6afd-101">New-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="f6afd-101">New-AzSqlSyncAgent</span></span>

## <span data-ttu-id="f6afd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f6afd-102">SYNOPSIS</span></span>
<span data-ttu-id="f6afd-103">Erstellt einen Azure SQL-Synchronisierungs-Agent.</span><span class="sxs-lookup"><span data-stu-id="f6afd-103">Creates an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="f6afd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f6afd-104">SYNTAX</span></span>

### <span data-ttu-id="f6afd-105">SyncDatabaseComponent (Standard)</span><span class="sxs-lookup"><span data-stu-id="f6afd-105">SyncDatabaseComponent (Default)</span></span>
```
New-AzSqlSyncAgent [-Name] <String> -SyncDatabaseName <String> [-SyncDatabaseServerName <String>]
 [-SyncDatabaseResourceGroupName <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6afd-106">SyncDatabaseResourceID</span><span class="sxs-lookup"><span data-stu-id="f6afd-106">SyncDatabaseResourceID</span></span>
```
New-AzSqlSyncAgent [-Name] <String> -SyncDatabaseResourceID <String> [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f6afd-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f6afd-107">DESCRIPTION</span></span>
<span data-ttu-id="f6afd-108">Das Cmdlet **New-AzSqlSyncAgent** erstellt einen Azure SQL-Synchronisierungs-Agent.</span><span class="sxs-lookup"><span data-stu-id="f6afd-108">The **New-AzSqlSyncAgent** cmdlet creates an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="f6afd-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f6afd-109">EXAMPLES</span></span>

### <span data-ttu-id="f6afd-110">Beispiel 1: Erstellen eines Synchronisierungs-Agents für einen Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f6afd-110">Example 1: Create a sync agent for an Azure SQL server.</span></span>
```
PS C:\> New-AzSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "SyncAgent01" -SyncDatabaseServerName "syncDatabaseServer01" 
-SyncDatabaseName "syncDatabaseName01" -SyncDatabaseResourceGroupName "syncDatabaseResourceGroup01" | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/syncAgents/{SyncAgent01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncAgentName               : SyncAgent01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
LastAliveTime:              : 
Version                     : 4.2.0.0
IsUpToDate                  : True
ExpiryTime                  : 12/31/9999 11:59:59 PM
State                       : NeverConnected
```

<span data-ttu-id="f6afd-111">Dieser Befehl erstellt einen Synchronisierungs-Agent für einen Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f6afd-111">This command creates a sync agent for an Azure SQL server.</span></span>

## <span data-ttu-id="f6afd-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f6afd-112">PARAMETERS</span></span>

### <span data-ttu-id="f6afd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6afd-113">-DefaultProfile</span></span>
<span data-ttu-id="f6afd-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="f6afd-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f6afd-115">-Name</span><span class="sxs-lookup"><span data-stu-id="f6afd-115">-Name</span></span>
<span data-ttu-id="f6afd-116">Der Name des Synchronisierungs-Agents.</span><span class="sxs-lookup"><span data-stu-id="f6afd-116">The sync agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncAgentName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6afd-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6afd-117">-ResourceGroupName</span></span>
<span data-ttu-id="f6afd-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f6afd-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="f6afd-119">-Servername</span><span class="sxs-lookup"><span data-stu-id="f6afd-119">-ServerName</span></span>
<span data-ttu-id="f6afd-120">Der Name des Azure SQL Server, in dem sich der Synchronisierungs-Agent befindet.</span><span class="sxs-lookup"><span data-stu-id="f6afd-120">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="f6afd-121">-SyncDatabaseName</span><span class="sxs-lookup"><span data-stu-id="f6afd-121">-SyncDatabaseName</span></span>
<span data-ttu-id="f6afd-122">Die Datenbank, die zum Speichern von Synchronisierungs bezogenen Metadaten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f6afd-122">The database used to store sync related metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: SyncDatabaseComponent
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6afd-123">-SyncDatabaseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6afd-123">-SyncDatabaseResourceGroupName</span></span>
<span data-ttu-id="f6afd-124">Die Ressourcengruppe, zu der die Synchronisierungsmetadaten-Datenbank gehört.</span><span class="sxs-lookup"><span data-stu-id="f6afd-124">The resource group the sync metadata database belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: SyncDatabaseComponent
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6afd-125">-SyncDatabaseResourceID</span><span class="sxs-lookup"><span data-stu-id="f6afd-125">-SyncDatabaseResourceID</span></span>
<span data-ttu-id="f6afd-126">Die Ressourcen-ID der Synchronisierungsmetadaten-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="f6afd-126">The resource ID of  the sync metadata database.</span></span>

```yaml
Type: System.String
Parameter Sets: SyncDatabaseResourceID
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6afd-127">-SyncDatabaseServerName</span><span class="sxs-lookup"><span data-stu-id="f6afd-127">-SyncDatabaseServerName</span></span>
<span data-ttu-id="f6afd-128">Der Server, auf dem die Synchronisierungsmetadaten-Datenbank gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="f6afd-128">The server on which the sync metadata database is hosted.</span></span>

```yaml
Type: System.String
Parameter Sets: SyncDatabaseComponent
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6afd-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f6afd-129">-Confirm</span></span>
<span data-ttu-id="f6afd-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f6afd-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6afd-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6afd-131">-WhatIf</span></span>
<span data-ttu-id="f6afd-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f6afd-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6afd-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f6afd-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6afd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6afd-134">CommonParameters</span></span>
<span data-ttu-id="f6afd-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6afd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6afd-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f6afd-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6afd-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f6afd-137">INPUTS</span></span>

### <span data-ttu-id="f6afd-138">System. String</span><span class="sxs-lookup"><span data-stu-id="f6afd-138">System.String</span></span>

## <span data-ttu-id="f6afd-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f6afd-139">OUTPUTS</span></span>

### <span data-ttu-id="f6afd-140">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="f6afd-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="f6afd-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="f6afd-141">NOTES</span></span>

## <span data-ttu-id="f6afd-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f6afd-142">RELATED LINKS</span></span>

[<span data-ttu-id="f6afd-143">Remove-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="f6afd-143">Remove-AzSqlSyncAgent</span></span>](./Remove-AzSqlSyncAgent.md)

[<span data-ttu-id="f6afd-144">Get-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="f6afd-144">Get-AzSqlSyncAgent</span></span>](./Get-AzSqlSyncAgent.md)

