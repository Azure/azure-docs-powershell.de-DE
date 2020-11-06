---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseActivity.md
ms.openlocfilehash: b37ae31c1f0dc6360743a863f0305fd5823cbb3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503926"
---
# <span data-ttu-id="e9686-101">Get-AzureRmSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="e9686-101">Get-AzureRmSqlDatabaseActivity</span></span>

## <span data-ttu-id="e9686-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e9686-102">SYNOPSIS</span></span>
<span data-ttu-id="e9686-103">Ruft den Status des Verschiebens von elastischen Datenbanken ab.</span><span class="sxs-lookup"><span data-stu-id="e9686-103">Gets the status of moving elastic databases.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9686-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e9686-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseActivity [-ServerName] <String> -ElasticPoolName <String> -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9686-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e9686-105">DESCRIPTION</span></span>
<span data-ttu-id="e9686-106">Das Cmdlet " **Get-AzureRmSqlDatabaseActivity** " Ruft den Status von elastischen Datenbanken ab, die in einen elastischen datenbankpool in Azure SQL-Datenbank verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="e9686-106">The **Get-AzureRmSqlDatabaseActivity** cmdlet gets the status of elastic databases moving into or out of an elastic database pool in Azure SQL Database.</span></span>

## <span data-ttu-id="e9686-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e9686-107">EXAMPLES</span></span>

### <span data-ttu-id="e9686-108">Beispiel 1: Abrufen des Status für alle SQL-Datenbankinstanzen</span><span class="sxs-lookup"><span data-stu-id="e9686-108">Example 1: Get status for all SQL Database instances</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="e9686-109">Dieser Befehl gibt den Vorgangsstatus aller SQL-Datenbankinstanzen in einem elastischen Pool mit dem Namen "ElasticPool01" zurück.</span><span class="sxs-lookup"><span data-stu-id="e9686-109">This command returns the operation status of all SQL Database instances in an elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="e9686-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e9686-110">PARAMETERS</span></span>

### <span data-ttu-id="e9686-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e9686-111">-DatabaseName</span></span>
<span data-ttu-id="e9686-112">Gibt den Namen der Datenbank an, für die dieses Cmdlet den Status erhält.</span><span class="sxs-lookup"><span data-stu-id="e9686-112">Specifies the name of the database for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="e9686-113">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="e9686-113">-ElasticPoolName</span></span>
<span data-ttu-id="e9686-114">Gibt den Namen des elastischen Daten Bank Pools an, für den dieses Cmdlet den Status erhält.</span><span class="sxs-lookup"><span data-stu-id="e9686-114">Specifies the name of the elastic database pool for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="e9686-115">-Vorgangs-Nr</span><span class="sxs-lookup"><span data-stu-id="e9686-115">-OperationId</span></span>
<span data-ttu-id="e9686-116">Gibt die ID des Vorgangs an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="e9686-116">Specifies the ID of the operation that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e9686-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9686-117">-ResourceGroupName</span></span>
<span data-ttu-id="e9686-118">Gibt den Namen der Ressourcengruppe an, der die Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="e9686-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="e9686-119">-Servername</span><span class="sxs-lookup"><span data-stu-id="e9686-119">-ServerName</span></span>
<span data-ttu-id="e9686-120">Gibt den Namen des Microsoft SQL Server an, der den elastischen datenbankpool hostet.</span><span class="sxs-lookup"><span data-stu-id="e9686-120">Specifies the name of the Microsoft SQL Server that hosts the elastic database pool.</span></span>

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

### <span data-ttu-id="e9686-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e9686-121">-Confirm</span></span>
<span data-ttu-id="e9686-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e9686-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9686-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9686-123">-WhatIf</span></span>
<span data-ttu-id="e9686-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e9686-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9686-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e9686-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9686-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9686-126">-DefaultProfile</span></span>
<span data-ttu-id="e9686-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e9686-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9686-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9686-128">CommonParameters</span></span>
<span data-ttu-id="e9686-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9686-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9686-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9686-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9686-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e9686-131">INPUTS</span></span>

## <span data-ttu-id="e9686-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e9686-132">OUTPUTS</span></span>

### <span data-ttu-id="e9686-133">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseActivityModel</span><span class="sxs-lookup"><span data-stu-id="e9686-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="e9686-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="e9686-134">NOTES</span></span>

## <span data-ttu-id="e9686-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e9686-135">RELATED LINKS</span></span>

