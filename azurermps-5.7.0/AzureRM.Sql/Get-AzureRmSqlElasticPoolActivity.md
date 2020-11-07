---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 0DB0B08A-F948-4F6E-9CF0-2FB5DD5064D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlelasticpoolactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolActivity.md
ms.openlocfilehash: 88052c9f47359e0080e193f5a2dbb1004b48b0e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663038"
---
# <span data-ttu-id="94112-101">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="94112-101">Get-AzureRmSqlElasticPoolActivity</span></span>

## <span data-ttu-id="94112-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="94112-102">SYNOPSIS</span></span>
<span data-ttu-id="94112-103">Ruft den Status von Vorgängen in einem elastischen Pool ab.</span><span class="sxs-lookup"><span data-stu-id="94112-103">Gets the status of operations on an elastic pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94112-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="94112-104">SYNTAX</span></span>

```
Get-AzureRmSqlElasticPoolActivity [-ServerName] <String> [-ElasticPoolName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="94112-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="94112-105">DESCRIPTION</span></span>
<span data-ttu-id="94112-106">Das Cmdlet " **Get-AzureRmSqlElasticPoolActivity** " Ruft den Status von Vorgängen in einem elastischen Pool für eine Azure SQL-Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="94112-106">The **Get-AzureRmSqlElasticPoolActivity** cmdlet gets the status of operations on an elastic pool for an Azure SQL Database.</span></span>
<span data-ttu-id="94112-107">Sie können den Status beider Pool Erstellungs-und Konfigurationsupdates sehen.</span><span class="sxs-lookup"><span data-stu-id="94112-107">You can see the status of both pool creation and configuration updates.</span></span>

## <span data-ttu-id="94112-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="94112-108">EXAMPLES</span></span>

### <span data-ttu-id="94112-109">Beispiel 1: Abrufen des Status von Vorgängen für einen elastischen Pool</span><span class="sxs-lookup"><span data-stu-id="94112-109">Example 1: Get the status of operations for an elastic pool</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="94112-110">Dieser Befehl ruft den Status der Vorgänge für den elastischen Pool mit dem Namen ElasticPool01 ab.</span><span class="sxs-lookup"><span data-stu-id="94112-110">This command gets the status of the operations for the elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="94112-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="94112-111">PARAMETERS</span></span>

### <span data-ttu-id="94112-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94112-112">-DefaultProfile</span></span>
<span data-ttu-id="94112-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="94112-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="94112-114">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="94112-114">-ElasticPoolName</span></span>
<span data-ttu-id="94112-115">Gibt den Namen eines elastischen Pools an.</span><span class="sxs-lookup"><span data-stu-id="94112-115">Specifies the name of an elastic pool.</span></span>

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

### <span data-ttu-id="94112-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94112-116">-ResourceGroupName</span></span>
<span data-ttu-id="94112-117">Gibt den Namen einer Ressourcengruppe an, der der elastische Pool zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="94112-117">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="94112-118">-Servername</span><span class="sxs-lookup"><span data-stu-id="94112-118">-ServerName</span></span>
<span data-ttu-id="94112-119">Gibt den Namen eines Servers an, der einen elastischen Pool enthält.</span><span class="sxs-lookup"><span data-stu-id="94112-119">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="94112-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="94112-120">-Confirm</span></span>
<span data-ttu-id="94112-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="94112-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94112-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94112-122">-WhatIf</span></span>
<span data-ttu-id="94112-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="94112-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94112-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="94112-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94112-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94112-125">CommonParameters</span></span>
<span data-ttu-id="94112-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94112-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94112-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94112-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94112-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="94112-128">INPUTS</span></span>

### <span data-ttu-id="94112-129">Keine</span><span class="sxs-lookup"><span data-stu-id="94112-129">None</span></span>
<span data-ttu-id="94112-130">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="94112-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="94112-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="94112-131">OUTPUTS</span></span>

### <span data-ttu-id="94112-132">Microsoft. Azure. Commands. SQL. ElasticPool. Model. AzureSqlElasticPoolActivityModel</span><span class="sxs-lookup"><span data-stu-id="94112-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span></span>

## <span data-ttu-id="94112-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="94112-133">NOTES</span></span>

## <span data-ttu-id="94112-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="94112-134">RELATED LINKS</span></span>

[<span data-ttu-id="94112-135">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="94112-135">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="94112-136">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="94112-136">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="94112-137">Neu – AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="94112-137">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="94112-138">Remove-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="94112-138">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="94112-139">Satz-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="94112-139">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)


