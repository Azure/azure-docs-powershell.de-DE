---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/update-azurermsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncMember.md
ms.openlocfilehash: afaa0446b46fca343b4d53ae491c67ef1ceb923a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501337"
---
# <span data-ttu-id="2444d-101">Update-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="2444d-101">Update-AzureRmSqlSyncMember</span></span>

## <span data-ttu-id="2444d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2444d-102">SYNOPSIS</span></span>
<span data-ttu-id="2444d-103">Aktualisiert ein Azure SQL-Daten Bank Synchronisierungs Mitglied.</span><span class="sxs-lookup"><span data-stu-id="2444d-103">Updates an Azure SQL Database Sync Member.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2444d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2444d-104">SYNTAX</span></span>

```
Update-AzureRmSqlSyncMember -Name <String> -MemberDatabaseCredential <PSCredential> [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2444d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2444d-105">DESCRIPTION</span></span>
<span data-ttu-id="2444d-106">Das Cmdlet **Update-AzureRmSqlSyncGroup** ändert die Eigenschaften eines Azure SQL-Daten Bank Synchronisierungs Elements.</span><span class="sxs-lookup"><span data-stu-id="2444d-106">The **Update-AzureRmSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="2444d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2444d-107">EXAMPLES</span></span>

### <span data-ttu-id="2444d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2444d-108">Example 1</span></span>
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

<span data-ttu-id="2444d-109">Mit diesem Befehl wird das Administratorkennwort für die Mitgliedsdatenbank zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="2444d-109">This command resets the administrator password for the member database.</span></span>

## <span data-ttu-id="2444d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2444d-110">PARAMETERS</span></span>

### <span data-ttu-id="2444d-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2444d-111">-DatabaseName</span></span>
<span data-ttu-id="2444d-112">Der Name der Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="2444d-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="2444d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2444d-113">-DefaultProfile</span></span>
<span data-ttu-id="2444d-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="2444d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2444d-115">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="2444d-115">-MemberDatabaseCredential</span></span>
<span data-ttu-id="2444d-116">Die Anmeldeinformationen (Benutzername und Kennwort) der Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="2444d-116">The credential (username and password) of the Azure SQL Database.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2444d-117">-Name</span><span class="sxs-lookup"><span data-stu-id="2444d-117">-Name</span></span>
<span data-ttu-id="2444d-118">Der Name des Synchronisierungs Mitglieds.</span><span class="sxs-lookup"><span data-stu-id="2444d-118">The sync member name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SyncMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2444d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2444d-119">-ResourceGroupName</span></span>
<span data-ttu-id="2444d-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2444d-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="2444d-121">-Servername</span><span class="sxs-lookup"><span data-stu-id="2444d-121">-ServerName</span></span>
<span data-ttu-id="2444d-122">Der Name des Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="2444d-122">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="2444d-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="2444d-123">-SyncGroupName</span></span>
<span data-ttu-id="2444d-124">Der Name der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="2444d-124">The sync group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2444d-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2444d-125">-Confirm</span></span>
<span data-ttu-id="2444d-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2444d-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2444d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2444d-127">-WhatIf</span></span>
<span data-ttu-id="2444d-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2444d-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2444d-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2444d-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2444d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2444d-130">CommonParameters</span></span>
<span data-ttu-id="2444d-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2444d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2444d-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2444d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2444d-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2444d-133">INPUTS</span></span>

### <span data-ttu-id="2444d-134">Keine</span><span class="sxs-lookup"><span data-stu-id="2444d-134">None</span></span>
<span data-ttu-id="2444d-135">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="2444d-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2444d-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2444d-136">OUTPUTS</span></span>

### <span data-ttu-id="2444d-137">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="2444d-137">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="2444d-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="2444d-138">NOTES</span></span>

## <span data-ttu-id="2444d-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2444d-139">RELATED LINKS</span></span>

[<span data-ttu-id="2444d-140">Neu – AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="2444d-140">New-AzureRmSqlSyncMember</span></span>](./New-AzureRmSqlSyncMember.md)

[<span data-ttu-id="2444d-141">Get-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="2444d-141">Get-AzureRmSqlSyncMember</span></span>](./Get-AzureRmSqlSyncMember.md)

[<span data-ttu-id="2444d-142">Remove-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="2444d-142">Remove-AzureRmSqlSyncMember</span></span>](./Remove-AzureRmSqlSyncMember.md)

