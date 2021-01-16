---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqlelasticpoolactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticPoolActivity.md
ms.openlocfilehash: dc1dffd84a95bd9cffac1dbafb5183d56e0b7c52
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98300424"
---
# <span data-ttu-id="588b5-101">Stop-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="588b5-101">Stop-AzSqlElasticPoolActivity</span></span>

## <span data-ttu-id="588b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="588b5-102">SYNOPSIS</span></span>
<span data-ttu-id="588b5-103">Bricht den asynchronen Aktualisierungsvorgang für einen Pool mit Drosselung ab.</span><span class="sxs-lookup"><span data-stu-id="588b5-103">Cancels the asynchronous update operation on an elastic pool.</span></span>

## <span data-ttu-id="588b5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="588b5-104">SYNTAX</span></span>

```
Stop-AzSqlElasticPoolActivity [-PassThru] [-ServerName] <String> [-ElasticPoolName] <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="588b5-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="588b5-105">DESCRIPTION</span></span>
<span data-ttu-id="588b5-106">Das **Cmdlet "Stop-AzSqlElasticPoolActivity"** bricht den asynchronen Aktualisierungsvorgang für einen Pool aus.</span><span class="sxs-lookup"><span data-stu-id="588b5-106">The **Stop-AzSqlElasticPoolActivity** cmdlet cancels the asynchronous update operation on an elastic pool.</span></span>

## <span data-ttu-id="588b5-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="588b5-107">EXAMPLES</span></span>

### <span data-ttu-id="588b5-108">Beispiel 1: Abbrechen des asynchronen Aktualisierungsvorgangs für einen Pool</span><span class="sxs-lookup"><span data-stu-id="588b5-108">Example 1: Cancel the asynchronous update operation on an elastic pool</span></span>
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

<span data-ttu-id="588b5-109">Dieser Befehl bricht den Vorgang für asynchrone Updates im Pool ab.</span><span class="sxs-lookup"><span data-stu-id="588b5-109">This command cancels the asynchronous updates operation on the elastic pool.</span></span>

## <span data-ttu-id="588b5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="588b5-110">PARAMETERS</span></span>

### <span data-ttu-id="588b5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="588b5-111">-DefaultProfile</span></span>
<span data-ttu-id="588b5-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="588b5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="588b5-113">-PoolName</span><span class="sxs-lookup"><span data-stu-id="588b5-113">-ElasticPoolName</span></span>
<span data-ttu-id="588b5-114">Der Name des Azure SQL Pool pool.</span><span class="sxs-lookup"><span data-stu-id="588b5-114">The name of the Azure SQL Elastic Pool.</span></span>

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

### <span data-ttu-id="588b5-115">-OperationId</span><span class="sxs-lookup"><span data-stu-id="588b5-115">-OperationId</span></span>
<span data-ttu-id="588b5-116">Die ID des abzurufende Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="588b5-116">The ID of the operation to retrieve.</span></span>

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

### <span data-ttu-id="588b5-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="588b5-117">-PassThru</span></span>
<span data-ttu-id="588b5-118">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="588b5-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="588b5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="588b5-119">-ResourceGroupName</span></span>
<span data-ttu-id="588b5-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="588b5-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="588b5-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="588b5-121">-ServerName</span></span>
<span data-ttu-id="588b5-122">Der Name des Azure SQL Server, in dem sich der Pool "Pool" befindet.</span><span class="sxs-lookup"><span data-stu-id="588b5-122">The name of the Azure SQL Server the Elastic Pool is in.</span></span>

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

### <span data-ttu-id="588b5-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="588b5-123">-Confirm</span></span>
<span data-ttu-id="588b5-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="588b5-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="588b5-125">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="588b5-125">-WhatIf</span></span>
<span data-ttu-id="588b5-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="588b5-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="588b5-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="588b5-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="588b5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="588b5-128">CommonParameters</span></span>
<span data-ttu-id="588b5-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="588b5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="588b5-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="588b5-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="588b5-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="588b5-131">INPUTS</span></span>

### <span data-ttu-id="588b5-132">System.String</span><span class="sxs-lookup"><span data-stu-id="588b5-132">System.String</span></span>

### <span data-ttu-id="588b5-133">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="588b5-133">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="588b5-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="588b5-134">OUTPUTS</span></span>

### <span data-ttu-id="588b5-135">Microsoft.Azure.Commands.Sql.Pool.Model.AzureSqlElasticPoolActivityModel</span><span class="sxs-lookup"><span data-stu-id="588b5-135">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span></span>

## <span data-ttu-id="588b5-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="588b5-136">NOTES</span></span>

## <span data-ttu-id="588b5-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="588b5-137">RELATED LINKS</span></span>
