---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesPool.md
ms.openlocfilehash: e1ebab6e0b32c6358defee30512185868581b6e7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359930"
---
# <span data-ttu-id="b6f9a-101">New-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="b6f9a-101">New-AzNetAppFilesPool</span></span>

## <span data-ttu-id="b6f9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6f9a-102">SYNOPSIS</span></span>
<span data-ttu-id="b6f9a-103">Erstellt einen neuen Azure NetApp Files (ANF)-Pool.</span><span class="sxs-lookup"><span data-stu-id="b6f9a-103">Creates a new Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="b6f9a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b6f9a-104">SYNTAX</span></span>

### <span data-ttu-id="b6f9a-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b6f9a-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesPool -ResourceGroupName <String> -Location <String> -AccountName <String> -Name <String>
 -PoolSize <Int64> -ServiceLevel <String> [-QosType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6f9a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6f9a-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesPool -Name <String> -PoolSize <Int64> -ServiceLevel <String> [-QosType <String>]
 [-Tag <Hashtable>] -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6f9a-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b6f9a-107">DESCRIPTION</span></span>
<span data-ttu-id="b6f9a-108">Das **Cmdlet "New-AzNetAppFilesPool"** erstellt einen ANF-Pool.</span><span class="sxs-lookup"><span data-stu-id="b6f9a-108">The **New-AzNetAppFilesPool** cmdlet creates an ANF pool.</span></span>

## <span data-ttu-id="b6f9a-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b6f9a-109">EXAMPLES</span></span>

### <span data-ttu-id="b6f9a-110">Beispiel 1: Erstellen eines ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="b6f9a-110">Example 1: Create an ANF pool</span></span>
```
PS C:\>New-AzNetAppFilesPool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MyAnfPool" -l "westus2" -PoolSize 4398046511104 -ServiceLevel "Premium" -QosType "Auto"

Output:

Location          : westus2
Id                : /subscriptions/subsID/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool
Name              : MyAnfAccount/MyAnfPool
Type              : Microsoft.NetApp/netAppAccounts/capacityPools
Tags              :
PoolId            : a3a53a09-fd70-37ab-39dc-392a04cba525
Size              : 4398046511104
ServiceLevel      : Premium
TotalThroughputMibps: 262.144
UtilizedThroughputMibps: 164.221
QosType           : Auto
ProvisioningState : Succeeded
```

<span data-ttu-id="b6f9a-111">Mit diesem Befehl wird der neue ANF-Pool "MyAnfPool" im Konto "MyAnfAccount" erstellt.</span><span class="sxs-lookup"><span data-stu-id="b6f9a-111">This command creates the new ANF pool "MyAnfPool" within the account "MyAnfAccount".</span></span>

## <span data-ttu-id="b6f9a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b6f9a-112">PARAMETERS</span></span>

### <span data-ttu-id="b6f9a-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b6f9a-113">-AccountName</span></span>
<span data-ttu-id="b6f9a-114">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="b6f9a-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="b6f9a-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="b6f9a-115">-AccountObject</span></span>
<span data-ttu-id="b6f9a-116">Das Konto für das neue Poolobjekt</span><span class="sxs-lookup"><span data-stu-id="b6f9a-116">The account for the new pool object</span></span>

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

### <span data-ttu-id="b6f9a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6f9a-117">-DefaultProfile</span></span>
<span data-ttu-id="b6f9a-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b6f9a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6f9a-119">-Location</span><span class="sxs-lookup"><span data-stu-id="b6f9a-119">-Location</span></span>
<span data-ttu-id="b6f9a-120">Der Speicherort der Ressource</span><span class="sxs-lookup"><span data-stu-id="b6f9a-120">The location of the resource</span></span>

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

### <span data-ttu-id="b6f9a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b6f9a-121">-Name</span></span>
<span data-ttu-id="b6f9a-122">Der Name des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="b6f9a-122">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6f9a-123">-PoolSize</span><span class="sxs-lookup"><span data-stu-id="b6f9a-123">-PoolSize</span></span>
<span data-ttu-id="b6f9a-124">Die Größe des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="b6f9a-124">The size of the ANF pool</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6f9a-125">-QosType</span><span class="sxs-lookup"><span data-stu-id="b6f9a-125">-QosType</span></span>
<span data-ttu-id="b6f9a-126">Der qos-Typ des Pools.</span><span class="sxs-lookup"><span data-stu-id="b6f9a-126">The qos type of the pool.</span></span> <span data-ttu-id="b6f9a-127">Mögliche Werte sind: "Auto", "Manuell".</span><span class="sxs-lookup"><span data-stu-id="b6f9a-127">Possible values include: 'Auto', 'Manual'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Auto
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6f9a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6f9a-128">-ResourceGroupName</span></span>
<span data-ttu-id="b6f9a-129">Die Ressourcengruppe des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="b6f9a-129">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="b6f9a-130">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="b6f9a-130">-ServiceLevel</span></span>
<span data-ttu-id="b6f9a-131">Der Dienstlevel des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="b6f9a-131">The service level of the ANF pool</span></span>

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

### <span data-ttu-id="b6f9a-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="b6f9a-132">-Tag</span></span>
<span data-ttu-id="b6f9a-133">Eine Hashtable, die Ressourcentags darstellt</span><span class="sxs-lookup"><span data-stu-id="b6f9a-133">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="b6f9a-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b6f9a-134">-Confirm</span></span>
<span data-ttu-id="b6f9a-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b6f9a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6f9a-136">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b6f9a-136">-WhatIf</span></span>
<span data-ttu-id="b6f9a-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b6f9a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6f9a-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b6f9a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6f9a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6f9a-139">CommonParameters</span></span>
<span data-ttu-id="b6f9a-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6f9a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6f9a-141">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b6f9a-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6f9a-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b6f9a-142">INPUTS</span></span>

### <span data-ttu-id="b6f9a-143">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="b6f9a-143">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="b6f9a-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b6f9a-144">OUTPUTS</span></span>

### <span data-ttu-id="b6f9a-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="b6f9a-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="b6f9a-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b6f9a-146">NOTES</span></span>

## <span data-ttu-id="b6f9a-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b6f9a-147">RELATED LINKS</span></span>
