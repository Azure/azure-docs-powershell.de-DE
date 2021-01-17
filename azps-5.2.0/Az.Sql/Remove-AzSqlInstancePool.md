---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstancePool.md
ms.openlocfilehash: b10187938613f9ab6e0c12cb0d83162450be8445
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369548"
---
# <span data-ttu-id="ce8e7-101">Remove-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="ce8e7-101">Remove-AzSqlInstancePool</span></span>

## <span data-ttu-id="ce8e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce8e7-102">SYNOPSIS</span></span>
<span data-ttu-id="ce8e7-103">Entfernt einen Azure SQL-Instanzpool.</span><span class="sxs-lookup"><span data-stu-id="ce8e7-103">Removes an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="ce8e7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ce8e7-104">SYNTAX</span></span>

### <span data-ttu-id="ce8e7-105">DeleteByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ce8e7-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSqlInstancePool [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce8e7-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce8e7-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSqlInstancePool [-InputObject] <AzureSqlInstancePoolModel> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce8e7-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce8e7-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSqlInstancePool [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ce8e7-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ce8e7-108">DESCRIPTION</span></span>
<span data-ttu-id="ce8e7-109">Das **Cmdlet "Remove-AzSqlInstancePool"** entfernt einen Azure SQL-Instanzpool.</span><span class="sxs-lookup"><span data-stu-id="ce8e7-109">The **Remove-AzSqlInstancePool** cmdlet removes an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="ce8e7-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ce8e7-110">EXAMPLES</span></span>

### <span data-ttu-id="ce8e7-111">Beispiel 1: Entfernen eines Instanzpools</span><span class="sxs-lookup"><span data-stu-id="ce8e7-111">Example 1: Remove an instance pool</span></span>
```powershell
PS C:\> Remove-AzSqlInstancePool -ResourceGroup resourcegroup01 -Name instancePool0
```

### <span data-ttu-id="ce8e7-112">Beispiel 2: Entfernen eines Instanzpools durch dessen Ressourcenbezeichner</span><span class="sxs-lookup"><span data-stu-id="ce8e7-112">Example 2: Remove an instance pool by its resource identifier</span></span>
```powershell
PS C:\> Remove-AzSqlInstancePool -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0"
```

### <span data-ttu-id="ce8e7-113">Beispiel 3: Entfernen eines Instanzpools durch ein Instanzpoolobjekt</span><span class="sxs-lookup"><span data-stu-id="ce8e7-113">Example 3: Remove an instance pool by an instance pool object</span></span>
```powershell
PS C:\> Get-AzSqlInstancePool -ResourceGroup resourcegroup01 -Name instancePool0
PS C:\> Remove-AzSqlInstancePool -InputObject $instancePool
```

<span data-ttu-id="ce8e7-114">Mit diesem Befehl wird ein Instanzpool namens "instancePool0" entfernt.</span><span class="sxs-lookup"><span data-stu-id="ce8e7-114">This command removes an instance pool named instancePool0.</span></span>

## <span data-ttu-id="ce8e7-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ce8e7-115">PARAMETERS</span></span>

### <span data-ttu-id="ce8e7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce8e7-116">-DefaultProfile</span></span>
<span data-ttu-id="ce8e7-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ce8e7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce8e7-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ce8e7-118">-InputObject</span></span>
<span data-ttu-id="ce8e7-119">Das zu entfernende Instanzpoolobjekt.</span><span class="sxs-lookup"><span data-stu-id="ce8e7-119">The instance pool object to remove.</span></span>

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

### <span data-ttu-id="ce8e7-120">-Name</span><span class="sxs-lookup"><span data-stu-id="ce8e7-120">-Name</span></span>
<span data-ttu-id="ce8e7-121">Der Name des Instanzpools.</span><span class="sxs-lookup"><span data-stu-id="ce8e7-121">The name of the instance pool.</span></span>

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

### <span data-ttu-id="ce8e7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce8e7-122">-ResourceGroupName</span></span>
<span data-ttu-id="ce8e7-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ce8e7-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="ce8e7-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ce8e7-124">-ResourceId</span></span>
<span data-ttu-id="ce8e7-125">Die zu entfernende Ressourcen-ID des Instanzpools.</span><span class="sxs-lookup"><span data-stu-id="ce8e7-125">The instance pool resource id to remove.</span></span>

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

### <span data-ttu-id="ce8e7-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ce8e7-126">-Confirm</span></span>
<span data-ttu-id="ce8e7-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ce8e7-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce8e7-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ce8e7-128">-WhatIf</span></span>
<span data-ttu-id="ce8e7-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ce8e7-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce8e7-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ce8e7-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce8e7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce8e7-131">CommonParameters</span></span>
<span data-ttu-id="ce8e7-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce8e7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce8e7-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ce8e7-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce8e7-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ce8e7-134">INPUTS</span></span>

### <span data-ttu-id="ce8e7-135">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span><span class="sxs-lookup"><span data-stu-id="ce8e7-135">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span></span>

### <span data-ttu-id="ce8e7-136">System.String</span><span class="sxs-lookup"><span data-stu-id="ce8e7-136">System.String</span></span>

## <span data-ttu-id="ce8e7-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ce8e7-137">OUTPUTS</span></span>

### <span data-ttu-id="ce8e7-138">System.Object</span><span class="sxs-lookup"><span data-stu-id="ce8e7-138">System.Object</span></span>
## <span data-ttu-id="ce8e7-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ce8e7-139">NOTES</span></span>

## <span data-ttu-id="ce8e7-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ce8e7-140">RELATED LINKS</span></span>
