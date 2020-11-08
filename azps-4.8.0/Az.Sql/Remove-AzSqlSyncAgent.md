---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncAgent.md
ms.openlocfilehash: ca3ef83fab80e73d687fd11cde418c9ad43f499e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174106"
---
# <span data-ttu-id="46d71-101">Remove-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="46d71-101">Remove-AzSqlSyncAgent</span></span>

## <span data-ttu-id="46d71-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="46d71-102">SYNOPSIS</span></span>
<span data-ttu-id="46d71-103">Entfernt einen Azure SQL-Synchronisierungs-Agent.</span><span class="sxs-lookup"><span data-stu-id="46d71-103">Removes an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="46d71-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="46d71-104">SYNTAX</span></span>

```
Remove-AzSqlSyncAgent [-Name] <String> [-Force] [-PassThru] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="46d71-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="46d71-105">DESCRIPTION</span></span>
<span data-ttu-id="46d71-106">Mit dem Cmdlet **Remove-AzSqlSyncAgent** wird ein Azure SQL-Synchronisierungs-Agent entfernt.</span><span class="sxs-lookup"><span data-stu-id="46d71-106">The **Remove-AzSqlSyncAgent** cmdlet removes an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="46d71-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="46d71-107">EXAMPLES</span></span>

### <span data-ttu-id="46d71-108">Beispiel 1: Entfernen eines Synchronisierungs-Agents</span><span class="sxs-lookup"><span data-stu-id="46d71-108">Example 1: Remove a sync agent</span></span>
```
PS C:\>Remove-AzSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "syncAgent01"
```

<span data-ttu-id="46d71-109">Mit diesem Befehl wird der Azure SQL-Synchronisierungs-Agent mit dem Namen syncAgent01 entfernt.</span><span class="sxs-lookup"><span data-stu-id="46d71-109">This command removes the Azure SQL Sync Agent named syncAgent01.</span></span>

## <span data-ttu-id="46d71-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="46d71-110">PARAMETERS</span></span>

### <span data-ttu-id="46d71-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46d71-111">-DefaultProfile</span></span>
<span data-ttu-id="46d71-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="46d71-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="46d71-113">-Force</span><span class="sxs-lookup"><span data-stu-id="46d71-113">-Force</span></span>
<span data-ttu-id="46d71-114">Bestätigungsmeldung zum Durchführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="46d71-114">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="46d71-115">-Name</span><span class="sxs-lookup"><span data-stu-id="46d71-115">-Name</span></span>
<span data-ttu-id="46d71-116">Der Name des Synchronisierungs-Agents.</span><span class="sxs-lookup"><span data-stu-id="46d71-116">The sync agent name.</span></span>

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

### <span data-ttu-id="46d71-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="46d71-117">-PassThru</span></span>
<span data-ttu-id="46d71-118">Definiert, ob der entfernte Synchronisierungs-Agent zurückgegeben wird</span><span class="sxs-lookup"><span data-stu-id="46d71-118">Defines Whether return the removed sync agent</span></span>

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

### <span data-ttu-id="46d71-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46d71-119">-ResourceGroupName</span></span>
<span data-ttu-id="46d71-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="46d71-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="46d71-121">-Servername</span><span class="sxs-lookup"><span data-stu-id="46d71-121">-ServerName</span></span>
<span data-ttu-id="46d71-122">Der Name des Azure SQL Server, in dem sich der Synchronisierungs-Agent befindet.</span><span class="sxs-lookup"><span data-stu-id="46d71-122">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="46d71-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="46d71-123">-Confirm</span></span>
<span data-ttu-id="46d71-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="46d71-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46d71-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46d71-125">-WhatIf</span></span>
<span data-ttu-id="46d71-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="46d71-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46d71-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="46d71-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46d71-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46d71-128">CommonParameters</span></span>
<span data-ttu-id="46d71-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46d71-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46d71-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="46d71-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46d71-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="46d71-131">INPUTS</span></span>

### <span data-ttu-id="46d71-132">System. String</span><span class="sxs-lookup"><span data-stu-id="46d71-132">System.String</span></span>

## <span data-ttu-id="46d71-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="46d71-133">OUTPUTS</span></span>

### <span data-ttu-id="46d71-134">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="46d71-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="46d71-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="46d71-135">NOTES</span></span>

## <span data-ttu-id="46d71-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="46d71-136">RELATED LINKS</span></span>

[<span data-ttu-id="46d71-137">Neu – AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="46d71-137">New-AzSqlSyncAgent</span></span>](./New-AzSqlSyncAgent.md)

[<span data-ttu-id="46d71-138">Get-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="46d71-138">Get-AzSqlSyncAgent</span></span>](./Get-AzSqlSyncAgent.md)

