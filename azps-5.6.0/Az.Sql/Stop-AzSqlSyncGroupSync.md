---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/stop-azsqlsyncgroupsync
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlSyncGroupSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlSyncGroupSync.md
ms.openlocfilehash: ea8390de90fff5fb1e228884b131551a5be86e48
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939368"
---
# <span data-ttu-id="854b6-101">Stop-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="854b6-101">Stop-AzSqlSyncGroupSync</span></span>

## <span data-ttu-id="854b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="854b6-102">SYNOPSIS</span></span>
<span data-ttu-id="854b6-103">Beendet die Synchronisierung einer Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="854b6-103">Stops a sync group synchronization.</span></span>

## <span data-ttu-id="854b6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="854b6-104">SYNTAX</span></span>

```
Stop-AzSqlSyncGroupSync [-SyncGroupName] <String> [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="854b6-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="854b6-105">DESCRIPTION</span></span>
<span data-ttu-id="854b6-106">Das **Cmdlet Stop-AzSqlSyncGroupSync** beendet die Synchronisierung einer Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="854b6-106">The **Stop-AzSqlSyncGroupSync** cmdlet stops a sync group synchronization.</span></span>

## <span data-ttu-id="854b6-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="854b6-107">EXAMPLES</span></span>

### <span data-ttu-id="854b6-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="854b6-108">Example 1</span></span>
```
PS C:\> Stop-AzSqlSyncGroupSync -SyncGroupName mysg [-ServerName] mysrv [-DatabaseName] mydb [-ResourceGroupName] myrg
```

<span data-ttu-id="854b6-109">Mit diesem Befehl wird die Synchronisierung beendet, die für die Synchronisierungsgruppe mysg ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="854b6-109">This command stops the synchronization which is ongoing for the sync group mysg.</span></span>

## <span data-ttu-id="854b6-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="854b6-110">PARAMETERS</span></span>

### <span data-ttu-id="854b6-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="854b6-111">-DatabaseName</span></span>
<span data-ttu-id="854b6-112">Der Name der Azure SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="854b6-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="854b6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="854b6-113">-DefaultProfile</span></span>
<span data-ttu-id="854b6-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="854b6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="854b6-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="854b6-115">-PassThru</span></span>
<span data-ttu-id="854b6-116">Definiert, ob die Synchronisierungsgruppe zurückgeben wird</span><span class="sxs-lookup"><span data-stu-id="854b6-116">Defines Whether return the sync group</span></span>

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

### <span data-ttu-id="854b6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="854b6-117">-ResourceGroupName</span></span>
<span data-ttu-id="854b6-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="854b6-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="854b6-119">-Servername</span><span class="sxs-lookup"><span data-stu-id="854b6-119">-ServerName</span></span>
<span data-ttu-id="854b6-120">Der Name der Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="854b6-120">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="854b6-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="854b6-121">-SyncGroupName</span></span>
<span data-ttu-id="854b6-122">Der Name der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="854b6-122">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="854b6-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="854b6-123">-Confirm</span></span>
<span data-ttu-id="854b6-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="854b6-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="854b6-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="854b6-125">-WhatIf</span></span>
<span data-ttu-id="854b6-126">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="854b6-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="854b6-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="854b6-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="854b6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="854b6-128">CommonParameters</span></span>
<span data-ttu-id="854b6-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="854b6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="854b6-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="854b6-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="854b6-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="854b6-131">INPUTS</span></span>

### <span data-ttu-id="854b6-132">System.String</span><span class="sxs-lookup"><span data-stu-id="854b6-132">System.String</span></span>

## <span data-ttu-id="854b6-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="854b6-133">OUTPUTS</span></span>

### <span data-ttu-id="854b6-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="854b6-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="854b6-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="854b6-135">NOTES</span></span>

## <span data-ttu-id="854b6-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="854b6-136">RELATED LINKS</span></span>

[<span data-ttu-id="854b6-137">Start-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="854b6-137">Start-AzSqlSyncGroupSync</span></span>](./Start-AzSqlSyncGroupSync.md)

