---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/remove-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistry.md
ms.openlocfilehash: 2235e533e999fedbb06b79548bf4e2ce8de3586a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664082"
---
# <span data-ttu-id="68123-101">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="68123-101">Remove-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="68123-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="68123-102">SYNOPSIS</span></span>
<span data-ttu-id="68123-103">Entfernt eine Container Registrierung.</span><span class="sxs-lookup"><span data-stu-id="68123-103">Removes a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68123-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="68123-104">SYNTAX</span></span>

### <span data-ttu-id="68123-105">NameResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="68123-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68123-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="68123-106">RegistryObjectParameterSet</span></span>
```
Remove-AzureRmContainerRegistry -Registry <PSContainerRegistry> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68123-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="68123-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmContainerRegistry -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68123-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="68123-108">DESCRIPTION</span></span>
<span data-ttu-id="68123-109">Das Remove-AzureRmContainerRegistry-Cmdlet entfernt eine Container Registrierung.</span><span class="sxs-lookup"><span data-stu-id="68123-109">The Remove-AzureRmContainerRegistry cmdlet removes a container registry.</span></span>

## <span data-ttu-id="68123-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="68123-110">EXAMPLES</span></span>

### <span data-ttu-id="68123-111">Beispiel 1: Entfernen einer angegebenen Container Registrierung</span><span class="sxs-lookup"><span data-stu-id="68123-111">Example 1: Remove a specified container registry</span></span>
```powershell
PS C:\>Remove-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"
```

<span data-ttu-id="68123-112">Dieser Befehl entfernt die angegebene Container Registrierung.</span><span class="sxs-lookup"><span data-stu-id="68123-112">This command removes the specified container registry.</span></span>

## <span data-ttu-id="68123-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="68123-113">PARAMETERS</span></span>

### <span data-ttu-id="68123-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68123-114">-DefaultProfile</span></span>
<span data-ttu-id="68123-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="68123-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="68123-116">-Name</span><span class="sxs-lookup"><span data-stu-id="68123-116">-Name</span></span>
<span data-ttu-id="68123-117">Container Registrierungs Name</span><span class="sxs-lookup"><span data-stu-id="68123-117">Container Registry Name.</span></span>

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

### <span data-ttu-id="68123-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="68123-118">-PassThru</span></span>
<span data-ttu-id="68123-119">Gibt an, dass dieses Cmdlet "true" zurückgibt, wenn die Entfernung erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="68123-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="68123-120">-Registry</span><span class="sxs-lookup"><span data-stu-id="68123-120">-Registry</span></span>
<span data-ttu-id="68123-121">Container Registrierungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="68123-121">Container Registry Object.</span></span>

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

### <span data-ttu-id="68123-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68123-122">-ResourceGroupName</span></span>
<span data-ttu-id="68123-123">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="68123-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="68123-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="68123-124">-ResourceId</span></span>
<span data-ttu-id="68123-125">Die Ressourcen-ID der Container-Registrierung</span><span class="sxs-lookup"><span data-stu-id="68123-125">The container registry resource id</span></span>

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

### <span data-ttu-id="68123-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="68123-126">-Confirm</span></span>
<span data-ttu-id="68123-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="68123-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68123-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68123-128">-WhatIf</span></span>
<span data-ttu-id="68123-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="68123-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68123-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="68123-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68123-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68123-131">CommonParameters</span></span>
<span data-ttu-id="68123-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68123-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68123-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68123-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68123-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="68123-134">INPUTS</span></span>

### <span data-ttu-id="68123-135">System. String</span><span class="sxs-lookup"><span data-stu-id="68123-135">System.String</span></span>

## <span data-ttu-id="68123-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="68123-136">OUTPUTS</span></span>

### <span data-ttu-id="68123-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="68123-137">System.Boolean</span></span>

## <span data-ttu-id="68123-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="68123-138">NOTES</span></span>

## <span data-ttu-id="68123-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="68123-139">RELATED LINKS</span></span>

[<span data-ttu-id="68123-140">Neu – AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="68123-140">New-AzureRmContainerRegistry</span></span>]()

[<span data-ttu-id="68123-141">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="68123-141">Get-AzureRmContainerRegistry</span></span>]()

[<span data-ttu-id="68123-142">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="68123-142">Update-AzureRmContainerRegistry</span></span>]()

