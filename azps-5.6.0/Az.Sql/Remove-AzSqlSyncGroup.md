---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncGroup.md
ms.openlocfilehash: ce69f6b087a7ed61f415e3d6a649f757bb10178f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940928"
---
# <span data-ttu-id="3067f-101">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="3067f-101">Remove-AzSqlSyncGroup</span></span>

## <span data-ttu-id="3067f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3067f-102">SYNOPSIS</span></span>
<span data-ttu-id="3067f-103">Entfernt eine Azure SQL Database Sync Group.</span><span class="sxs-lookup"><span data-stu-id="3067f-103">Removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="3067f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3067f-104">SYNTAX</span></span>

```
Remove-AzSqlSyncGroup [-Name] <String> [-Force] [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3067f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3067f-105">DESCRIPTION</span></span>
<span data-ttu-id="3067f-106">Das **Cmdlet Remove-AzSqlSyncGroup** entfernt eine Azure SQL Database Sync Group.</span><span class="sxs-lookup"><span data-stu-id="3067f-106">The **Remove-AzSqlSyncGroup** cmdlet removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="3067f-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3067f-107">EXAMPLES</span></span>

### <span data-ttu-id="3067f-108">Beispiel 1: Entfernen einer Synchronisierungsgruppe</span><span class="sxs-lookup"><span data-stu-id="3067f-108">Example 1: Remove a sync group</span></span>
```
PS C:\>Remove-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -Name "syncGroup01"
```

<span data-ttu-id="3067f-109">Mit diesem Befehl wird die Azure SQL-Datenbanksynchronisierungsgruppe mit dem Namen syncGroup01 entfernt.</span><span class="sxs-lookup"><span data-stu-id="3067f-109">This command removes the Azure SQL Database Sync Group named syncGroup01.</span></span>

## <span data-ttu-id="3067f-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3067f-110">PARAMETERS</span></span>

### <span data-ttu-id="3067f-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3067f-111">-DatabaseName</span></span>
<span data-ttu-id="3067f-112">Der Name der Azure SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="3067f-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="3067f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3067f-113">-DefaultProfile</span></span>
<span data-ttu-id="3067f-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="3067f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3067f-115">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="3067f-115">-Force</span></span>
<span data-ttu-id="3067f-116">Bestätigungsmeldung überspringen zum Ausführen der Aktion</span><span class="sxs-lookup"><span data-stu-id="3067f-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="3067f-117">-Name</span><span class="sxs-lookup"><span data-stu-id="3067f-117">-Name</span></span>
<span data-ttu-id="3067f-118">Der Name der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="3067f-118">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3067f-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3067f-119">-PassThru</span></span>
<span data-ttu-id="3067f-120">Definiert, ob die entfernte Synchronisierungsgruppe zurückgeben wird</span><span class="sxs-lookup"><span data-stu-id="3067f-120">Defines Whether return the removed sync group</span></span>

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

### <span data-ttu-id="3067f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3067f-121">-ResourceGroupName</span></span>
<span data-ttu-id="3067f-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3067f-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="3067f-123">-Servername</span><span class="sxs-lookup"><span data-stu-id="3067f-123">-ServerName</span></span>
<span data-ttu-id="3067f-124">Der Name der Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3067f-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="3067f-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3067f-125">-Confirm</span></span>
<span data-ttu-id="3067f-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3067f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3067f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3067f-127">-WhatIf</span></span>
<span data-ttu-id="3067f-128">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3067f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3067f-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3067f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3067f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3067f-130">CommonParameters</span></span>
<span data-ttu-id="3067f-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3067f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3067f-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3067f-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3067f-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3067f-133">INPUTS</span></span>

### <span data-ttu-id="3067f-134">System.String</span><span class="sxs-lookup"><span data-stu-id="3067f-134">System.String</span></span>

## <span data-ttu-id="3067f-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3067f-135">OUTPUTS</span></span>

### <span data-ttu-id="3067f-136">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="3067f-136">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="3067f-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="3067f-137">NOTES</span></span>

## <span data-ttu-id="3067f-138">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="3067f-138">RELATED LINKS</span></span>

[<span data-ttu-id="3067f-139">New-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="3067f-139">New-AzSqlSyncGroup</span></span>](./New-AzSqlSyncGroup.md)

[<span data-ttu-id="3067f-140">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="3067f-140">Update-AzSqlSyncGroup</span></span>](./Update-AzSqlSyncGroup.md)

[<span data-ttu-id="3067f-141">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="3067f-141">Get-AzSqlSyncGroup</span></span>](./Get-AzSqlSyncGroup.md)

