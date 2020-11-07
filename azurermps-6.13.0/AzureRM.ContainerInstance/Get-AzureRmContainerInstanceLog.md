---
external help file: Microsoft.Azure.Commands.ContainerInstance.dll-Help.xml
Module Name: AzureRM.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerinstance/get-azurermcontainerinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Get-AzureRmContainerInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Get-AzureRmContainerInstanceLog.md
ms.openlocfilehash: 08a4ab0f0d937f06ee0ac958aa57a2f0eed5e4a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662184"
---
# <span data-ttu-id="ee602-101">Get-AzureRmContainerInstanceLog</span><span class="sxs-lookup"><span data-stu-id="ee602-101">Get-AzureRmContainerInstanceLog</span></span>

## <span data-ttu-id="ee602-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ee602-102">SYNOPSIS</span></span>
<span data-ttu-id="ee602-103">Rufen Sie die Protokolle einer Containerinstanz in einer Containergruppe ab.</span><span class="sxs-lookup"><span data-stu-id="ee602-103">Get the logs of a container instance in a container group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee602-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ee602-104">SYNTAX</span></span>

### <span data-ttu-id="ee602-105">GetContainerInstanceLogByNamesParamSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ee602-105">GetContainerInstanceLogByNamesParamSet (Default)</span></span>
```
Get-AzureRmContainerInstanceLog [-ResourceGroupName] <String> -ContainerGroupName <String> [-Name <String>]
 [-Tail <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ee602-106">GetContainerInstanceLogByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="ee602-106">GetContainerInstanceLogByPSContainerGroupParamSet</span></span>
```
Get-AzureRmContainerInstanceLog -InputContainerGroup <PSContainerGroup> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ee602-107">GetContainerInstanceLogByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="ee602-107">GetContainerInstanceLogByResourceIdParamSet</span></span>
```
Get-AzureRmContainerInstanceLog -ResourceId <String> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee602-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ee602-108">DESCRIPTION</span></span>
<span data-ttu-id="ee602-109">Das Cmdlet " **Get-AzureRmContainerInstanceLog** " Ruft die Protokolle eines Containers in einer Containergruppe ab.</span><span class="sxs-lookup"><span data-stu-id="ee602-109">The **Get-AzureRmContainerInstanceLog** cmdlet gets the logs of a container in a container group.</span></span>

## <span data-ttu-id="ee602-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ee602-110">EXAMPLES</span></span>

### <span data-ttu-id="ee602-111">Beispiel 1: Abrufen des Tail-Protokolls einer Containerinstanz</span><span class="sxs-lookup"><span data-stu-id="ee602-111">Example 1: Get the tail log of a container instance</span></span>
```
PS C:\> Get-AzureRmContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="ee602-112">Rufen Sie das Protokoll `container1` in der Containergruppe ab `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="ee602-112">Get the log from `container1` in container group `mycontainer`.</span></span> <span data-ttu-id="ee602-113">Standardmäßig werden bis zu 4MB Protokollinhalte zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ee602-113">By default, it will return up to 4MB log content.</span></span>

### <span data-ttu-id="ee602-114">Beispiel 2: Abrufen des Tail-Protokolls einer Containerinstanz mit dem gleichen Namen wie die Containergruppe</span><span class="sxs-lookup"><span data-stu-id="ee602-114">Example 2: Get the tail log of a container instance that has the same name as the container group</span></span>
```
PS C:\> Get-AzureRmContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="ee602-115">Rufen Sie das Protokoll `mycontainer` in der Containergruppe ab `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="ee602-115">Get the log from `mycontainer` in container group `mycontainer`.</span></span> <span data-ttu-id="ee602-116">Standardmäßig werden bis zu 4MB Protokollinhalte zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ee602-116">By default, it will return up to 4MB log content.</span></span>

### <span data-ttu-id="ee602-117">Beispiel 3: Abrufen des Tail 2-Protokollzeilen einer Containerinstanz</span><span class="sxs-lookup"><span data-stu-id="ee602-117">Example 3: Get the tail 2 lines of log of a container instance</span></span>
```
PS C:\> Get-AzureRmContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1 -Tail 2

Log line 3.
Log line 4.
```

<span data-ttu-id="ee602-118">Besorgen Sie sich die Tail 2-Zeilen des Protokolls `container1` in der Containergruppe `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="ee602-118">Get the tail 2 lines of log from `container1` in container group `mycontainer`.</span></span>

