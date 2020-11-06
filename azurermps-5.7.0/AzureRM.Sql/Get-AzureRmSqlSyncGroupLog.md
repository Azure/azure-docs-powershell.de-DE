---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlsyncgrouplog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncGroupLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncGroupLog.md
ms.openlocfilehash: f8a939dbaac0dadb52aff28b208f7fb69ef836df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500377"
---
# <span data-ttu-id="db527-101">Get-AzureRmSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="db527-101">Get-AzureRmSqlSyncGroupLog</span></span>

## <span data-ttu-id="db527-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="db527-102">SYNOPSIS</span></span>
<span data-ttu-id="db527-103">Gibt die Protokolle einer Azure SQL-Daten Bank Synchronisierungsgruppe zurück.</span><span class="sxs-lookup"><span data-stu-id="db527-103">Returns the logs of an Azure SQL Database Sync Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db527-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="db527-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncGroupLog [-SyncGroupName] <String> -StartTime <DateTime> [-EndTime <DateTime>]
 [-LogLevel <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db527-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="db527-105">DESCRIPTION</span></span>
<span data-ttu-id="db527-106">Das Cmdlet " **Get-AzureRmSqlSyncGroupLog** " gibt die Protokolle einer Azure SQL-Daten Bank Synchronisierungsgruppe zurück.</span><span class="sxs-lookup"><span data-stu-id="db527-106">The **Get-AzureRmSqlSyncGroupLog** cmdlet returns the logs of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="db527-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="db527-107">EXAMPLES</span></span>

### <span data-ttu-id="db527-108">Beispiel 1: Abrufen der Protokolle einer Azure SQL-Synchronisierungsgruppe</span><span class="sxs-lookup"><span data-stu-id="db527-108">Example 1: Get the logs of an Azure SQL Sync Group</span></span>
```
PS C:\>Get-AzureRmSqlSyncGroupLog -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -StartTime "9/16/2016 11:31:12" -EndTime "9/16/2016 12:31:00" -LogLevel "All"
TimeStamp            LogLevel Details                                   Source
---------            -------- -------                                   ------
6/13/2017 9:14:26 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
6/13/2017 7:11:59 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
```

<span data-ttu-id="db527-109">Dieser Befehl ruft die Protokolle einer Azure SQL-Synchronisierungsgruppe ab.</span><span class="sxs-lookup"><span data-stu-id="db527-109">This command gets the logs of an Azure SQL Sync Group.</span></span>

## <span data-ttu-id="db527-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="db527-110">PARAMETERS</span></span>

### <span data-ttu-id="db527-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="db527-111">-DatabaseName</span></span>
<span data-ttu-id="db527-112">Der Name der Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="db527-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="db527-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db527-113">-DefaultProfile</span></span>
<span data-ttu-id="db527-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="db527-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="db527-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="db527-115">-EndTime</span></span>
<span data-ttu-id="db527-116">Die Endzeit der abzufragenden Protokolle.</span><span class="sxs-lookup"><span data-stu-id="db527-116">The end time of the logs to query.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db527-117">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="db527-117">-LogLevel</span></span>
<span data-ttu-id="db527-118">Der Typ der abzufragenden Protokolle.</span><span class="sxs-lookup"><span data-stu-id="db527-118">The type of the logs to query.</span></span>
<span data-ttu-id="db527-119">Gültige Werte sind: "Fehler", "Warnung", "Erfolg" und "alle".</span><span class="sxs-lookup"><span data-stu-id="db527-119">Valid values are: 'Error', 'Warning', 'Success' and 'All'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Error, Warning, Success, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db527-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db527-120">-ResourceGroupName</span></span>
<span data-ttu-id="db527-121">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="db527-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="db527-122">-Servername</span><span class="sxs-lookup"><span data-stu-id="db527-122">-ServerName</span></span>
<span data-ttu-id="db527-123">Der Name des Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="db527-123">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="db527-124">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="db527-124">-StartTime</span></span>
<span data-ttu-id="db527-125">Die Startzeit der abzufragenden Protokolle.</span><span class="sxs-lookup"><span data-stu-id="db527-125">The start time of the logs to query.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db527-126">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="db527-126">-SyncGroupName</span></span>
<span data-ttu-id="db527-127">Der Name der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="db527-127">The sync group name.</span></span>

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

### <span data-ttu-id="db527-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db527-128">CommonParameters</span></span>
<span data-ttu-id="db527-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db527-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db527-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db527-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db527-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="db527-131">INPUTS</span></span>

### <span data-ttu-id="db527-132">Keine</span><span class="sxs-lookup"><span data-stu-id="db527-132">None</span></span>
<span data-ttu-id="db527-133">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="db527-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="db527-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="db527-134">OUTPUTS</span></span>

### <span data-ttu-id="db527-135">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncGroupLogModel</span><span class="sxs-lookup"><span data-stu-id="db527-135">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupLogModel</span></span>

## <span data-ttu-id="db527-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="db527-136">NOTES</span></span>

## <span data-ttu-id="db527-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="db527-137">RELATED LINKS</span></span>
