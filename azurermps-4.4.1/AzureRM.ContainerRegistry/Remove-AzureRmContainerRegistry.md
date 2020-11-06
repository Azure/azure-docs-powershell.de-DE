---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistry.md
ms.openlocfilehash: 5a5ea87044c18e82f4c17294356a35adb254eee4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479361"
---
# <span data-ttu-id="21a8f-101">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="21a8f-101">Remove-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="21a8f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="21a8f-102">SYNOPSIS</span></span>
<span data-ttu-id="21a8f-103">Entfernt eine Container Registrierung.</span><span class="sxs-lookup"><span data-stu-id="21a8f-103">Removes a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21a8f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="21a8f-104">SYNTAX</span></span>

### <span data-ttu-id="21a8f-105">NameResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="21a8f-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21a8f-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="21a8f-106">RegistryObjectParameterSet</span></span>
```
Remove-AzureRmContainerRegistry -Registry <PSContainerRegistry> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21a8f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="21a8f-107">DESCRIPTION</span></span>
<span data-ttu-id="21a8f-108">Das Cmdlet **Remove-AzureRmContainerRegistry** entfernt eine Container Registrierung.</span><span class="sxs-lookup"><span data-stu-id="21a8f-108">The **Remove-AzureRmContainerRegistry** cmdlet removes a container registry.</span></span>

## <span data-ttu-id="21a8f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="21a8f-109">EXAMPLES</span></span>

### <span data-ttu-id="21a8f-110">Beispiel 1: Entfernen einer angegebenen Container Registrierung</span><span class="sxs-lookup"><span data-stu-id="21a8f-110">Example 1: Remove a specified container registry</span></span>
```
PS C:\>Remove-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"
```

<span data-ttu-id="21a8f-111">Dieser Befehl entfernt die angegebene Container Registrierung.</span><span class="sxs-lookup"><span data-stu-id="21a8f-111">This command removes the specified container registry.</span></span>

## <span data-ttu-id="21a8f-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="21a8f-112">PARAMETERS</span></span>

### <span data-ttu-id="21a8f-113">-Name</span><span class="sxs-lookup"><span data-stu-id="21a8f-113">-Name</span></span>
<span data-ttu-id="21a8f-114">Container Registrierungs Name</span><span class="sxs-lookup"><span data-stu-id="21a8f-114">Container Registry Name.</span></span>

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

### <span data-ttu-id="21a8f-115">-Registry</span><span class="sxs-lookup"><span data-stu-id="21a8f-115">-Registry</span></span>
<span data-ttu-id="21a8f-116">Container Registrierungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="21a8f-116">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="21a8f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21a8f-117">-ResourceGroupName</span></span>
<span data-ttu-id="21a8f-118">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="21a8f-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="21a8f-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="21a8f-119">-Confirm</span></span>
<span data-ttu-id="21a8f-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="21a8f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21a8f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21a8f-121">-WhatIf</span></span>
<span data-ttu-id="21a8f-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="21a8f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21a8f-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="21a8f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21a8f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21a8f-124">-DefaultProfile</span></span>
<span data-ttu-id="21a8f-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="21a8f-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21a8f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21a8f-126">CommonParameters</span></span>
<span data-ttu-id="21a8f-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21a8f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21a8f-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21a8f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21a8f-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="21a8f-129">INPUTS</span></span>

### <span data-ttu-id="21a8f-130">PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="21a8f-130">PSContainerRegistry</span></span>
<span data-ttu-id="21a8f-131">Der Parameter "Registry" akzeptiert den Wert vom Typ "PSContainerRegistry" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="21a8f-131">Parameter 'Registry' accepts value of type 'PSContainerRegistry' from the pipeline</span></span>

## <span data-ttu-id="21a8f-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="21a8f-132">OUTPUTS</span></span>

### <span data-ttu-id="21a8f-133">Keine</span><span class="sxs-lookup"><span data-stu-id="21a8f-133">None</span></span>

## <span data-ttu-id="21a8f-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="21a8f-134">NOTES</span></span>

## <span data-ttu-id="21a8f-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="21a8f-135">RELATED LINKS</span></span>

[<span data-ttu-id="21a8f-136">Neu – AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="21a8f-136">New-AzureRmContainerRegistry</span></span>](./New-AzureRmContainerRegistry.md)

[<span data-ttu-id="21a8f-137">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="21a8f-137">Get-AzureRmContainerRegistry</span></span>](./Get-AzureRmContainerRegistry.md)

[<span data-ttu-id="21a8f-138">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="21a8f-138">Update-AzureRmContainerRegistry</span></span>](./Update-AzureRmContainerRegistry.md)

