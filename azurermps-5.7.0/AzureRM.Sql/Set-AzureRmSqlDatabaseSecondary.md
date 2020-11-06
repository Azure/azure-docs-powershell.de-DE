---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F9703508-DD4D-4D25-A7CA-7E3432B5DCA9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseSecondary.md
ms.openlocfilehash: 2c1853de6eb11c304014ac45b5469c5699105824
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480766"
---
# <span data-ttu-id="ceec7-101">Set-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="ceec7-101">Set-AzureRmSqlDatabaseSecondary</span></span>

## <span data-ttu-id="ceec7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ceec7-102">SYNOPSIS</span></span>
<span data-ttu-id="ceec7-103">Wechselt eine sekundäre Datenbank als primäre Datenbank, um ein Failover zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="ceec7-103">Switches a secondary database to be primary in order to initiate failover.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ceec7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ceec7-104">SYNTAX</span></span>

### <span data-ttu-id="ceec7-105">Nooptions (Standard)</span><span class="sxs-lookup"><span data-stu-id="ceec7-105">NoOptionsSet (Default)</span></span>
```
Set-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ceec7-106">ByFailoverParams</span><span class="sxs-lookup"><span data-stu-id="ceec7-106">ByFailoverParams</span></span>
```
Set-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-Failover]
 [-AllowDataLoss] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ceec7-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ceec7-107">DESCRIPTION</span></span>
<span data-ttu-id="ceec7-108">Das Cmdlet " **Satz-AzureRmSqlDatabaseSecondary** " wechselt eine sekundäre Datenbank als primär, um ein Failover zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="ceec7-108">The **Set-AzureRmSqlDatabaseSecondary** cmdlet switches a secondary database to be primary in order to initiate failover.</span></span>
<span data-ttu-id="ceec7-109">Dieses Cmdlet wurde als allgemeiner Konfigurationsbefehl konzipiert, ist aber derzeit auf das Initiieren eines Failovers limitiert.</span><span class="sxs-lookup"><span data-stu-id="ceec7-109">This cmdlet is designed as a general configuration command, but is currently limited to initiating failover.</span></span>
<span data-ttu-id="ceec7-110">Geben Sie den *AllowDataLoss* -Parameter an, um bei einem Ausfall ein erzwungenes Failover zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="ceec7-110">Specify the *AllowDataLoss* parameter to initiate a force failover during an outage.</span></span>
<span data-ttu-id="ceec7-111">Sie müssen diesen Parameter nicht angeben, wenn Sie einen geplanten Vorgang wie beispielsweise die Wiederherstellungs Übung ausführen.</span><span class="sxs-lookup"><span data-stu-id="ceec7-111">You do not have to specify this parameter when you perform a planned operation, such as recovery drill.</span></span>
<span data-ttu-id="ceec7-112">In diesem Fall wird die sekundäre Datenbank mit der primären Datenbank synchronisiert, bevor Sie gewechselt wird.</span><span class="sxs-lookup"><span data-stu-id="ceec7-112">In the latter case, the secondary database is synchronized with the primary before it is switched.</span></span>

## <span data-ttu-id="ceec7-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ceec7-113">EXAMPLES</span></span>

## <span data-ttu-id="ceec7-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="ceec7-114">PARAMETERS</span></span>

### <span data-ttu-id="ceec7-115">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="ceec7-115">-AllowDataLoss</span></span>
<span data-ttu-id="ceec7-116">Gibt an, dass dieser Failover-Vorgang Datenverlust zulässt.</span><span class="sxs-lookup"><span data-stu-id="ceec7-116">Indicates that this failover operation permits data loss.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByFailoverParams
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ceec7-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ceec7-117">-AsJob</span></span>
<span data-ttu-id="ceec7-118">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="ceec7-118">Run cmdlet in the background</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ceec7-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ceec7-119">-DatabaseName</span></span>
<span data-ttu-id="ceec7-120">Gibt den Namen der Azure SQL-Datenbank Secondary an.</span><span class="sxs-lookup"><span data-stu-id="ceec7-120">Specifies the name of the Azure SQL Database Secondary.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ceec7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ceec7-121">-DefaultProfile</span></span>
<span data-ttu-id="ceec7-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="ceec7-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ceec7-123">-Failover</span><span class="sxs-lookup"><span data-stu-id="ceec7-123">-Failover</span></span>
<span data-ttu-id="ceec7-124">Gibt an, dass es sich bei diesem Vorgang um ein Failover handelt.</span><span class="sxs-lookup"><span data-stu-id="ceec7-124">Indicates that this operation is a failover.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByFailoverParams
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ceec7-125">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ceec7-125">-PartnerResourceGroupName</span></span>
<span data-ttu-id="ceec7-126">Gibt den Namen der Ressourcengruppe an, der die Partner Azure SQL-Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="ceec7-126">Specifies the name of the resource group to which the partner Azure SQL Database is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ceec7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ceec7-127">-ResourceGroupName</span></span>
<span data-ttu-id="ceec7-128">Gibt den Namen der Ressourcengruppe an, der die Azure SQL-Datenbank Secondary zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="ceec7-128">Specifies the name of the resource group to which the Azure SQL Database Secondary is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ceec7-129">-Servername</span><span class="sxs-lookup"><span data-stu-id="ceec7-129">-ServerName</span></span>
<span data-ttu-id="ceec7-130">Gibt den Namen des SQL-Servers an, der die Azure SQL-Datenbank Secondary hostet.</span><span class="sxs-lookup"><span data-stu-id="ceec7-130">Specifies the name of the SQL Server that hosts the Azure SQL Database Secondary.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ceec7-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ceec7-131">-Confirm</span></span>
<span data-ttu-id="ceec7-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ceec7-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ceec7-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ceec7-133">-WhatIf</span></span>
<span data-ttu-id="ceec7-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ceec7-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ceec7-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ceec7-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ceec7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ceec7-136">CommonParameters</span></span>
<span data-ttu-id="ceec7-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ceec7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ceec7-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ceec7-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ceec7-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ceec7-139">INPUTS</span></span>

###  
<span data-ttu-id="ceec7-140">Sie können Instanzen des **Daten Bank** Objekts für die sekundäre Datenbank übergeben, um einen Failover durchführen und die primäre Datenbank zu diesem Cmdlet machen.</span><span class="sxs-lookup"><span data-stu-id="ceec7-140">You can pipe instances of the **Database** object for the secondary database to fail over and make the primary database to this cmdlet.</span></span>

## <span data-ttu-id="ceec7-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ceec7-141">OUTPUTS</span></span>

###  
<span data-ttu-id="ceec7-142">Dieses Cmdlet gibt einen **ReplicationLink** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ceec7-142">This cmdlet returns a **ReplicationLink**.</span></span>

## <span data-ttu-id="ceec7-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="ceec7-143">NOTES</span></span>

## <span data-ttu-id="ceec7-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ceec7-144">RELATED LINKS</span></span>

[<span data-ttu-id="ceec7-145">Neu – AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="ceec7-145">New-AzureRmSqlDatabaseSecondary</span></span>](./New-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="ceec7-146">Remove-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="ceec7-146">Remove-AzureRmSqlDatabaseSecondary</span></span>](./Remove-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="ceec7-147">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="ceec7-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
