---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistry.md
ms.openlocfilehash: c389f62f6f9b76f0ebdab30ddf600d333263a87c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651823"
---
# <span data-ttu-id="f1f43-101">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f1f43-101">Remove-AzContainerRegistry</span></span>

## <span data-ttu-id="f1f43-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f1f43-102">SYNOPSIS</span></span>
<span data-ttu-id="f1f43-103">Entfernt eine Container Registrierung.</span><span class="sxs-lookup"><span data-stu-id="f1f43-103">Removes a container registry.</span></span>

## <span data-ttu-id="f1f43-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1f43-104">SYNTAX</span></span>

### <span data-ttu-id="f1f43-105">NameResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f1f43-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1f43-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1f43-106">RegistryObjectParameterSet</span></span>
```
Remove-AzContainerRegistry -Registry <PSContainerRegistry> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1f43-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1f43-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistry -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1f43-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f1f43-108">DESCRIPTION</span></span>
<span data-ttu-id="f1f43-109">Das Remove-AzContainerRegistry-Cmdlet entfernt eine Container Registrierung.</span><span class="sxs-lookup"><span data-stu-id="f1f43-109">The Remove-AzContainerRegistry cmdlet removes a container registry.</span></span>

## <span data-ttu-id="f1f43-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f1f43-110">EXAMPLES</span></span>

### <span data-ttu-id="f1f43-111">Beispiel 1: Entfernen einer angegebenen Container Registrierung</span><span class="sxs-lookup"><span data-stu-id="f1f43-111">Example 1: Remove a specified container registry</span></span>
```powershell
PS C:\>Remove-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"
```

<span data-ttu-id="f1f43-112">Dieser Befehl entfernt die angegebene Container Registrierung.</span><span class="sxs-lookup"><span data-stu-id="f1f43-112">This command removes the specified container registry.</span></span>

## <span data-ttu-id="f1f43-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="f1f43-113">PARAMETERS</span></span>

### <span data-ttu-id="f1f43-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1f43-114">-DefaultProfile</span></span>
<span data-ttu-id="f1f43-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="f1f43-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f1f43-116">-Name</span><span class="sxs-lookup"><span data-stu-id="f1f43-116">-Name</span></span>
<span data-ttu-id="f1f43-117">Container Registrierungs Name</span><span class="sxs-lookup"><span data-stu-id="f1f43-117">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1f43-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f1f43-118">-PassThru</span></span>
<span data-ttu-id="f1f43-119">Gibt an, dass dieses Cmdlet "true" zurückgibt, wenn die Entfernung erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="f1f43-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="f1f43-120">-Registry</span><span class="sxs-lookup"><span data-stu-id="f1f43-120">-Registry</span></span>
<span data-ttu-id="f1f43-121">Container Registrierungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="f1f43-121">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1f43-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1f43-122">-ResourceGroupName</span></span>
<span data-ttu-id="f1f43-123">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f1f43-123">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1f43-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="f1f43-124">-ResourceId</span></span>
<span data-ttu-id="f1f43-125">Die Ressourcen-ID der Container-Registrierung</span><span class="sxs-lookup"><span data-stu-id="f1f43-125">The container registry resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1f43-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f1f43-126">-Confirm</span></span>
<span data-ttu-id="f1f43-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f1f43-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1f43-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1f43-128">-WhatIf</span></span>
<span data-ttu-id="f1f43-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f1f43-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1f43-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f1f43-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1f43-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1f43-131">CommonParameters</span></span>
<span data-ttu-id="f1f43-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1f43-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1f43-133">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f1f43-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1f43-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f1f43-134">INPUTS</span></span>

### <span data-ttu-id="f1f43-135">System. String</span><span class="sxs-lookup"><span data-stu-id="f1f43-135">System.String</span></span>

## <span data-ttu-id="f1f43-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f1f43-136">OUTPUTS</span></span>

### <span data-ttu-id="f1f43-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f1f43-137">System.Boolean</span></span>

## <span data-ttu-id="f1f43-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="f1f43-138">NOTES</span></span>

## <span data-ttu-id="f1f43-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f1f43-139">RELATED LINKS</span></span>

[<span data-ttu-id="f1f43-140">Neu – AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f1f43-140">New-AzContainerRegistry</span></span>]()

[<span data-ttu-id="f1f43-141">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f1f43-141">Get-AzContainerRegistry</span></span>]()

[<span data-ttu-id="f1f43-142">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f1f43-142">Update-AzContainerRegistry</span></span>]()

