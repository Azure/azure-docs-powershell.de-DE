---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncMember.md
ms.openlocfilehash: 5ef51d83cf2b4cc43693da1697ee15620db04ff7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497249"
---
# <span data-ttu-id="292d8-101">Remove-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="292d8-101">Remove-AzureRmSqlSyncMember</span></span>

## <span data-ttu-id="292d8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="292d8-102">SYNOPSIS</span></span>
<span data-ttu-id="292d8-103">Entfernt ein Azure SQL-Daten Bank Synchronisierungs Mitglied.</span><span class="sxs-lookup"><span data-stu-id="292d8-103">Removes an Azure SQL Database Sync Member.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="292d8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="292d8-104">SYNTAX</span></span>

```
Remove-AzureRmSqlSyncMember -Name <String> [-Force] [-PassThru] [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="292d8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="292d8-105">DESCRIPTION</span></span>
<span data-ttu-id="292d8-106">Das Cmdlet **Remove-AzureRmSqlSyncMember** entfernt ein Azure SQL-Daten Bank Synchronisierungs Mitglied.</span><span class="sxs-lookup"><span data-stu-id="292d8-106">The **Remove-AzureRmSqlSyncMember** cmdlet removes an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="292d8-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="292d8-107">EXAMPLES</span></span>

### <span data-ttu-id="292d8-108">Beispiel 1: Entfernen eines Synchronisierungs Mitglieds</span><span class="sxs-lookup"><span data-stu-id="292d8-108">Example 1: Remove a sync member</span></span>
```
PS C:\>Remove-AzureRmSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -Name "syncMember01"
```

<span data-ttu-id="292d8-109">Dieser Befehl entfernt das Azure SQL-Daten Bank Synchronisierungselement mit dem Namen syncMember01.</span><span class="sxs-lookup"><span data-stu-id="292d8-109">This command removes the Azure SQL Database Sync Member named syncMember01.</span></span>

## <span data-ttu-id="292d8-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="292d8-110">PARAMETERS</span></span>

### <span data-ttu-id="292d8-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="292d8-111">-DatabaseName</span></span>
<span data-ttu-id="292d8-112">Der Name der Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="292d8-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="292d8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="292d8-113">-DefaultProfile</span></span>
<span data-ttu-id="292d8-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="292d8-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="292d8-115">-Force</span><span class="sxs-lookup"><span data-stu-id="292d8-115">-Force</span></span>
<span data-ttu-id="292d8-116">Bestätigungsmeldung zum Durchführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="292d8-116">Skip confirmation message for performing the action</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="292d8-117">-Name</span><span class="sxs-lookup"><span data-stu-id="292d8-117">-Name</span></span>
<span data-ttu-id="292d8-118">Der Name des Synchronisierungs Mitglieds.</span><span class="sxs-lookup"><span data-stu-id="292d8-118">The sync member name.</span></span>

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

### <span data-ttu-id="292d8-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="292d8-119">-PassThru</span></span>
<span data-ttu-id="292d8-120">Definiert, ob der entfernte Synchronisierungs Member zurückgegeben wird</span><span class="sxs-lookup"><span data-stu-id="292d8-120">Defines Whether return the removed sync member</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="292d8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="292d8-121">-ResourceGroupName</span></span>
<span data-ttu-id="292d8-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="292d8-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="292d8-123">-Servername</span><span class="sxs-lookup"><span data-stu-id="292d8-123">-ServerName</span></span>
<span data-ttu-id="292d8-124">Der Name des Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="292d8-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="292d8-125">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="292d8-125">-SyncGroupName</span></span>
<span data-ttu-id="292d8-126">Der Name der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="292d8-126">The sync group name.</span></span>

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

### <span data-ttu-id="292d8-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="292d8-127">-Confirm</span></span>
<span data-ttu-id="292d8-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="292d8-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="292d8-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="292d8-129">-WhatIf</span></span>
<span data-ttu-id="292d8-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="292d8-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="292d8-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="292d8-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="292d8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="292d8-132">CommonParameters</span></span>
<span data-ttu-id="292d8-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="292d8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="292d8-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="292d8-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="292d8-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="292d8-135">INPUTS</span></span>

### <span data-ttu-id="292d8-136">System. String</span><span class="sxs-lookup"><span data-stu-id="292d8-136">System.String</span></span>

## <span data-ttu-id="292d8-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="292d8-137">OUTPUTS</span></span>

### <span data-ttu-id="292d8-138">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="292d8-138">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="292d8-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="292d8-139">NOTES</span></span>

## <span data-ttu-id="292d8-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="292d8-140">RELATED LINKS</span></span>

[<span data-ttu-id="292d8-141">Neu – AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="292d8-141">New-AzureRmSqlSyncMember</span></span>](./New-AzureRmSqlSyncMember.md)

[<span data-ttu-id="292d8-142">Update-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="292d8-142">Update-AzureRmSqlSyncMember</span></span>](./Update-AzureRmSqlSyncMember.md)

[<span data-ttu-id="292d8-143">Get-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="292d8-143">Get-AzureRmSqlSyncMember</span></span>](./Get-AzureRmSqlSyncMember.md)

