---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/update-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncMember.md
ms.openlocfilehash: 634ce84e355dbd106865b0f1072b693bd03a623b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846432"
---
# <span data-ttu-id="d35a1-101">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="d35a1-101">Update-AzSqlSyncMember</span></span>

## <span data-ttu-id="d35a1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d35a1-102">SYNOPSIS</span></span>
<span data-ttu-id="d35a1-103">Aktualisiert ein Azure SQL-Daten Bank Synchronisierungs Mitglied.</span><span class="sxs-lookup"><span data-stu-id="d35a1-103">Updates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="d35a1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d35a1-104">SYNTAX</span></span>

```
Update-AzSqlSyncMember -Name <String> -MemberDatabaseCredential <PSCredential> [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d35a1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d35a1-105">DESCRIPTION</span></span>
<span data-ttu-id="d35a1-106">Das Cmdlet **Update-AzSqlSyncGroup** ändert die Eigenschaften eines Azure SQL-Daten Bank Synchronisierungs Elements.</span><span class="sxs-lookup"><span data-stu-id="d35a1-106">The **Update-AzSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="d35a1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d35a1-107">EXAMPLES</span></span>

### <span data-ttu-id="d35a1-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d35a1-108">Example 1</span></span>
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

<span data-ttu-id="d35a1-109">Mit diesem Befehl wird das Administratorkennwort für die Mitgliedsdatenbank zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="d35a1-109">This command resets the administrator password for the member database.</span></span>

## <span data-ttu-id="d35a1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d35a1-110">PARAMETERS</span></span>

### <span data-ttu-id="d35a1-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d35a1-111">-DatabaseName</span></span>
<span data-ttu-id="d35a1-112">Der Name der Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="d35a1-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="d35a1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d35a1-113">-DefaultProfile</span></span>
<span data-ttu-id="d35a1-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="d35a1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d35a1-115">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="d35a1-115">-MemberDatabaseCredential</span></span>
<span data-ttu-id="d35a1-116">Die Anmeldeinformationen (Benutzername und Kennwort) der Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="d35a1-116">The credential (username and password) of the Azure SQL Database.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d35a1-117">-Name</span><span class="sxs-lookup"><span data-stu-id="d35a1-117">-Name</span></span>
<span data-ttu-id="d35a1-118">Der Name des Synchronisierungs Mitglieds.</span><span class="sxs-lookup"><span data-stu-id="d35a1-118">The sync member name.</span></span>

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

### <span data-ttu-id="d35a1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d35a1-119">-ResourceGroupName</span></span>
<span data-ttu-id="d35a1-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d35a1-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="d35a1-121">-Servername</span><span class="sxs-lookup"><span data-stu-id="d35a1-121">-ServerName</span></span>
<span data-ttu-id="d35a1-122">Der Name des Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d35a1-122">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="d35a1-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="d35a1-123">-SyncGroupName</span></span>
<span data-ttu-id="d35a1-124">Der Name der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="d35a1-124">The sync group name.</span></span>

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

### <span data-ttu-id="d35a1-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d35a1-125">-Confirm</span></span>
<span data-ttu-id="d35a1-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d35a1-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d35a1-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d35a1-127">-WhatIf</span></span>
<span data-ttu-id="d35a1-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d35a1-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d35a1-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d35a1-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d35a1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d35a1-130">CommonParameters</span></span>
<span data-ttu-id="d35a1-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d35a1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d35a1-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d35a1-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d35a1-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d35a1-133">INPUTS</span></span>

### <span data-ttu-id="d35a1-134">System. String</span><span class="sxs-lookup"><span data-stu-id="d35a1-134">System.String</span></span>

## <span data-ttu-id="d35a1-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d35a1-135">OUTPUTS</span></span>

### <span data-ttu-id="d35a1-136">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="d35a1-136">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="d35a1-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="d35a1-137">NOTES</span></span>

## <span data-ttu-id="d35a1-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d35a1-138">RELATED LINKS</span></span>

[<span data-ttu-id="d35a1-139">Neu – AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="d35a1-139">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="d35a1-140">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="d35a1-140">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

[<span data-ttu-id="d35a1-141">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="d35a1-141">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)

