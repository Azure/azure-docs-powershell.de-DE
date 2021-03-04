---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstancePool.md
ms.openlocfilehash: 0a7874079b7de782fa7471e9087f04fdc3a9e754
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926320"
---
# <span data-ttu-id="f4579-101">Remove-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="f4579-101">Remove-AzSqlInstancePool</span></span>

## <span data-ttu-id="f4579-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4579-102">SYNOPSIS</span></span>
<span data-ttu-id="f4579-103">Entfernt einen Azure SQL-Instanzpool.</span><span class="sxs-lookup"><span data-stu-id="f4579-103">Removes an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="f4579-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f4579-104">SYNTAX</span></span>

### <span data-ttu-id="f4579-105">DeleteByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f4579-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSqlInstancePool [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4579-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4579-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSqlInstancePool [-InputObject] <AzureSqlInstancePoolModel> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4579-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4579-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSqlInstancePool [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f4579-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f4579-108">DESCRIPTION</span></span>
<span data-ttu-id="f4579-109">Das **Cmdlet Remove-AzSqlInstancePool** entfernt einen Azure SQL-Instanz-Pool.</span><span class="sxs-lookup"><span data-stu-id="f4579-109">The **Remove-AzSqlInstancePool** cmdlet removes an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="f4579-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f4579-110">EXAMPLES</span></span>

### <span data-ttu-id="f4579-111">Beispiel 1: Entfernen eines Instanzpools</span><span class="sxs-lookup"><span data-stu-id="f4579-111">Example 1: Remove an instance pool</span></span>
```powershell
PS C:\> Remove-AzSqlInstancePool -ResourceGroup resourcegroup01 -Name instancePool0
```

### <span data-ttu-id="f4579-112">Beispiel 2: Entfernen eines Instanzpools nach dem Ressourcenbezeichner</span><span class="sxs-lookup"><span data-stu-id="f4579-112">Example 2: Remove an instance pool by its resource identifier</span></span>
```powershell
PS C:\> Remove-AzSqlInstancePool -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0"
```

### <span data-ttu-id="f4579-113">Beispiel 3: Entfernen eines Instanzpools durch ein Instanzpoolobjekt</span><span class="sxs-lookup"><span data-stu-id="f4579-113">Example 3: Remove an instance pool by an instance pool object</span></span>
```powershell
PS C:\> Get-AzSqlInstancePool -ResourceGroup resourcegroup01 -Name instancePool0
PS C:\> Remove-AzSqlInstancePool -InputObject $instancePool
```

<span data-ttu-id="f4579-114">Mit diesem Befehl wird ein Instanzpool mit dem Namen "instancePool0" entfernt.</span><span class="sxs-lookup"><span data-stu-id="f4579-114">This command removes an instance pool named instancePool0.</span></span>

## <span data-ttu-id="f4579-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f4579-115">PARAMETERS</span></span>

### <span data-ttu-id="f4579-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4579-116">-DefaultProfile</span></span>
<span data-ttu-id="f4579-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f4579-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4579-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4579-118">-InputObject</span></span>
<span data-ttu-id="f4579-119">Das zu entfernende Instanzpoolobjekt.</span><span class="sxs-lookup"><span data-stu-id="f4579-119">The instance pool object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4579-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f4579-120">-Name</span></span>
<span data-ttu-id="f4579-121">Der Name des Instanzpools.</span><span class="sxs-lookup"><span data-stu-id="f4579-121">The name of the instance pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: InstancePoolName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4579-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4579-122">-ResourceGroupName</span></span>
<span data-ttu-id="f4579-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f4579-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4579-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4579-124">-ResourceId</span></span>
<span data-ttu-id="f4579-125">Die zu entfernende Ressourcen-ID des Instanzpools.</span><span class="sxs-lookup"><span data-stu-id="f4579-125">The instance pool resource id to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4579-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f4579-126">-Confirm</span></span>
<span data-ttu-id="f4579-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f4579-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4579-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4579-128">-WhatIf</span></span>
<span data-ttu-id="f4579-129">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f4579-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4579-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f4579-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4579-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4579-131">CommonParameters</span></span>
<span data-ttu-id="f4579-132">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4579-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4579-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f4579-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4579-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f4579-134">INPUTS</span></span>

### <span data-ttu-id="f4579-135">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span><span class="sxs-lookup"><span data-stu-id="f4579-135">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span></span>

### <span data-ttu-id="f4579-136">System.String</span><span class="sxs-lookup"><span data-stu-id="f4579-136">System.String</span></span>

## <span data-ttu-id="f4579-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f4579-137">OUTPUTS</span></span>

### <span data-ttu-id="f4579-138">System.Object</span><span class="sxs-lookup"><span data-stu-id="f4579-138">System.Object</span></span>
## <span data-ttu-id="f4579-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f4579-139">NOTES</span></span>

## <span data-ttu-id="f4579-140">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f4579-140">RELATED LINKS</span></span>
