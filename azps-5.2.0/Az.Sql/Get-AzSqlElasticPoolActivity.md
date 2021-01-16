---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 0DB0B08A-F948-4F6E-9CF0-2FB5DD5064D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpoolactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolActivity.md
ms.openlocfilehash: 2e0768b14337f4504df1e6cdf9565533584e0339
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360673"
---
# <span data-ttu-id="bc86e-101">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="bc86e-101">Get-AzSqlElasticPoolActivity</span></span>

## <span data-ttu-id="bc86e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc86e-102">SYNOPSIS</span></span>
<span data-ttu-id="bc86e-103">Ruft den Status von Vorgängen in einem Pool mit Gängen ab.</span><span class="sxs-lookup"><span data-stu-id="bc86e-103">Gets the status of operations on an elastic pool.</span></span>

## <span data-ttu-id="bc86e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bc86e-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolActivity [-ServerName] <String> [-ElasticPoolName] <String> [-OperationId <Guid>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bc86e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bc86e-105">DESCRIPTION</span></span>
<span data-ttu-id="bc86e-106">Das **Cmdlet "Get-AzSqlElasticPoolActivity"** ruft den Status von Vorgängen in einem Pool für ein Azure SQL ab.</span><span class="sxs-lookup"><span data-stu-id="bc86e-106">The **Get-AzSqlElasticPoolActivity** cmdlet gets the status of operations on an elastic pool for an Azure SQL Database.</span></span>
<span data-ttu-id="bc86e-107">Sie können den Status von Poolerstellungs- und Konfigurationsupdates sehen.</span><span class="sxs-lookup"><span data-stu-id="bc86e-107">You can see the status of both pool creation and configuration updates.</span></span>

## <span data-ttu-id="bc86e-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bc86e-108">EXAMPLES</span></span>

### <span data-ttu-id="bc86e-109">Beispiel 1: Anzeigen des Status von Vorgängen für einen Pool mit Pool</span><span class="sxs-lookup"><span data-stu-id="bc86e-109">Example 1: Get the status of operations for an elastic pool</span></span>
```
PS C:\>Get-AzSqlElasticPoolActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="bc86e-110">Dieser Befehl ruft den Status der Vorgänge für den Pool mit dem Namen "PoolsPool01" ab.</span><span class="sxs-lookup"><span data-stu-id="bc86e-110">This command gets the status of the operations for the elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="bc86e-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bc86e-111">PARAMETERS</span></span>

### <span data-ttu-id="bc86e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc86e-112">-DefaultProfile</span></span>
<span data-ttu-id="bc86e-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="bc86e-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bc86e-114">-PoolName</span><span class="sxs-lookup"><span data-stu-id="bc86e-114">-ElasticPoolName</span></span>
<span data-ttu-id="bc86e-115">Gibt den Namen eines Poolpools an.</span><span class="sxs-lookup"><span data-stu-id="bc86e-115">Specifies the name of an elastic pool.</span></span>

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

### <span data-ttu-id="bc86e-116">-OperationId</span><span class="sxs-lookup"><span data-stu-id="bc86e-116">-OperationId</span></span>
<span data-ttu-id="bc86e-117">Die ID des abzurufende Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="bc86e-117">The ID of the operation to retrieve.</span></span>

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

### <span data-ttu-id="bc86e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc86e-118">-ResourceGroupName</span></span>
<span data-ttu-id="bc86e-119">Gibt den Namen einer Ressourcengruppe an, der der Pool "Pool" zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="bc86e-119">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="bc86e-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="bc86e-120">-ServerName</span></span>
<span data-ttu-id="bc86e-121">Gibt den Namen eines Servers an, der einen Pool mit Pools enthält.</span><span class="sxs-lookup"><span data-stu-id="bc86e-121">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="bc86e-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bc86e-122">-Confirm</span></span>
<span data-ttu-id="bc86e-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bc86e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc86e-124">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="bc86e-124">-WhatIf</span></span>
<span data-ttu-id="bc86e-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bc86e-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc86e-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bc86e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc86e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc86e-127">CommonParameters</span></span>
<span data-ttu-id="bc86e-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc86e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc86e-129">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bc86e-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc86e-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bc86e-130">INPUTS</span></span>

### <span data-ttu-id="bc86e-131">System.String</span><span class="sxs-lookup"><span data-stu-id="bc86e-131">System.String</span></span>

### <span data-ttu-id="bc86e-132">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="bc86e-132">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="bc86e-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bc86e-133">OUTPUTS</span></span>

### <span data-ttu-id="bc86e-134">Microsoft.Azure.Commands.Sql.Pool.Model.AzureSqlElasticPoolActivityModel</span><span class="sxs-lookup"><span data-stu-id="bc86e-134">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span></span>

## <span data-ttu-id="bc86e-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="bc86e-135">NOTES</span></span>

## <span data-ttu-id="bc86e-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="bc86e-136">RELATED LINKS</span></span>

[<span data-ttu-id="bc86e-137">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="bc86e-137">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="bc86e-138">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="bc86e-138">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="bc86e-139">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="bc86e-139">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="bc86e-140">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="bc86e-140">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="bc86e-141">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="bc86e-141">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)


