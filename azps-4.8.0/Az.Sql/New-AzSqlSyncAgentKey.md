---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncagentkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgentKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgentKey.md
ms.openlocfilehash: e6ccf84d2de6c64000a6663de5a5b696d9033eae
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94007762"
---
# <span data-ttu-id="88bd0-101">New-AzSqlSyncAgentKey</span><span class="sxs-lookup"><span data-stu-id="88bd0-101">New-AzSqlSyncAgentKey</span></span>

## <span data-ttu-id="88bd0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="88bd0-102">SYNOPSIS</span></span>
<span data-ttu-id="88bd0-103">Erstellt einen Azure SQL-Synchronisierungs-Agent-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="88bd0-103">Creates an Azure SQL Sync Agent Key.</span></span>

## <span data-ttu-id="88bd0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="88bd0-104">SYNTAX</span></span>

```
New-AzSqlSyncAgentKey [-ServerName] <String> [-SyncAgentName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88bd0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="88bd0-105">DESCRIPTION</span></span>
<span data-ttu-id="88bd0-106">Mit dem Cmdlet **New-AzSqlSyncAgentKey** wird ein Azure SQL-Synchronisierungs-Agent-Schlüssel erstellt.</span><span class="sxs-lookup"><span data-stu-id="88bd0-106">The **New-AzSqlSyncAgentKey** cmdlet creates an Azure SQL Sync Agent key.</span></span>

## <span data-ttu-id="88bd0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="88bd0-107">EXAMPLES</span></span>

### <span data-ttu-id="88bd0-108">Beispiel 1: Erstellen eines Synchronisierungs-Agent-Schlüssels für einen Azure SQL-Synchronisierungs-Agent</span><span class="sxs-lookup"><span data-stu-id="88bd0-108">Example 1: Create a sync agent key for an Azure SQL sync agent.</span></span>
```
PS C:\> New-AzSqlSyncAgentKey -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SyncAgentName "SyncAgent01"
SyncAgentKey                  : Key
```

<span data-ttu-id="88bd0-109">Mit diesem Befehl wird ein Synchronisierungs-Agent-Schlüssel für einen Azure SQL-Synchronisierungs-Agent erstellt.</span><span class="sxs-lookup"><span data-stu-id="88bd0-109">This command creates a sync agent key for an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="88bd0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="88bd0-110">PARAMETERS</span></span>

### <span data-ttu-id="88bd0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88bd0-111">-DefaultProfile</span></span>
<span data-ttu-id="88bd0-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="88bd0-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="88bd0-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88bd0-113">-ResourceGroupName</span></span>
<span data-ttu-id="88bd0-114">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="88bd0-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="88bd0-115">-Servername</span><span class="sxs-lookup"><span data-stu-id="88bd0-115">-ServerName</span></span>
<span data-ttu-id="88bd0-116">Der Name des Azure SQL Server, in dem sich der Synchronisierungs-Agent befindet.</span><span class="sxs-lookup"><span data-stu-id="88bd0-116">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="88bd0-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="88bd0-117">-SyncAgentName</span></span>
<span data-ttu-id="88bd0-118">Der Name des Synchronisierungs-Agents.</span><span class="sxs-lookup"><span data-stu-id="88bd0-118">The sync agent name.</span></span>

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

### <span data-ttu-id="88bd0-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="88bd0-119">-Confirm</span></span>
<span data-ttu-id="88bd0-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="88bd0-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88bd0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88bd0-121">-WhatIf</span></span>
<span data-ttu-id="88bd0-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="88bd0-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88bd0-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="88bd0-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88bd0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88bd0-124">CommonParameters</span></span>
<span data-ttu-id="88bd0-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88bd0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88bd0-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="88bd0-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88bd0-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="88bd0-127">INPUTS</span></span>

### <span data-ttu-id="88bd0-128">System. String</span><span class="sxs-lookup"><span data-stu-id="88bd0-128">System.String</span></span>

## <span data-ttu-id="88bd0-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="88bd0-129">OUTPUTS</span></span>

### <span data-ttu-id="88bd0-130">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncAgentKeyModel</span><span class="sxs-lookup"><span data-stu-id="88bd0-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentKeyModel</span></span>

## <span data-ttu-id="88bd0-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="88bd0-131">NOTES</span></span>

## <span data-ttu-id="88bd0-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="88bd0-132">RELATED LINKS</span></span>
