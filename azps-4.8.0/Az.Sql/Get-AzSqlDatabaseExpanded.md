---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 952967EB-AEAD-4597-B837-6669CE73739E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseexpanded
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseExpanded.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseExpanded.md
ms.openlocfilehash: 18d387aeb8ca9e777af0767ce407e373fc2adf09
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166839"
---
# <span data-ttu-id="58e67-101">Get-AzSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="58e67-101">Get-AzSqlDatabaseExpanded</span></span>

## <span data-ttu-id="58e67-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="58e67-102">SYNOPSIS</span></span>
<span data-ttu-id="58e67-103">Ruft eine Datenbank und deren erweiterte Eigenschaftswerte ab.</span><span class="sxs-lookup"><span data-stu-id="58e67-103">Gets a database and its expanded property values.</span></span>

## <span data-ttu-id="58e67-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="58e67-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseExpanded [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58e67-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="58e67-105">DESCRIPTION</span></span>
<span data-ttu-id="58e67-106">Das Cmdlet " **Get-AzSqlDatabaseExpanded** " Ruft eine Datenbank und deren erweiterte Eigenschaftswerte ab.</span><span class="sxs-lookup"><span data-stu-id="58e67-106">The **Get-AzSqlDatabaseExpanded** cmdlet gets a database and its expanded property values.</span></span>
<span data-ttu-id="58e67-107">Dieses Cmdlet wird auch vom SQL Server Stretch-Datenbankdienst auf Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="58e67-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="58e67-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="58e67-108">EXAMPLES</span></span>

### <span data-ttu-id="58e67-109">Beispiel 1: Abrufen von Datenbankobjekten mit Informationen zum Dienststatus-Ratgeber</span><span class="sxs-lookup"><span data-stu-id="58e67-109">Example 1: Get database object that has service tier advisor information</span></span>
```
PS C:\> Get-AzSqlDatabaseExpanded -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="58e67-110">Dieser Befehl gibt die Datenbank mit erweiterten Eigenschaften zurück, die die Informationen zum Dienststatus-Ratgeber enthalten.</span><span class="sxs-lookup"><span data-stu-id="58e67-110">This command returns the database that has expanded properties that contain the service tier advisor information.</span></span>

### <span data-ttu-id="58e67-111">Beispiel 2: Auflisten von Datenbankobjekten mithilfe von Filtern</span><span class="sxs-lookup"><span data-stu-id="58e67-111">Example 2: List database objects using filtering</span></span>
```
PS C:\> Get-AzSqlDatabaseExpanded -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database*"
```

<span data-ttu-id="58e67-112">Dieser Befehl gibt das erweiterte Datenbankobjekt für alle Datenbanken in Server01 zurück, die mit "Datenbank" beginnen.</span><span class="sxs-lookup"><span data-stu-id="58e67-112">This command returns expanded database object for all databases in Server01 that start with "Database".</span></span>

## <span data-ttu-id="58e67-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="58e67-113">PARAMETERS</span></span>

### <span data-ttu-id="58e67-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="58e67-114">-DatabaseName</span></span>
<span data-ttu-id="58e67-115">Gibt den Namen der Datenbank an, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="58e67-115">Specifies the name of the database to get.</span></span>

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

### <span data-ttu-id="58e67-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58e67-116">-DefaultProfile</span></span>
<span data-ttu-id="58e67-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="58e67-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="58e67-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58e67-118">-ResourceGroupName</span></span>
<span data-ttu-id="58e67-119">Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="58e67-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="58e67-120">-Servername</span><span class="sxs-lookup"><span data-stu-id="58e67-120">-ServerName</span></span>
<span data-ttu-id="58e67-121">Gibt den Namen des Servers an, der die Datenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="58e67-121">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="58e67-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="58e67-122">-Confirm</span></span>
<span data-ttu-id="58e67-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="58e67-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58e67-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58e67-124">-WhatIf</span></span>
<span data-ttu-id="58e67-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="58e67-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58e67-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="58e67-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58e67-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58e67-127">CommonParameters</span></span>
<span data-ttu-id="58e67-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58e67-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58e67-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="58e67-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58e67-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="58e67-130">INPUTS</span></span>

### <span data-ttu-id="58e67-131">System. String</span><span class="sxs-lookup"><span data-stu-id="58e67-131">System.String</span></span>

## <span data-ttu-id="58e67-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="58e67-132">OUTPUTS</span></span>

### <span data-ttu-id="58e67-133">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModelExpanded</span><span class="sxs-lookup"><span data-stu-id="58e67-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModelExpanded</span></span>

## <span data-ttu-id="58e67-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="58e67-134">NOTES</span></span>

## <span data-ttu-id="58e67-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="58e67-135">RELATED LINKS</span></span>

[<span data-ttu-id="58e67-136">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="58e67-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
