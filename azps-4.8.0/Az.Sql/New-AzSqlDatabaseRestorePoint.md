---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 67A9BB67-CF17-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseRestorePoint.md
ms.openlocfilehash: d2dc1b6acf1978976ce29adea2e79146828accb1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008858"
---
# <span data-ttu-id="483f9-101">New-AzSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="483f9-101">New-AzSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="483f9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="483f9-102">SYNOPSIS</span></span>
<span data-ttu-id="483f9-103">Erstellt einen neuen Wiederherstellungspunkt, von dem eine SQL-Datenbank wiederhergestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="483f9-103">Creates a new restore point from which a SQL Database can be restored.</span></span>

## <span data-ttu-id="483f9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="483f9-104">SYNTAX</span></span>

```
New-AzSqlDatabaseRestorePoint -RestorePointLabel <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="483f9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="483f9-105">DESCRIPTION</span></span>
<span data-ttu-id="483f9-106">Das Cmdlet **New-AzSqlDatabaseRestorePoint** erstellt einen neuen Wiederherstellungspunkt, aus dem ein Azure SQL-Data Warehouse wiederhergestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="483f9-106">The **New-AzSqlDatabaseRestorePoint** cmdlet creates a new restore point that an Azure SQL Data Warehouse can be restored from.</span></span>
<span data-ttu-id="483f9-107">Dieses Cmdlet wird derzeit für Azure SQL Data Warehouse unterstützt.</span><span class="sxs-lookup"><span data-stu-id="483f9-107">This cmdlet is currently supported for Azure SQL Data Warehouse.</span></span>

## <span data-ttu-id="483f9-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="483f9-108">EXAMPLES</span></span>

### <span data-ttu-id="483f9-109">Beispiel 1: Erstellen eines Wiederherstellungspunkts</span><span class="sxs-lookup"><span data-stu-id="483f9-109">Example 1: Create a restore point</span></span>
```
PS C:\>New-AzSqlDatabaseRestorePoint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RestorePointLabel "RestorePoint01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
DatabaseName             : database01
Location                 : Central US
RestorePointType         : DISCRETE
RestorePointCreationDate : 8/12/2015 12:00:00 AM
EarliestRestoreDate      : 
RestorePointLabel        : RestorePoint01
```

<span data-ttu-id="483f9-110">Dieser Befehl erstellt einen Wiederherstellungspunkt für Azure SQL Data Warehouse und gibt die Details des Wiederherstellungspunkts zurück.</span><span class="sxs-lookup"><span data-stu-id="483f9-110">This command creates a restore point for Azure SQL Data Warehouse and returns the details of the restore point.</span></span>

## <span data-ttu-id="483f9-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="483f9-111">PARAMETERS</span></span>

### <span data-ttu-id="483f9-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="483f9-112">-DatabaseName</span></span>
<span data-ttu-id="483f9-113">Gibt den Namen der SQL-Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="483f9-113">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="483f9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="483f9-114">-DefaultProfile</span></span>
<span data-ttu-id="483f9-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="483f9-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="483f9-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="483f9-116">-ResourceGroupName</span></span>
<span data-ttu-id="483f9-117">Gibt den Namen der Ressourcengruppe an, der die SQL-Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="483f9-117">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="483f9-118">-RestorePointLabel</span><span class="sxs-lookup"><span data-stu-id="483f9-118">-RestorePointLabel</span></span>
<span data-ttu-id="483f9-119">Gibt die Beschriftung des Wiederherstellungspunkts zur einfachen Identifizierung an.</span><span class="sxs-lookup"><span data-stu-id="483f9-119">Specifies the label of the restore point for easy identification.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="483f9-120">-Servername</span><span class="sxs-lookup"><span data-stu-id="483f9-120">-ServerName</span></span>
<span data-ttu-id="483f9-121">Gibt den Namen des AzureSQL-Servers an, der die Datenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="483f9-121">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="483f9-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="483f9-122">-Confirm</span></span>
<span data-ttu-id="483f9-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="483f9-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="483f9-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="483f9-124">-WhatIf</span></span>
<span data-ttu-id="483f9-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="483f9-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="483f9-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="483f9-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="483f9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="483f9-127">CommonParameters</span></span>
<span data-ttu-id="483f9-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="483f9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="483f9-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="483f9-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="483f9-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="483f9-130">INPUTS</span></span>

### <span data-ttu-id="483f9-131">System. String</span><span class="sxs-lookup"><span data-stu-id="483f9-131">System.String</span></span>

## <span data-ttu-id="483f9-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="483f9-132">OUTPUTS</span></span>

### <span data-ttu-id="483f9-133">Microsoft. Azure. Commands. SQL. Backup. Model. AzureSqlDatabaseRestorePointModel</span><span class="sxs-lookup"><span data-stu-id="483f9-133">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span></span>

## <span data-ttu-id="483f9-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="483f9-134">NOTES</span></span>

## <span data-ttu-id="483f9-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="483f9-135">RELATED LINKS</span></span>
