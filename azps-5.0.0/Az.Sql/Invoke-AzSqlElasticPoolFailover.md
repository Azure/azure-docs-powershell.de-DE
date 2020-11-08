---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/invoke-azsqlelasticpoolfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlElasticPoolFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlElasticPoolFailover.md
ms.openlocfilehash: 631a8edcc3709e80b36a3ff8661b7ea6027b9f78
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175866"
---
# <span data-ttu-id="49cd8-101">Invoke-AzSqlElasticPoolFailover</span><span class="sxs-lookup"><span data-stu-id="49cd8-101">Invoke-AzSqlElasticPoolFailover</span></span>

## <span data-ttu-id="49cd8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="49cd8-102">SYNOPSIS</span></span>
<span data-ttu-id="49cd8-103">Failover eines elastischen Pools.</span><span class="sxs-lookup"><span data-stu-id="49cd8-103">Failovers an elastic pool.</span></span>

## <span data-ttu-id="49cd8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="49cd8-104">SYNTAX</span></span>

```
Invoke-AzSqlElasticPoolFailover [-ElasticPoolName] <String> [-AsJob] [-PassThru] [-Force]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49cd8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="49cd8-105">DESCRIPTION</span></span>
<span data-ttu-id="49cd8-106">Das Invoke-AzSqlElasticPoolFailover-Cmdlet Failover einen elastischen Pool.</span><span class="sxs-lookup"><span data-stu-id="49cd8-106">The Invoke-AzSqlElasticPoolFailover cmdlet failovers an elastic pool.</span></span> <span data-ttu-id="49cd8-107">Nach dem Ausführen dieses Cmdlets tritt ein Failover für alle Datenbanken im elastischen Pool auf.</span><span class="sxs-lookup"><span data-stu-id="49cd8-107">Failover will occur on all databases in the elastic pool after running this cmdlet.</span></span>

## <span data-ttu-id="49cd8-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="49cd8-108">EXAMPLES</span></span>

### <span data-ttu-id="49cd8-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="49cd8-109">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlElasticPoolFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="49cd8-110">Mit diesem Befehl wird der elastische Pool mit dem Namen "ElasticPool01" auf dem Server mit dem Namen "Server01" Failover.</span><span class="sxs-lookup"><span data-stu-id="49cd8-110">This command will failover the elastic pool named "ElasticPool01" on the server named "Server01".</span></span>  <span data-ttu-id="49cd8-111">Dies bedeutet, dass ein Failover für alle Datenbanken im Elastic-Pool mit dem Namen "ElasticPool01" ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="49cd8-111">This means failover will occur on all databases in the elastic pool named "ElasticPool01".</span></span>

## <span data-ttu-id="49cd8-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="49cd8-112">PARAMETERS</span></span>

### <span data-ttu-id="49cd8-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="49cd8-113">-AsJob</span></span>
<span data-ttu-id="49cd8-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="49cd8-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="49cd8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49cd8-115">-DefaultProfile</span></span>
<span data-ttu-id="49cd8-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="49cd8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49cd8-117">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="49cd8-117">-ElasticPoolName</span></span>
<span data-ttu-id="49cd8-118">Der Name des zu entfernenden Azure SQL-Pools.</span><span class="sxs-lookup"><span data-stu-id="49cd8-118">The name of the Azure SQL Elastic Pool to remove.</span></span>

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

### <span data-ttu-id="49cd8-119">-Force</span><span class="sxs-lookup"><span data-stu-id="49cd8-119">-Force</span></span>
<span data-ttu-id="49cd8-120">Bestätigungsmeldung zum Durchführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="49cd8-120">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="49cd8-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="49cd8-121">-PassThru</span></span>
<span data-ttu-id="49cd8-122">Gibt bei erfolgreicher Ausführung true zurück.</span><span class="sxs-lookup"><span data-stu-id="49cd8-122">On Successful execution, returns true.</span></span>  <span data-ttu-id="49cd8-123">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="49cd8-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="49cd8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49cd8-124">-ResourceGroupName</span></span>
<span data-ttu-id="49cd8-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="49cd8-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="49cd8-126">-Servername</span><span class="sxs-lookup"><span data-stu-id="49cd8-126">-ServerName</span></span>
<span data-ttu-id="49cd8-127">Der Name des Azure SQL Server, in dem sich der elastische Pool befindet.</span><span class="sxs-lookup"><span data-stu-id="49cd8-127">The name of the Azure SQL Server the Elastic Pool is in.</span></span>

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

### <span data-ttu-id="49cd8-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="49cd8-128">-Confirm</span></span>
<span data-ttu-id="49cd8-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="49cd8-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49cd8-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49cd8-130">-WhatIf</span></span>
<span data-ttu-id="49cd8-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="49cd8-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="49cd8-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="49cd8-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49cd8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49cd8-133">CommonParameters</span></span>
<span data-ttu-id="49cd8-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49cd8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49cd8-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="49cd8-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49cd8-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="49cd8-136">INPUTS</span></span>

### <span data-ttu-id="49cd8-137">System. String</span><span class="sxs-lookup"><span data-stu-id="49cd8-137">System.String</span></span>

## <span data-ttu-id="49cd8-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="49cd8-138">OUTPUTS</span></span>

## <span data-ttu-id="49cd8-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="49cd8-139">NOTES</span></span>

## <span data-ttu-id="49cd8-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="49cd8-140">RELATED LINKS</span></span>

[<span data-ttu-id="49cd8-141">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="49cd8-141">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="49cd8-142">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="49cd8-142">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="49cd8-143">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="49cd8-143">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="49cd8-144">Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="49cd8-144">Invoke-AzSqlDatabaseFailover</span></span>](./Invoke-AzSqlDatabaseFailover.md)

[<span data-ttu-id="49cd8-145">Neu – AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="49cd8-145">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="49cd8-146">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="49cd8-146">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="49cd8-147">Satz-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="49cd8-147">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="49cd8-148">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="49cd8-148">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)