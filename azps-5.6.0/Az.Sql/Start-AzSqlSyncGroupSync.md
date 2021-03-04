---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/start-azsqlsyncgroupsync
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlSyncGroupSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlSyncGroupSync.md
ms.openlocfilehash: 13f58f454fb84a4bcd003afd84761197d41c16ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946859"
---
# <span data-ttu-id="9dad4-101">Start-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="9dad4-101">Start-AzSqlSyncGroupSync</span></span>

## <span data-ttu-id="9dad4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9dad4-102">SYNOPSIS</span></span>
<span data-ttu-id="9dad4-103">Startet die Synchronisierung einer Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="9dad4-103">Starts a sync group synchronization.</span></span>

## <span data-ttu-id="9dad4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9dad4-104">SYNTAX</span></span>

```
Start-AzSqlSyncGroupSync [-SyncGroupName] <String> [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9dad4-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9dad4-105">DESCRIPTION</span></span>
<span data-ttu-id="9dad4-106">Das **Cmdlet Start-AzSqlSyncGroupSync** startet eine Synchronisierungsgruppesynchronisierung.</span><span class="sxs-lookup"><span data-stu-id="9dad4-106">The **Start-AzSqlSyncGroupSync** cmdlet starts a sync group synchronization.</span></span>

## <span data-ttu-id="9dad4-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9dad4-107">EXAMPLES</span></span>

### <span data-ttu-id="9dad4-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9dad4-108">Example 1</span></span>
```
PS C:\> Start-AzSqlSyncGroupSync -SyncGroupName mysg [-ServerName] mysrv [-DatabaseName] mydb [-ResourceGroupName] myrg
```

<span data-ttu-id="9dad4-109">Mit diesem Befehl wird eine Synchronisierungsrunde für die Synchronisierungsgruppe mysg gestartet.</span><span class="sxs-lookup"><span data-stu-id="9dad4-109">This command starts a round of synchronization for the sync group mysg.</span></span>

## <span data-ttu-id="9dad4-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9dad4-110">PARAMETERS</span></span>

### <span data-ttu-id="9dad4-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9dad4-111">-DatabaseName</span></span>
<span data-ttu-id="9dad4-112">Der Name der Azure SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="9dad4-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="9dad4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dad4-113">-DefaultProfile</span></span>
<span data-ttu-id="9dad4-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="9dad4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9dad4-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9dad4-115">-PassThru</span></span>
<span data-ttu-id="9dad4-116">Definiert, ob die Synchronisierungsgruppe zurückgeben wird</span><span class="sxs-lookup"><span data-stu-id="9dad4-116">Defines Whether return the sync group</span></span>

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

### <span data-ttu-id="9dad4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9dad4-117">-ResourceGroupName</span></span>
<span data-ttu-id="9dad4-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9dad4-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="9dad4-119">-Servername</span><span class="sxs-lookup"><span data-stu-id="9dad4-119">-ServerName</span></span>
<span data-ttu-id="9dad4-120">Der Name der Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="9dad4-120">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="9dad4-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="9dad4-121">-SyncGroupName</span></span>
<span data-ttu-id="9dad4-122">Der Name der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="9dad4-122">The sync group name.</span></span>

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

### <span data-ttu-id="9dad4-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9dad4-123">-Confirm</span></span>
<span data-ttu-id="9dad4-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9dad4-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9dad4-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9dad4-125">-WhatIf</span></span>
<span data-ttu-id="9dad4-126">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9dad4-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9dad4-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9dad4-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9dad4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dad4-128">CommonParameters</span></span>
<span data-ttu-id="9dad4-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9dad4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dad4-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9dad4-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dad4-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9dad4-131">INPUTS</span></span>

### <span data-ttu-id="9dad4-132">System.String</span><span class="sxs-lookup"><span data-stu-id="9dad4-132">System.String</span></span>

## <span data-ttu-id="9dad4-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9dad4-133">OUTPUTS</span></span>

### <span data-ttu-id="9dad4-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="9dad4-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="9dad4-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="9dad4-135">NOTES</span></span>

## <span data-ttu-id="9dad4-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="9dad4-136">RELATED LINKS</span></span>

[<span data-ttu-id="9dad4-137">Stop-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="9dad4-137">Stop-AzSqlSyncGroupSync</span></span>](./Stop-AzSqlSyncGroupSync.md)

