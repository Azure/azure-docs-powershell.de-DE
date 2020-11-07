---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncgrouplog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroupLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroupLog.md
ms.openlocfilehash: 0343cddd12fdf1fe438ec2c4c9c3c5763719cd43
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93826039"
---
# <span data-ttu-id="48784-101">Get-AzSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="48784-101">Get-AzSqlSyncGroupLog</span></span>

## <span data-ttu-id="48784-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="48784-102">SYNOPSIS</span></span>
<span data-ttu-id="48784-103">Gibt die Protokolle einer Azure SQL-Daten Bank Synchronisierungsgruppe zurück.</span><span class="sxs-lookup"><span data-stu-id="48784-103">Returns the logs of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="48784-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="48784-104">SYNTAX</span></span>

```
Get-AzSqlSyncGroupLog [-SyncGroupName] <String> -StartTime <DateTime> [-EndTime <DateTime>]
 [-LogLevel <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48784-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="48784-105">DESCRIPTION</span></span>
<span data-ttu-id="48784-106">Das Cmdlet " **Get-AzSqlSyncGroupLog** " gibt die Protokolle einer Azure SQL-Daten Bank Synchronisierungsgruppe zurück.</span><span class="sxs-lookup"><span data-stu-id="48784-106">The **Get-AzSqlSyncGroupLog** cmdlet returns the logs of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="48784-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="48784-107">EXAMPLES</span></span>

### <span data-ttu-id="48784-108">Beispiel 1: Abrufen der Protokolle einer Azure SQL-Synchronisierungsgruppe</span><span class="sxs-lookup"><span data-stu-id="48784-108">Example 1: Get the logs of an Azure SQL Sync Group</span></span>
```
PS C:\>Get-AzSqlSyncGroupLog -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -StartTime "9/16/2016 11:31:12" -EndTime "9/16/2016 12:31:00" -LogLevel "All"
TimeStamp            LogLevel Details                                   Source
---------            -------- -------                                   ------
6/13/2017 9:14:26 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
6/13/2017 7:11:59 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
```

<span data-ttu-id="48784-109">Dieser Befehl ruft die Protokolle einer Azure SQL-Synchronisierungsgruppe ab.</span><span class="sxs-lookup"><span data-stu-id="48784-109">This command gets the logs of an Azure SQL Sync Group.</span></span>

## <span data-ttu-id="48784-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="48784-110">PARAMETERS</span></span>

### <span data-ttu-id="48784-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="48784-111">-DatabaseName</span></span>
<span data-ttu-id="48784-112">Der Name der Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="48784-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="48784-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48784-113">-DefaultProfile</span></span>
<span data-ttu-id="48784-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="48784-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="48784-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="48784-115">-EndTime</span></span>
<span data-ttu-id="48784-116">Die Endzeit der abzufragenden Protokolle.</span><span class="sxs-lookup"><span data-stu-id="48784-116">The end time of the logs to query.</span></span>

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

### <span data-ttu-id="48784-117">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="48784-117">-LogLevel</span></span>
<span data-ttu-id="48784-118">Der Typ der abzufragenden Protokolle.</span><span class="sxs-lookup"><span data-stu-id="48784-118">The type of the logs to query.</span></span>
<span data-ttu-id="48784-119">Gültige Werte sind: "Fehler", "Warnung", "Erfolg" und "alle".</span><span class="sxs-lookup"><span data-stu-id="48784-119">Valid values are: 'Error', 'Warning', 'Success' and 'All'.</span></span>

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

### <span data-ttu-id="48784-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48784-120">-ResourceGroupName</span></span>
<span data-ttu-id="48784-121">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="48784-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="48784-122">-Servername</span><span class="sxs-lookup"><span data-stu-id="48784-122">-ServerName</span></span>
<span data-ttu-id="48784-123">Der Name des Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="48784-123">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="48784-124">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="48784-124">-StartTime</span></span>
<span data-ttu-id="48784-125">Die Startzeit der abzufragenden Protokolle.</span><span class="sxs-lookup"><span data-stu-id="48784-125">The start time of the logs to query.</span></span>

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

### <span data-ttu-id="48784-126">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="48784-126">-SyncGroupName</span></span>
<span data-ttu-id="48784-127">Der Name der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="48784-127">The sync group name.</span></span>

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

### <span data-ttu-id="48784-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48784-128">CommonParameters</span></span>
<span data-ttu-id="48784-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48784-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48784-130">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="48784-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48784-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="48784-131">INPUTS</span></span>

### <span data-ttu-id="48784-132">System. String</span><span class="sxs-lookup"><span data-stu-id="48784-132">System.String</span></span>

## <span data-ttu-id="48784-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="48784-133">OUTPUTS</span></span>

### <span data-ttu-id="48784-134">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncGroupLogModel</span><span class="sxs-lookup"><span data-stu-id="48784-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupLogModel</span></span>

## <span data-ttu-id="48784-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="48784-135">NOTES</span></span>

## <span data-ttu-id="48784-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="48784-136">RELATED LINKS</span></span>
