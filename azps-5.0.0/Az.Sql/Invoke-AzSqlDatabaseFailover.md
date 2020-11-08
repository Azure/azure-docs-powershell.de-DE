---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/invoke-azsqldatabasefailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlDatabaseFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlDatabaseFailover.md
ms.openlocfilehash: e5cd2c2e6e903afd5afeafe2ca5fcdc70551e582
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175867"
---
# <span data-ttu-id="c80df-101">Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="c80df-101">Invoke-AzSqlDatabaseFailover</span></span>

## <span data-ttu-id="c80df-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c80df-102">SYNOPSIS</span></span>
<span data-ttu-id="c80df-103">Failover einer Datenbank.</span><span class="sxs-lookup"><span data-stu-id="c80df-103">Failovers a database.</span></span>

## <span data-ttu-id="c80df-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c80df-104">SYNTAX</span></span>

```
Invoke-AzSqlDatabaseFailover [-DatabaseName] <String> [-ReadableSecondary] [-AsJob] [-PassThru] [-Force]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c80df-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c80df-105">DESCRIPTION</span></span>
<span data-ttu-id="c80df-106">Das Invoke-AzSqlDatabaseFailover-Cmdlet Failover eine Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="c80df-106">The Invoke-AzSqlDatabaseFailover cmdlet failovers an Azure SQL database.</span></span> <span data-ttu-id="c80df-107">Wenn sich die Datenbank in einem elastischen Pool befindet, wird durch diesen Befehl ein Failover der angegebenen Datenbank durchgesetzt, ohne dass sich dies auf die anderen Datenbanken im gleichen elastischen Pool auswirkt.</span><span class="sxs-lookup"><span data-stu-id="c80df-107">If the database is in an elastic pool, this command will failover the given database without affecting the other databases in the same elastic pool.</span></span>

## <span data-ttu-id="c80df-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c80df-108">EXAMPLES</span></span>

### <span data-ttu-id="c80df-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c80df-109">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlDatabaseFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="c80df-110">Mit diesem Befehl wird das primäre Replikat der Datenbank mit dem Namen "database01" auf dem Server mit dem Namen "Server01" Failover</span><span class="sxs-lookup"><span data-stu-id="c80df-110">This command will failover the primary replica of the database named "Database01" on the server named "Server01"</span></span>

### <span data-ttu-id="c80df-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c80df-111">Example 2</span></span>
```powershell
PS C:\> Invoke-AzSqlDatabaseFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -ReadableSecondary
```

<span data-ttu-id="c80df-112">Mit diesem Befehl wird das lesbare sekundäre Replikat der Datenbank mit dem Namen "database01" auf dem Server mit dem Namen "Server01" Failover</span><span class="sxs-lookup"><span data-stu-id="c80df-112">This command will failover the readable secondary replica of the database named "Database01" on the server named "Server01"</span></span>

## <span data-ttu-id="c80df-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="c80df-113">PARAMETERS</span></span>

### <span data-ttu-id="c80df-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c80df-114">-AsJob</span></span>
<span data-ttu-id="c80df-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="c80df-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c80df-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c80df-116">-DatabaseName</span></span>
<span data-ttu-id="c80df-117">Der Name der Azure SQL-Datenbank für Failover.</span><span class="sxs-lookup"><span data-stu-id="c80df-117">The name of the Azure SQL Database to failover.</span></span>

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

### <span data-ttu-id="c80df-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c80df-118">-DefaultProfile</span></span>
<span data-ttu-id="c80df-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c80df-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c80df-120">-Force</span><span class="sxs-lookup"><span data-stu-id="c80df-120">-Force</span></span>
<span data-ttu-id="c80df-121">Bestätigungsmeldung zum Durchführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="c80df-121">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="c80df-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c80df-122">-PassThru</span></span>
<span data-ttu-id="c80df-123">Gibt bei erfolgreicher Ausführung true zurück.</span><span class="sxs-lookup"><span data-stu-id="c80df-123">On Successful execution, returns true.</span></span>  <span data-ttu-id="c80df-124">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="c80df-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c80df-125">-ReadableSecondary</span><span class="sxs-lookup"><span data-stu-id="c80df-125">-ReadableSecondary</span></span>
<span data-ttu-id="c80df-126">Failover des lesbaren sekundären Replikats anstelle des standardmäßigen primären Replikats</span><span class="sxs-lookup"><span data-stu-id="c80df-126">Failover the readable secondary replica instead of the default primary replica</span></span>

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

### <span data-ttu-id="c80df-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c80df-127">-ResourceGroupName</span></span>
<span data-ttu-id="c80df-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c80df-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="c80df-129">-Servername</span><span class="sxs-lookup"><span data-stu-id="c80df-129">-ServerName</span></span>
<span data-ttu-id="c80df-130">Der Name des Azure SQL-Datenbankservers, in dem sich die Datenbank befindet.</span><span class="sxs-lookup"><span data-stu-id="c80df-130">The name of the Azure SQL Database Server the database is in.</span></span>

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

### <span data-ttu-id="c80df-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c80df-131">-Confirm</span></span>
<span data-ttu-id="c80df-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c80df-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c80df-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c80df-133">-WhatIf</span></span>
<span data-ttu-id="c80df-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c80df-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c80df-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c80df-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c80df-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c80df-136">CommonParameters</span></span>
<span data-ttu-id="c80df-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c80df-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c80df-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c80df-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c80df-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c80df-139">INPUTS</span></span>

### <span data-ttu-id="c80df-140">System. String</span><span class="sxs-lookup"><span data-stu-id="c80df-140">System.String</span></span>

## <span data-ttu-id="c80df-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c80df-141">OUTPUTS</span></span>

## <span data-ttu-id="c80df-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="c80df-142">NOTES</span></span>

## <span data-ttu-id="c80df-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c80df-143">RELATED LINKS</span></span>

[<span data-ttu-id="c80df-144">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c80df-144">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="c80df-145">Invoke-AzSqlElasticPoolFailover</span><span class="sxs-lookup"><span data-stu-id="c80df-145">Invoke-AzSqlElasticPoolFailover</span></span>](./Invoke-AzSqlElasticPoolFailover.md)

[<span data-ttu-id="c80df-146">Neu – AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c80df-146">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="c80df-147">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c80df-147">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="c80df-148">Lebenslauf-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c80df-148">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="c80df-149">Satz-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c80df-149">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="c80df-150">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c80df-150">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="c80df-151">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="c80df-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
