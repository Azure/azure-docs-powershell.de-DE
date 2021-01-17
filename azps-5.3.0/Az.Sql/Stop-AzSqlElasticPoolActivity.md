---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqlelasticpoolactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticPoolActivity.md
ms.openlocfilehash: dc1dffd84a95bd9cffac1dbafb5183d56e0b7c52
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468384"
---
# <span data-ttu-id="fdcfc-101">Stop-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="fdcfc-101">Stop-AzSqlElasticPoolActivity</span></span>

## <span data-ttu-id="fdcfc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fdcfc-102">SYNOPSIS</span></span>
<span data-ttu-id="fdcfc-103">Bricht den asynchronen Aktualisierungsvorgang für einen Pool mit Drosselung ab.</span><span class="sxs-lookup"><span data-stu-id="fdcfc-103">Cancels the asynchronous update operation on an elastic pool.</span></span>

## <span data-ttu-id="fdcfc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fdcfc-104">SYNTAX</span></span>

```
Stop-AzSqlElasticPoolActivity [-PassThru] [-ServerName] <String> [-ElasticPoolName] <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fdcfc-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fdcfc-105">DESCRIPTION</span></span>
<span data-ttu-id="fdcfc-106">Das **Cmdlet "Stop-AzSqlElasticPoolActivity"** bricht den asynchronen Aktualisierungsvorgang für einen Pool ab.</span><span class="sxs-lookup"><span data-stu-id="fdcfc-106">The **Stop-AzSqlElasticPoolActivity** cmdlet cancels the asynchronous update operation on an elastic pool.</span></span>

## <span data-ttu-id="fdcfc-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fdcfc-107">EXAMPLES</span></span>

### <span data-ttu-id="fdcfc-108">Beispiel 1: Abbrechen des asynchronen Aktualisierungsvorgangs für einen Pool</span><span class="sxs-lookup"><span data-stu-id="fdcfc-108">Example 1: Cancel the asynchronous update operation on an elastic pool</span></span>
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

<span data-ttu-id="fdcfc-109">Dieser Befehl bricht den Vorgang für asynchrone Updates im Pool ab.</span><span class="sxs-lookup"><span data-stu-id="fdcfc-109">This command cancels the asynchronous updates operation on the elastic pool.</span></span>

## <span data-ttu-id="fdcfc-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fdcfc-110">PARAMETERS</span></span>

### <span data-ttu-id="fdcfc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdcfc-111">-DefaultProfile</span></span>
<span data-ttu-id="fdcfc-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fdcfc-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fdcfc-113">-PoolName</span><span class="sxs-lookup"><span data-stu-id="fdcfc-113">-ElasticPoolName</span></span>
<span data-ttu-id="fdcfc-114">Der Name des Azure SQL Pool pool.</span><span class="sxs-lookup"><span data-stu-id="fdcfc-114">The name of the Azure SQL Elastic Pool.</span></span>

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

### <span data-ttu-id="fdcfc-115">-OperationId</span><span class="sxs-lookup"><span data-stu-id="fdcfc-115">-OperationId</span></span>
<span data-ttu-id="fdcfc-116">Die ID des abzurufende Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="fdcfc-116">The ID of the operation to retrieve.</span></span>

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

### <span data-ttu-id="fdcfc-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fdcfc-117">-PassThru</span></span>
<span data-ttu-id="fdcfc-118">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="fdcfc-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="fdcfc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdcfc-119">-ResourceGroupName</span></span>
<span data-ttu-id="fdcfc-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="fdcfc-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="fdcfc-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fdcfc-121">-ServerName</span></span>
<span data-ttu-id="fdcfc-122">Der Name des Azure SQL Server, in dem sich der Pool "Pool" befindet.</span><span class="sxs-lookup"><span data-stu-id="fdcfc-122">The name of the Azure SQL Server the Elastic Pool is in.</span></span>

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

### <span data-ttu-id="fdcfc-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fdcfc-123">-Confirm</span></span>
<span data-ttu-id="fdcfc-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fdcfc-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fdcfc-125">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="fdcfc-125">-WhatIf</span></span>
<span data-ttu-id="fdcfc-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fdcfc-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fdcfc-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fdcfc-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fdcfc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdcfc-128">CommonParameters</span></span>
<span data-ttu-id="fdcfc-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdcfc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdcfc-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fdcfc-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdcfc-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fdcfc-131">INPUTS</span></span>

### <span data-ttu-id="fdcfc-132">System.String</span><span class="sxs-lookup"><span data-stu-id="fdcfc-132">System.String</span></span>

### <span data-ttu-id="fdcfc-133">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="fdcfc-133">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="fdcfc-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fdcfc-134">OUTPUTS</span></span>

### <span data-ttu-id="fdcfc-135">Microsoft.Azure.Commands.Sql.Pool.Model.AzureSqlElasticPoolActivityModel</span><span class="sxs-lookup"><span data-stu-id="fdcfc-135">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span></span>

## <span data-ttu-id="fdcfc-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fdcfc-136">NOTES</span></span>

## <span data-ttu-id="fdcfc-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fdcfc-137">RELATED LINKS</span></span>
