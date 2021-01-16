---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerinstance/get-azcontainerinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Get-AzContainerInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Get-AzContainerInstanceLog.md
ms.openlocfilehash: d279e5c08b43640d629e4146faf306d0e85482a8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98295936"
---
# <span data-ttu-id="0ba86-101">Get-AzContainerInstanceLog</span><span class="sxs-lookup"><span data-stu-id="0ba86-101">Get-AzContainerInstanceLog</span></span>

## <span data-ttu-id="0ba86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ba86-102">SYNOPSIS</span></span>
<span data-ttu-id="0ba86-103">Sie können die Protokolle einer Containerinstanz in einer Containergruppe erhalten.</span><span class="sxs-lookup"><span data-stu-id="0ba86-103">Get the logs of a container instance in a container group.</span></span>

## <span data-ttu-id="0ba86-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0ba86-104">SYNTAX</span></span>

### <span data-ttu-id="0ba86-105">GetContainerInstanceLogByNamesParamSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="0ba86-105">GetContainerInstanceLogByNamesParamSet (Default)</span></span>
```
Get-AzContainerInstanceLog [-ResourceGroupName] <String> -ContainerGroupName <String> [-Name <String>]
 [-Tail <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ba86-106">GetContainerInstanceLogByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="0ba86-106">GetContainerInstanceLogByPSContainerGroupParamSet</span></span>
```
Get-AzContainerInstanceLog -InputContainerGroup <PSContainerGroup> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ba86-107">GetContainerInstanceLogByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="0ba86-107">GetContainerInstanceLogByResourceIdParamSet</span></span>
```
Get-AzContainerInstanceLog -ResourceId <String> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ba86-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0ba86-108">DESCRIPTION</span></span>
<span data-ttu-id="0ba86-109">Das **Cmdlet "Get-AzContainerInstanceLog"** ruft die Protokolle eines Containers in einer Containergruppe ab.</span><span class="sxs-lookup"><span data-stu-id="0ba86-109">The **Get-AzContainerInstanceLog** cmdlet gets the logs of a container in a container group.</span></span>

## <span data-ttu-id="0ba86-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0ba86-110">EXAMPLES</span></span>

### <span data-ttu-id="0ba86-111">Beispiel 1: Das Tailprotokoll einer Containerinstanz erhalten</span><span class="sxs-lookup"><span data-stu-id="0ba86-111">Example 1: Get the tail log of a container instance</span></span>
```
PS C:\> Get-AzContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="0ba86-112">Das Protokoll aus der `container1` Containergruppe `mycontainer` erhalten.</span><span class="sxs-lookup"><span data-stu-id="0ba86-112">Get the log from `container1` in container group `mycontainer`.</span></span> <span data-ttu-id="0ba86-113">Standardmäßig werden bis zu 4 MB Protokollinhalt angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0ba86-113">By default, it will return up to 4MB log content.</span></span>

### <span data-ttu-id="0ba86-114">Beispiel 2: Das Tailprotokoll einer Containerinstanz mit demselben Namen wie die Containergruppe erhalten</span><span class="sxs-lookup"><span data-stu-id="0ba86-114">Example 2: Get the tail log of a container instance that has the same name as the container group</span></span>
```
PS C:\> Get-AzContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="0ba86-115">Das Protokoll aus der `mycontainer` Containergruppe `mycontainer` erhalten.</span><span class="sxs-lookup"><span data-stu-id="0ba86-115">Get the log from `mycontainer` in container group `mycontainer`.</span></span> <span data-ttu-id="0ba86-116">Standardmäßig werden bis zu 4 MB Protokollinhalt angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0ba86-116">By default, it will return up to 4MB log content.</span></span>

### <span data-ttu-id="0ba86-117">Beispiel 3: Erhalten der zwei Zeilen des Protokolls einer Containerinstanz</span><span class="sxs-lookup"><span data-stu-id="0ba86-117">Example 3: Get the tail 2 lines of log of a container instance</span></span>
```
PS C:\> Get-AzContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1 -Tail 2

