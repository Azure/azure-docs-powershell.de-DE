---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstancePool.md
ms.openlocfilehash: 1b4f405e9bf6377855439d1f6d3cad9f0538920f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008848"
---
# <span data-ttu-id="39b3f-101">New-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="39b3f-101">New-AzSqlInstancePool</span></span>

## <span data-ttu-id="39b3f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="39b3f-102">SYNOPSIS</span></span>
<span data-ttu-id="39b3f-103">Erstellt einen Azure SQL-Instanzen Pool.</span><span class="sxs-lookup"><span data-stu-id="39b3f-103">Creates an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="39b3f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="39b3f-104">SYNTAX</span></span>

```
New-AzSqlInstancePool [-ResourceGroupName] <String> [-Name] <String> -Location <String> -SubnetId <String>
 -VCore <Int32> -Edition <String> -ComputeGeneration <String> -LicenseType <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39b3f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="39b3f-105">DESCRIPTION</span></span>
<span data-ttu-id="39b3f-106">Das Cmdlet **New-AzSqlInstancePool** erstellt einen Azure SQL-Instanzen Pool.</span><span class="sxs-lookup"><span data-stu-id="39b3f-106">The **New-AzSqlInstancePool** cmdlet creates an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="39b3f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="39b3f-107">EXAMPLES</span></span>

### <span data-ttu-id="39b3f-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="39b3f-108">Example 1</span></span>
```powershell
PS C:\> New-AzSqlInstancePool -ResourceGroupName resourcegroup01 -Name instancepool0 -Location canadacentral -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -VCore 8 -Edition GeneralPurpose -ComputeGeneration Gen5 -LicenseType LicenseIncluded
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

<span data-ttu-id="39b3f-109">Dieser Befehl erstellt einen neuen Azure SQL-Instanzen Pool.</span><span class="sxs-lookup"><span data-stu-id="39b3f-109">This command creates a new Azure SQL Instance pool.</span></span>

## <span data-ttu-id="39b3f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="39b3f-110">PARAMETERS</span></span>

### <span data-ttu-id="39b3f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="39b3f-111">-AsJob</span></span>
<span data-ttu-id="39b3f-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="39b3f-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="39b3f-113">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="39b3f-113">-ComputeGeneration</span></span>
<span data-ttu-id="39b3f-114">Die COMPUTE-Generierung für den Instanzen Pool.</span><span class="sxs-lookup"><span data-stu-id="39b3f-114">The compute generation for the instance pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39b3f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39b3f-115">-DefaultProfile</span></span>
<span data-ttu-id="39b3f-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="39b3f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39b3f-117">-Edition</span><span class="sxs-lookup"><span data-stu-id="39b3f-117">-Edition</span></span>
<span data-ttu-id="39b3f-118">Die Edition für den Instanzen Pool.</span><span class="sxs-lookup"><span data-stu-id="39b3f-118">The edition for the instance pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39b3f-119">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="39b3f-119">-LicenseType</span></span>
<span data-ttu-id="39b3f-120">Bestimmt den zu verwendenden Lizenztyp.</span><span class="sxs-lookup"><span data-stu-id="39b3f-120">Determines which License Type to use.</span></span>
<span data-ttu-id="39b3f-121">Mögliche Werte sind Grundpr. (mit AHB-Rabatt) und LicenseIncluded (ohne AHB-Rabatt).</span><span class="sxs-lookup"><span data-stu-id="39b3f-121">Possible values are BasePrice (with AHB discount) and LicenseIncluded (without AHB discount).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39b3f-122">-Standort</span><span class="sxs-lookup"><span data-stu-id="39b3f-122">-Location</span></span>
<span data-ttu-id="39b3f-123">Der Speicherort, an dem der Instanz Pool erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="39b3f-123">The location to create the instance pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39b3f-124">-Name</span><span class="sxs-lookup"><span data-stu-id="39b3f-124">-Name</span></span>
<span data-ttu-id="39b3f-125">Der Name des Instanzen Pools.</span><span class="sxs-lookup"><span data-stu-id="39b3f-125">The name of the instance pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstancePoolName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39b3f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39b3f-126">-ResourceGroupName</span></span>
<span data-ttu-id="39b3f-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="39b3f-127">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39b3f-128">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="39b3f-128">-SubnetId</span></span>
<span data-ttu-id="39b3f-129">Die zu verwendende Subnetz-ID für die Erstellung von Instanzen Pools.</span><span class="sxs-lookup"><span data-stu-id="39b3f-129">The subnet id to use for instance pool creation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39b3f-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="39b3f-130">-Tag</span></span>
<span data-ttu-id="39b3f-131">Die Tags, die der Instanz zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="39b3f-131">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="39b3f-132">-VCore</span><span class="sxs-lookup"><span data-stu-id="39b3f-132">-VCore</span></span>
<span data-ttu-id="39b3f-133">Bestimmt, wie viel Vcore mit instance verknüpft werden soll.</span><span class="sxs-lookup"><span data-stu-id="39b3f-133">Determines how much VCore to associate with instance.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: VCores

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39b3f-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="39b3f-134">-Confirm</span></span>
<span data-ttu-id="39b3f-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="39b3f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39b3f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39b3f-136">-WhatIf</span></span>
<span data-ttu-id="39b3f-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="39b3f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39b3f-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="39b3f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39b3f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39b3f-139">CommonParameters</span></span>
<span data-ttu-id="39b3f-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39b3f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39b3f-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="39b3f-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39b3f-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="39b3f-142">INPUTS</span></span>

### <span data-ttu-id="39b3f-143">Keine</span><span class="sxs-lookup"><span data-stu-id="39b3f-143">None</span></span>

## <span data-ttu-id="39b3f-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="39b3f-144">OUTPUTS</span></span>

### <span data-ttu-id="39b3f-145">System. Object</span><span class="sxs-lookup"><span data-stu-id="39b3f-145">System.Object</span></span>
## <span data-ttu-id="39b3f-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="39b3f-146">NOTES</span></span>

## <span data-ttu-id="39b3f-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="39b3f-147">RELATED LINKS</span></span>