### <span data-ttu-id="ee602-119">Beispiel 4: Abrufen des Tail-Protokolls einer Containerinstanz in einer Pipeline in einer Containergruppe</span><span class="sxs-lookup"><span data-stu-id="ee602-119">Example 4: Get the tail log of a container instance in a piped in container group</span></span>
```
PS C:\> Get-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer | Get-AzureRmContainerInstanceLog

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="ee602-120">Rufen Sie das Protokoll `mycontainer` in der Containergruppe ab `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="ee602-120">Get the log from `mycontainer` in piped in container group `mycontainer`.</span></span> <span data-ttu-id="ee602-121">Standardmäßig werden bis zu 4MB Protokollinhalte zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ee602-121">By default, it will return up to 4MB log content.</span></span>

## <span data-ttu-id="ee602-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="ee602-122">PARAMETERS</span></span>

### <span data-ttu-id="ee602-123">-ContainerGroupName</span><span class="sxs-lookup"><span data-stu-id="ee602-123">-ContainerGroupName</span></span>
<span data-ttu-id="ee602-124">Der Name der Containergruppe.</span><span class="sxs-lookup"><span data-stu-id="ee602-124">The container group name.</span></span>

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

### <span data-ttu-id="ee602-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee602-125">-DefaultProfile</span></span>
<span data-ttu-id="ee602-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ee602-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee602-127">-InputContainerGroup</span><span class="sxs-lookup"><span data-stu-id="ee602-127">-InputContainerGroup</span></span>
<span data-ttu-id="ee602-128">Das Gruppenobjekt "Eingabe Container".</span><span class="sxs-lookup"><span data-stu-id="ee602-128">The input container group object.</span></span>

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

### <span data-ttu-id="ee602-129">-Name</span><span class="sxs-lookup"><span data-stu-id="ee602-129">-Name</span></span>
<span data-ttu-id="ee602-130">Der Name der Containerinstanz in der Containergruppe.</span><span class="sxs-lookup"><span data-stu-id="ee602-130">The container instance name in the container group.</span></span>
<span data-ttu-id="ee602-131">Standard: identisch mit dem Namen der Containergruppe</span><span class="sxs-lookup"><span data-stu-id="ee602-131">Default: the same as the container group name</span></span>

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

### <span data-ttu-id="ee602-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee602-132">-ResourceGroupName</span></span>
<span data-ttu-id="ee602-133">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ee602-133">The resource group name.</span></span>

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

### <span data-ttu-id="ee602-134">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="ee602-134">-ResourceId</span></span>
<span data-ttu-id="ee602-135">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="ee602-135">The resource id.</span></span>

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

### <span data-ttu-id="ee602-136">-Tail</span><span class="sxs-lookup"><span data-stu-id="ee602-136">-Tail</span></span>
<span data-ttu-id="ee602-137">Die Anzahl der Zeilen, die das Protokoll abschweifen sollen.</span><span class="sxs-lookup"><span data-stu-id="ee602-137">The number of lines to tail the log.</span></span>
<span data-ttu-id="ee602-138">Wenn nicht angegeben, gibt das Cmdlet bis zu 4MB-tailed-Protokoll zurück.</span><span class="sxs-lookup"><span data-stu-id="ee602-138">If not specify, the cmdlet will return up to 4MB tailed log</span></span>

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

### <span data-ttu-id="ee602-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee602-139">CommonParameters</span></span>
<span data-ttu-id="ee602-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee602-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee602-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee602-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee602-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ee602-142">INPUTS</span></span>

### <span data-ttu-id="ee602-143">Microsoft. Azure. Commands. ContainerInstance. Models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="ee602-143">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>
<span data-ttu-id="ee602-144">Parameter: InputContainerGroup (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ee602-144">Parameters: InputContainerGroup (ByValue)</span></span>

### <span data-ttu-id="ee602-145">System. String</span><span class="sxs-lookup"><span data-stu-id="ee602-145">System.String</span></span>

## <span data-ttu-id="ee602-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ee602-146">OUTPUTS</span></span>

### <span data-ttu-id="ee602-147">System. String</span><span class="sxs-lookup"><span data-stu-id="ee602-147">System.String</span></span>

## <span data-ttu-id="ee602-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="ee602-148">NOTES</span></span>

## <span data-ttu-id="ee602-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ee602-149">RELATED LINKS</span></span>