Log line 3.
Log line 4.
```

<span data-ttu-id="0ba86-118">Holen Sie sich die zwei Protokollzeilen aus der `container1` Gruppe "In Container". `mycontainer`</span><span class="sxs-lookup"><span data-stu-id="0ba86-118">Get the tail 2 lines of log from `container1` in container group `mycontainer`.</span></span>

### <span data-ttu-id="0ba86-119">Beispiel 4: Get the tail log of a container instance in a piped in container group</span><span class="sxs-lookup"><span data-stu-id="0ba86-119">Example 4: Get the tail log of a container instance in a piped in container group</span></span>
```
PS C:\> Get-AzContainerGroup -ResourceGroupName demo -Name mycontainer | Get-AzContainerInstanceLog

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="0ba86-120">Das Protokoll aus der `mycontainer` Gruppe "In Piped in Container" `mycontainer` erhalten.</span><span class="sxs-lookup"><span data-stu-id="0ba86-120">Get the log from `mycontainer` in piped in container group `mycontainer`.</span></span> <span data-ttu-id="0ba86-121">Standardmäßig werden bis zu 4 MB Protokollinhalt angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0ba86-121">By default, it will return up to 4MB log content.</span></span>

## <span data-ttu-id="0ba86-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0ba86-122">PARAMETERS</span></span>

### <span data-ttu-id="0ba86-123">-ContainerGroupName</span><span class="sxs-lookup"><span data-stu-id="0ba86-123">-ContainerGroupName</span></span>
<span data-ttu-id="0ba86-124">Der Containergruppenname.</span><span class="sxs-lookup"><span data-stu-id="0ba86-124">The container group name.</span></span>

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

### <span data-ttu-id="0ba86-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ba86-125">-DefaultProfile</span></span>
<span data-ttu-id="0ba86-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0ba86-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ba86-127">-InputContainerGroup</span><span class="sxs-lookup"><span data-stu-id="0ba86-127">-InputContainerGroup</span></span>
<span data-ttu-id="0ba86-128">Das Gruppenobjekt des Eingabecontainers.</span><span class="sxs-lookup"><span data-stu-id="0ba86-128">The input container group object.</span></span>

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

### <span data-ttu-id="0ba86-129">-Name</span><span class="sxs-lookup"><span data-stu-id="0ba86-129">-Name</span></span>
<span data-ttu-id="0ba86-130">Der Containerinstanzname in der Containergruppe.</span><span class="sxs-lookup"><span data-stu-id="0ba86-130">The container instance name in the container group.</span></span>
<span data-ttu-id="0ba86-131">Standard: identisch mit dem Namen der Containergruppe</span><span class="sxs-lookup"><span data-stu-id="0ba86-131">Default: the same as the container group name</span></span>

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

### <span data-ttu-id="0ba86-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ba86-132">-ResourceGroupName</span></span>
<span data-ttu-id="0ba86-133">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0ba86-133">The resource group name.</span></span>

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

### <span data-ttu-id="0ba86-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0ba86-134">-ResourceId</span></span>
<span data-ttu-id="0ba86-135">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="0ba86-135">The resource id.</span></span>

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

### <span data-ttu-id="0ba86-136">-Tail</span><span class="sxs-lookup"><span data-stu-id="0ba86-136">-Tail</span></span>
<span data-ttu-id="0ba86-137">Die Anzahl der Zeilen, mit der das Protokoll enden soll.</span><span class="sxs-lookup"><span data-stu-id="0ba86-137">The number of lines to tail the log.</span></span>
<span data-ttu-id="0ba86-138">Ist dies nicht angegeben, gibt das Cmdlet bis zu 4 MB langes Protokoll zurück.</span><span class="sxs-lookup"><span data-stu-id="0ba86-138">If not specify, the cmdlet will return up to 4MB tailed log</span></span>

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

### <span data-ttu-id="0ba86-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ba86-139">CommonParameters</span></span>
<span data-ttu-id="0ba86-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ba86-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ba86-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ba86-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ba86-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0ba86-142">INPUTS</span></span>

### <span data-ttu-id="0ba86-143">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="0ba86-143">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

### <span data-ttu-id="0ba86-144">System.String</span><span class="sxs-lookup"><span data-stu-id="0ba86-144">System.String</span></span>

## <span data-ttu-id="0ba86-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0ba86-145">OUTPUTS</span></span>

### <span data-ttu-id="0ba86-146">System.String</span><span class="sxs-lookup"><span data-stu-id="0ba86-146">System.String</span></span>

## <span data-ttu-id="0ba86-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0ba86-147">NOTES</span></span>

## <span data-ttu-id="0ba86-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0ba86-148">RELATED LINKS</span></span>
