---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/powershell/module/az.containerinstance/get-azcontainerinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Get-AzContainerInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Get-AzContainerInstanceLog.md
ms.openlocfilehash: 2ab0102534a8773ca1ca206bde2075e2bd7930f4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948744"
---
# <span data-ttu-id="7e1c7-101">Get-AzContainerInstanceLog</span><span class="sxs-lookup"><span data-stu-id="7e1c7-101">Get-AzContainerInstanceLog</span></span>

## <span data-ttu-id="7e1c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e1c7-102">SYNOPSIS</span></span>
<span data-ttu-id="7e1c7-103">Holen Sie sich die Protokolle einer Containerinstanz in einer Containergruppe.</span><span class="sxs-lookup"><span data-stu-id="7e1c7-103">Get the logs of a container instance in a container group.</span></span>

## <span data-ttu-id="7e1c7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7e1c7-104">SYNTAX</span></span>

### <span data-ttu-id="7e1c7-105">GetContainerInstanceLogByNamesParamSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="7e1c7-105">GetContainerInstanceLogByNamesParamSet (Default)</span></span>
```
Get-AzContainerInstanceLog [-ResourceGroupName] <String> -ContainerGroupName <String> [-Name <String>]
 [-Tail <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e1c7-106">GetContainerInstanceLogByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="7e1c7-106">GetContainerInstanceLogByPSContainerGroupParamSet</span></span>
```
Get-AzContainerInstanceLog -InputContainerGroup <PSContainerGroup> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e1c7-107">GetContainerInstanceLogByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="7e1c7-107">GetContainerInstanceLogByResourceIdParamSet</span></span>
```
Get-AzContainerInstanceLog -ResourceId <String> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e1c7-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7e1c7-108">DESCRIPTION</span></span>
<span data-ttu-id="7e1c7-109">Das **Get-AzContainerInstanceLog-Cmdlet** ruft die Protokolle eines Containers in einer Containergruppe ab.</span><span class="sxs-lookup"><span data-stu-id="7e1c7-109">The **Get-AzContainerInstanceLog** cmdlet gets the logs of a container in a container group.</span></span>

## <span data-ttu-id="7e1c7-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7e1c7-110">EXAMPLES</span></span>

### <span data-ttu-id="7e1c7-111">Beispiel 1: Das Endprotokoll einer Containerinstanz</span><span class="sxs-lookup"><span data-stu-id="7e1c7-111">Example 1: Get the tail log of a container instance</span></span>
```
PS C:\> Get-AzContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="7e1c7-112">Holen Sie sich das Protokoll `container1` aus der Containergruppe `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="7e1c7-112">Get the log from `container1` in container group `mycontainer`.</span></span> <span data-ttu-id="7e1c7-113">Standardmäßig gibt es bis zu 4 MB Protokollinhalt zurück.</span><span class="sxs-lookup"><span data-stu-id="7e1c7-113">By default, it will return up to 4MB log content.</span></span>

### <span data-ttu-id="7e1c7-114">Beispiel 2: Das Endprotokoll einer Containerinstanz mit demselben Namen wie die Containergruppe</span><span class="sxs-lookup"><span data-stu-id="7e1c7-114">Example 2: Get the tail log of a container instance that has the same name as the container group</span></span>
```
PS C:\> Get-AzContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="7e1c7-115">Holen Sie sich das Protokoll `mycontainer` aus der Containergruppe `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="7e1c7-115">Get the log from `mycontainer` in container group `mycontainer`.</span></span> <span data-ttu-id="7e1c7-116">Standardmäßig gibt es bis zu 4 MB Protokollinhalt zurück.</span><span class="sxs-lookup"><span data-stu-id="7e1c7-116">By default, it will return up to 4MB log content.</span></span>

### <span data-ttu-id="7e1c7-117">Beispiel 3: Holen Sie sich die 2-Zeilen des Protokolls einer Containerinstanz</span><span class="sxs-lookup"><span data-stu-id="7e1c7-117">Example 3: Get the tail 2 lines of log of a container instance</span></span>
```
PS C:\> Get-AzContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1 -Tail 2

Log line 3.
Log line 4.
```

<span data-ttu-id="7e1c7-118">Holen Sie sich die zwei Zeilen des Protokolls aus `container1` der Containergruppe `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="7e1c7-118">Get the tail 2 lines of log from `container1` in container group `mycontainer`.</span></span>

