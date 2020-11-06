---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 54E01B3B-FFA5-4E3C-BA5A-A281FF5C9F8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseSecondary.md
ms.openlocfilehash: d326abcd7cc0aee627d56250ac63d68549be610d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501342"
---
# <span data-ttu-id="c81ae-101">Remove-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="c81ae-101">Remove-AzureRmSqlDatabaseSecondary</span></span>

## <span data-ttu-id="c81ae-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c81ae-102">SYNOPSIS</span></span>
<span data-ttu-id="c81ae-103">Beendet die Datenreplikation zwischen einer SQL-Datenbank und der angegebenen sekundären Datenbank.</span><span class="sxs-lookup"><span data-stu-id="c81ae-103">Terminates data replication between a SQL Database and the specified secondary database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c81ae-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c81ae-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c81ae-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c81ae-105">DESCRIPTION</span></span>
<span data-ttu-id="c81ae-106">Das Cmdlet **Remove-AzureRmSqlDatabaseSecondary** erzwingt die Beendigung eines Geo-Replikationslinks.</span><span class="sxs-lookup"><span data-stu-id="c81ae-106">The **Remove-AzureRmSqlDatabaseSecondary** cmdlet forces termination of a geo-replication link.</span></span>
<span data-ttu-id="c81ae-107">Dieses Cmdlet ersetzt das Stop-AzureSqlDatabaseCopy-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c81ae-107">This cmdlet replaces the Stop-AzureSqlDatabaseCopy cmdlet.</span></span>
<span data-ttu-id="c81ae-108">Vor dem Beenden erfolgt keine Replikationssynchronisierung.</span><span class="sxs-lookup"><span data-stu-id="c81ae-108">There is no replication synchronization before termination.</span></span>

## <span data-ttu-id="c81ae-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c81ae-109">EXAMPLES</span></span>

## <span data-ttu-id="c81ae-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c81ae-110">PARAMETERS</span></span>

### <span data-ttu-id="c81ae-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c81ae-111">-DatabaseName</span></span>
<span data-ttu-id="c81ae-112">Gibt den Namen der primären Azure SQL-Datenbank mit dem Replikations Link an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="c81ae-112">Specifies the name of the primary Azure SQL Database that has the replication link that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c81ae-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c81ae-113">-DefaultProfile</span></span>
<span data-ttu-id="c81ae-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="c81ae-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c81ae-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c81ae-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="c81ae-116">Gibt den Namen der Partner Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="c81ae-116">Specifies the name of the partner  resource group.</span></span>

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

### <span data-ttu-id="c81ae-117">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="c81ae-117">-PartnerServerName</span></span>
<span data-ttu-id="c81ae-118">Gibt den Namen des SQL Server-Partners an.</span><span class="sxs-lookup"><span data-stu-id="c81ae-118">Specifies the name of the partner SQL Server.</span></span>

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

### <span data-ttu-id="c81ae-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c81ae-119">-ResourceGroupName</span></span>
<span data-ttu-id="c81ae-120">Gibt den Namen der Ressourcengruppe an, die dem zu entfernenden Replikations Link zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c81ae-120">Specifies the name of the resource group that is associated with the replication link to remove.</span></span>

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

### <span data-ttu-id="c81ae-121">-Servername</span><span class="sxs-lookup"><span data-stu-id="c81ae-121">-ServerName</span></span>
<span data-ttu-id="c81ae-122">Gibt den Namen des SQL-Servers an, der den zu entfernenden Replikations Link enthält.</span><span class="sxs-lookup"><span data-stu-id="c81ae-122">Specifies the name of the SQL Server that has the replication link to remove.</span></span>

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

### <span data-ttu-id="c81ae-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c81ae-123">-Confirm</span></span>
<span data-ttu-id="c81ae-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c81ae-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c81ae-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c81ae-125">-WhatIf</span></span>
<span data-ttu-id="c81ae-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c81ae-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c81ae-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c81ae-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c81ae-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c81ae-128">CommonParameters</span></span>
<span data-ttu-id="c81ae-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c81ae-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c81ae-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c81ae-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c81ae-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c81ae-131">INPUTS</span></span>

###  
<span data-ttu-id="c81ae-132">Sie können Instanzen des **Daten Bank** Objekts für die primäre oder sekundäre Datenbank an dieses Cmdlet weiterleiten.</span><span class="sxs-lookup"><span data-stu-id="c81ae-132">You can pipe instances of the **Database** object for the primary or secondary database to this cmdlet.</span></span>

## <span data-ttu-id="c81ae-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c81ae-133">OUTPUTS</span></span>

###  
<span data-ttu-id="c81ae-134">Dieses Cmdlet generiert keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="c81ae-134">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="c81ae-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="c81ae-135">NOTES</span></span>

## <span data-ttu-id="c81ae-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c81ae-136">RELATED LINKS</span></span>

[<span data-ttu-id="c81ae-137">Neu – AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="c81ae-137">New-AzureRmSqlDatabaseSecondary</span></span>](./New-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="c81ae-138">Satz-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="c81ae-138">Set-AzureRmSqlDatabaseSecondary</span></span>](./Set-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="c81ae-139">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="c81ae-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
