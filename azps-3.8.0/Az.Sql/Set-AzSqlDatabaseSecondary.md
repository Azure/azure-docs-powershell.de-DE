---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F9703508-DD4D-4D25-A7CA-7E3432B5DCA9
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSecondary.md
ms.openlocfilehash: 9e0af4c5110fe0732782293eb9d8c67fb7d89600
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846611"
---
# <span data-ttu-id="ad6b5-101">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="ad6b5-101">Set-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="ad6b5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ad6b5-102">SYNOPSIS</span></span>
<span data-ttu-id="ad6b5-103">Wechselt eine sekundäre Datenbank als primäre Datenbank, um ein Failover zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="ad6b5-103">Switches a secondary database to be primary in order to initiate failover.</span></span>

## <span data-ttu-id="ad6b5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad6b5-104">SYNTAX</span></span>

### <span data-ttu-id="ad6b5-105">Nooptions (Standard)</span><span class="sxs-lookup"><span data-stu-id="ad6b5-105">NoOptionsSet (Default)</span></span>
```
Set-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad6b5-106">ByFailoverParams</span><span class="sxs-lookup"><span data-stu-id="ad6b5-106">ByFailoverParams</span></span>
```
Set-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-Failover]
 [-AllowDataLoss] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad6b5-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ad6b5-107">DESCRIPTION</span></span>
<span data-ttu-id="ad6b5-108">Das Cmdlet " **Satz-AzSqlDatabaseSecondary** " wechselt eine sekundäre Datenbank als primär, um ein Failover zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="ad6b5-108">The **Set-AzSqlDatabaseSecondary** cmdlet switches a secondary database to be primary in order to initiate failover.</span></span>
<span data-ttu-id="ad6b5-109">Dieses Cmdlet wurde als allgemeiner Konfigurationsbefehl konzipiert, ist aber derzeit auf das Initiieren eines Failovers limitiert.</span><span class="sxs-lookup"><span data-stu-id="ad6b5-109">This cmdlet is designed as a general configuration command, but is currently limited to initiating failover.</span></span>
<span data-ttu-id="ad6b5-110">Geben Sie den *AllowDataLoss* -Parameter an, um bei einem Ausfall ein erzwungenes Failover zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="ad6b5-110">Specify the *AllowDataLoss* parameter to initiate a force failover during an outage.</span></span>
<span data-ttu-id="ad6b5-111">Sie müssen diesen Parameter nicht angeben, wenn Sie einen geplanten Vorgang wie beispielsweise die Wiederherstellungs Übung ausführen.</span><span class="sxs-lookup"><span data-stu-id="ad6b5-111">You do not have to specify this parameter when you perform a planned operation, such as recovery drill.</span></span>
<span data-ttu-id="ad6b5-112">In diesem Fall wird die sekundäre Datenbank mit der primären Datenbank synchronisiert, bevor Sie gewechselt wird.</span><span class="sxs-lookup"><span data-stu-id="ad6b5-112">In the latter case, the secondary database is synchronized with the primary before it is switched.</span></span>

## <span data-ttu-id="ad6b5-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ad6b5-113">EXAMPLES</span></span>

### <span data-ttu-id="ad6b5-114">1: Initiieren eines geplanten Failovers</span><span class="sxs-lookup"><span data-stu-id="ad6b5-114">1: Initiate a planned failover</span></span>
```
$database = Get-AzSqlDatabase -DatabaseName $databaseName -ResourceGroupName $secondaryResourceGroupName -ServerName $secondaryServerName
$database | Set-AzSqlDatabaseSecondary -PartnerResourceGroupName $primaryResourceGroupName -Failover
```

### <span data-ttu-id="ad6b5-115">2: Initiieren eines erzwungenen Failovers (mit potenziellem Datenverlust)</span><span class="sxs-lookup"><span data-stu-id="ad6b5-115">2: Initiate a forced failover (with potential data loss)</span></span>
```
$database = Get-AzSqlDatabase -DatabaseName $databaseName -ResourceGroupName $secondaryResourceGroupName -ServerName $secondaryServerName
$database | Set-AzSqlDatabaseSecondary -PartnerResourceGroupName $primaryResourceGroupName -Failover -AllowDataLoss
```

