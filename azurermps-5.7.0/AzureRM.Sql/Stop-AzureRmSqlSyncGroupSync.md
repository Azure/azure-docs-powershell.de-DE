---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/stop-azurermsqlsyncgroupsync
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlSyncGroupSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlSyncGroupSync.md
ms.openlocfilehash: 24e61d466ac691f0f6faaa0b87bf819671517809
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482665"
---
# <span data-ttu-id="f2cba-101">Stop-AzureRmSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="f2cba-101">Stop-AzureRmSqlSyncGroupSync</span></span>

## <span data-ttu-id="f2cba-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f2cba-102">SYNOPSIS</span></span>
<span data-ttu-id="f2cba-103">Beendet die Synchronisierung einer Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="f2cba-103">Stops a sync group synchronization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2cba-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2cba-104">SYNTAX</span></span>

```
Stop-AzureRmSqlSyncGroupSync [-SyncGroupName] <String> [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2cba-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f2cba-105">DESCRIPTION</span></span>
<span data-ttu-id="f2cba-106">Das Cmdlet " **Stop-AzureRmSqlSyncGroupSync** " beendet die Synchronisierung der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="f2cba-106">The **Stop-AzureRmSqlSyncGroupSync** cmdlet stops a sync group synchronization.</span></span>

## <span data-ttu-id="f2cba-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f2cba-107">EXAMPLES</span></span>

### <span data-ttu-id="f2cba-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f2cba-108">Example 1</span></span>
```
PS C:\> Stop-AzureRmSqlSyncGroupSync -SyncGroupName mysg [-ServerName] mysrv [-DatabaseName] mydb [-ResourceGroupName] myrg
```

<span data-ttu-id="f2cba-109">Dieser Befehl beendet die Synchronisierung, die für die Synchronisierungsgruppe mysg fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="f2cba-109">This command stops the synchronization which is ongoing for the sync group mysg.</span></span>

## <span data-ttu-id="f2cba-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f2cba-110">PARAMETERS</span></span>

### <span data-ttu-id="f2cba-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f2cba-111">-DatabaseName</span></span>
<span data-ttu-id="f2cba-112">Der Name der Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="f2cba-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="f2cba-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2cba-113">-DefaultProfile</span></span>
<span data-ttu-id="f2cba-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="f2cba-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f2cba-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f2cba-115">-PassThru</span></span>
<span data-ttu-id="f2cba-116">Definiert, ob die Synchronisierungsgruppe zurückgegeben wird</span><span class="sxs-lookup"><span data-stu-id="f2cba-116">Defines Whether return the sync group</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2cba-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2cba-117">-ResourceGroupName</span></span>
<span data-ttu-id="f2cba-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f2cba-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="f2cba-119">-Servername</span><span class="sxs-lookup"><span data-stu-id="f2cba-119">-ServerName</span></span>
<span data-ttu-id="f2cba-120">Der Name des Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f2cba-120">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="f2cba-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="f2cba-121">-SyncGroupName</span></span>
<span data-ttu-id="f2cba-122">Der Name der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="f2cba-122">The sync group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2cba-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f2cba-123">-Confirm</span></span>
<span data-ttu-id="f2cba-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f2cba-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2cba-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2cba-125">-WhatIf</span></span>
<span data-ttu-id="f2cba-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f2cba-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2cba-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f2cba-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2cba-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2cba-128">CommonParameters</span></span>
<span data-ttu-id="f2cba-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2cba-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2cba-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2cba-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2cba-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f2cba-131">INPUTS</span></span>

### <span data-ttu-id="f2cba-132">Keine</span><span class="sxs-lookup"><span data-stu-id="f2cba-132">None</span></span>
<span data-ttu-id="f2cba-133">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="f2cba-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f2cba-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f2cba-134">OUTPUTS</span></span>

### <span data-ttu-id="f2cba-135">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="f2cba-135">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="f2cba-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="f2cba-136">NOTES</span></span>

## <span data-ttu-id="f2cba-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f2cba-137">RELATED LINKS</span></span>

[<span data-ttu-id="f2cba-138">Anfang-AzureRmSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="f2cba-138">Start-AzureRmSqlSyncGroupSync</span></span>](./Start-AzureRmSqlSyncGroupSync.md)

