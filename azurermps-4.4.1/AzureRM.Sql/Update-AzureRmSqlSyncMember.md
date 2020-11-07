---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncMember.md
ms.openlocfilehash: f72091d142b57cc7ef3897eceda2219634376daf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663299"
---
# <span data-ttu-id="ef4a9-101">Update-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="ef4a9-101">Update-AzureRmSqlSyncMember</span></span>

## <span data-ttu-id="ef4a9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ef4a9-102">SYNOPSIS</span></span>
<span data-ttu-id="ef4a9-103">Aktualisiert ein Azure SQL-Daten Bank Synchronisierungs Mitglied.</span><span class="sxs-lookup"><span data-stu-id="ef4a9-103">Updates an Azure SQL Database Sync Member.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef4a9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef4a9-104">SYNTAX</span></span>

```
Update-AzureRmSqlSyncMember -Name <String> -MemberDatabaseCredential <PSCredential> [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef4a9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ef4a9-105">DESCRIPTION</span></span>
<span data-ttu-id="ef4a9-106">Das Cmdlet **Update-AzureRmSqlSyncGroup** ändert die Eigenschaften eines Azure SQL-Daten Bank Synchronisierungs Elements.</span><span class="sxs-lookup"><span data-stu-id="ef4a9-106">The **Update-AzureRmSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="ef4a9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ef4a9-107">EXAMPLES</span></span>

### <span data-ttu-id="ef4a9-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ef4a9-108">Example 1</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> Update-AzureRmSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01"
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

<span data-ttu-id="ef4a9-109">Mit diesem Befehl wird das Administratorkennwort für die Mitgliedsdatenbank zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="ef4a9-109">This command resets the administrator password for the member database.</span></span>

## <span data-ttu-id="ef4a9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ef4a9-110">PARAMETERS</span></span>

### <span data-ttu-id="ef4a9-111">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ef4a9-111">-Confirm</span></span>
<span data-ttu-id="ef4a9-112">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ef4a9-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef4a9-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ef4a9-113">-DatabaseName</span></span>
<span data-ttu-id="ef4a9-114">Der Name der Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="ef4a9-114">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="ef4a9-115">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="ef4a9-115">-MemberDatabaseCredential</span></span>
<span data-ttu-id="ef4a9-116">Die Anmeldeinformationen (Benutzername und Kennwort) der Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="ef4a9-116">The credential (username and password) of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="ef4a9-117">-Name</span><span class="sxs-lookup"><span data-stu-id="ef4a9-117">-Name</span></span>
<span data-ttu-id="ef4a9-118">Der Name des Synchronisierungs Mitglieds.</span><span class="sxs-lookup"><span data-stu-id="ef4a9-118">The sync member name.</span></span>

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

### <span data-ttu-id="ef4a9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef4a9-119">-ResourceGroupName</span></span>
<span data-ttu-id="ef4a9-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ef4a9-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="ef4a9-121">-Servername</span><span class="sxs-lookup"><span data-stu-id="ef4a9-121">-ServerName</span></span>
<span data-ttu-id="ef4a9-122">Der Name des Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ef4a9-122">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="ef4a9-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="ef4a9-123">-SyncGroupName</span></span>
<span data-ttu-id="ef4a9-124">Der Name der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="ef4a9-124">The sync group name.</span></span>

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

### <span data-ttu-id="ef4a9-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef4a9-125">-WhatIf</span></span>
<span data-ttu-id="ef4a9-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ef4a9-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef4a9-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ef4a9-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef4a9-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef4a9-128">-DefaultProfile</span></span>
<span data-ttu-id="ef4a9-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ef4a9-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef4a9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef4a9-130">CommonParameters</span></span>
<span data-ttu-id="ef4a9-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef4a9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef4a9-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef4a9-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef4a9-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ef4a9-133">INPUTS</span></span>

## <span data-ttu-id="ef4a9-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ef4a9-134">OUTPUTS</span></span>

### <span data-ttu-id="ef4a9-135">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="ef4a9-135">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="ef4a9-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="ef4a9-136">NOTES</span></span>

## <span data-ttu-id="ef4a9-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ef4a9-137">RELATED LINKS</span></span>

[<span data-ttu-id="ef4a9-138">Neu – AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="ef4a9-138">New-AzureRmSqlSyncMember</span></span>](./New-AzureRmSqlSyncMember.md)

[<span data-ttu-id="ef4a9-139">Get-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="ef4a9-139">Get-AzureRmSqlSyncMember</span></span>](./Get-AzureRmSqlSyncMember.md)

[<span data-ttu-id="ef4a9-140">Remove-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="ef4a9-140">Remove-AzureRmSqlSyncMember</span></span>](./Remove-AzureRmSqlSyncMember.md)

