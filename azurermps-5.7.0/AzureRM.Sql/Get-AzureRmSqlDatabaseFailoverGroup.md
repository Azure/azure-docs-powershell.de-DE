---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseFailoverGroup.md
ms.openlocfilehash: a4440601610af0b55282cbe0e78209379f570edb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476509"
---
# <span data-ttu-id="8e3dd-101">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="8e3dd-101">Get-AzureRmSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="8e3dd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8e3dd-102">SYNOPSIS</span></span>
<span data-ttu-id="8e3dd-103">Ruft Azure SQL-Datenbank-failovergruppen ab oder listet Sie auf.</span><span class="sxs-lookup"><span data-stu-id="8e3dd-103">Gets or lists Azure SQL Database Failover Groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e3dd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e3dd-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e3dd-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8e3dd-105">DESCRIPTION</span></span>
<span data-ttu-id="8e3dd-106">Ruft eine bestimmte Azure SQL-Datenbankfailover-Gruppe ab oder listet die Failovercluster auf einem Server auf.</span><span class="sxs-lookup"><span data-stu-id="8e3dd-106">Gets a specific Azure SQL Database Failover Group or lists the Failover Groups on a server.</span></span>

<span data-ttu-id="8e3dd-107">Für die Ausführung des Befehls kann entweder der Server in der Gruppe Failover verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8e3dd-107">Either server in the Failover Group may be used to execute the command.</span></span> <span data-ttu-id="8e3dd-108">Die zurückgegebenen Werte geben den Zustand des angegebenen Servers in Bezug auf die failovergruppe wieder.</span><span class="sxs-lookup"><span data-stu-id="8e3dd-108">The returned values will reflect the state of the specified server with respect to the Failover Group.</span></span>

## <span data-ttu-id="8e3dd-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8e3dd-109">EXAMPLES</span></span>

### <span data-ttu-id="8e3dd-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8e3dd-110">Example 1</span></span>
```
PS C:\> $failoverGroups = Get-AzureRMSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server
```

<span data-ttu-id="8e3dd-111">Listet alle Failovercluster auf einem Server auf.</span><span class="sxs-lookup"><span data-stu-id="8e3dd-111">Lists all Failover Groups on a server.</span></span>

### <span data-ttu-id="8e3dd-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="8e3dd-112">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzureRMSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server -FailoverGroupName fg
```

<span data-ttu-id="8e3dd-113">Abrufen einer bestimmten failovergruppe</span><span class="sxs-lookup"><span data-stu-id="8e3dd-113">Get a specific Failover Group.</span></span>

## <span data-ttu-id="8e3dd-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="8e3dd-114">PARAMETERS</span></span>

### <span data-ttu-id="8e3dd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e3dd-115">-DefaultProfile</span></span>
<span data-ttu-id="8e3dd-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="8e3dd-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8e3dd-117">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="8e3dd-117">-FailoverGroupName</span></span>
<span data-ttu-id="8e3dd-118">Der Name der Azure SQL-Daten Bank Failover-Gruppe, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="8e3dd-118">The name of the Azure SQL Database Failover Group to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e3dd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e3dd-119">-ResourceGroupName</span></span>
<span data-ttu-id="8e3dd-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8e3dd-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="8e3dd-121">-Servername</span><span class="sxs-lookup"><span data-stu-id="8e3dd-121">-ServerName</span></span>
<span data-ttu-id="8e3dd-122">Der Name des Azure SQL-Datenbankservers, aus dem die failovergruppe abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="8e3dd-122">The name of the Azure SQL Database Server from which to retrieve the Failover Group.</span></span>

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

### <span data-ttu-id="8e3dd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e3dd-123">CommonParameters</span></span>
<span data-ttu-id="8e3dd-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e3dd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e3dd-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e3dd-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e3dd-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8e3dd-126">INPUTS</span></span>

### <span data-ttu-id="8e3dd-127">System. String</span><span class="sxs-lookup"><span data-stu-id="8e3dd-127">System.String</span></span>

## <span data-ttu-id="8e3dd-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8e3dd-128">OUTPUTS</span></span>

### <span data-ttu-id="8e3dd-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="8e3dd-129">System.Object</span></span>

## <span data-ttu-id="8e3dd-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="8e3dd-130">NOTES</span></span>

## <span data-ttu-id="8e3dd-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8e3dd-131">RELATED LINKS</span></span>

[<span data-ttu-id="8e3dd-132">Neu – AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="8e3dd-132">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="8e3dd-133">Satz-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="8e3dd-133">Set-AzureRmSqlDatabaseFailoverGroup</span></span>](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="8e3dd-134">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="8e3dd-134">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="8e3dd-135">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="8e3dd-135">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="8e3dd-136">Switch-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="8e3dd-136">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="8e3dd-137">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="8e3dd-137">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="8e3dd-138">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="8e3dd-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
