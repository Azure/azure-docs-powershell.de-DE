---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncAgent.md
ms.openlocfilehash: ca3ef83fab80e73d687fd11cde418c9ad43f499e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98289588"
---
# <span data-ttu-id="e6c60-101">Remove-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="e6c60-101">Remove-AzSqlSyncAgent</span></span>

## <span data-ttu-id="e6c60-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6c60-102">SYNOPSIS</span></span>
<span data-ttu-id="e6c60-103">Entfernt einen Azure SQL-Synchronisierungs-Agent.</span><span class="sxs-lookup"><span data-stu-id="e6c60-103">Removes an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="e6c60-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e6c60-104">SYNTAX</span></span>

```
Remove-AzSqlSyncAgent [-Name] <String> [-Force] [-PassThru] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e6c60-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e6c60-105">DESCRIPTION</span></span>
<span data-ttu-id="e6c60-106">Das **Cmdlet "Remove-AzSqlSyncAgent"** entfernt einen Azure SQL-Agent.</span><span class="sxs-lookup"><span data-stu-id="e6c60-106">The **Remove-AzSqlSyncAgent** cmdlet removes an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="e6c60-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e6c60-107">EXAMPLES</span></span>

### <span data-ttu-id="e6c60-108">Beispiel 1: Entfernen eines Synchronisierungs-Agents</span><span class="sxs-lookup"><span data-stu-id="e6c60-108">Example 1: Remove a sync agent</span></span>
```
PS C:\>Remove-AzSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "syncAgent01"
```

<span data-ttu-id="e6c60-109">Mit diesem Befehl wird der Azure SQL-Synchronisierungs-Agent namens "syncAgent01" entfernt.</span><span class="sxs-lookup"><span data-stu-id="e6c60-109">This command removes the Azure SQL Sync Agent named syncAgent01.</span></span>

## <span data-ttu-id="e6c60-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e6c60-110">PARAMETERS</span></span>

### <span data-ttu-id="e6c60-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6c60-111">-DefaultProfile</span></span>
<span data-ttu-id="e6c60-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="e6c60-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e6c60-113">-Force</span><span class="sxs-lookup"><span data-stu-id="e6c60-113">-Force</span></span>
<span data-ttu-id="e6c60-114">Bestätigungsmeldung zum Ausführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="e6c60-114">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="e6c60-115">-Name</span><span class="sxs-lookup"><span data-stu-id="e6c60-115">-Name</span></span>
<span data-ttu-id="e6c60-116">Der Name des Synchronisierungs-Agents.</span><span class="sxs-lookup"><span data-stu-id="e6c60-116">The sync agent name.</span></span>

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

### <span data-ttu-id="e6c60-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e6c60-117">-PassThru</span></span>
<span data-ttu-id="e6c60-118">Definiert, ob der entfernte Synchronisierungs-Agent zurückgeben wird.</span><span class="sxs-lookup"><span data-stu-id="e6c60-118">Defines Whether return the removed sync agent</span></span>

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

### <span data-ttu-id="e6c60-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6c60-119">-ResourceGroupName</span></span>
<span data-ttu-id="e6c60-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e6c60-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="e6c60-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e6c60-121">-ServerName</span></span>
<span data-ttu-id="e6c60-122">Der Name des Azure-SQL Server, in dem sich der Synchronisierungs-Agent befindet.</span><span class="sxs-lookup"><span data-stu-id="e6c60-122">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="e6c60-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e6c60-123">-Confirm</span></span>
<span data-ttu-id="e6c60-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e6c60-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6c60-125">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="e6c60-125">-WhatIf</span></span>
<span data-ttu-id="e6c60-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e6c60-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6c60-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e6c60-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6c60-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6c60-128">CommonParameters</span></span>
<span data-ttu-id="e6c60-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6c60-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6c60-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e6c60-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6c60-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e6c60-131">INPUTS</span></span>

### <span data-ttu-id="e6c60-132">System.String</span><span class="sxs-lookup"><span data-stu-id="e6c60-132">System.String</span></span>

## <span data-ttu-id="e6c60-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e6c60-133">OUTPUTS</span></span>

### <span data-ttu-id="e6c60-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="e6c60-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="e6c60-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e6c60-135">NOTES</span></span>

## <span data-ttu-id="e6c60-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e6c60-136">RELATED LINKS</span></span>

[<span data-ttu-id="e6c60-137">New-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="e6c60-137">New-AzSqlSyncAgent</span></span>](./New-AzSqlSyncAgent.md)

[<span data-ttu-id="e6c60-138">Get-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="e6c60-138">Get-AzSqlSyncAgent</span></span>](./Get-AzSqlSyncAgent.md)

