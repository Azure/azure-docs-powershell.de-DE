---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 47E8E8C1-A63D-4243-A004-ABD5CA1A559E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlElasticPool.md
ms.openlocfilehash: 57f5f656f3c85e9d1c0d29c07a602a303208e7f7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499134"
---
# <span data-ttu-id="43798-101">Remove-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="43798-101">Remove-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="43798-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="43798-102">SYNOPSIS</span></span>
<span data-ttu-id="43798-103">Löscht einen elastischen datenbankpool.</span><span class="sxs-lookup"><span data-stu-id="43798-103">Deletes an elastic database pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43798-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="43798-104">SYNTAX</span></span>

```
Remove-AzureRmSqlElasticPool [-ElasticPoolName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="43798-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="43798-105">DESCRIPTION</span></span>
<span data-ttu-id="43798-106">Das Cmdlet **Remove-AzureRmSqlElasticPool** löscht einen Azure SQL-Datenbank-Elastic-Pool.</span><span class="sxs-lookup"><span data-stu-id="43798-106">The **Remove-AzureRmSqlElasticPool** cmdlet deletes an Azure SQL Database elastic pool.</span></span>

## <span data-ttu-id="43798-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="43798-107">EXAMPLES</span></span>

### <span data-ttu-id="43798-108">Beispiel 1: Löschen eines elastischen Pools</span><span class="sxs-lookup"><span data-stu-id="43798-108">Example 1: Delete an elastic pool</span></span>
```
PS C:\>Remove-AzureRmSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="43798-109">Dieser Befehl löscht einen elastischen Pool mit dem Namen ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="43798-109">This command deletes an elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="43798-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="43798-110">PARAMETERS</span></span>

### <span data-ttu-id="43798-111">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="43798-111">-ElasticPoolName</span></span>
<span data-ttu-id="43798-112">Gibt den Namen des elastischen Pools an, den dieses Cmdlet löscht.</span><span class="sxs-lookup"><span data-stu-id="43798-112">Specifies the name of the elastic pool that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43798-113">-Force</span><span class="sxs-lookup"><span data-stu-id="43798-113">-Force</span></span>
<span data-ttu-id="43798-114">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="43798-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43798-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43798-115">-ResourceGroupName</span></span>
<span data-ttu-id="43798-116">Gibt den Namen der Ressourcengruppe an, der der elastische Pool zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="43798-116">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="43798-117">-Servername</span><span class="sxs-lookup"><span data-stu-id="43798-117">-ServerName</span></span>
<span data-ttu-id="43798-118">Gibt den Namen des Servers an, der den elastischen Pool hostet.</span><span class="sxs-lookup"><span data-stu-id="43798-118">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="43798-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="43798-119">-Confirm</span></span>
<span data-ttu-id="43798-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="43798-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43798-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43798-121">-WhatIf</span></span>
<span data-ttu-id="43798-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="43798-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43798-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="43798-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43798-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43798-124">-DefaultProfile</span></span>
<span data-ttu-id="43798-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="43798-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43798-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43798-126">CommonParameters</span></span>
<span data-ttu-id="43798-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43798-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43798-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43798-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43798-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="43798-129">INPUTS</span></span>

### <span data-ttu-id="43798-130">Microsoft. Azure. Commands. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="43798-130">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="43798-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="43798-131">OUTPUTS</span></span>

### <span data-ttu-id="43798-132">Microsoft. Azure. Commands. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="43798-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="43798-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="43798-133">NOTES</span></span>

## <span data-ttu-id="43798-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="43798-134">RELATED LINKS</span></span>

[<span data-ttu-id="43798-135">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="43798-135">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="43798-136">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="43798-136">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="43798-137">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="43798-137">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="43798-138">Neu – AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="43798-138">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="43798-139">Satz-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="43798-139">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)

[<span data-ttu-id="43798-140">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="43798-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


