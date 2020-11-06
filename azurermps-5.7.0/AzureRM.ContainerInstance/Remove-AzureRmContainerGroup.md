---
external help file: Microsoft.Azure.Commands.ContainerInstance.dll-Help.xml
Module Name: AzureRM.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerinstance/remove-azurermcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Remove-AzureRmContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Remove-AzureRmContainerGroup.md
ms.openlocfilehash: 80343713c9bf7a0e34a1d9a3b3b75825cbb97a12
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503814"
---
# <span data-ttu-id="b4cd5-101">Remove-AzureRmContainerGroup</span><span class="sxs-lookup"><span data-stu-id="b4cd5-101">Remove-AzureRmContainerGroup</span></span>

## <span data-ttu-id="b4cd5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b4cd5-102">SYNOPSIS</span></span>
<span data-ttu-id="b4cd5-103">Entfernt eine Containergruppe.</span><span class="sxs-lookup"><span data-stu-id="b4cd5-103">Removes a container group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4cd5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4cd5-104">SYNTAX</span></span>

### <span data-ttu-id="b4cd5-105">RemoveContainerGroupByResourceGroupAndNameParamSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b4cd5-105">RemoveContainerGroupByResourceGroupAndNameParamSet (Default)</span></span>
```
Remove-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4cd5-106">RemoveContainerGroupByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="b4cd5-106">RemoveContainerGroupByPSContainerGroupParamSet</span></span>
```
Remove-AzureRmContainerGroup -InputObject <PSContainerGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4cd5-107">RemoveContainerGroupByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="b4cd5-107">RemoveContainerGroupByResourceIdParamSet</span></span>
```
Remove-AzureRmContainerGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4cd5-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b4cd5-108">DESCRIPTION</span></span>
<span data-ttu-id="b4cd5-109">Das Cmdlet **Remove-AzureRmContainerGroup** entfernt eine Containergruppe.</span><span class="sxs-lookup"><span data-stu-id="b4cd5-109">The **Remove-AzureRmContainerGroup** cmdlet removes a container group.</span></span>

## <span data-ttu-id="b4cd5-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b4cd5-110">EXAMPLES</span></span>

### <span data-ttu-id="b4cd5-111">Beispiel 1: entfernt eine Containergruppe</span><span class="sxs-lookup"><span data-stu-id="b4cd5-111">Example 1: Removes a container group</span></span>
```
PS C:\> Remove-AzureRmContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer
```

<span data-ttu-id="b4cd5-112">Dieser Befehl entfernt die angegebene Containergruppe.</span><span class="sxs-lookup"><span data-stu-id="b4cd5-112">This command removes the specified container group.</span></span>

### <span data-ttu-id="b4cd5-113">Beispiel 2: entfernt eine Containergruppe durch Piping</span><span class="sxs-lookup"><span data-stu-id="b4cd5-113">Example 2: Removes a container group by piping</span></span>
```
PS C:\> Get-AzureRmContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer | Remove-AzureRmContainerGroup
```

<span data-ttu-id="b4cd5-114">Mit diesem Befehl wird eine Containergruppe durch Piping entfernt.</span><span class="sxs-lookup"><span data-stu-id="b4cd5-114">This command removes a container group by piping.</span></span>

### <span data-ttu-id="b4cd5-115">Beispiel 3: entfernt eine Containergruppe nach Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="b4cd5-115">Example 3: Removes a container group by resource Id.</span></span>
```
PS C:\> Find-AzureRmResource -ResourceGroupEquals MyResourceGroup -ResourceNameEquals MyContainer | Remove-AzureRmContainerGroup
```

<span data-ttu-id="b4cd5-116">Mit diesem Befehl wird eine Containergruppe nach Ressourcen-ID entfernt.</span><span class="sxs-lookup"><span data-stu-id="b4cd5-116">This command removes a container group by resource Id.</span></span>

## <span data-ttu-id="b4cd5-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="b4cd5-117">PARAMETERS</span></span>

### <span data-ttu-id="b4cd5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4cd5-118">-DefaultProfile</span></span>
<span data-ttu-id="b4cd5-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b4cd5-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4cd5-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b4cd5-120">-InputObject</span></span>
<span data-ttu-id="b4cd5-121">Die zu entfernende Containergruppe.</span><span class="sxs-lookup"><span data-stu-id="b4cd5-121">The container group to remove.</span></span>

```yaml
Type: PSContainerGroup
Parameter Sets: RemoveContainerGroupByPSContainerGroupParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4cd5-122">-Name</span><span class="sxs-lookup"><span data-stu-id="b4cd5-122">-Name</span></span>
<span data-ttu-id="b4cd5-123">Der Name der Containergruppe.</span><span class="sxs-lookup"><span data-stu-id="b4cd5-123">The container group name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveContainerGroupByResourceGroupAndNameParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4cd5-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b4cd5-124">-PassThru</span></span>
<span data-ttu-id="b4cd5-125">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="b4cd5-125">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4cd5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4cd5-126">-ResourceGroupName</span></span>
<span data-ttu-id="b4cd5-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b4cd5-127">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveContainerGroupByResourceGroupAndNameParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4cd5-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="b4cd5-128">-ResourceId</span></span>
<span data-ttu-id="b4cd5-129">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="b4cd5-129">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: RemoveContainerGroupByResourceIdParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4cd5-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b4cd5-130">-Confirm</span></span>
<span data-ttu-id="b4cd5-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b4cd5-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4cd5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4cd5-132">-WhatIf</span></span>
<span data-ttu-id="b4cd5-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b4cd5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4cd5-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b4cd5-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4cd5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4cd5-135">CommonParameters</span></span>
<span data-ttu-id="b4cd5-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4cd5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4cd5-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4cd5-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4cd5-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b4cd5-138">INPUTS</span></span>

### <span data-ttu-id="b4cd5-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b4cd5-139">System.String</span></span>
<span data-ttu-id="b4cd5-140">Microsoft. Azure. Commands. ContainerInstance. Models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="b4cd5-140">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="b4cd5-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b4cd5-141">OUTPUTS</span></span>

### <span data-ttu-id="b4cd5-142">Microsoft. Azure. Commands. ContainerInstance. Models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="b4cd5-142">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="b4cd5-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="b4cd5-143">NOTES</span></span>

## <span data-ttu-id="b4cd5-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b4cd5-144">RELATED LINKS</span></span>
