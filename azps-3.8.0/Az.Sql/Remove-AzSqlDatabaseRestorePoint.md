---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 67A9BB67-EF14-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseRestorePoint.md
ms.openlocfilehash: 2e98f832bd13509a853d85037a413b6fd5895695
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003402"
---
# <span data-ttu-id="9eb88-101">Remove-AzSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="9eb88-101">Remove-AzSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="9eb88-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9eb88-102">SYNOPSIS</span></span>
<span data-ttu-id="9eb88-103">Entfernt den angegebenen Wiederherstellungspunkt aus einer SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="9eb88-103">Removes given restore point from a SQL Database.</span></span>

## <span data-ttu-id="9eb88-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9eb88-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseRestorePoint -RestorePointCreationDate <DateTime> [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9eb88-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9eb88-105">DESCRIPTION</span></span>
<span data-ttu-id="9eb88-106">Das Cmdlet **Remove-AzSqlDatabaseRestorePoint** entfernt den angegebenen Wiederherstellungspunkt aus der Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="9eb88-106">The **Remove-AzSqlDatabaseRestorePoint** cmdlet removes given restore point from Azure SQL Database.</span></span>
<span data-ttu-id="9eb88-107">Dieses Cmdlet wird derzeit vom SQL Server Datawarehouse-Dienst in Azure SQL-Datenbank unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9eb88-107">This cmdlet is currently supported by the SQL Server Datawarehouse service on Azure SQL Database.</span></span>

## <span data-ttu-id="9eb88-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9eb88-108">EXAMPLES</span></span>

### <span data-ttu-id="9eb88-109">Beispiel 1: entfernt einen Wiederherstellungspunkt</span><span class="sxs-lookup"><span data-stu-id="9eb88-109">Example 1: Removes a restore point</span></span>
```
PS C:\>$RestorePointCreationDate = Get-Date "3/11/2017 1:50:00 AM"
PS C:\>Remove-AzSqlDatabaseRestorePoint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RestorePointCreationDate $RestorePointCreationDate
```

<span data-ttu-id="9eb88-110">Dieser Befehl entfernt einen Wiederherstellungspunkt für die Azure SQL-Datenbank, wobei das Erstellungsdatum angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="9eb88-110">This command removes a restore point for Azure SQL Database given creation date.</span></span>

## <span data-ttu-id="9eb88-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="9eb88-111">PARAMETERS</span></span>

### <span data-ttu-id="9eb88-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9eb88-112">-DatabaseName</span></span>
<span data-ttu-id="9eb88-113">Gibt den Namen der SQL-Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="9eb88-113">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="9eb88-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9eb88-114">-DefaultProfile</span></span>
<span data-ttu-id="9eb88-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="9eb88-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9eb88-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9eb88-116">-PassThru</span></span>
<span data-ttu-id="9eb88-117">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="9eb88-117">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9eb88-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9eb88-118">-ResourceGroupName</span></span>
<span data-ttu-id="9eb88-119">Gibt den Namen der Ressourcengruppe an, der die SQL-Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="9eb88-119">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="9eb88-120">-RestorePointCreationDate</span><span class="sxs-lookup"><span data-stu-id="9eb88-120">-RestorePointCreationDate</span></span>
<span data-ttu-id="9eb88-121">Gibt das Erstellungsdatum des Wiederherstellungspunkts an.</span><span class="sxs-lookup"><span data-stu-id="9eb88-121">Specifies the restore point creation date.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9eb88-122">-Servername</span><span class="sxs-lookup"><span data-stu-id="9eb88-122">-ServerName</span></span>
<span data-ttu-id="9eb88-123">Gibt den Namen des AzureSQL-Servers an, der die Datenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="9eb88-123">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="9eb88-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9eb88-124">-Confirm</span></span>
<span data-ttu-id="9eb88-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9eb88-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9eb88-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9eb88-126">-WhatIf</span></span>
<span data-ttu-id="9eb88-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9eb88-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9eb88-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9eb88-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9eb88-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9eb88-129">CommonParameters</span></span>
<span data-ttu-id="9eb88-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9eb88-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9eb88-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9eb88-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9eb88-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9eb88-132">INPUTS</span></span>

### <span data-ttu-id="9eb88-133">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="9eb88-133">System.DateTime</span></span>

### <span data-ttu-id="9eb88-134">System. String</span><span class="sxs-lookup"><span data-stu-id="9eb88-134">System.String</span></span>

## <span data-ttu-id="9eb88-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9eb88-135">OUTPUTS</span></span>

### <span data-ttu-id="9eb88-136">Microsoft. Azure. Commands. SQL. Backup. Model. AzureSqlDatabaseRestorePointModel</span><span class="sxs-lookup"><span data-stu-id="9eb88-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span></span>

## <span data-ttu-id="9eb88-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="9eb88-137">NOTES</span></span>

## <span data-ttu-id="9eb88-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9eb88-138">RELATED LINKS</span></span>
