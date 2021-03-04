---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/update-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
ms.openlocfilehash: e8b367b724a4310eb5a3ed76bcf02e8538299845
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926672"
---
# <span data-ttu-id="22d5e-101">Update-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="22d5e-101">Update-AzNetAppFilesPool</span></span>

## <span data-ttu-id="22d5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22d5e-102">SYNOPSIS</span></span>
<span data-ttu-id="22d5e-103">Aktualisiert einen Azure NetApp Files (ANF)-Pool entsprechend den optionalen Modifizierern, die bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="22d5e-103">Updates an Azure NetApp Files (ANF) pool according to the optional modifiers provided.</span></span>

## <span data-ttu-id="22d5e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="22d5e-104">SYNTAX</span></span>

### <span data-ttu-id="22d5e-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="22d5e-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesPool -ResourceGroupName <String> [-Location <String>] -AccountName <String> -Name <String>
 [-PoolSize <Int64>] [-QosType <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22d5e-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="22d5e-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool -Name <String> [-PoolSize <Int64>] [-QosType <String>] [-Tag <Hashtable>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="22d5e-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="22d5e-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesPool [-PoolSize <Int64>] [-QosType <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22d5e-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="22d5e-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool [-PoolSize <Int64>] [-QosType <String>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="22d5e-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="22d5e-109">DESCRIPTION</span></span>
<span data-ttu-id="22d5e-110">Das **Update-AzNetAppFilesPool-Cmdlet** ändert einen ANF-Pool.</span><span class="sxs-lookup"><span data-stu-id="22d5e-110">The **Update-AzNetAppFilesPool** cmdlet modifies an ANF pool.</span></span>

## <span data-ttu-id="22d5e-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="22d5e-111">EXAMPLES</span></span>

### <span data-ttu-id="22d5e-112">Beispiel 1: Ändern eines ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="22d5e-112">Example 1: Modify an ANF pool</span></span>
```
PS C:\>Update-AzNetAppFilesPool -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -PoolSize 4398046511104 -QosType "Auto"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool
Name              : MyAnfAccount/MyAnfPool
Type              : Microsoft.NetApp/netAppAccounts/capacityPools
Tags              :
PoolId            : 9fa2ca6d-1e48-4439-30e3-7de056e44e5a
Size              : 4398046511104
ServiceLevel      : Standard
QosType           : Auto
ProvisioningState : Succeeded
```

<span data-ttu-id="22d5e-113">Mit diesem Befehl wird der ANF-Pool "MyAnfPool" so geändert, dass er die angegebene Größe und QosType hat.</span><span class="sxs-lookup"><span data-stu-id="22d5e-113">This command changes the ANF pool "MyAnfPool" to have the given size and QosType.</span></span>

## <span data-ttu-id="22d5e-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="22d5e-114">PARAMETERS</span></span>

### <span data-ttu-id="22d5e-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="22d5e-115">-AccountName</span></span>
<span data-ttu-id="22d5e-116">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="22d5e-116">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22d5e-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="22d5e-117">-AccountObject</span></span>
<span data-ttu-id="22d5e-118">Das Kontoobjekt, das den zu aktualisierenden Pool enthält</span><span class="sxs-lookup"><span data-stu-id="22d5e-118">The account object containing the pool to update</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="22d5e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22d5e-119">-DefaultProfile</span></span>
<span data-ttu-id="22d5e-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="22d5e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22d5e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="22d5e-121">-InputObject</span></span>
<span data-ttu-id="22d5e-122">Das zu aktualisierende Poolobjekt</span><span class="sxs-lookup"><span data-stu-id="22d5e-122">The pool object to update</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="22d5e-123">-Location</span><span class="sxs-lookup"><span data-stu-id="22d5e-123">-Location</span></span>
<span data-ttu-id="22d5e-124">Der Speicherort der Ressource</span><span class="sxs-lookup"><span data-stu-id="22d5e-124">The location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22d5e-125">-Name</span><span class="sxs-lookup"><span data-stu-id="22d5e-125">-Name</span></span>
<span data-ttu-id="22d5e-126">Der Name des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="22d5e-126">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: PoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22d5e-127">-PoolSize</span><span class="sxs-lookup"><span data-stu-id="22d5e-127">-PoolSize</span></span>
<span data-ttu-id="22d5e-128">Die Größe des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="22d5e-128">The size of the ANF pool</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22d5e-129">-QosType</span><span class="sxs-lookup"><span data-stu-id="22d5e-129">-QosType</span></span>
<span data-ttu-id="22d5e-130">Der qos-Typ des Pools.</span><span class="sxs-lookup"><span data-stu-id="22d5e-130">The qos type of the pool.</span></span> <span data-ttu-id="22d5e-131">Mögliche Werte sind: "Auto", "Manuell"</span><span class="sxs-lookup"><span data-stu-id="22d5e-131">Possible values include: 'Auto', 'Manual'</span></span>

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

### <span data-ttu-id="22d5e-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22d5e-132">-ResourceGroupName</span></span>
<span data-ttu-id="22d5e-133">Die Ressourcengruppe des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="22d5e-133">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22d5e-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="22d5e-134">-ResourceId</span></span>
<span data-ttu-id="22d5e-135">Die Ressourcen-ID des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="22d5e-135">The resource id of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22d5e-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="22d5e-136">-Tag</span></span>
<span data-ttu-id="22d5e-137">Eine Hashtable, die Ressourcentags darstellt</span><span class="sxs-lookup"><span data-stu-id="22d5e-137">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="22d5e-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="22d5e-138">-Confirm</span></span>
<span data-ttu-id="22d5e-139">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="22d5e-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22d5e-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22d5e-140">-WhatIf</span></span>
<span data-ttu-id="22d5e-141">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="22d5e-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22d5e-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="22d5e-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22d5e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22d5e-143">CommonParameters</span></span>
<span data-ttu-id="22d5e-144">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22d5e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22d5e-145">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="22d5e-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22d5e-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="22d5e-146">INPUTS</span></span>

### <span data-ttu-id="22d5e-147">System.String</span><span class="sxs-lookup"><span data-stu-id="22d5e-147">System.String</span></span>

### <span data-ttu-id="22d5e-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="22d5e-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="22d5e-149">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="22d5e-149">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="22d5e-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="22d5e-150">OUTPUTS</span></span>

### <span data-ttu-id="22d5e-151">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="22d5e-151">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="22d5e-152">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="22d5e-152">NOTES</span></span>

## <span data-ttu-id="22d5e-153">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="22d5e-153">RELATED LINKS</span></span>
