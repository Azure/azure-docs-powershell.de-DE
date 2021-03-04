---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlsyncgrouplog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroupLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroupLog.md
ms.openlocfilehash: 40a269ab3d8378ce2f5a2024baee5bca18fe2134
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937331"
---
# <span data-ttu-id="2c33b-101">Get-AzSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="2c33b-101">Get-AzSqlSyncGroupLog</span></span>

## <span data-ttu-id="2c33b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c33b-102">SYNOPSIS</span></span>
<span data-ttu-id="2c33b-103">Gibt die Protokolle einer Azure SQL Database Sync Group zurück.</span><span class="sxs-lookup"><span data-stu-id="2c33b-103">Returns the logs of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="2c33b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2c33b-104">SYNTAX</span></span>

```
Get-AzSqlSyncGroupLog [-SyncGroupName] <String> -StartTime <DateTime> [-EndTime <DateTime>]
 [-LogLevel <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c33b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2c33b-105">DESCRIPTION</span></span>
<span data-ttu-id="2c33b-106">Das **Get-AzSqlSyncGroupLog-Cmdlet** gibt die Protokolle einer Azure SQL Database Sync Group zurück.</span><span class="sxs-lookup"><span data-stu-id="2c33b-106">The **Get-AzSqlSyncGroupLog** cmdlet returns the logs of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="2c33b-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2c33b-107">EXAMPLES</span></span>

### <span data-ttu-id="2c33b-108">Beispiel 1: Erfassen der Protokolle einer Azure SQL Synchronisierungsgruppe</span><span class="sxs-lookup"><span data-stu-id="2c33b-108">Example 1: Get the logs of an Azure SQL Sync Group</span></span>
```
PS C:\>Get-AzSqlSyncGroupLog -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -StartTime "9/16/2016 11:31:12" -EndTime "9/16/2016 12:31:00" -LogLevel "All"
TimeStamp            LogLevel Details                                   Source
---------            -------- -------                                   ------
6/13/2017 9:14:26 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
6/13/2017 7:11:59 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
```

<span data-ttu-id="2c33b-109">Dieser Befehl ruft die Protokolle einer Azure SQL Synchronisierungsgruppe ab.</span><span class="sxs-lookup"><span data-stu-id="2c33b-109">This command gets the logs of an Azure SQL Sync Group.</span></span>

## <span data-ttu-id="2c33b-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2c33b-110">PARAMETERS</span></span>

### <span data-ttu-id="2c33b-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2c33b-111">-DatabaseName</span></span>
<span data-ttu-id="2c33b-112">Der Name der Azure SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="2c33b-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="2c33b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c33b-113">-DefaultProfile</span></span>
<span data-ttu-id="2c33b-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="2c33b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2c33b-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="2c33b-115">-EndTime</span></span>
<span data-ttu-id="2c33b-116">Die Endzeit der Abfrageprotokolle.</span><span class="sxs-lookup"><span data-stu-id="2c33b-116">The end time of the logs to query.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c33b-117">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="2c33b-117">-LogLevel</span></span>
<span data-ttu-id="2c33b-118">Der Typ der zu abfragende Protokolle.</span><span class="sxs-lookup"><span data-stu-id="2c33b-118">The type of the logs to query.</span></span>
<span data-ttu-id="2c33b-119">Gültige Werte sind: "Fehler", "Warnung", "Erfolg" und "Alles".</span><span class="sxs-lookup"><span data-stu-id="2c33b-119">Valid values are: 'Error', 'Warning', 'Success' and 'All'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Error, Warning, Success, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c33b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c33b-120">-ResourceGroupName</span></span>
<span data-ttu-id="2c33b-121">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2c33b-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="2c33b-122">-Servername</span><span class="sxs-lookup"><span data-stu-id="2c33b-122">-ServerName</span></span>
<span data-ttu-id="2c33b-123">Der Name der Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="2c33b-123">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="2c33b-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="2c33b-124">-StartTime</span></span>
<span data-ttu-id="2c33b-125">Die Startzeit der zu abfragende Protokolle.</span><span class="sxs-lookup"><span data-stu-id="2c33b-125">The start time of the logs to query.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c33b-126">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="2c33b-126">-SyncGroupName</span></span>
<span data-ttu-id="2c33b-127">Der Name der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="2c33b-127">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c33b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c33b-128">CommonParameters</span></span>
<span data-ttu-id="2c33b-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c33b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c33b-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2c33b-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c33b-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2c33b-131">INPUTS</span></span>

### <span data-ttu-id="2c33b-132">System.String</span><span class="sxs-lookup"><span data-stu-id="2c33b-132">System.String</span></span>

## <span data-ttu-id="2c33b-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2c33b-133">OUTPUTS</span></span>

### <span data-ttu-id="2c33b-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupLogModel</span><span class="sxs-lookup"><span data-stu-id="2c33b-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupLogModel</span></span>

## <span data-ttu-id="2c33b-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="2c33b-135">NOTES</span></span>

## <span data-ttu-id="2c33b-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="2c33b-136">RELATED LINKS</span></span>
