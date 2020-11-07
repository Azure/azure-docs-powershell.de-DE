---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncMember.md
ms.openlocfilehash: 34db2f2307d60f1653b0a806350d96fa9e3380af
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659024"
---
# <span data-ttu-id="dbbfa-101">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="dbbfa-101">Remove-AzSqlSyncMember</span></span>

## <span data-ttu-id="dbbfa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dbbfa-102">SYNOPSIS</span></span>
<span data-ttu-id="dbbfa-103">Entfernt ein Azure SQL-Daten Bank Synchronisierungs Mitglied.</span><span class="sxs-lookup"><span data-stu-id="dbbfa-103">Removes an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="dbbfa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dbbfa-104">SYNTAX</span></span>

```
Remove-AzSqlSyncMember -Name <String> [-Force] [-PassThru] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dbbfa-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dbbfa-105">DESCRIPTION</span></span>
<span data-ttu-id="dbbfa-106">Das Cmdlet **Remove-AzSqlSyncMember** entfernt ein Azure SQL-Daten Bank Synchronisierungs Mitglied.</span><span class="sxs-lookup"><span data-stu-id="dbbfa-106">The **Remove-AzSqlSyncMember** cmdlet removes an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="dbbfa-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dbbfa-107">EXAMPLES</span></span>

### <span data-ttu-id="dbbfa-108">Beispiel 1: Entfernen eines Synchronisierungs Mitglieds</span><span class="sxs-lookup"><span data-stu-id="dbbfa-108">Example 1: Remove a sync member</span></span>
```
PS C:\>Remove-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -Name "syncMember01"
```

<span data-ttu-id="dbbfa-109">Dieser Befehl entfernt das Azure SQL-Daten Bank Synchronisierungselement mit dem Namen syncMember01.</span><span class="sxs-lookup"><span data-stu-id="dbbfa-109">This command removes the Azure SQL Database Sync Member named syncMember01.</span></span>

## <span data-ttu-id="dbbfa-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="dbbfa-110">PARAMETERS</span></span>

### <span data-ttu-id="dbbfa-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="dbbfa-111">-DatabaseName</span></span>
<span data-ttu-id="dbbfa-112">Der Name der Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="dbbfa-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="dbbfa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbbfa-113">-DefaultProfile</span></span>
<span data-ttu-id="dbbfa-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="dbbfa-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dbbfa-115">-Force</span><span class="sxs-lookup"><span data-stu-id="dbbfa-115">-Force</span></span>
<span data-ttu-id="dbbfa-116">Bestätigungsmeldung zum Durchführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="dbbfa-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="dbbfa-117">-Name</span><span class="sxs-lookup"><span data-stu-id="dbbfa-117">-Name</span></span>
<span data-ttu-id="dbbfa-118">Der Name des Synchronisierungs Mitglieds.</span><span class="sxs-lookup"><span data-stu-id="dbbfa-118">The sync member name.</span></span>

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

### <span data-ttu-id="dbbfa-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dbbfa-119">-PassThru</span></span>
<span data-ttu-id="dbbfa-120">Definiert, ob der entfernte Synchronisierungs Member zurückgegeben wird</span><span class="sxs-lookup"><span data-stu-id="dbbfa-120">Defines Whether return the removed sync member</span></span>

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

### <span data-ttu-id="dbbfa-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbbfa-121">-ResourceGroupName</span></span>
<span data-ttu-id="dbbfa-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="dbbfa-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="dbbfa-123">-Servername</span><span class="sxs-lookup"><span data-stu-id="dbbfa-123">-ServerName</span></span>
<span data-ttu-id="dbbfa-124">Der Name des Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="dbbfa-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="dbbfa-125">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="dbbfa-125">-SyncGroupName</span></span>
<span data-ttu-id="dbbfa-126">Der Name der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="dbbfa-126">The sync group name.</span></span>

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

### <span data-ttu-id="dbbfa-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dbbfa-127">-Confirm</span></span>
<span data-ttu-id="dbbfa-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dbbfa-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbbfa-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbbfa-129">-WhatIf</span></span>
<span data-ttu-id="dbbfa-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dbbfa-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbbfa-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dbbfa-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbbfa-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbbfa-132">CommonParameters</span></span>
<span data-ttu-id="dbbfa-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbbfa-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbbfa-134">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dbbfa-134">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbbfa-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dbbfa-135">INPUTS</span></span>

### <span data-ttu-id="dbbfa-136">System. String</span><span class="sxs-lookup"><span data-stu-id="dbbfa-136">System.String</span></span>

## <span data-ttu-id="dbbfa-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dbbfa-137">OUTPUTS</span></span>

### <span data-ttu-id="dbbfa-138">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="dbbfa-138">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="dbbfa-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="dbbfa-139">NOTES</span></span>

## <span data-ttu-id="dbbfa-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dbbfa-140">RELATED LINKS</span></span>

[<span data-ttu-id="dbbfa-141">Neu – AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="dbbfa-141">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="dbbfa-142">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="dbbfa-142">Update-AzSqlSyncMember</span></span>](./Update-AzSqlSyncMember.md)

[<span data-ttu-id="dbbfa-143">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="dbbfa-143">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

