---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 283a7963d7dcf278f203385bd790bd19cadc9d7c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176842"
---
# <span data-ttu-id="5e216-101">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5e216-101">Remove-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="5e216-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5e216-102">SYNOPSIS</span></span>
<span data-ttu-id="5e216-103">Entfernt eine Azure SQL-Daten Bank Failover-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="5e216-103">Removes an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="5e216-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5e216-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5e216-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5e216-105">DESCRIPTION</span></span>
<span data-ttu-id="5e216-106">Mit diesem Befehl wird die Gruppe Failover mit dem angegebenen Namen entfernt, sodass alle Datenbanken und Replikationsbeziehungen intakt bleiben.</span><span class="sxs-lookup"><span data-stu-id="5e216-106">This command removes the Failover Group with the specified name, leaving all databases and replication relationships intact.</span></span> <span data-ttu-id="5e216-107">Der Listener-Endpunkt wird aus DNS aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="5e216-107">The listener endpoint will be unregistered from DNS.</span></span>
<span data-ttu-id="5e216-108">Der primäre Server der failovergruppe sollte verwendet werden, um den Befehl auszuführen.</span><span class="sxs-lookup"><span data-stu-id="5e216-108">The Failover Group's primary server should be used to execute the command.</span></span>

## <span data-ttu-id="5e216-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5e216-109">EXAMPLES</span></span>

### <span data-ttu-id="5e216-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5e216-110">Example 1</span></span>
```
PS C:\> Remove-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="5e216-111">Entfernen Sie eine Failover-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="5e216-111">Remove a Failover Group.</span></span>

## <span data-ttu-id="5e216-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="5e216-112">PARAMETERS</span></span>

### <span data-ttu-id="5e216-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e216-113">-DefaultProfile</span></span>
<span data-ttu-id="5e216-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="5e216-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5e216-115">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="5e216-115">-FailoverGroupName</span></span>
<span data-ttu-id="5e216-116">Der Name der zu entfernenden Azure SQL-Daten Bank Failover-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="5e216-116">The name of the Azure SQL Database Failover Group to remove.</span></span>

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

### <span data-ttu-id="5e216-117">-Force</span><span class="sxs-lookup"><span data-stu-id="5e216-117">-Force</span></span>
<span data-ttu-id="5e216-118">Bestätigungsmeldung zum Durchführen der Aktion überspringen.</span><span class="sxs-lookup"><span data-stu-id="5e216-118">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="5e216-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e216-119">-ResourceGroupName</span></span>
<span data-ttu-id="5e216-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5e216-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="5e216-121">-Servername</span><span class="sxs-lookup"><span data-stu-id="5e216-121">-ServerName</span></span>
<span data-ttu-id="5e216-122">Der Name des primären Azure SQL-Datenbankservers der Gruppe "Failover".</span><span class="sxs-lookup"><span data-stu-id="5e216-122">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="5e216-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5e216-123">-Confirm</span></span>
<span data-ttu-id="5e216-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5e216-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e216-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e216-125">-WhatIf</span></span>
<span data-ttu-id="5e216-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5e216-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e216-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5e216-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e216-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e216-128">CommonParameters</span></span>
<span data-ttu-id="5e216-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e216-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e216-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5e216-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e216-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5e216-131">INPUTS</span></span>

### <span data-ttu-id="5e216-132">System. String</span><span class="sxs-lookup"><span data-stu-id="5e216-132">System.String</span></span>

## <span data-ttu-id="5e216-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5e216-133">OUTPUTS</span></span>

### <span data-ttu-id="5e216-134">Microsoft. Azure. Commands. SQL. failovergroup. Model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="5e216-134">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="5e216-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="5e216-135">NOTES</span></span>

## <span data-ttu-id="5e216-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5e216-136">RELATED LINKS</span></span>

[<span data-ttu-id="5e216-137">Neu – AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5e216-137">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="5e216-138">Satz-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5e216-138">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="5e216-139">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5e216-139">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="5e216-140">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5e216-140">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="5e216-141">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5e216-141">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="5e216-142">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5e216-142">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="5e216-143">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="5e216-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
