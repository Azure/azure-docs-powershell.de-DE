---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncMember.md
ms.openlocfilehash: 58a6ee3d51af355c0824025f856ed1646fa23cf1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940912"
---
# <span data-ttu-id="aa75b-101">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="aa75b-101">Remove-AzSqlSyncMember</span></span>

## <span data-ttu-id="aa75b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa75b-102">SYNOPSIS</span></span>
<span data-ttu-id="aa75b-103">Entfernt ein Azure SQL Database Sync Member.</span><span class="sxs-lookup"><span data-stu-id="aa75b-103">Removes an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="aa75b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aa75b-104">SYNTAX</span></span>

```
Remove-AzSqlSyncMember -Name <String> [-Force] [-PassThru] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa75b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aa75b-105">DESCRIPTION</span></span>
<span data-ttu-id="aa75b-106">Das **Cmdlet Remove-AzSqlSyncMember** entfernt ein Azure SQL Database Sync Member.</span><span class="sxs-lookup"><span data-stu-id="aa75b-106">The **Remove-AzSqlSyncMember** cmdlet removes an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="aa75b-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="aa75b-107">EXAMPLES</span></span>

### <span data-ttu-id="aa75b-108">Beispiel 1: Entfernen eines Synchronisierungsmitglieds</span><span class="sxs-lookup"><span data-stu-id="aa75b-108">Example 1: Remove a sync member</span></span>
```
PS C:\>Remove-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -Name "syncMember01"
```

<span data-ttu-id="aa75b-109">Mit diesem Befehl wird das Azure SQL Database Sync Member namens syncMember01 entfernt.</span><span class="sxs-lookup"><span data-stu-id="aa75b-109">This command removes the Azure SQL Database Sync Member named syncMember01.</span></span>

## <span data-ttu-id="aa75b-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="aa75b-110">PARAMETERS</span></span>

### <span data-ttu-id="aa75b-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="aa75b-111">-DatabaseName</span></span>
<span data-ttu-id="aa75b-112">Der Name der Azure SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="aa75b-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="aa75b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa75b-113">-DefaultProfile</span></span>
<span data-ttu-id="aa75b-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="aa75b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aa75b-115">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="aa75b-115">-Force</span></span>
<span data-ttu-id="aa75b-116">Bestätigungsmeldung überspringen zum Ausführen der Aktion</span><span class="sxs-lookup"><span data-stu-id="aa75b-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="aa75b-117">-Name</span><span class="sxs-lookup"><span data-stu-id="aa75b-117">-Name</span></span>
<span data-ttu-id="aa75b-118">Der Name des Synchronisierungsmitglieds.</span><span class="sxs-lookup"><span data-stu-id="aa75b-118">The sync member name.</span></span>

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

### <span data-ttu-id="aa75b-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aa75b-119">-PassThru</span></span>
<span data-ttu-id="aa75b-120">Definiert, ob das entfernte Synchronisierungsm member zurückgeben wird</span><span class="sxs-lookup"><span data-stu-id="aa75b-120">Defines Whether return the removed sync member</span></span>

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

### <span data-ttu-id="aa75b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa75b-121">-ResourceGroupName</span></span>
<span data-ttu-id="aa75b-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="aa75b-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="aa75b-123">-Servername</span><span class="sxs-lookup"><span data-stu-id="aa75b-123">-ServerName</span></span>
<span data-ttu-id="aa75b-124">Der Name der Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="aa75b-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="aa75b-125">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="aa75b-125">-SyncGroupName</span></span>
<span data-ttu-id="aa75b-126">Der Name der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="aa75b-126">The sync group name.</span></span>

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

### <span data-ttu-id="aa75b-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="aa75b-127">-Confirm</span></span>
<span data-ttu-id="aa75b-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="aa75b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa75b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa75b-129">-WhatIf</span></span>
<span data-ttu-id="aa75b-130">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="aa75b-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa75b-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="aa75b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa75b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa75b-132">CommonParameters</span></span>
<span data-ttu-id="aa75b-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa75b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa75b-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aa75b-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa75b-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="aa75b-135">INPUTS</span></span>

### <span data-ttu-id="aa75b-136">System.String</span><span class="sxs-lookup"><span data-stu-id="aa75b-136">System.String</span></span>

## <span data-ttu-id="aa75b-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="aa75b-137">OUTPUTS</span></span>

### <span data-ttu-id="aa75b-138">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="aa75b-138">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="aa75b-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="aa75b-139">NOTES</span></span>

## <span data-ttu-id="aa75b-140">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="aa75b-140">RELATED LINKS</span></span>

[<span data-ttu-id="aa75b-141">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="aa75b-141">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="aa75b-142">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="aa75b-142">Update-AzSqlSyncMember</span></span>](./Update-AzSqlSyncMember.md)

[<span data-ttu-id="aa75b-143">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="aa75b-143">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

