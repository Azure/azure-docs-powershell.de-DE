---
external help file: Microsoft.Azure.Commands.ContainerInstance.dll-Help.xml
Module Name: AzureRM.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerinstance/remove-azurermcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Remove-AzureRmContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Remove-AzureRmContainerGroup.md
ms.openlocfilehash: f1971f8bf0e7d8e779743739b8dd041effe3ba5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477870"
---
# <span data-ttu-id="7651d-101">Remove-AzureRmContainerGroup</span><span class="sxs-lookup"><span data-stu-id="7651d-101">Remove-AzureRmContainerGroup</span></span>

## <span data-ttu-id="7651d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7651d-102">SYNOPSIS</span></span>
<span data-ttu-id="7651d-103">Entfernt eine Containergruppe.</span><span class="sxs-lookup"><span data-stu-id="7651d-103">Removes a container group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7651d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7651d-104">SYNTAX</span></span>

### <span data-ttu-id="7651d-105">RemoveContainerGroupByResourceGroupAndNameParamSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="7651d-105">RemoveContainerGroupByResourceGroupAndNameParamSet (Default)</span></span>
```
Remove-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7651d-106">RemoveContainerGroupByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="7651d-106">RemoveContainerGroupByPSContainerGroupParamSet</span></span>
```
Remove-AzureRmContainerGroup -InputObject <PSContainerGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7651d-107">RemoveContainerGroupByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="7651d-107">RemoveContainerGroupByResourceIdParamSet</span></span>
```
Remove-AzureRmContainerGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7651d-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7651d-108">DESCRIPTION</span></span>
<span data-ttu-id="7651d-109">Das Cmdlet **Remove-AzureRmContainerGroup** entfernt eine Containergruppe.</span><span class="sxs-lookup"><span data-stu-id="7651d-109">The **Remove-AzureRmContainerGroup** cmdlet removes a container group.</span></span>

## <span data-ttu-id="7651d-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7651d-110">EXAMPLES</span></span>

### <span data-ttu-id="7651d-111">Beispiel 1: entfernt eine Containergruppe</span><span class="sxs-lookup"><span data-stu-id="7651d-111">Example 1: Removes a container group</span></span>
```
PS C:\> Remove-AzureRmContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer
```

<span data-ttu-id="7651d-112">Dieser Befehl entfernt die angegebene Containergruppe.</span><span class="sxs-lookup"><span data-stu-id="7651d-112">This command removes the specified container group.</span></span>

### <span data-ttu-id="7651d-113">Beispiel 2: entfernt eine Containergruppe durch Piping</span><span class="sxs-lookup"><span data-stu-id="7651d-113">Example 2: Removes a container group by piping</span></span>
```
PS C:\> Get-AzureRmContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer | Remove-AzureRmContainerGroup
```

<span data-ttu-id="7651d-114">Mit diesem Befehl wird eine Containergruppe durch Piping entfernt.</span><span class="sxs-lookup"><span data-stu-id="7651d-114">This command removes a container group by piping.</span></span>

### <span data-ttu-id="7651d-115">Beispiel 3: entfernt eine Containergruppe nach Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="7651d-115">Example 3: Removes a container group by resource Id.</span></span>
```
PS C:\> Find-AzureRmResource -ResourceGroupEquals MyResourceGroup -ResourceNameEquals MyContainer | Remove-AzureRmContainerGroup
```

<span data-ttu-id="7651d-116">Mit diesem Befehl wird eine Containergruppe nach Ressourcen-ID entfernt.</span><span class="sxs-lookup"><span data-stu-id="7651d-116">This command removes a container group by resource Id.</span></span>

## <span data-ttu-id="7651d-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="7651d-117">PARAMETERS</span></span>

### <span data-ttu-id="7651d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7651d-118">-DefaultProfile</span></span>
<span data-ttu-id="7651d-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7651d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7651d-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7651d-120">-InputObject</span></span>
<span data-ttu-id="7651d-121">Die zu entfernende Containergruppe.</span><span class="sxs-lookup"><span data-stu-id="7651d-121">The container group to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup
Parameter Sets: RemoveContainerGroupByPSContainerGroupParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7651d-122">-Name</span><span class="sxs-lookup"><span data-stu-id="7651d-122">-Name</span></span>
<span data-ttu-id="7651d-123">Der Name der Containergruppe.</span><span class="sxs-lookup"><span data-stu-id="7651d-123">The container group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveContainerGroupByResourceGroupAndNameParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7651d-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7651d-124">-PassThru</span></span>
<span data-ttu-id="7651d-125">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="7651d-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="7651d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7651d-126">-ResourceGroupName</span></span>
<span data-ttu-id="7651d-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7651d-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveContainerGroupByResourceGroupAndNameParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7651d-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="7651d-128">-ResourceId</span></span>
<span data-ttu-id="7651d-129">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="7651d-129">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveContainerGroupByResourceIdParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7651d-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7651d-130">-Confirm</span></span>
<span data-ttu-id="7651d-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7651d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7651d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7651d-132">-WhatIf</span></span>
<span data-ttu-id="7651d-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7651d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7651d-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7651d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7651d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7651d-135">CommonParameters</span></span>
<span data-ttu-id="7651d-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7651d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7651d-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7651d-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7651d-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7651d-138">INPUTS</span></span>

### <span data-ttu-id="7651d-139">Microsoft. Azure. Commands. ContainerInstance. Models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="7651d-139">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>
<span data-ttu-id="7651d-140">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7651d-140">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="7651d-141">System. String</span><span class="sxs-lookup"><span data-stu-id="7651d-141">System.String</span></span>

## <span data-ttu-id="7651d-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7651d-142">OUTPUTS</span></span>

### <span data-ttu-id="7651d-143">Microsoft. Azure. Commands. ContainerInstance. Models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="7651d-143">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="7651d-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="7651d-144">NOTES</span></span>

## <span data-ttu-id="7651d-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7651d-145">RELATED LINKS</span></span>
