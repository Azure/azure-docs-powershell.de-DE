---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: a2c7192fc1ce2055b05a4f943a0c04560f1e714e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179809"
---
# <span data-ttu-id="5d17d-101">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5d17d-101">Get-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="5d17d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5d17d-102">SYNOPSIS</span></span>
<span data-ttu-id="5d17d-103">Ruft Azure SQL-Datenbank-failovergruppen ab oder listet Sie auf.</span><span class="sxs-lookup"><span data-stu-id="5d17d-103">Gets or lists Azure SQL Database Failover Groups.</span></span>

## <span data-ttu-id="5d17d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5d17d-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d17d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5d17d-105">DESCRIPTION</span></span>
<span data-ttu-id="5d17d-106">Ruft eine bestimmte Azure SQL-Datenbankfailover-Gruppe ab oder listet die Failovercluster auf einem Server auf.</span><span class="sxs-lookup"><span data-stu-id="5d17d-106">Gets a specific Azure SQL Database Failover Group or lists the Failover Groups on a server.</span></span>
<span data-ttu-id="5d17d-107">Für die Ausführung des Befehls kann entweder der Server in der Gruppe Failover verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5d17d-107">Either server in the Failover Group may be used to execute the command.</span></span> <span data-ttu-id="5d17d-108">Die zurückgegebenen Werte geben den Zustand des angegebenen Servers in Bezug auf die failovergruppe wieder.</span><span class="sxs-lookup"><span data-stu-id="5d17d-108">The returned values will reflect the state of the specified server with respect to the Failover Group.</span></span>

## <span data-ttu-id="5d17d-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5d17d-109">EXAMPLES</span></span>

### <span data-ttu-id="5d17d-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5d17d-110">Example 1</span></span>
```
PS C:\> $failoverGroups = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server
```

<span data-ttu-id="5d17d-111">Listet alle Failovercluster auf einem Server auf.</span><span class="sxs-lookup"><span data-stu-id="5d17d-111">Lists all Failover Groups on a server.</span></span>

### <span data-ttu-id="5d17d-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="5d17d-112">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server -FailoverGroupName fg
```

<span data-ttu-id="5d17d-113">Abrufen einer bestimmten failovergruppe</span><span class="sxs-lookup"><span data-stu-id="5d17d-113">Get a specific Failover Group.</span></span>

### <span data-ttu-id="5d17d-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="5d17d-114">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server -FailoverGroupName fg*
```

<span data-ttu-id="5d17d-115">Rufen Sie alle Failovercluster auf einem Server ab, die mit "FG" beginnen.</span><span class="sxs-lookup"><span data-stu-id="5d17d-115">Get all failover groups in a server that start with "fg".</span></span>

## <span data-ttu-id="5d17d-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="5d17d-116">PARAMETERS</span></span>

### <span data-ttu-id="5d17d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d17d-117">-DefaultProfile</span></span>
<span data-ttu-id="5d17d-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="5d17d-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5d17d-119">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="5d17d-119">-FailoverGroupName</span></span>
<span data-ttu-id="5d17d-120">Der Name der Azure SQL-Daten Bank Failover-Gruppe, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="5d17d-120">The name of the Azure SQL Database Failover Group to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d17d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d17d-121">-ResourceGroupName</span></span>
<span data-ttu-id="5d17d-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5d17d-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="5d17d-123">-Servername</span><span class="sxs-lookup"><span data-stu-id="5d17d-123">-ServerName</span></span>
<span data-ttu-id="5d17d-124">Der Name des Azure SQL-Datenbankservers, aus dem die failovergruppe abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="5d17d-124">The name of the Azure SQL Database Server from which to retrieve the Failover Group.</span></span>

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

### <span data-ttu-id="5d17d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d17d-125">CommonParameters</span></span>
<span data-ttu-id="5d17d-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d17d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d17d-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5d17d-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d17d-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5d17d-128">INPUTS</span></span>

### <span data-ttu-id="5d17d-129">System. String</span><span class="sxs-lookup"><span data-stu-id="5d17d-129">System.String</span></span>

## <span data-ttu-id="5d17d-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5d17d-130">OUTPUTS</span></span>

### <span data-ttu-id="5d17d-131">Microsoft. Azure. Commands. SQL. failovergroup. Model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="5d17d-131">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="5d17d-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="5d17d-132">NOTES</span></span>

## <span data-ttu-id="5d17d-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5d17d-133">RELATED LINKS</span></span>

[<span data-ttu-id="5d17d-134">Neu – AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5d17d-134">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="5d17d-135">Satz-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5d17d-135">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="5d17d-136">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5d17d-136">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="5d17d-137">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5d17d-137">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="5d17d-138">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5d17d-138">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="5d17d-139">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5d17d-139">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="5d17d-140">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="5d17d-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
