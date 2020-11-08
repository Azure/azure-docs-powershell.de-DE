---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncMember.md
ms.openlocfilehash: c508dc9352bfcf70a9d3bad088f2b75de98db43d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003368"
---
# <span data-ttu-id="366ec-101">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="366ec-101">Remove-AzSqlSyncMember</span></span>

## <span data-ttu-id="366ec-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="366ec-102">SYNOPSIS</span></span>
<span data-ttu-id="366ec-103">Entfernt ein Azure SQL-Daten Bank Synchronisierungs Mitglied.</span><span class="sxs-lookup"><span data-stu-id="366ec-103">Removes an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="366ec-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="366ec-104">SYNTAX</span></span>

```
Remove-AzSqlSyncMember -Name <String> [-Force] [-PassThru] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="366ec-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="366ec-105">DESCRIPTION</span></span>
<span data-ttu-id="366ec-106">Das Cmdlet **Remove-AzSqlSyncMember** entfernt ein Azure SQL-Daten Bank Synchronisierungs Mitglied.</span><span class="sxs-lookup"><span data-stu-id="366ec-106">The **Remove-AzSqlSyncMember** cmdlet removes an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="366ec-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="366ec-107">EXAMPLES</span></span>

### <span data-ttu-id="366ec-108">Beispiel 1: Entfernen eines Synchronisierungs Mitglieds</span><span class="sxs-lookup"><span data-stu-id="366ec-108">Example 1: Remove a sync member</span></span>
```
PS C:\>Remove-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -Name "syncMember01"
```

<span data-ttu-id="366ec-109">Dieser Befehl entfernt das Azure SQL-Daten Bank Synchronisierungselement mit dem Namen syncMember01.</span><span class="sxs-lookup"><span data-stu-id="366ec-109">This command removes the Azure SQL Database Sync Member named syncMember01.</span></span>

## <span data-ttu-id="366ec-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="366ec-110">PARAMETERS</span></span>

### <span data-ttu-id="366ec-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="366ec-111">-DatabaseName</span></span>
<span data-ttu-id="366ec-112">Der Name der Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="366ec-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="366ec-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="366ec-113">-DefaultProfile</span></span>
<span data-ttu-id="366ec-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="366ec-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="366ec-115">-Force</span><span class="sxs-lookup"><span data-stu-id="366ec-115">-Force</span></span>
<span data-ttu-id="366ec-116">Bestätigungsmeldung zum Durchführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="366ec-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="366ec-117">-Name</span><span class="sxs-lookup"><span data-stu-id="366ec-117">-Name</span></span>
<span data-ttu-id="366ec-118">Der Name des Synchronisierungs Mitglieds.</span><span class="sxs-lookup"><span data-stu-id="366ec-118">The sync member name.</span></span>

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

### <span data-ttu-id="366ec-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="366ec-119">-PassThru</span></span>
<span data-ttu-id="366ec-120">Definiert, ob der entfernte Synchronisierungs Member zurückgegeben wird</span><span class="sxs-lookup"><span data-stu-id="366ec-120">Defines Whether return the removed sync member</span></span>

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

### <span data-ttu-id="366ec-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="366ec-121">-ResourceGroupName</span></span>
<span data-ttu-id="366ec-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="366ec-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="366ec-123">-Servername</span><span class="sxs-lookup"><span data-stu-id="366ec-123">-ServerName</span></span>
<span data-ttu-id="366ec-124">Der Name des Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="366ec-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="366ec-125">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="366ec-125">-SyncGroupName</span></span>
<span data-ttu-id="366ec-126">Der Name der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="366ec-126">The sync group name.</span></span>

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

### <span data-ttu-id="366ec-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="366ec-127">-Confirm</span></span>
<span data-ttu-id="366ec-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="366ec-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="366ec-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="366ec-129">-WhatIf</span></span>
<span data-ttu-id="366ec-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="366ec-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="366ec-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="366ec-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="366ec-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="366ec-132">CommonParameters</span></span>
<span data-ttu-id="366ec-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="366ec-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="366ec-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="366ec-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="366ec-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="366ec-135">INPUTS</span></span>

### <span data-ttu-id="366ec-136">System. String</span><span class="sxs-lookup"><span data-stu-id="366ec-136">System.String</span></span>

## <span data-ttu-id="366ec-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="366ec-137">OUTPUTS</span></span>

### <span data-ttu-id="366ec-138">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="366ec-138">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="366ec-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="366ec-139">NOTES</span></span>

## <span data-ttu-id="366ec-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="366ec-140">RELATED LINKS</span></span>

[<span data-ttu-id="366ec-141">Neu – AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="366ec-141">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="366ec-142">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="366ec-142">Update-AzSqlSyncMember</span></span>](./Update-AzSqlSyncMember.md)

[<span data-ttu-id="366ec-143">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="366ec-143">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

