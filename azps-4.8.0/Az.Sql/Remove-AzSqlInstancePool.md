---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstancePool.md
ms.openlocfilehash: b10187938613f9ab6e0c12cb0d83162450be8445
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173435"
---
# <span data-ttu-id="213b9-101">Remove-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="213b9-101">Remove-AzSqlInstancePool</span></span>

## <span data-ttu-id="213b9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="213b9-102">SYNOPSIS</span></span>
<span data-ttu-id="213b9-103">Entfernt einen Azure SQL-Instanzen Pool.</span><span class="sxs-lookup"><span data-stu-id="213b9-103">Removes an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="213b9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="213b9-104">SYNTAX</span></span>

### <span data-ttu-id="213b9-105">DeleteByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="213b9-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSqlInstancePool [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="213b9-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="213b9-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSqlInstancePool [-InputObject] <AzureSqlInstancePoolModel> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="213b9-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="213b9-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSqlInstancePool [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="213b9-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="213b9-108">DESCRIPTION</span></span>
<span data-ttu-id="213b9-109">Mit dem Cmdlet **Remove-AzSqlInstancePool** wird ein Azure SQL-Instanzen Pool entfernt.</span><span class="sxs-lookup"><span data-stu-id="213b9-109">The **Remove-AzSqlInstancePool** cmdlet removes an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="213b9-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="213b9-110">EXAMPLES</span></span>

### <span data-ttu-id="213b9-111">Beispiel 1: Entfernen eines Instanzen Pools</span><span class="sxs-lookup"><span data-stu-id="213b9-111">Example 1: Remove an instance pool</span></span>
```powershell
PS C:\> Remove-AzSqlInstancePool -ResourceGroup resourcegroup01 -Name instancePool0
```

### <span data-ttu-id="213b9-112">Beispiel 2: Entfernen eines Instanzen Pools anhand des Ressourcenbezeichners</span><span class="sxs-lookup"><span data-stu-id="213b9-112">Example 2: Remove an instance pool by its resource identifier</span></span>
```powershell
PS C:\> Remove-AzSqlInstancePool -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0"
```

### <span data-ttu-id="213b9-113">Beispiel 3: Entfernen eines Instanzen Pools durch ein Instanzen Pool Objekt</span><span class="sxs-lookup"><span data-stu-id="213b9-113">Example 3: Remove an instance pool by an instance pool object</span></span>
```powershell
PS C:\> Get-AzSqlInstancePool -ResourceGroup resourcegroup01 -Name instancePool0
PS C:\> Remove-AzSqlInstancePool -InputObject $instancePool
```

<span data-ttu-id="213b9-114">Dieser Befehl entfernt einen Instanz Pool mit dem Namen instancePool0.</span><span class="sxs-lookup"><span data-stu-id="213b9-114">This command removes an instance pool named instancePool0.</span></span>

## <span data-ttu-id="213b9-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="213b9-115">PARAMETERS</span></span>

### <span data-ttu-id="213b9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="213b9-116">-DefaultProfile</span></span>
<span data-ttu-id="213b9-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="213b9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="213b9-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="213b9-118">-InputObject</span></span>
<span data-ttu-id="213b9-119">Das zu entfernende Instanz Pool-Objekt.</span><span class="sxs-lookup"><span data-stu-id="213b9-119">The instance pool object to remove.</span></span>

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

### <span data-ttu-id="213b9-120">-Name</span><span class="sxs-lookup"><span data-stu-id="213b9-120">-Name</span></span>
<span data-ttu-id="213b9-121">Der Name des Instanzen Pools.</span><span class="sxs-lookup"><span data-stu-id="213b9-121">The name of the instance pool.</span></span>

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

### <span data-ttu-id="213b9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="213b9-122">-ResourceGroupName</span></span>
<span data-ttu-id="213b9-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="213b9-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="213b9-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="213b9-124">-ResourceId</span></span>
<span data-ttu-id="213b9-125">Die zu entfernende Ressourcen-ID des Instanzen Pools.</span><span class="sxs-lookup"><span data-stu-id="213b9-125">The instance pool resource id to remove.</span></span>

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

### <span data-ttu-id="213b9-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="213b9-126">-Confirm</span></span>
<span data-ttu-id="213b9-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="213b9-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="213b9-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="213b9-128">-WhatIf</span></span>
<span data-ttu-id="213b9-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="213b9-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="213b9-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="213b9-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="213b9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="213b9-131">CommonParameters</span></span>
<span data-ttu-id="213b9-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="213b9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="213b9-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="213b9-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="213b9-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="213b9-134">INPUTS</span></span>

### <span data-ttu-id="213b9-135">Microsoft.Azure.Commands.SQL.Instance_Pools. Model. AzureSqlInstancePoolModel</span><span class="sxs-lookup"><span data-stu-id="213b9-135">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span></span>

### <span data-ttu-id="213b9-136">System. String</span><span class="sxs-lookup"><span data-stu-id="213b9-136">System.String</span></span>

## <span data-ttu-id="213b9-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="213b9-137">OUTPUTS</span></span>

### <span data-ttu-id="213b9-138">System. Object</span><span class="sxs-lookup"><span data-stu-id="213b9-138">System.Object</span></span>
## <span data-ttu-id="213b9-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="213b9-139">NOTES</span></span>

## <span data-ttu-id="213b9-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="213b9-140">RELATED LINKS</span></span>
