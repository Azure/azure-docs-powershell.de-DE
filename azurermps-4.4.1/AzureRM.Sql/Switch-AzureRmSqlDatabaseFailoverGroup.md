---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Switch-AzureRmSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Switch-AzureRmSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 45be8d0ef10b040fd27a714444bb60bbf6a69951
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503150"
---
# <span data-ttu-id="8d4fd-101">Switch-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="8d4fd-101">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="8d4fd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8d4fd-102">SYNOPSIS</span></span>
<span data-ttu-id="8d4fd-103">Führt ein Failover einer Azure SQL-Datenbankfailover-Gruppe aus.</span><span class="sxs-lookup"><span data-stu-id="8d4fd-103">Executes a failover of an Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d4fd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8d4fd-104">SYNTAX</span></span>

```
Switch-AzureRmSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>] [-AllowDataLoss]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8d4fd-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8d4fd-105">DESCRIPTION</span></span>
<span data-ttu-id="8d4fd-106">Mit diesem Befehl werden die Rollen der Server in einer failovergruppe getauscht, und alle sekundären Datenbankenwerden in die primäre Rolle umgeschaltet.</span><span class="sxs-lookup"><span data-stu-id="8d4fd-106">This command swaps the roles of the servers in a Failover Group and switches all secondary databases to the primary role.</span></span> <span data-ttu-id="8d4fd-107">Alle neuen TDS-Sitzungen werden nach dem Aktualisieren des DNS-Clientcaches automatisch an den sekundären Server weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="8d4fd-107">All new TDS sessions are automatically re-routed to the secondary server after the DNS client cache is refreshed.</span></span> <span data-ttu-id="8d4fd-108">Wenn der ursprüngliche primäre Server wieder online ist, werden alle zuvor primären Datenbanken in die sekundäre Rolle gewechselt.</span><span class="sxs-lookup"><span data-stu-id="8d4fd-108">When the original primary server is back online, all formerly primary databases in it will switch to the secondary role.</span></span>

<span data-ttu-id="8d4fd-109">Zum Ausführen dieses Befehls muss der sekundäre Server der Failovercluster-Gruppe verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8d4fd-109">The Failover Group's secondary server must be used to execute this command.</span></span>

## <span data-ttu-id="8d4fd-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8d4fd-110">EXAMPLES</span></span>

### <span data-ttu-id="8d4fd-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8d4fd-111">Example 1</span></span>
```
C:\> Get-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg | Switch-AzureRmSqlDatabaseFailoverGroup -AllowDataLoss
```

<span data-ttu-id="8d4fd-112">Führen Sie einen Failover-Vorgang aus, der den Datenverlust durch Verrohrung in der Gruppe Failover ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="8d4fd-112">Issue a failover operation allowing data loss by piping in the Failover Group.</span></span>

### <span data-ttu-id="8d4fd-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="8d4fd-113">Example 2</span></span>
```
C:\> Switch-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg
```

<span data-ttu-id="8d4fd-114">Führen Sie einen bestmöglichen Failover-Vorgang aus, der entweder erfolgreich ist, ohne Daten zu verlieren oder einen Fehler zu verursachen und zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="8d4fd-114">Issue a best effort failover operation that will either succeed without losing data or fail and roll back.</span></span>

## <span data-ttu-id="8d4fd-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d4fd-115">PARAMETERS</span></span>

### <span data-ttu-id="8d4fd-116">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="8d4fd-116">-AllowDataLoss</span></span>
<span data-ttu-id="8d4fd-117">Führen Sie das Failover durch, auch wenn dies zu einem Datenverlust führen kann.</span><span class="sxs-lookup"><span data-stu-id="8d4fd-117">Complete the failover even if doing so may result in data loss.</span></span> <span data-ttu-id="8d4fd-118">Auf diese Weise kann das Failover fortgesetzt werden, selbst wenn eine primäre Datenbank nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="8d4fd-118">This will allow the failover to proceed even if a primary database is unavailable.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d4fd-119">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="8d4fd-119">-FailoverGroupName</span></span>
<span data-ttu-id="8d4fd-120">Der Name der Azure SQL-Daten Bank Failover-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="8d4fd-120">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="8d4fd-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d4fd-121">-ResourceGroupName</span></span>
<span data-ttu-id="8d4fd-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8d4fd-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="8d4fd-123">-Servername</span><span class="sxs-lookup"><span data-stu-id="8d4fd-123">-ServerName</span></span>
<span data-ttu-id="8d4fd-124">Der Name des sekundären Azure SQL-Datenbankservers der Gruppe "Failover".</span><span class="sxs-lookup"><span data-stu-id="8d4fd-124">The name of the secondary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="8d4fd-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8d4fd-125">-Confirm</span></span>
<span data-ttu-id="8d4fd-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8d4fd-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d4fd-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d4fd-127">-WhatIf</span></span>
<span data-ttu-id="8d4fd-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8d4fd-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d4fd-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8d4fd-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d4fd-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d4fd-130">-DefaultProfile</span></span>
<span data-ttu-id="8d4fd-131">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8d4fd-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d4fd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d4fd-132">CommonParameters</span></span>
<span data-ttu-id="8d4fd-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d4fd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d4fd-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d4fd-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d4fd-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8d4fd-135">INPUTS</span></span>

### <span data-ttu-id="8d4fd-136">System. String</span><span class="sxs-lookup"><span data-stu-id="8d4fd-136">System.String</span></span>

## <span data-ttu-id="8d4fd-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8d4fd-137">OUTPUTS</span></span>

### <span data-ttu-id="8d4fd-138">System. Object</span><span class="sxs-lookup"><span data-stu-id="8d4fd-138">System.Object</span></span>

## <span data-ttu-id="8d4fd-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="8d4fd-139">NOTES</span></span>

## <span data-ttu-id="8d4fd-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8d4fd-140">RELATED LINKS</span></span>

[<span data-ttu-id="8d4fd-141">Neu – AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="8d4fd-141">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="8d4fd-142">Satz-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="8d4fd-142">Set-AzureRmSqlDatabaseFailoverGroup</span></span>](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="8d4fd-143">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="8d4fd-143">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="8d4fd-144">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="8d4fd-144">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="8d4fd-145">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="8d4fd-145">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="8d4fd-146">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="8d4fd-146">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="8d4fd-147">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="8d4fd-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
