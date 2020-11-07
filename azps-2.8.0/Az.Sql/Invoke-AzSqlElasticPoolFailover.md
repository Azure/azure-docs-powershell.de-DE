---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/invoke-azsqlelasticpoolfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlElasticPoolFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlElasticPoolFailover.md
ms.openlocfilehash: c07141d8a91974d511653217885b21a50a0b87f1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825488"
---
# <span data-ttu-id="16a2d-101">Invoke-AzSqlElasticPoolFailover</span><span class="sxs-lookup"><span data-stu-id="16a2d-101">Invoke-AzSqlElasticPoolFailover</span></span>

## <span data-ttu-id="16a2d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="16a2d-102">SYNOPSIS</span></span>
<span data-ttu-id="16a2d-103">Failover eines elastischen Pools.</span><span class="sxs-lookup"><span data-stu-id="16a2d-103">Failovers an elastic pool.</span></span>

## <span data-ttu-id="16a2d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="16a2d-104">SYNTAX</span></span>

```
Invoke-AzSqlElasticPoolFailover [-ElasticPoolName] <String> [-AsJob] [-PassThru] [-Force]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16a2d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="16a2d-105">DESCRIPTION</span></span>
<span data-ttu-id="16a2d-106">Das Invoke-AzSqlElasticPoolFailover-Cmdlet Failover einen elastischen Pool.</span><span class="sxs-lookup"><span data-stu-id="16a2d-106">The Invoke-AzSqlElasticPoolFailover cmdlet failovers an elastic pool.</span></span> <span data-ttu-id="16a2d-107">Nach dem Ausführen dieses Cmdlets tritt ein Failover für alle Datenbanken im elastischen Pool auf.</span><span class="sxs-lookup"><span data-stu-id="16a2d-107">Failover will occur on all databases in the elastic pool after running this cmdlet.</span></span>

## <span data-ttu-id="16a2d-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="16a2d-108">EXAMPLES</span></span>

### <span data-ttu-id="16a2d-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="16a2d-109">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlElasticPoolFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="16a2d-110">Mit diesem Befehl wird der elastische Pool mit dem Namen "ElasticPool01" auf dem Server mit dem Namen "Server01" Failover.</span><span class="sxs-lookup"><span data-stu-id="16a2d-110">This command will failover the elastic pool named "ElasticPool01" on the server named "Server01".</span></span>  <span data-ttu-id="16a2d-111">Dies bedeutet, dass ein Failover für alle Datenbanken im Elastic-Pool mit dem Namen "ElasticPool01" ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="16a2d-111">This means failover will occur on all databases in the elastic pool named "ElasticPool01".</span></span>

## <span data-ttu-id="16a2d-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="16a2d-112">PARAMETERS</span></span>

### <span data-ttu-id="16a2d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="16a2d-113">-AsJob</span></span>
<span data-ttu-id="16a2d-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="16a2d-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="16a2d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16a2d-115">-DefaultProfile</span></span>
<span data-ttu-id="16a2d-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="16a2d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16a2d-117">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="16a2d-117">-ElasticPoolName</span></span>
<span data-ttu-id="16a2d-118">Der Name des zu entfernenden Azure SQL-Pools.</span><span class="sxs-lookup"><span data-stu-id="16a2d-118">The name of the Azure SQL Elastic Pool to remove.</span></span>

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

### <span data-ttu-id="16a2d-119">-Force</span><span class="sxs-lookup"><span data-stu-id="16a2d-119">-Force</span></span>
<span data-ttu-id="16a2d-120">Bestätigungsmeldung zum Durchführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="16a2d-120">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="16a2d-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="16a2d-121">-PassThru</span></span>
<span data-ttu-id="16a2d-122">Gibt bei erfolgreicher Ausführung true zurück.</span><span class="sxs-lookup"><span data-stu-id="16a2d-122">On Successful execution, returns true.</span></span>  <span data-ttu-id="16a2d-123">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="16a2d-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="16a2d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16a2d-124">-ResourceGroupName</span></span>
<span data-ttu-id="16a2d-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="16a2d-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="16a2d-126">-Servername</span><span class="sxs-lookup"><span data-stu-id="16a2d-126">-ServerName</span></span>
<span data-ttu-id="16a2d-127">Der Name des Azure SQL Server, in dem sich der elastische Pool befindet.</span><span class="sxs-lookup"><span data-stu-id="16a2d-127">The name of the Azure SQL Server the Elastic Pool is in.</span></span>

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

### <span data-ttu-id="16a2d-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="16a2d-128">-Confirm</span></span>
<span data-ttu-id="16a2d-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="16a2d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16a2d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16a2d-130">-WhatIf</span></span>
<span data-ttu-id="16a2d-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="16a2d-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="16a2d-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="16a2d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16a2d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16a2d-133">CommonParameters</span></span>
<span data-ttu-id="16a2d-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16a2d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16a2d-135">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="16a2d-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16a2d-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="16a2d-136">INPUTS</span></span>

### <span data-ttu-id="16a2d-137">System. String</span><span class="sxs-lookup"><span data-stu-id="16a2d-137">System.String</span></span>

## <span data-ttu-id="16a2d-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="16a2d-138">OUTPUTS</span></span>

## <span data-ttu-id="16a2d-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="16a2d-139">NOTES</span></span>

## <span data-ttu-id="16a2d-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="16a2d-140">RELATED LINKS</span></span>

[<span data-ttu-id="16a2d-141">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="16a2d-141">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="16a2d-142">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="16a2d-142">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="16a2d-143">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="16a2d-143">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="16a2d-144">Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="16a2d-144">Invoke-AzSqlDatabaseFailover</span></span>](./Invoke-AzSqlDatabaseFailover.md)

[<span data-ttu-id="16a2d-145">Neu – AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="16a2d-145">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="16a2d-146">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="16a2d-146">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="16a2d-147">Satz-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="16a2d-147">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="16a2d-148">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="16a2d-148">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)