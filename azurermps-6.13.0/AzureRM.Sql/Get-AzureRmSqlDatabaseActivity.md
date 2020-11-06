---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaseactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseActivity.md
ms.openlocfilehash: 08c5778002a80bb4fb2effdd977f134079f3aa0d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499389"
---
# <span data-ttu-id="fd938-101">Get-AzureRmSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="fd938-101">Get-AzureRmSqlDatabaseActivity</span></span>

## <span data-ttu-id="fd938-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fd938-102">SYNOPSIS</span></span>
<span data-ttu-id="fd938-103">Ruft den Status von Datenbankvorgängen ab.</span><span class="sxs-lookup"><span data-stu-id="fd938-103">Gets the status of database operations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd938-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd938-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseActivity [-ServerName] <String> [-ElasticPoolName <String>] -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd938-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fd938-105">DESCRIPTION</span></span>
<span data-ttu-id="fd938-106">Das Cmdlet " **Get-AzureRmSqlDatabaseActivity** " Ruft den Status von Datenbankvorgängen in Azure SQL-Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="fd938-106">The **Get-AzureRmSqlDatabaseActivity** cmdlet gets the status of database operations in Azure SQL Database.</span></span>

## <span data-ttu-id="fd938-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fd938-107">EXAMPLES</span></span>

### <span data-ttu-id="fd938-108">Beispiel 1: Abrufen des Status für alle SQL-Datenbankinstanzen</span><span class="sxs-lookup"><span data-stu-id="fd938-108">Example 1: Get status for all SQL Database instances</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="fd938-109">Dieser Befehl gibt den Vorgangsstatus aller SQL-Datenbankinstanzen in einem elastischen Pool mit dem Namen "ElasticPool01" zurück.</span><span class="sxs-lookup"><span data-stu-id="fd938-109">This command returns the operation status of all SQL Database instances in an elastic pool named ElasticPool01.</span></span>

### <span data-ttu-id="fd938-110">Beispiel 2: Abrufen des Status für alle SQL-Datenbankvorgänge</span><span class="sxs-lookup"><span data-stu-id="fd938-110">Example 2: Get status for all SQL Database operations</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="fd938-111">Dieser Befehl gibt den Status aller SQL-Datenbankvorgänge in einer Datenbank zurück.</span><span class="sxs-lookup"><span data-stu-id="fd938-111">This command returns the status of all SQL Database operations in a database.</span></span>

## <span data-ttu-id="fd938-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="fd938-112">PARAMETERS</span></span>

### <span data-ttu-id="fd938-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fd938-113">-DatabaseName</span></span>
<span data-ttu-id="fd938-114">Gibt den Namen der Datenbank an, für die dieses Cmdlet den Status erhält.</span><span class="sxs-lookup"><span data-stu-id="fd938-114">Specifies the name of the database for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="fd938-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd938-115">-DefaultProfile</span></span>
<span data-ttu-id="fd938-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fd938-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd938-117">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="fd938-117">-ElasticPoolName</span></span>
<span data-ttu-id="fd938-118">Gibt den Namen des elastischen Daten Bank Pools an, für den dieses Cmdlet den Status erhält.</span><span class="sxs-lookup"><span data-stu-id="fd938-118">Specifies the name of the elastic database pool for which this cmdlet gets status.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd938-119">-Vorgangs-Nr</span><span class="sxs-lookup"><span data-stu-id="fd938-119">-OperationId</span></span>
<span data-ttu-id="fd938-120">Gibt die ID des Vorgangs an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="fd938-120">Specifies the ID of the operation that this cmdlet gets.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd938-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd938-121">-ResourceGroupName</span></span>
<span data-ttu-id="fd938-122">Gibt den Namen der Ressourcengruppe an, der die Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="fd938-122">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="fd938-123">-Servername</span><span class="sxs-lookup"><span data-stu-id="fd938-123">-ServerName</span></span>
<span data-ttu-id="fd938-124">Gibt den Namen des Microsoft SQL Server an, der die Datenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="fd938-124">Specifies the name of the Microsoft SQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="fd938-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fd938-125">-Confirm</span></span>
<span data-ttu-id="fd938-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fd938-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd938-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd938-127">-WhatIf</span></span>
<span data-ttu-id="fd938-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fd938-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd938-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fd938-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd938-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd938-130">CommonParameters</span></span>
<span data-ttu-id="fd938-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd938-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd938-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd938-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd938-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fd938-133">INPUTS</span></span>

### <span data-ttu-id="fd938-134">System. String</span><span class="sxs-lookup"><span data-stu-id="fd938-134">System.String</span></span>

### <span data-ttu-id="fd938-135">System. Nullable ' 1 [[System. Guid, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="fd938-135">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="fd938-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fd938-136">OUTPUTS</span></span>

### <span data-ttu-id="fd938-137">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseActivityModel</span><span class="sxs-lookup"><span data-stu-id="fd938-137">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="fd938-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="fd938-138">NOTES</span></span>

## <span data-ttu-id="fd938-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fd938-139">RELATED LINKS</span></span>
