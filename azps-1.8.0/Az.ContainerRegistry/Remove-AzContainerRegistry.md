---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistry.md
ms.openlocfilehash: dee0e1f4dab19af5de4d7f8ce7a9fe10b8f51d37
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661384"
---
# <span data-ttu-id="5c1e4-101">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="5c1e4-101">Remove-AzContainerRegistry</span></span>

## <span data-ttu-id="5c1e4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5c1e4-102">SYNOPSIS</span></span>
<span data-ttu-id="5c1e4-103">Entfernt eine Container Registrierung.</span><span class="sxs-lookup"><span data-stu-id="5c1e4-103">Removes a container registry.</span></span>

## <span data-ttu-id="5c1e4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5c1e4-104">SYNTAX</span></span>

### <span data-ttu-id="5c1e4-105">NameResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5c1e4-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c1e4-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c1e4-106">RegistryObjectParameterSet</span></span>
```
Remove-AzContainerRegistry -Registry <PSContainerRegistry> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c1e4-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c1e4-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistry -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c1e4-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5c1e4-108">DESCRIPTION</span></span>
<span data-ttu-id="5c1e4-109">Das Remove-AzContainerRegistry-Cmdlet entfernt eine Container Registrierung.</span><span class="sxs-lookup"><span data-stu-id="5c1e4-109">The Remove-AzContainerRegistry cmdlet removes a container registry.</span></span>

## <span data-ttu-id="5c1e4-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5c1e4-110">EXAMPLES</span></span>

### <span data-ttu-id="5c1e4-111">Beispiel 1: Entfernen einer angegebenen Container Registrierung</span><span class="sxs-lookup"><span data-stu-id="5c1e4-111">Example 1: Remove a specified container registry</span></span>
```powershell
PS C:\>Remove-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"
```

<span data-ttu-id="5c1e4-112">Dieser Befehl entfernt die angegebene Container Registrierung.</span><span class="sxs-lookup"><span data-stu-id="5c1e4-112">This command removes the specified container registry.</span></span>

## <span data-ttu-id="5c1e4-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="5c1e4-113">PARAMETERS</span></span>

### <span data-ttu-id="5c1e4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c1e4-114">-DefaultProfile</span></span>
<span data-ttu-id="5c1e4-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="5c1e4-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5c1e4-116">-Name</span><span class="sxs-lookup"><span data-stu-id="5c1e4-116">-Name</span></span>
<span data-ttu-id="5c1e4-117">Container Registrierungs Name</span><span class="sxs-lookup"><span data-stu-id="5c1e4-117">Container Registry Name.</span></span>

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

### <span data-ttu-id="5c1e4-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5c1e4-118">-PassThru</span></span>
<span data-ttu-id="5c1e4-119">Gibt an, dass dieses Cmdlet "true" zurückgibt, wenn die Entfernung erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="5c1e4-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="5c1e4-120">-Registry</span><span class="sxs-lookup"><span data-stu-id="5c1e4-120">-Registry</span></span>
<span data-ttu-id="5c1e4-121">Container Registrierungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="5c1e4-121">Container Registry Object.</span></span>

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

### <span data-ttu-id="5c1e4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c1e4-122">-ResourceGroupName</span></span>
<span data-ttu-id="5c1e4-123">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5c1e4-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="5c1e4-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="5c1e4-124">-ResourceId</span></span>
<span data-ttu-id="5c1e4-125">Die Ressourcen-ID der Container-Registrierung</span><span class="sxs-lookup"><span data-stu-id="5c1e4-125">The container registry resource id</span></span>

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

### <span data-ttu-id="5c1e4-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5c1e4-126">-Confirm</span></span>
<span data-ttu-id="5c1e4-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5c1e4-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c1e4-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c1e4-128">-WhatIf</span></span>
<span data-ttu-id="5c1e4-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5c1e4-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c1e4-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5c1e4-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c1e4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c1e4-131">CommonParameters</span></span>
<span data-ttu-id="5c1e4-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c1e4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c1e4-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c1e4-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c1e4-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5c1e4-134">INPUTS</span></span>

### <span data-ttu-id="5c1e4-135">System. String</span><span class="sxs-lookup"><span data-stu-id="5c1e4-135">System.String</span></span>

## <span data-ttu-id="5c1e4-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5c1e4-136">OUTPUTS</span></span>

### <span data-ttu-id="5c1e4-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5c1e4-137">System.Boolean</span></span>

## <span data-ttu-id="5c1e4-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="5c1e4-138">NOTES</span></span>

## <span data-ttu-id="5c1e4-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5c1e4-139">RELATED LINKS</span></span>

[<span data-ttu-id="5c1e4-140">Neu – AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="5c1e4-140">New-AzContainerRegistry</span></span>]()

[<span data-ttu-id="5c1e4-141">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="5c1e4-141">Get-AzContainerRegistry</span></span>]()

[<span data-ttu-id="5c1e4-142">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="5c1e4-142">Update-AzContainerRegistry</span></span>]()

