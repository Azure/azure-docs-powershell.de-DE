---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/invoke-azsqldatabasefailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlDatabaseFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlDatabaseFailover.md
ms.openlocfilehash: 5832b263f87ee0122dbc49c6dc765e7e54287311
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93826032"
---
# <span data-ttu-id="1584a-101">Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="1584a-101">Invoke-AzSqlDatabaseFailover</span></span>

## <span data-ttu-id="1584a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1584a-102">SYNOPSIS</span></span>
<span data-ttu-id="1584a-103">Failover einer Datenbank.</span><span class="sxs-lookup"><span data-stu-id="1584a-103">Failovers a database.</span></span>

## <span data-ttu-id="1584a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1584a-104">SYNTAX</span></span>

```
Invoke-AzSqlDatabaseFailover [-DatabaseName] <String> [-AsJob] [-PassThru] [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1584a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1584a-105">DESCRIPTION</span></span>
<span data-ttu-id="1584a-106">Das Invoke-AzSqlDatabaseFailover-Cmdlet Failover eine Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="1584a-106">The Invoke-AzSqlDatabaseFailover cmdlet failovers an Azure SQL database.</span></span> <span data-ttu-id="1584a-107">Wenn sich die Datenbank in einem elastischen Pool befindet, wird durch diesen Befehl ein Failover der angegebenen Datenbank durchgesetzt, ohne dass sich dies auf die anderen Datenbanken im gleichen elastischen Pool auswirkt.</span><span class="sxs-lookup"><span data-stu-id="1584a-107">If the database is in an elastic pool, this command will failover the given database without affecting the other databases in the same elastic pool.</span></span>

## <span data-ttu-id="1584a-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1584a-108">EXAMPLES</span></span>

### <span data-ttu-id="1584a-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1584a-109">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlDatabaseFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="1584a-110">Mit diesem Befehl wird die Datenbank mit dem Namen "database01" auf dem Server mit dem Namen "Server01" Failover</span><span class="sxs-lookup"><span data-stu-id="1584a-110">This command will failover the database named "Database01" on the server named "Server01"</span></span>

## <span data-ttu-id="1584a-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="1584a-111">PARAMETERS</span></span>

### <span data-ttu-id="1584a-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1584a-112">-AsJob</span></span>
<span data-ttu-id="1584a-113">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="1584a-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1584a-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1584a-114">-DatabaseName</span></span>
<span data-ttu-id="1584a-115">Der Name der Azure SQL-Datenbank für Failover.</span><span class="sxs-lookup"><span data-stu-id="1584a-115">The name of the Azure SQL Database to failover.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1584a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1584a-116">-DefaultProfile</span></span>
<span data-ttu-id="1584a-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1584a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1584a-118">-Force</span><span class="sxs-lookup"><span data-stu-id="1584a-118">-Force</span></span>
<span data-ttu-id="1584a-119">Bestätigungsmeldung zum Durchführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="1584a-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="1584a-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1584a-120">-PassThru</span></span>
<span data-ttu-id="1584a-121">Gibt bei erfolgreicher Ausführung true zurück.</span><span class="sxs-lookup"><span data-stu-id="1584a-121">On Successful execution, returns true.</span></span>  <span data-ttu-id="1584a-122">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="1584a-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1584a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1584a-123">-ResourceGroupName</span></span>
<span data-ttu-id="1584a-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1584a-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="1584a-125">-Servername</span><span class="sxs-lookup"><span data-stu-id="1584a-125">-ServerName</span></span>
<span data-ttu-id="1584a-126">Der Name des Azure SQL-Datenbankservers, in dem sich die Datenbank befindet.</span><span class="sxs-lookup"><span data-stu-id="1584a-126">The name of the Azure SQL Database Server the database is in.</span></span>

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

### <span data-ttu-id="1584a-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1584a-127">-Confirm</span></span>
<span data-ttu-id="1584a-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1584a-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1584a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1584a-129">-WhatIf</span></span>
<span data-ttu-id="1584a-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1584a-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1584a-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1584a-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1584a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1584a-132">CommonParameters</span></span>
<span data-ttu-id="1584a-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1584a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1584a-134">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1584a-134">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1584a-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1584a-135">INPUTS</span></span>

### <span data-ttu-id="1584a-136">System. String</span><span class="sxs-lookup"><span data-stu-id="1584a-136">System.String</span></span>

## <span data-ttu-id="1584a-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1584a-137">OUTPUTS</span></span>

## <span data-ttu-id="1584a-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="1584a-138">NOTES</span></span>

## <span data-ttu-id="1584a-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1584a-139">RELATED LINKS</span></span>

[<span data-ttu-id="1584a-140">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1584a-140">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="1584a-141">Invoke-AzSqlElasticPoolFailover</span><span class="sxs-lookup"><span data-stu-id="1584a-141">Invoke-AzSqlElasticPoolFailover</span></span>](./Invoke-AzSqlElasticPoolFailover.md)

[<span data-ttu-id="1584a-142">Neu – AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1584a-142">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="1584a-143">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1584a-143">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="1584a-144">Lebenslauf-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1584a-144">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="1584a-145">Satz-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1584a-145">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="1584a-146">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1584a-146">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="1584a-147">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="1584a-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
