---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncgrouplog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroupLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroupLog.md
ms.openlocfilehash: f8e73860d87d9389f2099a29039d90e0ac0534d6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145665"
---
# <span data-ttu-id="8e0c4-101">Get-AzSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="8e0c4-101">Get-AzSqlSyncGroupLog</span></span>

## <span data-ttu-id="8e0c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e0c4-102">SYNOPSIS</span></span>
<span data-ttu-id="8e0c4-103">Gibt die Protokolle einer Azure SQL Database Sync Group zurück.</span><span class="sxs-lookup"><span data-stu-id="8e0c4-103">Returns the logs of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="8e0c4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8e0c4-104">SYNTAX</span></span>

```
Get-AzSqlSyncGroupLog [-SyncGroupName] <String> -StartTime <DateTime> [-EndTime <DateTime>]
 [-LogLevel <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e0c4-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8e0c4-105">DESCRIPTION</span></span>
<span data-ttu-id="8e0c4-106">Das **Cmdlet "Get-AzSqlSyncGroupLog"** gibt die Protokolle einer Azure SQL Database Sync Group zurück.</span><span class="sxs-lookup"><span data-stu-id="8e0c4-106">The **Get-AzSqlSyncGroupLog** cmdlet returns the logs of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="8e0c4-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8e0c4-107">EXAMPLES</span></span>

### <span data-ttu-id="8e0c4-108">Beispiel 1: Erhalten der Protokolle einer Azure SQL-Synchronisierungsgruppe</span><span class="sxs-lookup"><span data-stu-id="8e0c4-108">Example 1: Get the logs of an Azure SQL Sync Group</span></span>
```
PS C:\>Get-AzSqlSyncGroupLog -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -StartTime "9/16/2016 11:31:12" -EndTime "9/16/2016 12:31:00" -LogLevel "All"
TimeStamp            LogLevel Details                                   Source
---------            -------- -------                                   ------
6/13/2017 9:14:26 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
6/13/2017 7:11:59 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
```

<span data-ttu-id="8e0c4-109">Dieser Befehl ruft die Protokolle einer Azure SQL-Synchronisierungsgruppe ab.</span><span class="sxs-lookup"><span data-stu-id="8e0c4-109">This command gets the logs of an Azure SQL Sync Group.</span></span>

## <span data-ttu-id="8e0c4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e0c4-110">PARAMETERS</span></span>

### <span data-ttu-id="8e0c4-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8e0c4-111">-DatabaseName</span></span>
<span data-ttu-id="8e0c4-112">Der Name der Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="8e0c4-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="8e0c4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e0c4-113">-DefaultProfile</span></span>
<span data-ttu-id="8e0c4-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="8e0c4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8e0c4-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="8e0c4-115">-EndTime</span></span>
<span data-ttu-id="8e0c4-116">Die Endzeit der zu abfragende Protokolle.</span><span class="sxs-lookup"><span data-stu-id="8e0c4-116">The end time of the logs to query.</span></span>

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

### <span data-ttu-id="8e0c4-117">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="8e0c4-117">-LogLevel</span></span>
<span data-ttu-id="8e0c4-118">Der Typ der zu abfragende Protokolle.</span><span class="sxs-lookup"><span data-stu-id="8e0c4-118">The type of the logs to query.</span></span>
<span data-ttu-id="8e0c4-119">Gültige Werte sind: "Fehler", "Warnung", "Erfolg" und "Alle".</span><span class="sxs-lookup"><span data-stu-id="8e0c4-119">Valid values are: 'Error', 'Warning', 'Success' and 'All'.</span></span>

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

### <span data-ttu-id="8e0c4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e0c4-120">-ResourceGroupName</span></span>
<span data-ttu-id="8e0c4-121">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8e0c4-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="8e0c4-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8e0c4-122">-ServerName</span></span>
<span data-ttu-id="8e0c4-123">Der Name des Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8e0c4-123">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="8e0c4-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="8e0c4-124">-StartTime</span></span>
<span data-ttu-id="8e0c4-125">Die Startzeit der zu abfragende Protokolle.</span><span class="sxs-lookup"><span data-stu-id="8e0c4-125">The start time of the logs to query.</span></span>

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

### <span data-ttu-id="8e0c4-126">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="8e0c4-126">-SyncGroupName</span></span>
<span data-ttu-id="8e0c4-127">Der Name der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="8e0c4-127">The sync group name.</span></span>

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

### <span data-ttu-id="8e0c4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e0c4-128">CommonParameters</span></span>
<span data-ttu-id="8e0c4-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e0c4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e0c4-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8e0c4-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e0c4-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8e0c4-131">INPUTS</span></span>

### <span data-ttu-id="8e0c4-132">System.String</span><span class="sxs-lookup"><span data-stu-id="8e0c4-132">System.String</span></span>

## <span data-ttu-id="8e0c4-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8e0c4-133">OUTPUTS</span></span>

### <span data-ttu-id="8e0c4-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupLogModel</span><span class="sxs-lookup"><span data-stu-id="8e0c4-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupLogModel</span></span>

## <span data-ttu-id="8e0c4-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8e0c4-135">NOTES</span></span>

## <span data-ttu-id="8e0c4-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8e0c4-136">RELATED LINKS</span></span>
