---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14620FBD-4B10-4366-94F7-891BC01B893F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlelasticpooldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolDatabase.md
ms.openlocfilehash: a9f86b9b316c14e40505932e0bf3b30fc66c55c2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501018"
---
# <span data-ttu-id="84903-101">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="84903-101">Get-AzureRmSqlElasticPoolDatabase</span></span>

## <span data-ttu-id="84903-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="84903-102">SYNOPSIS</span></span>
<span data-ttu-id="84903-103">Ruft elastische Datenbanken in einem elastischen Pool und deren Eigenschaftenwerten ab.</span><span class="sxs-lookup"><span data-stu-id="84903-103">Gets elastic databases in an elastic pool and their property values.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84903-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="84903-104">SYNTAX</span></span>

```
Get-AzureRmSqlElasticPoolDatabase [-ElasticPoolName] <String> [-DatabaseName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="84903-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="84903-105">DESCRIPTION</span></span>
<span data-ttu-id="84903-106">Das Cmdlet " **Get-AzureRmSqlElasticPoolDatabase** " erhält elastische Datenbanken in einem elastischen Pool und deren Eigenschaftswerte.</span><span class="sxs-lookup"><span data-stu-id="84903-106">The **Get-AzureRmSqlElasticPoolDatabase** cmdlet gets elastic databases in an elastic pool and their property values.</span></span>
<span data-ttu-id="84903-107">Sie können den Namen einer elastischen Datenbank in Azure SQL-Datenbank angeben, um die Eigenschaftswerte nur für diese Datenbank anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="84903-107">You can specify the name of an elastic database in Azure SQL Database to see the property values for only that database.</span></span>

## <span data-ttu-id="84903-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="84903-108">EXAMPLES</span></span>

### <span data-ttu-id="84903-109">Beispiel 1: Abrufen aller Datenbanken in einem elastischen Pool</span><span class="sxs-lookup"><span data-stu-id="84903-109">Example 1: Get all databases in an elastic pool</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="84903-110">Dieser Befehl ruft alle Datenbanken in einem elastischen Pool mit dem Namen ElasticPool01 ab.</span><span class="sxs-lookup"><span data-stu-id="84903-110">This command gets all databases in an elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="84903-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="84903-111">PARAMETERS</span></span>

### <span data-ttu-id="84903-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="84903-112">-DatabaseName</span></span>
<span data-ttu-id="84903-113">Gibt den Namen der SQL-Datenbank an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="84903-113">Specifies the name of the SQL Database that this cmdlet gets.</span></span>

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

### <span data-ttu-id="84903-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84903-114">-DefaultProfile</span></span>
<span data-ttu-id="84903-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="84903-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="84903-116">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="84903-116">-ElasticPoolName</span></span>
<span data-ttu-id="84903-117">Gibt den Namen eines elastischen Pools an.</span><span class="sxs-lookup"><span data-stu-id="84903-117">Specifies the name of an elastic pool.</span></span>

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

### <span data-ttu-id="84903-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84903-118">-ResourceGroupName</span></span>
<span data-ttu-id="84903-119">Gibt den Namen einer Ressourcengruppe an, der der elastische Pool zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="84903-119">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="84903-120">-Servername</span><span class="sxs-lookup"><span data-stu-id="84903-120">-ServerName</span></span>
<span data-ttu-id="84903-121">Gibt den Namen eines Servers an, der einen elastischen Pool enthält.</span><span class="sxs-lookup"><span data-stu-id="84903-121">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="84903-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="84903-122">-Confirm</span></span>
<span data-ttu-id="84903-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="84903-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84903-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84903-124">-WhatIf</span></span>
<span data-ttu-id="84903-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="84903-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84903-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="84903-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84903-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84903-127">CommonParameters</span></span>
<span data-ttu-id="84903-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84903-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84903-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84903-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84903-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="84903-130">INPUTS</span></span>

### <span data-ttu-id="84903-131">System. String</span><span class="sxs-lookup"><span data-stu-id="84903-131">System.String</span></span>

## <span data-ttu-id="84903-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="84903-132">OUTPUTS</span></span>

### <span data-ttu-id="84903-133">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="84903-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="84903-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="84903-134">NOTES</span></span>

## <span data-ttu-id="84903-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="84903-135">RELATED LINKS</span></span>

[<span data-ttu-id="84903-136">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="84903-136">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="84903-137">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="84903-137">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="84903-138">Neu – AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="84903-138">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="84903-139">Remove-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="84903-139">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="84903-140">Satz-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="84903-140">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)

