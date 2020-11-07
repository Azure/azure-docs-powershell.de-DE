---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 54E01B3B-FFA5-4E3C-BA5A-A281FF5C9F8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSecondary.md
ms.openlocfilehash: 6e77f70c92d9075671a0011e54c4cc4fc5df764c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659062"
---
# <span data-ttu-id="ba625-101">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="ba625-101">Remove-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="ba625-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ba625-102">SYNOPSIS</span></span>
<span data-ttu-id="ba625-103">Beendet die Datenreplikation zwischen einer SQL-Datenbank und der angegebenen sekundären Datenbank.</span><span class="sxs-lookup"><span data-stu-id="ba625-103">Terminates data replication between a SQL Database and the specified secondary database.</span></span>

## <span data-ttu-id="ba625-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba625-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba625-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ba625-105">DESCRIPTION</span></span>
<span data-ttu-id="ba625-106">Das Cmdlet **Remove-AzSqlDatabaseSecondary** erzwingt die Beendigung eines Geo-Replikationslinks.</span><span class="sxs-lookup"><span data-stu-id="ba625-106">The **Remove-AzSqlDatabaseSecondary** cmdlet forces termination of a geo-replication link.</span></span>
<span data-ttu-id="ba625-107">Dieses Cmdlet ersetzt das Stop-AzSqlDatabaseCopy-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba625-107">This cmdlet replaces the Stop-AzSqlDatabaseCopy cmdlet.</span></span>
<span data-ttu-id="ba625-108">Vor dem Beenden erfolgt keine Replikationssynchronisierung.</span><span class="sxs-lookup"><span data-stu-id="ba625-108">There is no replication synchronization before termination.</span></span>

## <span data-ttu-id="ba625-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ba625-109">EXAMPLES</span></span>

## <span data-ttu-id="ba625-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ba625-110">PARAMETERS</span></span>

### <span data-ttu-id="ba625-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ba625-111">-DatabaseName</span></span>
<span data-ttu-id="ba625-112">Gibt den Namen der primären Azure SQL-Datenbank mit dem Replikations Link an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="ba625-112">Specifies the name of the primary Azure SQL Database that has the replication link that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ba625-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba625-113">-DefaultProfile</span></span>
<span data-ttu-id="ba625-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="ba625-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ba625-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba625-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="ba625-116">Gibt den Namen der Partner Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="ba625-116">Specifies the name of the partner  resource group.</span></span>

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

### <span data-ttu-id="ba625-117">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="ba625-117">-PartnerServerName</span></span>
<span data-ttu-id="ba625-118">Gibt den Namen des SQL Server-Partners an.</span><span class="sxs-lookup"><span data-stu-id="ba625-118">Specifies the name of the partner SQL Server.</span></span>

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

### <span data-ttu-id="ba625-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba625-119">-ResourceGroupName</span></span>
<span data-ttu-id="ba625-120">Gibt den Namen der Ressourcengruppe an, die dem zu entfernenden Replikations Link zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="ba625-120">Specifies the name of the resource group that is associated with the replication link to remove.</span></span>

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

### <span data-ttu-id="ba625-121">-Servername</span><span class="sxs-lookup"><span data-stu-id="ba625-121">-ServerName</span></span>
<span data-ttu-id="ba625-122">Gibt den Namen des SQL-Servers an, der den zu entfernenden Replikations Link enthält.</span><span class="sxs-lookup"><span data-stu-id="ba625-122">Specifies the name of the SQL Server that has the replication link to remove.</span></span>

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

### <span data-ttu-id="ba625-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ba625-123">-Confirm</span></span>
<span data-ttu-id="ba625-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ba625-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba625-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba625-125">-WhatIf</span></span>
<span data-ttu-id="ba625-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ba625-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba625-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ba625-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba625-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba625-128">CommonParameters</span></span>
<span data-ttu-id="ba625-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba625-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba625-130">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ba625-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba625-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ba625-131">INPUTS</span></span>

### <span data-ttu-id="ba625-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ba625-132">System.String</span></span>

## <span data-ttu-id="ba625-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ba625-133">OUTPUTS</span></span>

### <span data-ttu-id="ba625-134">Microsoft. Azure. Commands. SQL. Replication. Model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="ba625-134">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="ba625-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="ba625-135">NOTES</span></span>

## <span data-ttu-id="ba625-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ba625-136">RELATED LINKS</span></span>

[<span data-ttu-id="ba625-137">Neu – AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="ba625-137">New-AzSqlDatabaseSecondary</span></span>](./New-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="ba625-138">Satz-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="ba625-138">Set-AzSqlDatabaseSecondary</span></span>](./Set-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="ba625-139">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="ba625-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
