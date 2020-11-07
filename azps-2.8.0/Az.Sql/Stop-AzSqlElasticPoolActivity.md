---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqlelasticpoolactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticPoolActivity.md
ms.openlocfilehash: 0082918e09c0f42910ead42d03319577d4b4c9c8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93826196"
---
# <span data-ttu-id="6bda2-101">Stop-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="6bda2-101">Stop-AzSqlElasticPoolActivity</span></span>

## <span data-ttu-id="6bda2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6bda2-102">SYNOPSIS</span></span>
<span data-ttu-id="6bda2-103">Bricht den asynchronen Aktualisierungsvorgang für einen elastischen Pool ab.</span><span class="sxs-lookup"><span data-stu-id="6bda2-103">Cancels the asynchronous update operation on an elastic pool.</span></span>

## <span data-ttu-id="6bda2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6bda2-104">SYNTAX</span></span>

```
Stop-AzSqlElasticPoolActivity [-PassThru] [-ServerName] <String> [-ElasticPoolName] <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6bda2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6bda2-105">DESCRIPTION</span></span>
<span data-ttu-id="6bda2-106">Mit dem Cmdlet " **Stop-AzSqlElasticPoolActivity** " wird der asynchrone Aktualisierungsvorgang in einem elastischen Pool abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="6bda2-106">The **Stop-AzSqlElasticPoolActivity** cmdlet cancels the asynchronous update operation on an elastic pool.</span></span>

## <span data-ttu-id="6bda2-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6bda2-107">EXAMPLES</span></span>

### <span data-ttu-id="6bda2-108">Beispiel 1: Abbrechen des asynchronen Aktualisierungsvorgangs in einem elastischen Pool</span><span class="sxs-lookup"><span data-stu-id="6bda2-108">Example 1: Cancel the asynchronous update operation on an elastic pool</span></span>
```
PS C:\> Stop-AzSqlElasticPoolActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -OperationId af97005d-9243-4f8a-844e-402d1cc855f5

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

<span data-ttu-id="6bda2-109">Mit diesem Befehl wird der asynchrone Aktualisierungsvorgang für den elastischen Pool abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="6bda2-109">This command cancels the asynchronous updates operation on the elastic pool.</span></span>

## <span data-ttu-id="6bda2-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6bda2-110">PARAMETERS</span></span>

### <span data-ttu-id="6bda2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bda2-111">-DefaultProfile</span></span>
<span data-ttu-id="6bda2-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6bda2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6bda2-113">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="6bda2-113">-ElasticPoolName</span></span>
<span data-ttu-id="6bda2-114">Der Name des Azure SQL-elastischen Pools.</span><span class="sxs-lookup"><span data-stu-id="6bda2-114">The name of the Azure SQL Elastic Pool.</span></span>

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

### <span data-ttu-id="6bda2-115">-Vorgangs-Nr</span><span class="sxs-lookup"><span data-stu-id="6bda2-115">-OperationId</span></span>
<span data-ttu-id="6bda2-116">Die ID des abzurufenden Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="6bda2-116">The ID of the operation to retrieve.</span></span>

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

### <span data-ttu-id="6bda2-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6bda2-117">-PassThru</span></span>
<span data-ttu-id="6bda2-118">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="6bda2-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="6bda2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bda2-119">-ResourceGroupName</span></span>
<span data-ttu-id="6bda2-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6bda2-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="6bda2-121">-Servername</span><span class="sxs-lookup"><span data-stu-id="6bda2-121">-ServerName</span></span>
<span data-ttu-id="6bda2-122">Der Name des Azure SQL Server, in dem sich der elastische Pool befindet.</span><span class="sxs-lookup"><span data-stu-id="6bda2-122">The name of the Azure SQL Server the Elastic Pool is in.</span></span>

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

### <span data-ttu-id="6bda2-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6bda2-123">-Confirm</span></span>
<span data-ttu-id="6bda2-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6bda2-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bda2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bda2-125">-WhatIf</span></span>
<span data-ttu-id="6bda2-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6bda2-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6bda2-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6bda2-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bda2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bda2-128">CommonParameters</span></span>
<span data-ttu-id="6bda2-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6bda2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bda2-130">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6bda2-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bda2-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6bda2-131">INPUTS</span></span>

### <span data-ttu-id="6bda2-132">System. String</span><span class="sxs-lookup"><span data-stu-id="6bda2-132">System.String</span></span>

### <span data-ttu-id="6bda2-133">System. Nullable ' 1 [[System. Guid, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6bda2-133">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="6bda2-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6bda2-134">OUTPUTS</span></span>

### <span data-ttu-id="6bda2-135">Microsoft. Azure. Commands. SQL. ElasticPool. Model. AzureSqlElasticPoolActivityModel</span><span class="sxs-lookup"><span data-stu-id="6bda2-135">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span></span>

## <span data-ttu-id="6bda2-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="6bda2-136">NOTES</span></span>

## <span data-ttu-id="6bda2-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6bda2-137">RELATED LINKS</span></span>
