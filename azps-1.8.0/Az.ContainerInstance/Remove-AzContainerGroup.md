---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerinstance/remove-azcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Remove-AzContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Remove-AzContainerGroup.md
ms.openlocfilehash: fb9b2c23618d731f6f107f755ca6ef41dfe439ff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661394"
---
# <span data-ttu-id="06d79-101">Remove-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="06d79-101">Remove-AzContainerGroup</span></span>

## <span data-ttu-id="06d79-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="06d79-102">SYNOPSIS</span></span>
<span data-ttu-id="06d79-103">Entfernt eine Containergruppe.</span><span class="sxs-lookup"><span data-stu-id="06d79-103">Removes a container group.</span></span>

## <span data-ttu-id="06d79-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="06d79-104">SYNTAX</span></span>

### <span data-ttu-id="06d79-105">RemoveContainerGroupByResourceGroupAndNameParamSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="06d79-105">RemoveContainerGroupByResourceGroupAndNameParamSet (Default)</span></span>
```
Remove-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06d79-106">RemoveContainerGroupByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="06d79-106">RemoveContainerGroupByPSContainerGroupParamSet</span></span>
```
Remove-AzContainerGroup -InputObject <PSContainerGroup> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06d79-107">RemoveContainerGroupByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="06d79-107">RemoveContainerGroupByResourceIdParamSet</span></span>
```
Remove-AzContainerGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06d79-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="06d79-108">DESCRIPTION</span></span>
<span data-ttu-id="06d79-109">Das Cmdlet **Remove-AzContainerGroup** entfernt eine Containergruppe.</span><span class="sxs-lookup"><span data-stu-id="06d79-109">The **Remove-AzContainerGroup** cmdlet removes a container group.</span></span>

## <span data-ttu-id="06d79-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="06d79-110">EXAMPLES</span></span>

### <span data-ttu-id="06d79-111">Beispiel 1: entfernt eine Containergruppe</span><span class="sxs-lookup"><span data-stu-id="06d79-111">Example 1: Removes a container group</span></span>
```
PS C:\> Remove-AzContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer
```

<span data-ttu-id="06d79-112">Dieser Befehl entfernt die angegebene Containergruppe.</span><span class="sxs-lookup"><span data-stu-id="06d79-112">This command removes the specified container group.</span></span>

### <span data-ttu-id="06d79-113">Beispiel 2: entfernt eine Containergruppe durch Piping</span><span class="sxs-lookup"><span data-stu-id="06d79-113">Example 2: Removes a container group by piping</span></span>
```
PS C:\> Get-AzContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer | Remove-AzContainerGroup
```

<span data-ttu-id="06d79-114">Mit diesem Befehl wird eine Containergruppe durch Piping entfernt.</span><span class="sxs-lookup"><span data-stu-id="06d79-114">This command removes a container group by piping.</span></span>

### <span data-ttu-id="06d79-115">Beispiel 3: entfernt eine Containergruppe nach Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="06d79-115">Example 3: Removes a container group by resource Id.</span></span>
```
PS C:\> Find-AzResource -ResourceGroupEquals MyResourceGroup -ResourceNameEquals MyContainer | Remove-AzContainerGroup
```

<span data-ttu-id="06d79-116">Mit diesem Befehl wird eine Containergruppe nach Ressourcen-ID entfernt.</span><span class="sxs-lookup"><span data-stu-id="06d79-116">This command removes a container group by resource Id.</span></span>

## <span data-ttu-id="06d79-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="06d79-117">PARAMETERS</span></span>

### <span data-ttu-id="06d79-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06d79-118">-DefaultProfile</span></span>
<span data-ttu-id="06d79-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="06d79-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06d79-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="06d79-120">-InputObject</span></span>
<span data-ttu-id="06d79-121">Die zu entfernende Containergruppe.</span><span class="sxs-lookup"><span data-stu-id="06d79-121">The container group to remove.</span></span>

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

### <span data-ttu-id="06d79-122">-Name</span><span class="sxs-lookup"><span data-stu-id="06d79-122">-Name</span></span>
<span data-ttu-id="06d79-123">Der Name der Containergruppe.</span><span class="sxs-lookup"><span data-stu-id="06d79-123">The container group name.</span></span>

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

### <span data-ttu-id="06d79-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="06d79-124">-PassThru</span></span>
<span data-ttu-id="06d79-125">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="06d79-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="06d79-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06d79-126">-ResourceGroupName</span></span>
<span data-ttu-id="06d79-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="06d79-127">The resource group name.</span></span>

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

### <span data-ttu-id="06d79-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="06d79-128">-ResourceId</span></span>
<span data-ttu-id="06d79-129">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="06d79-129">The resource id.</span></span>

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

### <span data-ttu-id="06d79-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="06d79-130">-Confirm</span></span>
<span data-ttu-id="06d79-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="06d79-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06d79-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06d79-132">-WhatIf</span></span>
<span data-ttu-id="06d79-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="06d79-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06d79-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="06d79-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06d79-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06d79-135">CommonParameters</span></span>
<span data-ttu-id="06d79-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06d79-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06d79-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06d79-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06d79-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="06d79-138">INPUTS</span></span>

### <span data-ttu-id="06d79-139">Microsoft. Azure. Commands. ContainerInstance. Models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="06d79-139">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

### <span data-ttu-id="06d79-140">System. String</span><span class="sxs-lookup"><span data-stu-id="06d79-140">System.String</span></span>

## <span data-ttu-id="06d79-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="06d79-141">OUTPUTS</span></span>

### <span data-ttu-id="06d79-142">Microsoft. Azure. Commands. ContainerInstance. Models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="06d79-142">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="06d79-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="06d79-143">NOTES</span></span>

## <span data-ttu-id="06d79-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="06d79-144">RELATED LINKS</span></span>
