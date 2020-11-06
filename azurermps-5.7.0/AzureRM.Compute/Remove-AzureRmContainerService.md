---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 8180092D-5B1D-43A0-B830-D009B30E2DDF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmContainerService.md
ms.openlocfilehash: da4f9846f8fceaaecc6d4385374f6525d3243e3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478593"
---
# <span data-ttu-id="b30d5-101">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="b30d5-101">Remove-AzureRmContainerService</span></span>

## <span data-ttu-id="b30d5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b30d5-102">SYNOPSIS</span></span>
<span data-ttu-id="b30d5-103">Entfernt einen Containerdienst.</span><span class="sxs-lookup"><span data-stu-id="b30d5-103">Removes a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b30d5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b30d5-104">SYNTAX</span></span>

```
Remove-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b30d5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b30d5-105">DESCRIPTION</span></span>
<span data-ttu-id="b30d5-106">Das Cmdlet **Remove-AzureRmContainerService** entfernt einen Containerdienst aus Ihrem Azure-Konto.</span><span class="sxs-lookup"><span data-stu-id="b30d5-106">The **Remove-AzureRmContainerService** cmdlet removes a container service from your Azure account.</span></span>

## <span data-ttu-id="b30d5-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b30d5-107">EXAMPLES</span></span>

### <span data-ttu-id="b30d5-108">Beispiel 1: Entfernen eines Container Diensts</span><span class="sxs-lookup"><span data-stu-id="b30d5-108">Example 1: Remove a container service</span></span>
```
PS C:\> Remove-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="b30d5-109">Dieser Befehl entfernt den Containerdienst mit dem Namen CSResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="b30d5-109">This command removes the container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="b30d5-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b30d5-110">PARAMETERS</span></span>

### <span data-ttu-id="b30d5-111">-Force</span><span class="sxs-lookup"><span data-stu-id="b30d5-111">-Force</span></span>
<span data-ttu-id="b30d5-112">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="b30d5-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b30d5-113">-Name</span><span class="sxs-lookup"><span data-stu-id="b30d5-113">-Name</span></span>
<span data-ttu-id="b30d5-114">Gibt den Namen des Container Diensts an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="b30d5-114">Specifies the name of the container service that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b30d5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b30d5-115">-ResourceGroupName</span></span>
<span data-ttu-id="b30d5-116">Gibt die Ressourcengruppe des Container Diensts an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="b30d5-116">Specifies the resource group of the container service that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b30d5-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b30d5-117">-Confirm</span></span>
<span data-ttu-id="b30d5-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b30d5-118">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="b30d5-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b30d5-119">-WhatIf</span></span>
<span data-ttu-id="b30d5-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b30d5-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b30d5-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b30d5-121">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="b30d5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b30d5-122">CommonParameters</span></span>
<span data-ttu-id="b30d5-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b30d5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b30d5-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b30d5-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b30d5-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b30d5-125">INPUTS</span></span>

### <span data-ttu-id="b30d5-126">Keine</span><span class="sxs-lookup"><span data-stu-id="b30d5-126">None</span></span>
<span data-ttu-id="b30d5-127">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="b30d5-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b30d5-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b30d5-128">OUTPUTS</span></span>

## <span data-ttu-id="b30d5-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="b30d5-129">NOTES</span></span>

## <span data-ttu-id="b30d5-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b30d5-130">RELATED LINKS</span></span>

[<span data-ttu-id="b30d5-131">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="b30d5-131">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="b30d5-132">Neu – AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="b30d5-132">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="b30d5-133">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="b30d5-133">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)


