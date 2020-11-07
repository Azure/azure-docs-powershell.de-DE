---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 67A9BB67-CF17-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseRestorePoint.md
ms.openlocfilehash: 52024cfa0adcc93ecb278f0d9bfbad7ea8023530
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659225"
---
# <span data-ttu-id="c635b-101">Get-AzSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="c635b-101">Get-AzSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="c635b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c635b-102">SYNOPSIS</span></span>
<span data-ttu-id="c635b-103">Ruft die eindeutigen Wiederherstellungspunkte ab, aus denen ein SQL Data Warehouse wiederhergestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="c635b-103">Retrieves the distinct restore points from which a SQL Data Warehouse can be restored.</span></span>

## <span data-ttu-id="c635b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c635b-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseRestorePoint [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c635b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c635b-105">DESCRIPTION</span></span>
<span data-ttu-id="c635b-106">Das Cmdlet " **Get-AzSqlDatabaseRestorePoint** " Ruft die eindeutigen Wiederherstellungspunkte ab, aus denen ein Azure SQL-Data Warehouse wiederhergestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="c635b-106">The **Get-AzSqlDatabaseRestorePoint** cmdlet retrieves the distinct restore points that an Azure SQL Data Warehouse can be restored from.</span></span>
<span data-ttu-id="c635b-107">Bei einer Azure SQL-Datenbank ist das Fenster wiederherstellen fortlaufend.</span><span class="sxs-lookup"><span data-stu-id="c635b-107">For an Azure SQL Database, the restore window is continuous.</span></span>
<span data-ttu-id="c635b-108">Dies bedeutet, dass jeder Zeitpunkt in der Aufbewahrungszeit der Datenbank als Wiederherstellungspunkt verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c635b-108">This means that any point in time in the backup retention period of the database can be used as a restore point.</span></span>
<span data-ttu-id="c635b-109">Dieses Cmdlet wird auch vom SQL Server Stretch-Datenbankdienst auf Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c635b-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="c635b-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c635b-110">EXAMPLES</span></span>

### <span data-ttu-id="c635b-111">Beispiel 1: Abrufen aller Wiederherstellungspunkte</span><span class="sxs-lookup"><span data-stu-id="c635b-111">Example 1: Get all restore points</span></span>
```
PS C:\>Get-AzSqlDatabaseRestorePoint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
DatabaseName             : database01
Location                 : Central US
RestorePointType         : CONTINUOUS
RestorePointCreationDate : 
EarliestRestoreDate      : 8/12/2015 12:00:00 AM
RestorePointLabel        : RestorePoint01
```

<span data-ttu-id="c635b-112">Dieser Befehl gibt alle verfügbaren Wiederherstellungspunkte für die Azure SQL-Datenbank mit dem Namen database01 zurück.</span><span class="sxs-lookup"><span data-stu-id="c635b-112">This command returns all available restore points for the Azure SQL Database named Database01.</span></span>

## <span data-ttu-id="c635b-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="c635b-113">PARAMETERS</span></span>

### <span data-ttu-id="c635b-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c635b-114">-DatabaseName</span></span>
<span data-ttu-id="c635b-115">Gibt den Namen der SQL-Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="c635b-115">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="c635b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c635b-116">-DefaultProfile</span></span>
<span data-ttu-id="c635b-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="c635b-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c635b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c635b-118">-ResourceGroupName</span></span>
<span data-ttu-id="c635b-119">Gibt den Namen der Ressourcengruppe an, der die SQL-Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="c635b-119">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="c635b-120">-Servername</span><span class="sxs-lookup"><span data-stu-id="c635b-120">-ServerName</span></span>
<span data-ttu-id="c635b-121">Gibt den Namen des AzureSQL-Servers an, der die Datenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="c635b-121">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="c635b-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c635b-122">-Confirm</span></span>
<span data-ttu-id="c635b-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c635b-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c635b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c635b-124">-WhatIf</span></span>
<span data-ttu-id="c635b-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c635b-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c635b-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c635b-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c635b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c635b-127">CommonParameters</span></span>
<span data-ttu-id="c635b-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c635b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c635b-129">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c635b-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c635b-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c635b-130">INPUTS</span></span>

### <span data-ttu-id="c635b-131">System. String</span><span class="sxs-lookup"><span data-stu-id="c635b-131">System.String</span></span>

## <span data-ttu-id="c635b-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c635b-132">OUTPUTS</span></span>

### <span data-ttu-id="c635b-133">Microsoft. Azure. Commands. SQL. Backup. Model. AzureSqlDatabaseRestorePointModel</span><span class="sxs-lookup"><span data-stu-id="c635b-133">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span></span>

## <span data-ttu-id="c635b-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="c635b-134">NOTES</span></span>

## <span data-ttu-id="c635b-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c635b-135">RELATED LINKS</span></span>
