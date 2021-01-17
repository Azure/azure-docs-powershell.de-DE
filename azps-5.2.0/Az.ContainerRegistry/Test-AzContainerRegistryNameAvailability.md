---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/test-azcontainerregistrynameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryNameAvailability.md
ms.openlocfilehash: 153ed152c68444327f379fda9ab5009290cbc00a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98302800"
---
# <span data-ttu-id="edcb7-101">Test-AzContainerRegistryNameAvailability</span><span class="sxs-lookup"><span data-stu-id="edcb7-101">Test-AzContainerRegistryNameAvailability</span></span>

## <span data-ttu-id="edcb7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="edcb7-102">SYNOPSIS</span></span>
<span data-ttu-id="edcb7-103">Überprüft die Verfügbarkeit eines Containerregistrierungsnamens.</span><span class="sxs-lookup"><span data-stu-id="edcb7-103">Checks the availability of a container registry name.</span></span>

## <span data-ttu-id="edcb7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="edcb7-104">SYNTAX</span></span>

```
Test-AzContainerRegistryNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="edcb7-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="edcb7-105">DESCRIPTION</span></span>
<span data-ttu-id="edcb7-106">Das Test-AzContainerRegistryNameAvailability cmdlet überprüft, ob ein Containerregistrierungsname gültig und verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="edcb7-106">The Test-AzContainerRegistryNameAvailability cmdlet checks whether a container registry name is valid and available to use.</span></span>

## <span data-ttu-id="edcb7-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="edcb7-107">EXAMPLES</span></span>

### <span data-ttu-id="edcb7-108">Beispiel 1: Überprüft die Verfügbarkeit eines Containerregistrierungsnamens</span><span class="sxs-lookup"><span data-stu-id="edcb7-108">Example 1: Checks the availability of a container registry name</span></span>
```powershell
PS C:\>Test-AzContainerRegistryNameAvailability -Name 'SomeRegistryName'

NameAvailable Reason Message
------------- ------ -------
         True
```

<span data-ttu-id="edcb7-109">Mit diesem Befehl wird die Verfügbarkeit des Containerregistrierungsnamens \` "SomeRegistryName" \` überprüft.</span><span class="sxs-lookup"><span data-stu-id="edcb7-109">This command checks the availability of the container registry name \`SomeRegistryName\`.</span></span>

## <span data-ttu-id="edcb7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="edcb7-110">PARAMETERS</span></span>

### <span data-ttu-id="edcb7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edcb7-111">-DefaultProfile</span></span>
<span data-ttu-id="edcb7-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="edcb7-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="edcb7-113">-Name</span><span class="sxs-lookup"><span data-stu-id="edcb7-113">-Name</span></span>
<span data-ttu-id="edcb7-114">Containerregistrierungsname.</span><span class="sxs-lookup"><span data-stu-id="edcb7-114">Container Registry Name.</span></span>

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

### <span data-ttu-id="edcb7-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edcb7-115">CommonParameters</span></span>
<span data-ttu-id="edcb7-116">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edcb7-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edcb7-117">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="edcb7-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edcb7-118">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="edcb7-118">INPUTS</span></span>

### <span data-ttu-id="edcb7-119">System.String</span><span class="sxs-lookup"><span data-stu-id="edcb7-119">System.String</span></span>

## <span data-ttu-id="edcb7-120">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="edcb7-120">OUTPUTS</span></span>

### <span data-ttu-id="edcb7-121">Microsoft.Azure.Management.ContainerRegistry.Models.RegistryNameStatus</span><span class="sxs-lookup"><span data-stu-id="edcb7-121">Microsoft.Azure.Management.ContainerRegistry.Models.RegistryNameStatus</span></span>

## <span data-ttu-id="edcb7-122">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="edcb7-122">NOTES</span></span>

## <span data-ttu-id="edcb7-123">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="edcb7-123">RELATED LINKS</span></span>

[<span data-ttu-id="edcb7-124">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="edcb7-124">New-AzContainerRegistry</span></span>]()

