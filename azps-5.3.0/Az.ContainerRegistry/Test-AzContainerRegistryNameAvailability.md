---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/test-azcontainerregistrynameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryNameAvailability.md
ms.openlocfilehash: 153ed152c68444327f379fda9ab5009290cbc00a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472873"
---
# <span data-ttu-id="1b2af-101">Test-AzContainerRegistryNameAvailability</span><span class="sxs-lookup"><span data-stu-id="1b2af-101">Test-AzContainerRegistryNameAvailability</span></span>

## <span data-ttu-id="1b2af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b2af-102">SYNOPSIS</span></span>
<span data-ttu-id="1b2af-103">Überprüft die Verfügbarkeit eines Containerregistrierungsnamens.</span><span class="sxs-lookup"><span data-stu-id="1b2af-103">Checks the availability of a container registry name.</span></span>

## <span data-ttu-id="1b2af-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1b2af-104">SYNTAX</span></span>

```
Test-AzContainerRegistryNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1b2af-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1b2af-105">DESCRIPTION</span></span>
<span data-ttu-id="1b2af-106">Das Test-AzContainerRegistryNameAvailability cmdlet überprüft, ob ein Containerregistrierungsname gültig und verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="1b2af-106">The Test-AzContainerRegistryNameAvailability cmdlet checks whether a container registry name is valid and available to use.</span></span>

## <span data-ttu-id="1b2af-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1b2af-107">EXAMPLES</span></span>

### <span data-ttu-id="1b2af-108">Beispiel 1: Überprüft die Verfügbarkeit eines Containerregistrierungsnamens</span><span class="sxs-lookup"><span data-stu-id="1b2af-108">Example 1: Checks the availability of a container registry name</span></span>
```powershell
PS C:\>Test-AzContainerRegistryNameAvailability -Name 'SomeRegistryName'

NameAvailable Reason Message
------------- ------ -------
         True
```

<span data-ttu-id="1b2af-109">Mit diesem Befehl wird die Verfügbarkeit des Containerregistrierungsnamens \` "SomeRegistryName" \` überprüft.</span><span class="sxs-lookup"><span data-stu-id="1b2af-109">This command checks the availability of the container registry name \`SomeRegistryName\`.</span></span>

## <span data-ttu-id="1b2af-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1b2af-110">PARAMETERS</span></span>

### <span data-ttu-id="1b2af-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b2af-111">-DefaultProfile</span></span>
<span data-ttu-id="1b2af-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="1b2af-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1b2af-113">-Name</span><span class="sxs-lookup"><span data-stu-id="1b2af-113">-Name</span></span>
<span data-ttu-id="1b2af-114">Containerregistrierungsname.</span><span class="sxs-lookup"><span data-stu-id="1b2af-114">Container Registry Name.</span></span>

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

### <span data-ttu-id="1b2af-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b2af-115">CommonParameters</span></span>
<span data-ttu-id="1b2af-116">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b2af-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b2af-117">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1b2af-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b2af-118">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1b2af-118">INPUTS</span></span>

### <span data-ttu-id="1b2af-119">System.String</span><span class="sxs-lookup"><span data-stu-id="1b2af-119">System.String</span></span>

## <span data-ttu-id="1b2af-120">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1b2af-120">OUTPUTS</span></span>

### <span data-ttu-id="1b2af-121">Microsoft.Azure.Management.ContainerRegistry.Models.RegistryNameStatus</span><span class="sxs-lookup"><span data-stu-id="1b2af-121">Microsoft.Azure.Management.ContainerRegistry.Models.RegistryNameStatus</span></span>

## <span data-ttu-id="1b2af-122">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1b2af-122">NOTES</span></span>

## <span data-ttu-id="1b2af-123">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1b2af-123">RELATED LINKS</span></span>

[<span data-ttu-id="1b2af-124">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1b2af-124">New-AzContainerRegistry</span></span>]()

