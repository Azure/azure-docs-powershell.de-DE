---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/stop-azsqlelasticpoolactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticPoolActivity.md
ms.openlocfilehash: dbd0c93aca3750af846aa75ed369743fce5722ea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946832"
---
# <span data-ttu-id="9cd15-101">Stop-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="9cd15-101">Stop-AzSqlElasticPoolActivity</span></span>

## <span data-ttu-id="9cd15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9cd15-102">SYNOPSIS</span></span>
<span data-ttu-id="9cd15-103">Bricht den asynchronen Aktualisierungsvorgang in einem Pool mit einem flexiblen Pool ab.</span><span class="sxs-lookup"><span data-stu-id="9cd15-103">Cancels the asynchronous update operation on an elastic pool.</span></span>

## <span data-ttu-id="9cd15-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9cd15-104">SYNTAX</span></span>

```
Stop-AzSqlElasticPoolActivity [-PassThru] [-ServerName] <String> [-ElasticPoolName] <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9cd15-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9cd15-105">DESCRIPTION</span></span>
<span data-ttu-id="9cd15-106">Das **Cmdlet Stop-AzSqlElasticPoolActivity** beendet den asynchronen Aktualisierungsvorgang in einem Pool mit einem flexiblen Pool.</span><span class="sxs-lookup"><span data-stu-id="9cd15-106">The **Stop-AzSqlElasticPoolActivity** cmdlet cancels the asynchronous update operation on an elastic pool.</span></span>

## <span data-ttu-id="9cd15-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9cd15-107">EXAMPLES</span></span>

### <span data-ttu-id="9cd15-108">Beispiel 1: Abbrechen des asynchronen Aktualisierungsvorgangs für einen Pool mit einem flexiblen Pool</span><span class="sxs-lookup"><span data-stu-id="9cd15-108">Example 1: Cancel the asynchronous update operation on an elastic pool</span></span>
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

<span data-ttu-id="9cd15-109">Mit diesem Befehl wird der asynchrone Aktualisierungsvorgang im Pool für die flexiblen Daten abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="9cd15-109">This command cancels the asynchronous updates operation on the elastic pool.</span></span>

## <span data-ttu-id="9cd15-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9cd15-110">PARAMETERS</span></span>

### <span data-ttu-id="9cd15-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cd15-111">-DefaultProfile</span></span>
<span data-ttu-id="9cd15-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9cd15-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9cd15-113">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="9cd15-113">-ElasticPoolName</span></span>
<span data-ttu-id="9cd15-114">Der Name des Azure SQL -Pool.</span><span class="sxs-lookup"><span data-stu-id="9cd15-114">The name of the Azure SQL Elastic Pool.</span></span>

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

### <span data-ttu-id="9cd15-115">-OperationId</span><span class="sxs-lookup"><span data-stu-id="9cd15-115">-OperationId</span></span>
<span data-ttu-id="9cd15-116">Die ID des abzurufende Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="9cd15-116">The ID of the operation to retrieve.</span></span>

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

### <span data-ttu-id="9cd15-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9cd15-117">-PassThru</span></span>
<span data-ttu-id="9cd15-118">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="9cd15-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="9cd15-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cd15-119">-ResourceGroupName</span></span>
<span data-ttu-id="9cd15-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9cd15-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="9cd15-121">-Servername</span><span class="sxs-lookup"><span data-stu-id="9cd15-121">-ServerName</span></span>
<span data-ttu-id="9cd15-122">Der Name des Azure-SQL Server der "Pool für den flexiblen Pool" ist in.</span><span class="sxs-lookup"><span data-stu-id="9cd15-122">The name of the Azure SQL Server the Elastic Pool is in.</span></span>

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

### <span data-ttu-id="9cd15-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9cd15-123">-Confirm</span></span>
<span data-ttu-id="9cd15-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9cd15-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cd15-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cd15-125">-WhatIf</span></span>
<span data-ttu-id="9cd15-126">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9cd15-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9cd15-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9cd15-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9cd15-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cd15-128">CommonParameters</span></span>
<span data-ttu-id="9cd15-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cd15-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cd15-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9cd15-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cd15-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9cd15-131">INPUTS</span></span>

### <span data-ttu-id="9cd15-132">System.String</span><span class="sxs-lookup"><span data-stu-id="9cd15-132">System.String</span></span>

### <span data-ttu-id="9cd15-133">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9cd15-133">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="9cd15-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9cd15-134">OUTPUTS</span></span>

### <span data-ttu-id="9cd15-135">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span><span class="sxs-lookup"><span data-stu-id="9cd15-135">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span></span>

## <span data-ttu-id="9cd15-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="9cd15-136">NOTES</span></span>

## <span data-ttu-id="9cd15-137">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="9cd15-137">RELATED LINKS</span></span>