### <span data-ttu-id="7e1c7-119">Beispiel 4: Das Endprotokoll einer Containerinstanz in einer In-Container-Gruppe pipedieren</span><span class="sxs-lookup"><span data-stu-id="7e1c7-119">Example 4: Get the tail log of a container instance in a piped in container group</span></span>
```
PS C:\> Get-AzContainerGroup -ResourceGroupName demo -Name mycontainer | Get-AzContainerInstanceLog

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="7e1c7-120">Holen Sie sich das Protokoll `mycontainer` von in piped in container group `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="7e1c7-120">Get the log from `mycontainer` in piped in container group `mycontainer`.</span></span> <span data-ttu-id="7e1c7-121">Standardmäßig gibt es bis zu 4 MB Protokollinhalt zurück.</span><span class="sxs-lookup"><span data-stu-id="7e1c7-121">By default, it will return up to 4MB log content.</span></span>

## <span data-ttu-id="7e1c7-122">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="7e1c7-122">PARAMETERS</span></span>

### <span data-ttu-id="7e1c7-123">-ContainerGroupName</span><span class="sxs-lookup"><span data-stu-id="7e1c7-123">-ContainerGroupName</span></span>
<span data-ttu-id="7e1c7-124">Der Name der Containergruppe.</span><span class="sxs-lookup"><span data-stu-id="7e1c7-124">The container group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetContainerInstanceLogByNamesParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e1c7-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e1c7-125">-DefaultProfile</span></span>
<span data-ttu-id="7e1c7-126">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7e1c7-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e1c7-127">-InputContainerGroup</span><span class="sxs-lookup"><span data-stu-id="7e1c7-127">-InputContainerGroup</span></span>
<span data-ttu-id="7e1c7-128">Das Gruppenobjekt des Eingabecontainers.</span><span class="sxs-lookup"><span data-stu-id="7e1c7-128">The input container group object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup
Parameter Sets: GetContainerInstanceLogByPSContainerGroupParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e1c7-129">-Name</span><span class="sxs-lookup"><span data-stu-id="7e1c7-129">-Name</span></span>
<span data-ttu-id="7e1c7-130">Der Name der Containerinstanz in der Containergruppe.</span><span class="sxs-lookup"><span data-stu-id="7e1c7-130">The container instance name in the container group.</span></span>
<span data-ttu-id="7e1c7-131">Standard: identisch mit dem Namen der Containergruppe</span><span class="sxs-lookup"><span data-stu-id="7e1c7-131">Default: the same as the container group name</span></span>

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

### <span data-ttu-id="7e1c7-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e1c7-132">-ResourceGroupName</span></span>
<span data-ttu-id="7e1c7-133">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7e1c7-133">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetContainerInstanceLogByNamesParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e1c7-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7e1c7-134">-ResourceId</span></span>
<span data-ttu-id="7e1c7-135">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="7e1c7-135">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetContainerInstanceLogByResourceIdParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e1c7-136">-Tail</span><span class="sxs-lookup"><span data-stu-id="7e1c7-136">-Tail</span></span>
<span data-ttu-id="7e1c7-137">Die Anzahl der Zeilen, die das Protokoll schweifen soll.</span><span class="sxs-lookup"><span data-stu-id="7e1c7-137">The number of lines to tail the log.</span></span>
<span data-ttu-id="7e1c7-138">Wenn nicht angegeben, gibt das Cmdlet bis zu 4 MB tailed log zurück.</span><span class="sxs-lookup"><span data-stu-id="7e1c7-138">If not specify, the cmdlet will return up to 4MB tailed log</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e1c7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e1c7-139">CommonParameters</span></span>
<span data-ttu-id="7e1c7-140">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e1c7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e1c7-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e1c7-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e1c7-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7e1c7-142">INPUTS</span></span>

### <span data-ttu-id="7e1c7-143">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="7e1c7-143">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

### <span data-ttu-id="7e1c7-144">System.String</span><span class="sxs-lookup"><span data-stu-id="7e1c7-144">System.String</span></span>

## <span data-ttu-id="7e1c7-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7e1c7-145">OUTPUTS</span></span>

### <span data-ttu-id="7e1c7-146">System.String</span><span class="sxs-lookup"><span data-stu-id="7e1c7-146">System.String</span></span>

## <span data-ttu-id="7e1c7-147">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="7e1c7-147">NOTES</span></span>

## <span data-ttu-id="7e1c7-148">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="7e1c7-148">RELATED LINKS</span></span>
