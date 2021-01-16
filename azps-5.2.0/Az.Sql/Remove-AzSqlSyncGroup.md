---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncGroup.md
ms.openlocfilehash: 3a5da7972e70e3ebf9c86df62b2bbc79651e72a5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98293273"
---
# <span data-ttu-id="d0b02-101">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="d0b02-101">Remove-AzSqlSyncGroup</span></span>

## <span data-ttu-id="d0b02-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0b02-102">SYNOPSIS</span></span>
<span data-ttu-id="d0b02-103">Entfernt eine Azure SQL-Datenbanksynchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="d0b02-103">Removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="d0b02-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d0b02-104">SYNTAX</span></span>

```
Remove-AzSqlSyncGroup [-Name] <String> [-Force] [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d0b02-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d0b02-105">DESCRIPTION</span></span>
<span data-ttu-id="d0b02-106">Das **Cmdlet "Remove-AzSqlSyncGroup"** entfernt eine Azure SQL Database Sync Group.</span><span class="sxs-lookup"><span data-stu-id="d0b02-106">The **Remove-AzSqlSyncGroup** cmdlet removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="d0b02-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d0b02-107">EXAMPLES</span></span>

### <span data-ttu-id="d0b02-108">Beispiel 1: Entfernen einer Synchronisierungsgruppe</span><span class="sxs-lookup"><span data-stu-id="d0b02-108">Example 1: Remove a sync group</span></span>
```
PS C:\>Remove-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -Name "syncGroup01"
```

<span data-ttu-id="d0b02-109">Mit diesem Befehl wird die Azure SQL-Datenbanksynchronisierungsgruppe namens "syncGroup01" entfernt.</span><span class="sxs-lookup"><span data-stu-id="d0b02-109">This command removes the Azure SQL Database Sync Group named syncGroup01.</span></span>

## <span data-ttu-id="d0b02-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d0b02-110">PARAMETERS</span></span>

### <span data-ttu-id="d0b02-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d0b02-111">-DatabaseName</span></span>
<span data-ttu-id="d0b02-112">Der Name der Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="d0b02-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="d0b02-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0b02-113">-DefaultProfile</span></span>
<span data-ttu-id="d0b02-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="d0b02-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d0b02-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d0b02-115">-Force</span></span>
<span data-ttu-id="d0b02-116">Bestätigungsmeldung zum Ausführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="d0b02-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="d0b02-117">-Name</span><span class="sxs-lookup"><span data-stu-id="d0b02-117">-Name</span></span>
<span data-ttu-id="d0b02-118">Der Name der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="d0b02-118">The sync group name.</span></span>

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

### <span data-ttu-id="d0b02-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d0b02-119">-PassThru</span></span>
<span data-ttu-id="d0b02-120">Definiert, ob die entfernte Synchronisierungsgruppe zurückgeben wird.</span><span class="sxs-lookup"><span data-stu-id="d0b02-120">Defines Whether return the removed sync group</span></span>

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

### <span data-ttu-id="d0b02-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0b02-121">-ResourceGroupName</span></span>
<span data-ttu-id="d0b02-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d0b02-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="d0b02-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d0b02-123">-ServerName</span></span>
<span data-ttu-id="d0b02-124">Der Name des Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d0b02-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="d0b02-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d0b02-125">-Confirm</span></span>
<span data-ttu-id="d0b02-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d0b02-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0b02-127">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d0b02-127">-WhatIf</span></span>
<span data-ttu-id="d0b02-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d0b02-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0b02-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d0b02-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0b02-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0b02-130">CommonParameters</span></span>
<span data-ttu-id="d0b02-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0b02-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0b02-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d0b02-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0b02-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d0b02-133">INPUTS</span></span>

### <span data-ttu-id="d0b02-134">System.String</span><span class="sxs-lookup"><span data-stu-id="d0b02-134">System.String</span></span>

## <span data-ttu-id="d0b02-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d0b02-135">OUTPUTS</span></span>

### <span data-ttu-id="d0b02-136">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="d0b02-136">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="d0b02-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d0b02-137">NOTES</span></span>

## <span data-ttu-id="d0b02-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d0b02-138">RELATED LINKS</span></span>

[<span data-ttu-id="d0b02-139">New-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="d0b02-139">New-AzSqlSyncGroup</span></span>](./New-AzSqlSyncGroup.md)

[<span data-ttu-id="d0b02-140">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="d0b02-140">Update-AzSqlSyncGroup</span></span>](./Update-AzSqlSyncGroup.md)

[<span data-ttu-id="d0b02-141">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="d0b02-141">Get-AzSqlSyncGroup</span></span>](./Get-AzSqlSyncGroup.md)

