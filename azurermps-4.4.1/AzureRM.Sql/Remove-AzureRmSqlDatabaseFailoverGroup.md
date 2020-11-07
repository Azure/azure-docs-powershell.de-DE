---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 40a193e96bdfa3c209a15e4a7be801e6ce71a3a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665258"
---
# <span data-ttu-id="a84db-101">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a84db-101">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="a84db-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a84db-102">SYNOPSIS</span></span>
<span data-ttu-id="a84db-103">Entfernt eine Azure SQL-Daten Bank Failover-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="a84db-103">Removes an Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a84db-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a84db-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a84db-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a84db-105">DESCRIPTION</span></span>
<span data-ttu-id="a84db-106">Mit diesem Befehl wird die Gruppe Failover mit dem angegebenen Namen entfernt, sodass alle Datenbanken und Replikationsbeziehungen intakt bleiben.</span><span class="sxs-lookup"><span data-stu-id="a84db-106">This command removes the Failover Group with the specified name, leaving all databases and replication relationships intact.</span></span> <span data-ttu-id="a84db-107">Der Listener-Endpunkt wird aus DNS aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="a84db-107">The listener endpoint will be unregistered from DNS.</span></span>

<span data-ttu-id="a84db-108">Der primäre Server der failovergruppe sollte verwendet werden, um den Befehl auszuführen.</span><span class="sxs-lookup"><span data-stu-id="a84db-108">The Failover Group's primary server should be used to execute the command.</span></span>

## <span data-ttu-id="a84db-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a84db-109">EXAMPLES</span></span>

### <span data-ttu-id="a84db-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a84db-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="a84db-111">Entfernen Sie eine Failover-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="a84db-111">Remove a Failover Group.</span></span>

## <span data-ttu-id="a84db-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a84db-112">PARAMETERS</span></span>

### <span data-ttu-id="a84db-113">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="a84db-113">-FailoverGroupName</span></span>
<span data-ttu-id="a84db-114">Der Name der zu entfernenden Azure SQL-Daten Bank Failover-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="a84db-114">The name of the Azure SQL Database Failover Group to remove.</span></span>

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

### <span data-ttu-id="a84db-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a84db-115">-Force</span></span>
<span data-ttu-id="a84db-116">Bestätigungsmeldung zum Durchführen der Aktion überspringen.</span><span class="sxs-lookup"><span data-stu-id="a84db-116">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="a84db-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a84db-117">-ResourceGroupName</span></span>
<span data-ttu-id="a84db-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a84db-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="a84db-119">-Servername</span><span class="sxs-lookup"><span data-stu-id="a84db-119">-ServerName</span></span>
<span data-ttu-id="a84db-120">Der Name des primären Azure SQL-Datenbankservers der Gruppe "Failover".</span><span class="sxs-lookup"><span data-stu-id="a84db-120">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="a84db-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a84db-121">-Confirm</span></span>
<span data-ttu-id="a84db-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a84db-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a84db-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a84db-123">-WhatIf</span></span>
<span data-ttu-id="a84db-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a84db-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a84db-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a84db-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a84db-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a84db-126">-DefaultProfile</span></span>
<span data-ttu-id="a84db-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a84db-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a84db-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a84db-128">CommonParameters</span></span>
<span data-ttu-id="a84db-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a84db-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a84db-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a84db-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a84db-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a84db-131">INPUTS</span></span>

### <span data-ttu-id="a84db-132">System. String</span><span class="sxs-lookup"><span data-stu-id="a84db-132">System.String</span></span>

## <span data-ttu-id="a84db-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a84db-133">OUTPUTS</span></span>

### <span data-ttu-id="a84db-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="a84db-134">System.Object</span></span>

## <span data-ttu-id="a84db-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="a84db-135">NOTES</span></span>

## <span data-ttu-id="a84db-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a84db-136">RELATED LINKS</span></span>

[<span data-ttu-id="a84db-137">Neu – AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a84db-137">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="a84db-138">Satz-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a84db-138">Set-AzureRmSqlDatabaseFailoverGroup</span></span>](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="a84db-139">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a84db-139">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="a84db-140">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a84db-140">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="a84db-141">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a84db-141">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="a84db-142">Switch-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a84db-142">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="a84db-143">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="a84db-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