## <span data-ttu-id="ad6b5-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="ad6b5-116">PARAMETERS</span></span>

### <span data-ttu-id="ad6b5-117">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="ad6b5-117">-AllowDataLoss</span></span>
<span data-ttu-id="ad6b5-118">Gibt an, dass dieser Failover-Vorgang Datenverlust zulässt.</span><span class="sxs-lookup"><span data-stu-id="ad6b5-118">Indicates that this failover operation permits data loss.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFailoverParams
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad6b5-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ad6b5-119">-AsJob</span></span>
<span data-ttu-id="ad6b5-120">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="ad6b5-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ad6b5-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ad6b5-121">-DatabaseName</span></span>
<span data-ttu-id="ad6b5-122">Gibt den Namen der Azure SQL-Datenbank Secondary an.</span><span class="sxs-lookup"><span data-stu-id="ad6b5-122">Specifies the name of the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="ad6b5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad6b5-123">-DefaultProfile</span></span>
<span data-ttu-id="ad6b5-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="ad6b5-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ad6b5-125">-Failover</span><span class="sxs-lookup"><span data-stu-id="ad6b5-125">-Failover</span></span>
<span data-ttu-id="ad6b5-126">Gibt an, dass es sich bei diesem Vorgang um ein Failover handelt.</span><span class="sxs-lookup"><span data-stu-id="ad6b5-126">Indicates that this operation is a failover.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFailoverParams
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad6b5-127">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad6b5-127">-PartnerResourceGroupName</span></span>
<span data-ttu-id="ad6b5-128">Gibt den Namen der Ressourcengruppe an, der die Partner Azure SQL-Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="ad6b5-128">Specifies the name of the resource group to which the partner Azure SQL Database is assigned.</span></span>

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

### <span data-ttu-id="ad6b5-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad6b5-129">-ResourceGroupName</span></span>
<span data-ttu-id="ad6b5-130">Gibt den Namen der Ressourcengruppe an, der die Azure SQL-Datenbank Secondary zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="ad6b5-130">Specifies the name of the resource group to which the Azure SQL Database Secondary is assigned.</span></span>

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

### <span data-ttu-id="ad6b5-131">-Servername</span><span class="sxs-lookup"><span data-stu-id="ad6b5-131">-ServerName</span></span>
<span data-ttu-id="ad6b5-132">Gibt den Namen des SQL-Servers an, der die Azure SQL-Datenbank Secondary hostet.</span><span class="sxs-lookup"><span data-stu-id="ad6b5-132">Specifies the name of the SQL Server that hosts the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="ad6b5-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ad6b5-133">-Confirm</span></span>
<span data-ttu-id="ad6b5-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ad6b5-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad6b5-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad6b5-135">-WhatIf</span></span>
<span data-ttu-id="ad6b5-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ad6b5-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad6b5-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ad6b5-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad6b5-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad6b5-138">CommonParameters</span></span>
<span data-ttu-id="ad6b5-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad6b5-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad6b5-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ad6b5-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad6b5-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ad6b5-141">INPUTS</span></span>

### <span data-ttu-id="ad6b5-142">System. String</span><span class="sxs-lookup"><span data-stu-id="ad6b5-142">System.String</span></span>

## <span data-ttu-id="ad6b5-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ad6b5-143">OUTPUTS</span></span>

### <span data-ttu-id="ad6b5-144">Microsoft. Azure. Commands. SQL. Replication. Model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="ad6b5-144">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="ad6b5-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="ad6b5-145">NOTES</span></span>

## <span data-ttu-id="ad6b5-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ad6b5-146">RELATED LINKS</span></span>

[<span data-ttu-id="ad6b5-147">Neu – AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="ad6b5-147">New-AzSqlDatabaseSecondary</span></span>](./New-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="ad6b5-148">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="ad6b5-148">Remove-AzSqlDatabaseSecondary</span></span>](./Remove-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="ad6b5-149">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="ad6b5-149">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
