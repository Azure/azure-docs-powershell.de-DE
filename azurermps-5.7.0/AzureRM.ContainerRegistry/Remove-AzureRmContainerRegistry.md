---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/remove-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistry.md
ms.openlocfilehash: df0c938db8f44ebffedc9760e4a3d33ee175ae01
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497665"
---
# <span data-ttu-id="07bf9-101">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="07bf9-101">Remove-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="07bf9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="07bf9-102">SYNOPSIS</span></span>
<span data-ttu-id="07bf9-103">Entfernt eine Container Registrierung.</span><span class="sxs-lookup"><span data-stu-id="07bf9-103">Removes a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07bf9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="07bf9-104">SYNTAX</span></span>

### <span data-ttu-id="07bf9-105">NameResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="07bf9-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07bf9-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="07bf9-106">RegistryObjectParameterSet</span></span>
```
Remove-AzureRmContainerRegistry -Registry <PSContainerRegistry> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07bf9-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="07bf9-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmContainerRegistry -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07bf9-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="07bf9-108">DESCRIPTION</span></span>
<span data-ttu-id="07bf9-109">Das Remove-AzureRmContainerRegistry-Cmdlet entfernt eine Container Registrierung.</span><span class="sxs-lookup"><span data-stu-id="07bf9-109">The Remove-AzureRmContainerRegistry cmdlet removes a container registry.</span></span>

## <span data-ttu-id="07bf9-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="07bf9-110">EXAMPLES</span></span>

### <span data-ttu-id="07bf9-111">Beispiel 1: Entfernen einer angegebenen Container Registrierung</span><span class="sxs-lookup"><span data-stu-id="07bf9-111">Example 1: Remove a specified container registry</span></span>
```powershell
PS C:\>Remove-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"
```

<span data-ttu-id="07bf9-112">Dieser Befehl entfernt die angegebene Container Registrierung.</span><span class="sxs-lookup"><span data-stu-id="07bf9-112">This command removes the specified container registry.</span></span>

## <span data-ttu-id="07bf9-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="07bf9-113">PARAMETERS</span></span>

### <span data-ttu-id="07bf9-114">-Name</span><span class="sxs-lookup"><span data-stu-id="07bf9-114">-Name</span></span>
<span data-ttu-id="07bf9-115">Container Registrierungs Name</span><span class="sxs-lookup"><span data-stu-id="07bf9-115">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07bf9-116">-Registry</span><span class="sxs-lookup"><span data-stu-id="07bf9-116">-Registry</span></span>
<span data-ttu-id="07bf9-117">Container Registrierungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="07bf9-117">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07bf9-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07bf9-118">-ResourceGroupName</span></span>
<span data-ttu-id="07bf9-119">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="07bf9-119">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07bf9-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="07bf9-120">-Confirm</span></span>
<span data-ttu-id="07bf9-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="07bf9-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07bf9-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07bf9-122">-WhatIf</span></span>
<span data-ttu-id="07bf9-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="07bf9-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07bf9-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="07bf9-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07bf9-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07bf9-125">-DefaultProfile</span></span>
<span data-ttu-id="07bf9-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="07bf9-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="07bf9-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="07bf9-127">-ResourceId</span></span>
<span data-ttu-id="07bf9-128">Die Ressourcen-ID der Container-Registrierung</span><span class="sxs-lookup"><span data-stu-id="07bf9-128">The container registry resource id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07bf9-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="07bf9-129">-PassThru</span></span>
<span data-ttu-id="07bf9-130">Gibt an, dass dieses Cmdlet "true" zurückgibt, wenn die Entfernung erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="07bf9-130">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="07bf9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07bf9-131">CommonParameters</span></span>
<span data-ttu-id="07bf9-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07bf9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07bf9-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07bf9-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07bf9-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="07bf9-134">INPUTS</span></span>

### <span data-ttu-id="07bf9-135">PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="07bf9-135">PSContainerRegistry</span></span>
<span data-ttu-id="07bf9-136">Der Parameter "Registry" akzeptiert den Wert vom Typ "PSContainerRegistry" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="07bf9-136">Parameter 'Registry' accepts value of type 'PSContainerRegistry' from the pipeline</span></span>

## <span data-ttu-id="07bf9-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="07bf9-137">OUTPUTS</span></span>

### <span data-ttu-id="07bf9-138">Keine</span><span class="sxs-lookup"><span data-stu-id="07bf9-138">None</span></span>

## <span data-ttu-id="07bf9-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="07bf9-139">NOTES</span></span>

## <span data-ttu-id="07bf9-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="07bf9-140">RELATED LINKS</span></span>

[<span data-ttu-id="07bf9-141">Neu – AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="07bf9-141">New-AzureRmContainerRegistry</span></span>]()

[<span data-ttu-id="07bf9-142">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="07bf9-142">Get-AzureRmContainerRegistry</span></span>]()

[<span data-ttu-id="07bf9-143">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="07bf9-143">Update-AzureRmContainerRegistry</span></span>]()

