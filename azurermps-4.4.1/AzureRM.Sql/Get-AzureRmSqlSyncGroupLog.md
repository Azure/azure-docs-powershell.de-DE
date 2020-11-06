---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncGroupLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncGroupLog.md
ms.openlocfilehash: 924e00578383e103d1451e311d027edd02752496
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478881"
---
# <span data-ttu-id="67d88-101">Get-AzureRmSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="67d88-101">Get-AzureRmSqlSyncGroupLog</span></span>

## <span data-ttu-id="67d88-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="67d88-102">SYNOPSIS</span></span>
<span data-ttu-id="67d88-103">Gibt die Protokolle einer Azure SQL-Daten Bank Synchronisierungsgruppe zurück.</span><span class="sxs-lookup"><span data-stu-id="67d88-103">Returns the logs of an Azure SQL Database Sync Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67d88-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="67d88-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncGroupLog [-SyncGroupName] <String> -StartTime <DateTime> [-EndTime <DateTime>]
 [-LogLevel <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67d88-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="67d88-105">DESCRIPTION</span></span>
<span data-ttu-id="67d88-106">Das Cmdlet " **Get-AzureRmSqlSyncGroupLog** " gibt die Protokolle einer Azure SQL-Daten Bank Synchronisierungsgruppe zurück.</span><span class="sxs-lookup"><span data-stu-id="67d88-106">The **Get-AzureRmSqlSyncGroupLog** cmdlet returns the logs of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="67d88-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="67d88-107">EXAMPLES</span></span>

### <span data-ttu-id="67d88-108">Beispiel 1: Abrufen der Protokolle einer Azure SQL-Synchronisierungsgruppe</span><span class="sxs-lookup"><span data-stu-id="67d88-108">Example 1: Get the logs of an Azure SQL Sync Group</span></span>
```
PS C:\>Get-AzureRmSqlSyncGroupLog -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -StartTime "9/16/2016 11:31:12" -EndTime "9/16/2016 12:31:00" -LogLevel "All"
TimeStamp            LogLevel Details                                   Source
---------            -------- -------                                   ------
6/13/2017 9:14:26 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
6/13/2017 7:11:59 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
```

<span data-ttu-id="67d88-109">Dieser Befehl ruft die Protokolle einer Azure SQL-Synchronisierungsgruppe ab.</span><span class="sxs-lookup"><span data-stu-id="67d88-109">This command gets the logs of an Azure SQL Sync Group.</span></span>

## <span data-ttu-id="67d88-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="67d88-110">PARAMETERS</span></span>

### <span data-ttu-id="67d88-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="67d88-111">-DatabaseName</span></span>
<span data-ttu-id="67d88-112">Der Name der Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="67d88-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="67d88-113">-EndTime</span><span class="sxs-lookup"><span data-stu-id="67d88-113">-EndTime</span></span>
<span data-ttu-id="67d88-114">Die Endzeit der abzufragenden Protokolle.</span><span class="sxs-lookup"><span data-stu-id="67d88-114">The end time of the logs to query.</span></span>

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

### <span data-ttu-id="67d88-115">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="67d88-115">-LogLevel</span></span>
<span data-ttu-id="67d88-116">Der Typ der abzufragenden Protokolle.</span><span class="sxs-lookup"><span data-stu-id="67d88-116">The type of the logs to query.</span></span>
<span data-ttu-id="67d88-117">Gültige Werte sind: "Fehler", "Warnung", "Erfolg" und "alle".</span><span class="sxs-lookup"><span data-stu-id="67d88-117">Valid values are: 'Error', 'Warning', 'Success' and 'All'.</span></span>

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

### <span data-ttu-id="67d88-118">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="67d88-118">-SyncGroupName</span></span>
<span data-ttu-id="67d88-119">Der Name der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="67d88-119">The sync group name.</span></span>

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

### <span data-ttu-id="67d88-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67d88-120">-ResourceGroupName</span></span>
<span data-ttu-id="67d88-121">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="67d88-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="67d88-122">-Servername</span><span class="sxs-lookup"><span data-stu-id="67d88-122">-ServerName</span></span>
<span data-ttu-id="67d88-123">Der Name des Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="67d88-123">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="67d88-124">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="67d88-124">-StartTime</span></span>
<span data-ttu-id="67d88-125">Die Startzeit der abzufragenden Protokolle.</span><span class="sxs-lookup"><span data-stu-id="67d88-125">The start time of the logs to query.</span></span>

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

### <span data-ttu-id="67d88-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67d88-126">-DefaultProfile</span></span>
<span data-ttu-id="67d88-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="67d88-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67d88-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67d88-128">CommonParameters</span></span>
<span data-ttu-id="67d88-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67d88-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67d88-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67d88-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67d88-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="67d88-131">INPUTS</span></span>

## <span data-ttu-id="67d88-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="67d88-132">OUTPUTS</span></span>

### <span data-ttu-id="67d88-133">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncGroupLogModel</span><span class="sxs-lookup"><span data-stu-id="67d88-133">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupLogModel</span></span>

## <span data-ttu-id="67d88-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="67d88-134">NOTES</span></span>

## <span data-ttu-id="67d88-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="67d88-135">RELATED LINKS</span></span>

