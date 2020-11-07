---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncAgent.md
ms.openlocfilehash: 481f99baa432c00fc6a619754cee2df83015c047
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662474"
---
# <span data-ttu-id="f752a-101">Remove-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="f752a-101">Remove-AzureRmSqlSyncAgent</span></span>

## <span data-ttu-id="f752a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f752a-102">SYNOPSIS</span></span>
<span data-ttu-id="f752a-103">Entfernt einen Azure SQL-Synchronisierungs-Agent.</span><span class="sxs-lookup"><span data-stu-id="f752a-103">Removes an Azure SQL Sync Agent.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f752a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f752a-104">SYNTAX</span></span>

```
Remove-AzureRmSqlSyncAgent [-Name] <String> [-Force] [-PassThru] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f752a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f752a-105">DESCRIPTION</span></span>
<span data-ttu-id="f752a-106">Mit dem Cmdlet **Remove-AzureRmSqlSyncAgent** wird ein Azure SQL-Synchronisierungs-Agent entfernt.</span><span class="sxs-lookup"><span data-stu-id="f752a-106">The **Remove-AzureRmSqlSyncAgent** cmdlet removes an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="f752a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f752a-107">EXAMPLES</span></span>

### <span data-ttu-id="f752a-108">Beispiel 1: Entfernen eines Synchronisierungs-Agents</span><span class="sxs-lookup"><span data-stu-id="f752a-108">Example 1: Remove a sync agent</span></span>
```
PS C:\>Remove-AzureRmSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "syncAgent01"
```

<span data-ttu-id="f752a-109">Mit diesem Befehl wird der Azure SQL-Synchronisierungs-Agent mit dem Namen syncAgent01 entfernt.</span><span class="sxs-lookup"><span data-stu-id="f752a-109">This command removes the Azure SQL Sync Agent named syncAgent01.</span></span>

## <span data-ttu-id="f752a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f752a-110">PARAMETERS</span></span>

### <span data-ttu-id="f752a-111">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f752a-111">-Confirm</span></span>
<span data-ttu-id="f752a-112">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f752a-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f752a-113">-Force</span><span class="sxs-lookup"><span data-stu-id="f752a-113">-Force</span></span>
<span data-ttu-id="f752a-114">Bestätigungsmeldung zum Durchführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="f752a-114">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="f752a-115">-Name</span><span class="sxs-lookup"><span data-stu-id="f752a-115">-Name</span></span>
<span data-ttu-id="f752a-116">Der Name des Synchronisierungs-Agents.</span><span class="sxs-lookup"><span data-stu-id="f752a-116">The sync agent name.</span></span>

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

### <span data-ttu-id="f752a-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f752a-117">-PassThru</span></span>
<span data-ttu-id="f752a-118">Definiert, ob der entfernte Synchronisierungs-Agent zurückgegeben wird</span><span class="sxs-lookup"><span data-stu-id="f752a-118">Defines Whether return the removed sync agent</span></span>

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

### <span data-ttu-id="f752a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f752a-119">-ResourceGroupName</span></span>
<span data-ttu-id="f752a-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f752a-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="f752a-121">-Servername</span><span class="sxs-lookup"><span data-stu-id="f752a-121">-ServerName</span></span>
<span data-ttu-id="f752a-122">Der Name des Azure SQL Server, in dem sich der Synchronisierungs-Agent befindet.</span><span class="sxs-lookup"><span data-stu-id="f752a-122">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="f752a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f752a-123">-WhatIf</span></span>
<span data-ttu-id="f752a-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f752a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f752a-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f752a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f752a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f752a-126">-DefaultProfile</span></span>
<span data-ttu-id="f752a-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f752a-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f752a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f752a-128">CommonParameters</span></span>
<span data-ttu-id="f752a-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f752a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f752a-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f752a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f752a-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f752a-131">INPUTS</span></span>

## <span data-ttu-id="f752a-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f752a-132">OUTPUTS</span></span>

### <span data-ttu-id="f752a-133">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="f752a-133">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="f752a-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="f752a-134">NOTES</span></span>

## <span data-ttu-id="f752a-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f752a-135">RELATED LINKS</span></span>

[<span data-ttu-id="f752a-136">Neu – AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="f752a-136">New-AzureRmSqlSyncAgent</span></span>](./New-AzureRmSqlSyncAgent.md)

[<span data-ttu-id="f752a-137">Get-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="f752a-137">Get-AzureRmSqlSyncAgent</span></span>](./Get-AzureRmSqlSyncAgent.md)

