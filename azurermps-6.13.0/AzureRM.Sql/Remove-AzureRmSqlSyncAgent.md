---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncAgent.md
ms.openlocfilehash: 9886d2d32dd3bce8841dcf2652cf89054335b112
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502842"
---
# <span data-ttu-id="afb94-101">Remove-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="afb94-101">Remove-AzureRmSqlSyncAgent</span></span>

## <span data-ttu-id="afb94-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="afb94-102">SYNOPSIS</span></span>
<span data-ttu-id="afb94-103">Entfernt einen Azure SQL-Synchronisierungs-Agent.</span><span class="sxs-lookup"><span data-stu-id="afb94-103">Removes an Azure SQL Sync Agent.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="afb94-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="afb94-104">SYNTAX</span></span>

```
Remove-AzureRmSqlSyncAgent [-Name] <String> [-Force] [-PassThru] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="afb94-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="afb94-105">DESCRIPTION</span></span>
<span data-ttu-id="afb94-106">Mit dem Cmdlet **Remove-AzureRmSqlSyncAgent** wird ein Azure SQL-Synchronisierungs-Agent entfernt.</span><span class="sxs-lookup"><span data-stu-id="afb94-106">The **Remove-AzureRmSqlSyncAgent** cmdlet removes an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="afb94-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="afb94-107">EXAMPLES</span></span>

### <span data-ttu-id="afb94-108">Beispiel 1: Entfernen eines Synchronisierungs-Agents</span><span class="sxs-lookup"><span data-stu-id="afb94-108">Example 1: Remove a sync agent</span></span>
```
PS C:\>Remove-AzureRmSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "syncAgent01"
```

<span data-ttu-id="afb94-109">Mit diesem Befehl wird der Azure SQL-Synchronisierungs-Agent mit dem Namen syncAgent01 entfernt.</span><span class="sxs-lookup"><span data-stu-id="afb94-109">This command removes the Azure SQL Sync Agent named syncAgent01.</span></span>

## <span data-ttu-id="afb94-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="afb94-110">PARAMETERS</span></span>

### <span data-ttu-id="afb94-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afb94-111">-DefaultProfile</span></span>
<span data-ttu-id="afb94-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="afb94-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afb94-113">-Force</span><span class="sxs-lookup"><span data-stu-id="afb94-113">-Force</span></span>
<span data-ttu-id="afb94-114">Bestätigungsmeldung zum Durchführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="afb94-114">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="afb94-115">-Name</span><span class="sxs-lookup"><span data-stu-id="afb94-115">-Name</span></span>
<span data-ttu-id="afb94-116">Der Name des Synchronisierungs-Agents.</span><span class="sxs-lookup"><span data-stu-id="afb94-116">The sync agent name.</span></span>

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

### <span data-ttu-id="afb94-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="afb94-117">-PassThru</span></span>
<span data-ttu-id="afb94-118">Definiert, ob der entfernte Synchronisierungs-Agent zurückgegeben wird</span><span class="sxs-lookup"><span data-stu-id="afb94-118">Defines Whether return the removed sync agent</span></span>

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

### <span data-ttu-id="afb94-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afb94-119">-ResourceGroupName</span></span>
<span data-ttu-id="afb94-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="afb94-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="afb94-121">-Servername</span><span class="sxs-lookup"><span data-stu-id="afb94-121">-ServerName</span></span>
<span data-ttu-id="afb94-122">Der Name des Azure SQL Server, in dem sich der Synchronisierungs-Agent befindet.</span><span class="sxs-lookup"><span data-stu-id="afb94-122">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="afb94-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="afb94-123">-Confirm</span></span>
<span data-ttu-id="afb94-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="afb94-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afb94-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afb94-125">-WhatIf</span></span>
<span data-ttu-id="afb94-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="afb94-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afb94-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="afb94-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afb94-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afb94-128">CommonParameters</span></span>
<span data-ttu-id="afb94-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afb94-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afb94-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afb94-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afb94-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="afb94-131">INPUTS</span></span>

### <span data-ttu-id="afb94-132">System. String</span><span class="sxs-lookup"><span data-stu-id="afb94-132">System.String</span></span>

## <span data-ttu-id="afb94-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="afb94-133">OUTPUTS</span></span>

### <span data-ttu-id="afb94-134">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="afb94-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="afb94-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="afb94-135">NOTES</span></span>

## <span data-ttu-id="afb94-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="afb94-136">RELATED LINKS</span></span>

[<span data-ttu-id="afb94-137">Neu – AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="afb94-137">New-AzureRmSqlSyncAgent</span></span>](./New-AzureRmSqlSyncAgent.md)

[<span data-ttu-id="afb94-138">Get-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="afb94-138">Get-AzureRmSqlSyncAgent</span></span>](./Get-AzureRmSqlSyncAgent.md)

