---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/test-azcontainerregistrynameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryNameAvailability.md
ms.openlocfilehash: 153ed152c68444327f379fda9ab5009290cbc00a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166690"
---
# <span data-ttu-id="895e9-101">Test-AzContainerRegistryNameAvailability</span><span class="sxs-lookup"><span data-stu-id="895e9-101">Test-AzContainerRegistryNameAvailability</span></span>

## <span data-ttu-id="895e9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="895e9-102">SYNOPSIS</span></span>
<span data-ttu-id="895e9-103">Überprüft die Verfügbarkeit eines Container Registrierungs namens.</span><span class="sxs-lookup"><span data-stu-id="895e9-103">Checks the availability of a container registry name.</span></span>

## <span data-ttu-id="895e9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="895e9-104">SYNTAX</span></span>

```
Test-AzContainerRegistryNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="895e9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="895e9-105">DESCRIPTION</span></span>
<span data-ttu-id="895e9-106">Das Test-AzContainerRegistryNameAvailability-Cmdlet überprüft, ob ein Container Registrierungsname gültig und für die Verwendung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="895e9-106">The Test-AzContainerRegistryNameAvailability cmdlet checks whether a container registry name is valid and available to use.</span></span>

## <span data-ttu-id="895e9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="895e9-107">EXAMPLES</span></span>

### <span data-ttu-id="895e9-108">Beispiel 1: überprüft die Verfügbarkeit eines Container Registrierungs namens</span><span class="sxs-lookup"><span data-stu-id="895e9-108">Example 1: Checks the availability of a container registry name</span></span>
```powershell
PS C:\>Test-AzContainerRegistryNameAvailability -Name 'SomeRegistryName'

NameAvailable Reason Message
------------- ------ -------
         True
```

<span data-ttu-id="895e9-109">Dieser Befehl überprüft die Verfügbarkeit des Container Registrierungs namens \` SomeRegistryName \` .</span><span class="sxs-lookup"><span data-stu-id="895e9-109">This command checks the availability of the container registry name \`SomeRegistryName\`.</span></span>

## <span data-ttu-id="895e9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="895e9-110">PARAMETERS</span></span>

### <span data-ttu-id="895e9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="895e9-111">-DefaultProfile</span></span>
<span data-ttu-id="895e9-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="895e9-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="895e9-113">-Name</span><span class="sxs-lookup"><span data-stu-id="895e9-113">-Name</span></span>
<span data-ttu-id="895e9-114">Container Registrierungs Name</span><span class="sxs-lookup"><span data-stu-id="895e9-114">Container Registry Name.</span></span>

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

### <span data-ttu-id="895e9-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="895e9-115">CommonParameters</span></span>
<span data-ttu-id="895e9-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="895e9-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="895e9-117">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="895e9-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="895e9-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="895e9-118">INPUTS</span></span>

### <span data-ttu-id="895e9-119">System. String</span><span class="sxs-lookup"><span data-stu-id="895e9-119">System.String</span></span>

## <span data-ttu-id="895e9-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="895e9-120">OUTPUTS</span></span>

### <span data-ttu-id="895e9-121">Microsoft. Azure. Management. ContainerRegistry. Models. RegistryNameStatus</span><span class="sxs-lookup"><span data-stu-id="895e9-121">Microsoft.Azure.Management.ContainerRegistry.Models.RegistryNameStatus</span></span>

## <span data-ttu-id="895e9-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="895e9-122">NOTES</span></span>

## <span data-ttu-id="895e9-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="895e9-123">RELATED LINKS</span></span>

[<span data-ttu-id="895e9-124">Neu – AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="895e9-124">New-AzContainerRegistry</span></span>]()

