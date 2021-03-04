---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/test-azcontainerregistrynameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryNameAvailability.md
ms.openlocfilehash: 0a0701a073101b0611f74a9443473fcd9568ca50
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920784"
---
# <span data-ttu-id="3a5bb-101">Test-AzContainerRegistryNameAvailability</span><span class="sxs-lookup"><span data-stu-id="3a5bb-101">Test-AzContainerRegistryNameAvailability</span></span>

## <span data-ttu-id="3a5bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a5bb-102">SYNOPSIS</span></span>
<span data-ttu-id="3a5bb-103">Überprüft die Verfügbarkeit eines Containerregistrierungsnamens.</span><span class="sxs-lookup"><span data-stu-id="3a5bb-103">Checks the availability of a container registry name.</span></span>

## <span data-ttu-id="3a5bb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3a5bb-104">SYNTAX</span></span>

```
Test-AzContainerRegistryNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3a5bb-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3a5bb-105">DESCRIPTION</span></span>
<span data-ttu-id="3a5bb-106">Das Test-AzContainerRegistryNameAvailability cmdlet überprüft, ob ein Containerregistrierungsname gültig und zur Verwendung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="3a5bb-106">The Test-AzContainerRegistryNameAvailability cmdlet checks whether a container registry name is valid and available to use.</span></span>

## <span data-ttu-id="3a5bb-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3a5bb-107">EXAMPLES</span></span>

### <span data-ttu-id="3a5bb-108">Beispiel 1: Überprüft die Verfügbarkeit eines Containerregistrierungsnamens</span><span class="sxs-lookup"><span data-stu-id="3a5bb-108">Example 1: Checks the availability of a container registry name</span></span>
```powershell
PS C:\>Test-AzContainerRegistryNameAvailability -Name 'SomeRegistryName'

NameAvailable Reason Message
------------- ------ -------
         True
```

<span data-ttu-id="3a5bb-109">Mit diesem Befehl wird die Verfügbarkeit des Containerregistrierungsnamens \` SomeRegistryName \` überprüft.</span><span class="sxs-lookup"><span data-stu-id="3a5bb-109">This command checks the availability of the container registry name \`SomeRegistryName\`.</span></span>

## <span data-ttu-id="3a5bb-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3a5bb-110">PARAMETERS</span></span>

### <span data-ttu-id="3a5bb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a5bb-111">-DefaultProfile</span></span>
<span data-ttu-id="3a5bb-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="3a5bb-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3a5bb-113">-Name</span><span class="sxs-lookup"><span data-stu-id="3a5bb-113">-Name</span></span>
<span data-ttu-id="3a5bb-114">Containerregistrierungsname.</span><span class="sxs-lookup"><span data-stu-id="3a5bb-114">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a5bb-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a5bb-115">CommonParameters</span></span>
<span data-ttu-id="3a5bb-116">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a5bb-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a5bb-117">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3a5bb-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a5bb-118">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3a5bb-118">INPUTS</span></span>

### <span data-ttu-id="3a5bb-119">System.String</span><span class="sxs-lookup"><span data-stu-id="3a5bb-119">System.String</span></span>

## <span data-ttu-id="3a5bb-120">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3a5bb-120">OUTPUTS</span></span>

### <span data-ttu-id="3a5bb-121">Microsoft.Azure.Management.ContainerRegistry.Models.RegistryNameStatus</span><span class="sxs-lookup"><span data-stu-id="3a5bb-121">Microsoft.Azure.Management.ContainerRegistry.Models.RegistryNameStatus</span></span>

## <span data-ttu-id="3a5bb-122">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="3a5bb-122">NOTES</span></span>

## <span data-ttu-id="3a5bb-123">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="3a5bb-123">RELATED LINKS</span></span>

[<span data-ttu-id="3a5bb-124">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="3a5bb-124">New-AzContainerRegistry</span></span>]()

