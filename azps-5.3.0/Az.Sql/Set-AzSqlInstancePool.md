---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstancePool.md
ms.openlocfilehash: db7d9165b8aec6a69f31850f7a37eddb2450e53b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468055"
---
# <span data-ttu-id="1aa45-101">Set-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="1aa45-101">Set-AzSqlInstancePool</span></span>

## <span data-ttu-id="1aa45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1aa45-102">SYNOPSIS</span></span>
<span data-ttu-id="1aa45-103">Legt Eigenschaften für einen Azure SQL-Instanzpool fest.</span><span class="sxs-lookup"><span data-stu-id="1aa45-103">Sets properties for an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="1aa45-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1aa45-104">SYNTAX</span></span>

### <span data-ttu-id="1aa45-105">DefaultSetInstancePoolParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="1aa45-105">DefaultSetInstancePoolParameterSet (Default)</span></span>
```
Set-AzSqlInstancePool [-ResourceGroupName] <String> [-Name] <String> [-LicenseType <String>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1aa45-106">InputObjectSetInstancePoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="1aa45-106">InputObjectSetInstancePoolParameterSet</span></span>
```
Set-AzSqlInstancePool [-InputObject] <AzureSqlInstancePoolModel> [-LicenseType <String>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1aa45-107">ResourceIdSetInstancePoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="1aa45-107">ResourceIdSetInstancePoolParameterSet</span></span>
```
Set-AzSqlInstancePool [-ResourceId] <String> [-LicenseType <String>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1aa45-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1aa45-108">DESCRIPTION</span></span>
<span data-ttu-id="1aa45-109">Das **Cmdlet "Set-AzSqlInstancePool"** ändert die Eigenschaften eines Azure SQL-Instanzpools.</span><span class="sxs-lookup"><span data-stu-id="1aa45-109">The **Set-AzSqlInstancePool** cmdlet modifies properties of an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="1aa45-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1aa45-110">EXAMPLES</span></span>

### <span data-ttu-id="1aa45-111">Beispiel 1: Festlegen eines Instanzpoollizenztyps</span><span class="sxs-lookup"><span data-stu-id="1aa45-111">Example 1 : Set an instance pool license type</span></span>
```powershell
PS C:\> Set-AzSqlInstancePool -ResourceGroupName resourcegroup01 -Name instancePool0 -LicenseType LicenseIncluded
ResourceGroupName : resourcegroup01
Type              : Microsoft.Sql/instancePools
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0
InstancePoolName  : instancePool0
SubnetId          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
VCores            : 8
ComputeGeneration : Gen5
Edition           : GeneralPurpose
Tags              :
Sku               : Microsoft.Azure.Management.Sql.Models.Sku
Location          : canadacentral
LicenseType       : LicenseIncluded
```

<span data-ttu-id="1aa45-112">Dieser Befehl legt den Lizenztyp und/oder Tags für einen Instanzpool namens "instancePool0" fest.</span><span class="sxs-lookup"><span data-stu-id="1aa45-112">This command sets the license type and/or tags for an instance pool named instancePool0.</span></span>

### <span data-ttu-id="1aa45-113">Beispiel 2: Festlegen eines Instanzpoollizenztyps mithilfe eines Instanzpoolobjekts</span><span class="sxs-lookup"><span data-stu-id="1aa45-113">Example 2 : Set an instance pool license type using an instance pool object</span></span>
```powershell
PS C:\> $instancePool = Get-AzSqlInstancePool -ResourceGroupName resourcegroup01 -Name instancePool0
PS C:\> Set-AzSqlInstancePool -InputObject $instancePool -LicenseType LicenseIncluded
ResourceGroupName : resourcegroup01
Type              : Microsoft.Sql/instancePools
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0
InstancePoolName  : instancePool0
SubnetId          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
VCores            : 8
ComputeGeneration : Gen5
Edition           : GeneralPurpose
Tags              :
Sku               : Microsoft.Azure.Management.Sql.Models.Sku
Location          : canadacentral
LicenseType       : LicenseIncluded
```

<span data-ttu-id="1aa45-114">Dieser Befehl legt den Lizenztyp und/oder Tags für einen Instanzpool mithilfe eines Instanzpoolobjekts fest.</span><span class="sxs-lookup"><span data-stu-id="1aa45-114">This command sets the license type and/or tags for an instance pool using an instance pool object.</span></span>

### <span data-ttu-id="1aa45-115">Beispiel 3: Festlegen eines Instanzpoollizenztyps mithilfe einer Ressourcen-ID des Instanzpools</span><span class="sxs-lookup"><span data-stu-id="1aa45-115">Example 3 : Set an instance pool license type using an instance pool resource id</span></span>
```powershell
PS C:\> Set-AzSqlInstancePool -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0" -LicenseType LicenseIncluded
ResourceGroupName : resourcegroup01
Type              : Microsoft.Sql/instancePools
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0
InstancePoolName  : instancePool0
SubnetId          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
VCores            : 8
ComputeGeneration : Gen5
Edition           : GeneralPurpose
Tags              :
Sku               : Microsoft.Azure.Management.Sql.Models.Sku
Location          : canadacentral
LicenseType       : LicenseIncluded
```

<span data-ttu-id="1aa45-116">Dieser Befehl legt den Lizenztyp und/oder Tags für einen Instanzpool namens "instancePool0" fest.</span><span class="sxs-lookup"><span data-stu-id="1aa45-116">This command sets the license type and/or tags for an instance pool named instancePool0.</span></span>

## <span data-ttu-id="1aa45-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1aa45-117">PARAMETERS</span></span>

### <span data-ttu-id="1aa45-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1aa45-118">-AsJob</span></span>
<span data-ttu-id="1aa45-119">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="1aa45-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1aa45-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1aa45-120">-DefaultProfile</span></span>
<span data-ttu-id="1aa45-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1aa45-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1aa45-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1aa45-122">-InputObject</span></span>
<span data-ttu-id="1aa45-123">Das Eingabeobjekt des Instanzpools.</span><span class="sxs-lookup"><span data-stu-id="1aa45-123">The instance pool input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel
Parameter Sets: InputObjectSetInstancePoolParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1aa45-124">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="1aa45-124">-LicenseType</span></span>
<span data-ttu-id="1aa45-125">Bestimmt, welcher Lizenztyp verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1aa45-125">Determines which License Type to use.</span></span>
<span data-ttu-id="1aa45-126">Mögliche Werte sind "BasePrice" (mit AHB-Rabatt) und "LicenseIncluded" (ohne AHB-Rabatt).</span><span class="sxs-lookup"><span data-stu-id="1aa45-126">Possible values are BasePrice (with AHB discount) and LicenseIncluded (without AHB discount).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1aa45-127">-Name</span><span class="sxs-lookup"><span data-stu-id="1aa45-127">-Name</span></span>
<span data-ttu-id="1aa45-128">Der Name des Instanzpools.</span><span class="sxs-lookup"><span data-stu-id="1aa45-128">The name of the instance pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSetInstancePoolParameterSet
Aliases: InstancePoolName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1aa45-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1aa45-129">-ResourceGroupName</span></span>
<span data-ttu-id="1aa45-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1aa45-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSetInstancePoolParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1aa45-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1aa45-131">-ResourceId</span></span>
<span data-ttu-id="1aa45-132">Der Ressourcenbezeichner des Instanzpools.</span><span class="sxs-lookup"><span data-stu-id="1aa45-132">The instance pool resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSetInstancePoolParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1aa45-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="1aa45-133">-Tag</span></span>
<span data-ttu-id="1aa45-134">Die Tags, die der Instanz zugeordnet werden sollen</span><span class="sxs-lookup"><span data-stu-id="1aa45-134">The tags to associate with the instance</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1aa45-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1aa45-135">-Confirm</span></span>
<span data-ttu-id="1aa45-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1aa45-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1aa45-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="1aa45-137">-WhatIf</span></span>
<span data-ttu-id="1aa45-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1aa45-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1aa45-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1aa45-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1aa45-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1aa45-140">CommonParameters</span></span>
<span data-ttu-id="1aa45-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1aa45-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1aa45-142">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1aa45-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1aa45-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1aa45-143">INPUTS</span></span>

### <span data-ttu-id="1aa45-144">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span><span class="sxs-lookup"><span data-stu-id="1aa45-144">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span></span>

### <span data-ttu-id="1aa45-145">System.String</span><span class="sxs-lookup"><span data-stu-id="1aa45-145">System.String</span></span>

## <span data-ttu-id="1aa45-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1aa45-146">OUTPUTS</span></span>

### <span data-ttu-id="1aa45-147">System.Object</span><span class="sxs-lookup"><span data-stu-id="1aa45-147">System.Object</span></span>
## <span data-ttu-id="1aa45-148">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1aa45-148">NOTES</span></span>

## <span data-ttu-id="1aa45-149">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1aa45-149">RELATED LINKS</span></span>
