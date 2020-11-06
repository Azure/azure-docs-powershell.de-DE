---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 40054224-52FF-4AF6-A090-9F6D07A2BA99
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasereplicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseReplicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseReplicationLink.md
ms.openlocfilehash: 993d7ef8958e96cebcd104d25550e860cdfd1853
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501057"
---
# <span data-ttu-id="83380-101">Get-AzureRmSqlDatabaseReplicationLink</span><span class="sxs-lookup"><span data-stu-id="83380-101">Get-AzureRmSqlDatabaseReplicationLink</span></span>

## <span data-ttu-id="83380-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="83380-102">SYNOPSIS</span></span>
<span data-ttu-id="83380-103">Ruft die Geo-Replikationsverknüpfungen zwischen einer Azure SQL-Datenbank und einer Ressourcengruppe oder SQL Server ab.</span><span class="sxs-lookup"><span data-stu-id="83380-103">Gets the geo-replication links between an Azure SQL Database and a resource group or SQL Server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83380-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="83380-104">SYNTAX</span></span>

### <span data-ttu-id="83380-105">ByDatabaseName (Standard)</span><span class="sxs-lookup"><span data-stu-id="83380-105">ByDatabaseName (Default)</span></span>
```
Get-AzureRmSqlDatabaseReplicationLink [-DatabaseName] <String> -PartnerResourceGroupName <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83380-106">ByPartnerServerName</span><span class="sxs-lookup"><span data-stu-id="83380-106">ByPartnerServerName</span></span>
```
Get-AzureRmSqlDatabaseReplicationLink [-DatabaseName] <String> -PartnerResourceGroupName <String>
 [-PartnerServerName <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83380-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="83380-107">DESCRIPTION</span></span>
<span data-ttu-id="83380-108">Das Cmdlet **Get-AzureRMSqlDatabaseReplicationLink** ersetzt das Cmdlet **Get-AzureSqlDatabaseCopy** .</span><span class="sxs-lookup"><span data-stu-id="83380-108">The **Get-AzureRMSqlDatabaseReplicationLink** cmdlet replaces the **Get-AzureSqlDatabaseCopy** cmdlet.</span></span>
<span data-ttu-id="83380-109">Es werden alle Geo-Replikationsverknüpfungen zwischen der angegebenen Azure SQL-Datenbank und einer Ressourcengruppe oder einem AzureSQL-Server abgerufen.</span><span class="sxs-lookup"><span data-stu-id="83380-109">It gets all geo-replication links between the specified Azure SQL Database and a resource group or AzureSQL Server.</span></span>

## <span data-ttu-id="83380-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="83380-110">EXAMPLES</span></span>

## <span data-ttu-id="83380-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="83380-111">PARAMETERS</span></span>

### <span data-ttu-id="83380-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="83380-112">-DatabaseName</span></span>
<span data-ttu-id="83380-113">Gibt den Namen der SQL-Datenbank an, für die Links abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="83380-113">Specifies the name of the SQL Database for which to retrieve links.</span></span>

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

### <span data-ttu-id="83380-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83380-114">-DefaultProfile</span></span>
<span data-ttu-id="83380-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="83380-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="83380-116">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83380-116">-PartnerResourceGroupName</span></span>
<span data-ttu-id="83380-117">Gibt den Namen der Ressourcengruppe an, der der Partner zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="83380-117">Specifies the name of the resource group to which the partner is assigned.</span></span>

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

### <span data-ttu-id="83380-118">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="83380-118">-PartnerServerName</span></span>
<span data-ttu-id="83380-119">Gibt den Namen des Azure SQL Server für den Partner an.</span><span class="sxs-lookup"><span data-stu-id="83380-119">Specifies the name of the Azure SQL Server for the partner.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPartnerServerName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83380-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83380-120">-ResourceGroupName</span></span>
<span data-ttu-id="83380-121">Gibt den Namen der Azure-Ressourcengruppe für die Datenbank an, für die Verknüpfungen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="83380-121">Specifies the name of the Azure resource group for the database for which to retrieve links.</span></span>

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

### <span data-ttu-id="83380-122">-Servername</span><span class="sxs-lookup"><span data-stu-id="83380-122">-ServerName</span></span>
<span data-ttu-id="83380-123">Gibt den Namen des SQL Server für die Datenbank an, für den Links abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="83380-123">Specifies the name of the SQL Server for the database to retrieve links for.</span></span>

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

### <span data-ttu-id="83380-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="83380-124">-Confirm</span></span>
<span data-ttu-id="83380-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="83380-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83380-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83380-126">-WhatIf</span></span>
<span data-ttu-id="83380-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="83380-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="83380-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="83380-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83380-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83380-129">CommonParameters</span></span>
<span data-ttu-id="83380-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83380-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83380-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83380-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83380-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="83380-132">INPUTS</span></span>

### <span data-ttu-id="83380-133">System. String</span><span class="sxs-lookup"><span data-stu-id="83380-133">System.String</span></span>

## <span data-ttu-id="83380-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="83380-134">OUTPUTS</span></span>

### <span data-ttu-id="83380-135">Microsoft. Azure. Commands. SQL. Replication. Model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="83380-135">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="83380-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="83380-136">NOTES</span></span>

## <span data-ttu-id="83380-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="83380-137">RELATED LINKS</span></span>

[<span data-ttu-id="83380-138">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="83380-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
