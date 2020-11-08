---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 40054224-52FF-4AF6-A090-9F6D07A2BA99
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasereplicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseReplicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseReplicationLink.md
ms.openlocfilehash: 2bf632e0135031a9bc2454ac200cbe7aa40bef3c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996239"
---
# <span data-ttu-id="63d76-101">Get-AzSqlDatabaseReplicationLink</span><span class="sxs-lookup"><span data-stu-id="63d76-101">Get-AzSqlDatabaseReplicationLink</span></span>

## <span data-ttu-id="63d76-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="63d76-102">SYNOPSIS</span></span>
<span data-ttu-id="63d76-103">Ruft die Geo-Replikationsverknüpfungen zwischen einer Azure SQL-Datenbank und einer Ressourcengruppe oder SQL Server ab.</span><span class="sxs-lookup"><span data-stu-id="63d76-103">Gets the geo-replication links between an Azure SQL Database and a resource group or SQL Server.</span></span>

## <span data-ttu-id="63d76-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="63d76-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseReplicationLink [-DatabaseName] <String> -PartnerResourceGroupName <String>
 [-PartnerServerName <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63d76-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="63d76-105">DESCRIPTION</span></span>
<span data-ttu-id="63d76-106">Das Cmdlet **Get-AzSqlDatabaseReplicationLink** ersetzt das Cmdlet **Get-AzSqlDatabaseCopy** .</span><span class="sxs-lookup"><span data-stu-id="63d76-106">The **Get-AzSqlDatabaseReplicationLink** cmdlet replaces the **Get-AzSqlDatabaseCopy** cmdlet.</span></span>
<span data-ttu-id="63d76-107">Es werden alle Geo-Replikationsverknüpfungen zwischen der angegebenen Azure SQL-Datenbank und einer Ressourcengruppe oder einem AzureSQL-Server abgerufen.</span><span class="sxs-lookup"><span data-stu-id="63d76-107">It gets all geo-replication links between the specified Azure SQL Database and a resource group or AzureSQL Server.</span></span>

## <span data-ttu-id="63d76-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="63d76-108">EXAMPLES</span></span>

## <span data-ttu-id="63d76-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="63d76-109">PARAMETERS</span></span>

### <span data-ttu-id="63d76-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="63d76-110">-DatabaseName</span></span>
<span data-ttu-id="63d76-111">Gibt den Namen der SQL-Datenbank an, für die Links abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="63d76-111">Specifies the name of the SQL Database for which to retrieve links.</span></span>

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

### <span data-ttu-id="63d76-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63d76-112">-DefaultProfile</span></span>
<span data-ttu-id="63d76-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="63d76-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="63d76-114">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63d76-114">-PartnerResourceGroupName</span></span>
<span data-ttu-id="63d76-115">Gibt den Namen der Ressourcengruppe an, der der Partner zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="63d76-115">Specifies the name of the resource group to which the partner is assigned.</span></span>

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

### <span data-ttu-id="63d76-116">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="63d76-116">-PartnerServerName</span></span>
<span data-ttu-id="63d76-117">Gibt den Namen des Azure SQL Server für den Partner an.</span><span class="sxs-lookup"><span data-stu-id="63d76-117">Specifies the name of the Azure SQL Server for the partner.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63d76-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63d76-118">-ResourceGroupName</span></span>
<span data-ttu-id="63d76-119">Gibt den Namen der Azure-Ressourcengruppe für die Datenbank an, für die Verknüpfungen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="63d76-119">Specifies the name of the Azure resource group for the database for which to retrieve links.</span></span>

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

### <span data-ttu-id="63d76-120">-Servername</span><span class="sxs-lookup"><span data-stu-id="63d76-120">-ServerName</span></span>
<span data-ttu-id="63d76-121">Gibt den Namen des SQL Server für die Datenbank an, für den Links abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="63d76-121">Specifies the name of the SQL Server for the database to retrieve links for.</span></span>

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

### <span data-ttu-id="63d76-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="63d76-122">-Confirm</span></span>
<span data-ttu-id="63d76-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="63d76-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63d76-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63d76-124">-WhatIf</span></span>
<span data-ttu-id="63d76-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="63d76-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="63d76-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="63d76-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63d76-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63d76-127">CommonParameters</span></span>
<span data-ttu-id="63d76-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63d76-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63d76-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="63d76-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63d76-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="63d76-130">INPUTS</span></span>

### <span data-ttu-id="63d76-131">System. String</span><span class="sxs-lookup"><span data-stu-id="63d76-131">System.String</span></span>

## <span data-ttu-id="63d76-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="63d76-132">OUTPUTS</span></span>

### <span data-ttu-id="63d76-133">Microsoft. Azure. Commands. SQL. Replication. Model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="63d76-133">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="63d76-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="63d76-134">NOTES</span></span>

## <span data-ttu-id="63d76-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="63d76-135">RELATED LINKS</span></span>

[<span data-ttu-id="63d76-136">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="63d76-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
