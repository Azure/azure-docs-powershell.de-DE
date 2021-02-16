---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/update-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncMember.md
ms.openlocfilehash: eff96559dce38bd1a78fa4e8c789c514ea7b93ec
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100155172"
---
# <span data-ttu-id="a100a-101">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="a100a-101">Update-AzSqlSyncMember</span></span>

## <span data-ttu-id="a100a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a100a-102">SYNOPSIS</span></span>
<span data-ttu-id="a100a-103">Aktualisiert ein Azure SQL-Datenbanksynchronisierungsmitglied.</span><span class="sxs-lookup"><span data-stu-id="a100a-103">Updates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="a100a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a100a-104">SYNTAX</span></span>

```
Update-AzSqlSyncMember -Name <String> [-MemberDatabaseCredential <PSCredential>]
 [-UsePrivateLinkConnection <Boolean>] [-SyncMemberAzureDatabaseResourceId <String>] [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a100a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a100a-105">DESCRIPTION</span></span>
<span data-ttu-id="a100a-106">Das **Cmdlet "Update-AzSqlSyncGroup"** ändert die Eigenschaften eines Azure SQL Database Sync Member.</span><span class="sxs-lookup"><span data-stu-id="a100a-106">The **Update-AzSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="a100a-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a100a-107">EXAMPLES</span></span>

### <span data-ttu-id="a100a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a100a-108">Example 1</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> Update-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01"
-MemberDatabaseCredential $credential | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}/syncMembers/{SyncMember01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncMemberName              : SyncMember01
SyncDirection               : OneWayMemberToHub
MemberDatabaseType:         : AzureSqlDatabase
SyncAgentId                 : 
SqlServerDatabaseId         : 
MemberServerName            : memberServer01.full.dns.name
MemberDatabaseName          : memberDatabase01
MemberDatabaseUserName      : myAccount-new
MemberDatabasePassword      : 
SyncState                   : Good
```

<span data-ttu-id="a100a-109">Mit diesem Befehl wird das Administratorkennwort für die Memberdatenbank zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="a100a-109">This command resets the administrator password for the member database.</span></span>

## <span data-ttu-id="a100a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a100a-110">PARAMETERS</span></span>

### <span data-ttu-id="a100a-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a100a-111">-DatabaseName</span></span>
<span data-ttu-id="a100a-112">Der Name der Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="a100a-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="a100a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a100a-113">-DefaultProfile</span></span>
<span data-ttu-id="a100a-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="a100a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a100a-115">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="a100a-115">-MemberDatabaseCredential</span></span>
<span data-ttu-id="a100a-116">Die Anmeldeinformationen (Benutzername und Kennwort) der Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="a100a-116">The credential (username and password) of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="a100a-117">-Name</span><span class="sxs-lookup"><span data-stu-id="a100a-117">-Name</span></span>
<span data-ttu-id="a100a-118">Der Name des Synchronisierungsmitglieds.</span><span class="sxs-lookup"><span data-stu-id="a100a-118">The sync member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a100a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a100a-119">-ResourceGroupName</span></span>
<span data-ttu-id="a100a-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a100a-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="a100a-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a100a-121">-ServerName</span></span>
<span data-ttu-id="a100a-122">Der Name des Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a100a-122">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="a100a-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="a100a-123">-SyncGroupName</span></span>
<span data-ttu-id="a100a-124">Der Name der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="a100a-124">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a100a-125">-SyncMemberAzureDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="a100a-125">-SyncMemberAzureDatabaseResourceId</span></span>
<span data-ttu-id="a100a-126">Die Ressourcen-ID für die Datenbank des Synchronisierungsmitglieds, die verwendet wird, wenn "UsePrivateLinkConnection" auf "true" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a100a-126">The resource ID for the sync member database, used if UsePrivateLinkConnection is set to true.</span></span>

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

### <span data-ttu-id="a100a-127">-UsePrivateLinkConnection</span><span class="sxs-lookup"><span data-stu-id="a100a-127">-UsePrivateLinkConnection</span></span>
<span data-ttu-id="a100a-128">Gibt an, ob beim Herstellen einer Verbindung mit diesem Synchronisierungsmitglied ein privater Link verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a100a-128">Whether to use private link when connecting to this sync member.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a100a-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a100a-129">-Confirm</span></span>
<span data-ttu-id="a100a-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a100a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a100a-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a100a-131">-WhatIf</span></span>
<span data-ttu-id="a100a-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a100a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a100a-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a100a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a100a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a100a-134">CommonParameters</span></span>
<span data-ttu-id="a100a-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a100a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a100a-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a100a-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a100a-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a100a-137">INPUTS</span></span>

### <span data-ttu-id="a100a-138">System.String</span><span class="sxs-lookup"><span data-stu-id="a100a-138">System.String</span></span>

## <span data-ttu-id="a100a-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a100a-139">OUTPUTS</span></span>

### <span data-ttu-id="a100a-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="a100a-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="a100a-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a100a-141">NOTES</span></span>

## <span data-ttu-id="a100a-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a100a-142">RELATED LINKS</span></span>

[<span data-ttu-id="a100a-143">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="a100a-143">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="a100a-144">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="a100a-144">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

[<span data-ttu-id="a100a-145">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="a100a-145">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)

