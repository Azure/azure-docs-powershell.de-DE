---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/stop-azurermsqlelasticpoolactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlElasticPoolActivity.md
ms.openlocfilehash: 999fd83af11422f1499e386f194fd75d9b99e152
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481934"
---
# <span data-ttu-id="a07fa-101">Stop-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="a07fa-101">Stop-AzureRmSqlElasticPoolActivity</span></span>

## <span data-ttu-id="a07fa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a07fa-102">SYNOPSIS</span></span>
<span data-ttu-id="a07fa-103">Bricht den asynchronen Aktualisierungsvorgang für einen elastischen Pool ab.</span><span class="sxs-lookup"><span data-stu-id="a07fa-103">Cancels the asynchronous update operation on an elastic pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a07fa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a07fa-104">SYNTAX</span></span>

```
Stop-AzureRmSqlElasticPoolActivity [-PassThru] [-ServerName] <String> [-ElasticPoolName] <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a07fa-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a07fa-105">DESCRIPTION</span></span>
<span data-ttu-id="a07fa-106">Mit dem Cmdlet " **Stop-AzureRmSqlElasticPoolActivity** " wird der asynchrone Aktualisierungsvorgang in einem elastischen Pool abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="a07fa-106">The **Stop-AzureRmSqlElasticPoolActivity** cmdlet cancels the asynchronous update operation on an elastic pool.</span></span>

## <span data-ttu-id="a07fa-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a07fa-107">EXAMPLES</span></span>

### <span data-ttu-id="a07fa-108">Beispiel 1: Abbrechen des asynchronen Aktualisierungsvorgangs in einem elastischen Pool</span><span class="sxs-lookup"><span data-stu-id="a07fa-108">Example 1: Cancel the asynchronous update operation on an elastic pool</span></span>
```
PS C:\> Stop-AzureRmSqlElasticPoolActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -OperationId af97005d-9243-4f8a-844e-402d1cc855f5

OperationId     : af97005d-9243-4f8a-844e-402d1cc855f5
ServerName      : Server01
DatabaseName    : ElasticPool01
State           : CANCELLED
Operation       : UpdateLogicalElasticPool
ErrorCode       :
ErrorMessage    :
ErrorSeverity   :
StartTime       : 10/15/2017 02:49:42 PM
EndTime         : 10/15/2017 02:49:43 PM
PercentComplete :
```

<span data-ttu-id="a07fa-109">Mit diesem Befehl wird der asynchrone Aktualisierungsvorgang für den elastischen Pool abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="a07fa-109">This command cancels the asynchronous updates operation on the elastic pool.</span></span>

## <span data-ttu-id="a07fa-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a07fa-110">PARAMETERS</span></span>

### <span data-ttu-id="a07fa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a07fa-111">-DefaultProfile</span></span>
<span data-ttu-id="a07fa-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a07fa-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a07fa-113">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="a07fa-113">-ElasticPoolName</span></span>
<span data-ttu-id="a07fa-114">Der Name des Azure SQL-elastischen Pools.</span><span class="sxs-lookup"><span data-stu-id="a07fa-114">The name of the Azure SQL Elastic Pool.</span></span>

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

### <span data-ttu-id="a07fa-115">-Vorgangs-Nr</span><span class="sxs-lookup"><span data-stu-id="a07fa-115">-OperationId</span></span>
<span data-ttu-id="a07fa-116">Die ID des abzurufenden Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="a07fa-116">The ID of the operation to retrieve.</span></span>

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

### <span data-ttu-id="a07fa-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a07fa-117">-PassThru</span></span>
<span data-ttu-id="a07fa-118">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="a07fa-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="a07fa-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a07fa-119">-ResourceGroupName</span></span>
<span data-ttu-id="a07fa-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a07fa-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="a07fa-121">-Servername</span><span class="sxs-lookup"><span data-stu-id="a07fa-121">-ServerName</span></span>
<span data-ttu-id="a07fa-122">Der Name des Azure SQL Server, in dem sich der elastische Pool befindet.</span><span class="sxs-lookup"><span data-stu-id="a07fa-122">The name of the Azure SQL Server the Elastic Pool is in.</span></span>

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

### <span data-ttu-id="a07fa-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a07fa-123">-Confirm</span></span>
<span data-ttu-id="a07fa-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a07fa-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a07fa-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a07fa-125">-WhatIf</span></span>
<span data-ttu-id="a07fa-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a07fa-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a07fa-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a07fa-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a07fa-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a07fa-128">CommonParameters</span></span>
<span data-ttu-id="a07fa-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a07fa-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a07fa-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a07fa-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a07fa-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a07fa-131">INPUTS</span></span>

### <span data-ttu-id="a07fa-132">System. String</span><span class="sxs-lookup"><span data-stu-id="a07fa-132">System.String</span></span>

### <span data-ttu-id="a07fa-133">System. Nullable ' 1 [[System. Guid, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="a07fa-133">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="a07fa-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a07fa-134">OUTPUTS</span></span>

### <span data-ttu-id="a07fa-135">Microsoft. Azure. Commands. SQL. ElasticPool. Model. AzureSqlElasticPoolActivityModel</span><span class="sxs-lookup"><span data-stu-id="a07fa-135">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span></span>

## <span data-ttu-id="a07fa-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="a07fa-136">NOTES</span></span>

## <span data-ttu-id="a07fa-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a07fa-137">RELATED LINKS</span></span>
