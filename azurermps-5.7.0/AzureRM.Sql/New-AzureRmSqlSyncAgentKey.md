---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlsyncagentkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncAgentKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncAgentKey.md
ms.openlocfilehash: c6a9c1df9fca93b932ebc65a11c6b126b133465b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498710"
---
# <span data-ttu-id="2b957-101">New-AzureRmSqlSyncAgentKey</span><span class="sxs-lookup"><span data-stu-id="2b957-101">New-AzureRmSqlSyncAgentKey</span></span>

## <span data-ttu-id="2b957-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2b957-102">SYNOPSIS</span></span>
<span data-ttu-id="2b957-103">Erstellt einen Azure SQL-Synchronisierungs-Agent-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="2b957-103">Creates an Azure SQL Sync Agent Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b957-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2b957-104">SYNTAX</span></span>

```
New-AzureRmSqlSyncAgentKey [-ServerName] <String> [-SyncAgentName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b957-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2b957-105">DESCRIPTION</span></span>
<span data-ttu-id="2b957-106">Mit dem Cmdlet **New-AzureRmSqlSyncAgentKey** wird ein Azure SQL-Synchronisierungs-Agent-Schlüssel erstellt.</span><span class="sxs-lookup"><span data-stu-id="2b957-106">The **New-AzureRmSqlSyncAgentKey** cmdlet creates an Azure SQL Sync Agent key.</span></span>

## <span data-ttu-id="2b957-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2b957-107">EXAMPLES</span></span>

### <span data-ttu-id="2b957-108">Beispiel 1: Erstellen eines Synchronisierungs-Agent-Schlüssels für einen Azure SQL-Synchronisierungs-Agent</span><span class="sxs-lookup"><span data-stu-id="2b957-108">Example 1: Create a sync agent key for an Azure SQL sync agent.</span></span>
```
PS C:\> New-AzureRmSqlSyncAgentKey -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SyncAgentName "SyncAgent01"
SyncAgentKey                  : Key
```

<span data-ttu-id="2b957-109">Mit diesem Befehl wird ein Synchronisierungs-Agent-Schlüssel für einen Azure SQL-Synchronisierungs-Agent erstellt.</span><span class="sxs-lookup"><span data-stu-id="2b957-109">This command creates a sync agent key for an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="2b957-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2b957-110">PARAMETERS</span></span>

### <span data-ttu-id="2b957-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b957-111">-DefaultProfile</span></span>
<span data-ttu-id="2b957-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="2b957-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b957-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b957-113">-ResourceGroupName</span></span>
<span data-ttu-id="2b957-114">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2b957-114">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b957-115">-Servername</span><span class="sxs-lookup"><span data-stu-id="2b957-115">-ServerName</span></span>
<span data-ttu-id="2b957-116">Der Name des Azure SQL Server, in dem sich der Synchronisierungs-Agent befindet.</span><span class="sxs-lookup"><span data-stu-id="2b957-116">The name of the Azure SQL Server the sync agent is in.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b957-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="2b957-117">-SyncAgentName</span></span>
<span data-ttu-id="2b957-118">Der Name des Synchronisierungs-Agents.</span><span class="sxs-lookup"><span data-stu-id="2b957-118">The sync agent name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b957-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2b957-119">-Confirm</span></span>
<span data-ttu-id="2b957-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2b957-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b957-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b957-121">-WhatIf</span></span>
<span data-ttu-id="2b957-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2b957-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b957-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2b957-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b957-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b957-124">CommonParameters</span></span>
<span data-ttu-id="2b957-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b957-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b957-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b957-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b957-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2b957-127">INPUTS</span></span>

### <span data-ttu-id="2b957-128">Keine</span><span class="sxs-lookup"><span data-stu-id="2b957-128">None</span></span>
<span data-ttu-id="2b957-129">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="2b957-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2b957-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2b957-130">OUTPUTS</span></span>

### <span data-ttu-id="2b957-131">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncAgentKeyModel</span><span class="sxs-lookup"><span data-stu-id="2b957-131">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentKeyModel</span></span>

## <span data-ttu-id="2b957-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="2b957-132">NOTES</span></span>

## <span data-ttu-id="2b957-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2b957-133">RELATED LINKS</span></span>
