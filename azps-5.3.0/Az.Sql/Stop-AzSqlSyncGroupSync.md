---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqlsyncgroupsync
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlSyncGroupSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlSyncGroupSync.md
ms.openlocfilehash: d09f0032d44a0558c1052f1dcfc3a3c94a7dff00
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467999"
---
# <span data-ttu-id="7c0ac-101">Stop-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="7c0ac-101">Stop-AzSqlSyncGroupSync</span></span>

## <span data-ttu-id="7c0ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c0ac-102">SYNOPSIS</span></span>
<span data-ttu-id="7c0ac-103">Beendet die Synchronisierung einer Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="7c0ac-103">Stops a sync group synchronization.</span></span>

## <span data-ttu-id="7c0ac-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7c0ac-104">SYNTAX</span></span>

```
Stop-AzSqlSyncGroupSync [-SyncGroupName] <String> [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7c0ac-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7c0ac-105">DESCRIPTION</span></span>
<span data-ttu-id="7c0ac-106">Das **Cmdlet "Stop-AzSqlSyncGroupSync"** beendet die Synchronisierung einer Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="7c0ac-106">The **Stop-AzSqlSyncGroupSync** cmdlet stops a sync group synchronization.</span></span>

## <span data-ttu-id="7c0ac-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7c0ac-107">EXAMPLES</span></span>

### <span data-ttu-id="7c0ac-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7c0ac-108">Example 1</span></span>
```
PS C:\> Stop-AzSqlSyncGroupSync -SyncGroupName mysg [-ServerName] mysrv [-DatabaseName] mydb [-ResourceGroupName] myrg
```

<span data-ttu-id="7c0ac-109">Mit diesem Befehl wird die Synchronisierung beendet, die für die Synchronisierungsgruppe "mysg" ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7c0ac-109">This command stops the synchronization which is ongoing for the sync group mysg.</span></span>

## <span data-ttu-id="7c0ac-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7c0ac-110">PARAMETERS</span></span>

### <span data-ttu-id="7c0ac-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7c0ac-111">-DatabaseName</span></span>
<span data-ttu-id="7c0ac-112">Der Name der Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="7c0ac-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="7c0ac-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c0ac-113">-DefaultProfile</span></span>
<span data-ttu-id="7c0ac-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="7c0ac-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7c0ac-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7c0ac-115">-PassThru</span></span>
<span data-ttu-id="7c0ac-116">Definiert, ob die Synchronisierungsgruppe zurückgeben wird.</span><span class="sxs-lookup"><span data-stu-id="7c0ac-116">Defines Whether return the sync group</span></span>

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

### <span data-ttu-id="7c0ac-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c0ac-117">-ResourceGroupName</span></span>
<span data-ttu-id="7c0ac-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7c0ac-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="7c0ac-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7c0ac-119">-ServerName</span></span>
<span data-ttu-id="7c0ac-120">Der Name des Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="7c0ac-120">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="7c0ac-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="7c0ac-121">-SyncGroupName</span></span>
<span data-ttu-id="7c0ac-122">Der Name der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="7c0ac-122">The sync group name.</span></span>

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

### <span data-ttu-id="7c0ac-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7c0ac-123">-Confirm</span></span>
<span data-ttu-id="7c0ac-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7c0ac-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c0ac-125">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="7c0ac-125">-WhatIf</span></span>
<span data-ttu-id="7c0ac-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7c0ac-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c0ac-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7c0ac-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c0ac-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c0ac-128">CommonParameters</span></span>
<span data-ttu-id="7c0ac-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c0ac-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c0ac-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7c0ac-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c0ac-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7c0ac-131">INPUTS</span></span>

### <span data-ttu-id="7c0ac-132">System.String</span><span class="sxs-lookup"><span data-stu-id="7c0ac-132">System.String</span></span>

## <span data-ttu-id="7c0ac-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7c0ac-133">OUTPUTS</span></span>

### <span data-ttu-id="7c0ac-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="7c0ac-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="7c0ac-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7c0ac-135">NOTES</span></span>

## <span data-ttu-id="7c0ac-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7c0ac-136">RELATED LINKS</span></span>

[<span data-ttu-id="7c0ac-137">Start-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="7c0ac-137">Start-AzSqlSyncGroupSync</span></span>](./Start-AzSqlSyncGroupSync.md)

