---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncAgent.md
ms.openlocfilehash: 30c0cca7fb1d8eab2c5d0abe4d6c0d556cc92d7e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940955"
---
# <span data-ttu-id="aa930-101">Remove-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="aa930-101">Remove-AzSqlSyncAgent</span></span>

## <span data-ttu-id="aa930-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa930-102">SYNOPSIS</span></span>
<span data-ttu-id="aa930-103">Entfernt einen Azure SQL-Synchronisierungs-Agent.</span><span class="sxs-lookup"><span data-stu-id="aa930-103">Removes an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="aa930-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aa930-104">SYNTAX</span></span>

```
Remove-AzSqlSyncAgent [-Name] <String> [-Force] [-PassThru] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aa930-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aa930-105">DESCRIPTION</span></span>
<span data-ttu-id="aa930-106">Das **Cmdlet Remove-AzSqlSyncAgent** entfernt einen Azure SQL Synchronisierungs-Agent.</span><span class="sxs-lookup"><span data-stu-id="aa930-106">The **Remove-AzSqlSyncAgent** cmdlet removes an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="aa930-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="aa930-107">EXAMPLES</span></span>

### <span data-ttu-id="aa930-108">Beispiel 1: Entfernen eines Synchronisierungs-Agents</span><span class="sxs-lookup"><span data-stu-id="aa930-108">Example 1: Remove a sync agent</span></span>
```
PS C:\>Remove-AzSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "syncAgent01"
```

<span data-ttu-id="aa930-109">Mit diesem Befehl wird der Azure SQL Sync Agent namens syncAgent01 entfernt.</span><span class="sxs-lookup"><span data-stu-id="aa930-109">This command removes the Azure SQL Sync Agent named syncAgent01.</span></span>

## <span data-ttu-id="aa930-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="aa930-110">PARAMETERS</span></span>

### <span data-ttu-id="aa930-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa930-111">-DefaultProfile</span></span>
<span data-ttu-id="aa930-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="aa930-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aa930-113">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="aa930-113">-Force</span></span>
<span data-ttu-id="aa930-114">Bestätigungsmeldung überspringen zum Ausführen der Aktion</span><span class="sxs-lookup"><span data-stu-id="aa930-114">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="aa930-115">-Name</span><span class="sxs-lookup"><span data-stu-id="aa930-115">-Name</span></span>
<span data-ttu-id="aa930-116">Der Name des Synchronisierungs-Agents.</span><span class="sxs-lookup"><span data-stu-id="aa930-116">The sync agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncAgentName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa930-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aa930-117">-PassThru</span></span>
<span data-ttu-id="aa930-118">Definiert, ob der entfernte Synchronisierungs-Agent zurückgeben wird</span><span class="sxs-lookup"><span data-stu-id="aa930-118">Defines Whether return the removed sync agent</span></span>

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

### <span data-ttu-id="aa930-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa930-119">-ResourceGroupName</span></span>
<span data-ttu-id="aa930-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="aa930-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="aa930-121">-Servername</span><span class="sxs-lookup"><span data-stu-id="aa930-121">-ServerName</span></span>
<span data-ttu-id="aa930-122">Der Name des Azure-SQL Server, in dem sich der Synchronisierungs-Agent befindet.</span><span class="sxs-lookup"><span data-stu-id="aa930-122">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="aa930-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="aa930-123">-Confirm</span></span>
<span data-ttu-id="aa930-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="aa930-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa930-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa930-125">-WhatIf</span></span>
<span data-ttu-id="aa930-126">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="aa930-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa930-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="aa930-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa930-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa930-128">CommonParameters</span></span>
<span data-ttu-id="aa930-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa930-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa930-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aa930-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa930-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="aa930-131">INPUTS</span></span>

### <span data-ttu-id="aa930-132">System.String</span><span class="sxs-lookup"><span data-stu-id="aa930-132">System.String</span></span>

## <span data-ttu-id="aa930-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="aa930-133">OUTPUTS</span></span>

### <span data-ttu-id="aa930-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="aa930-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="aa930-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="aa930-135">NOTES</span></span>

## <span data-ttu-id="aa930-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="aa930-136">RELATED LINKS</span></span>

[<span data-ttu-id="aa930-137">New-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="aa930-137">New-AzSqlSyncAgent</span></span>](./New-AzSqlSyncAgent.md)

[<span data-ttu-id="aa930-138">Get-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="aa930-138">Get-AzSqlSyncAgent</span></span>](./Get-AzSqlSyncAgent.md)

