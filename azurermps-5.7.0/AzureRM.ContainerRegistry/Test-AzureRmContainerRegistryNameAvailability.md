---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/test-azurermcontainerregistrynameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryNameAvailability.md
ms.openlocfilehash: da415c21532ea0b2178cc2a75d6a3d09bdc2d50b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497662"
---
# <span data-ttu-id="3ea51-101">Test-AzureRmContainerRegistryNameAvailability</span><span class="sxs-lookup"><span data-stu-id="3ea51-101">Test-AzureRmContainerRegistryNameAvailability</span></span>

## <span data-ttu-id="3ea51-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3ea51-102">SYNOPSIS</span></span>
<span data-ttu-id="3ea51-103">Überprüft die Verfügbarkeit eines Container Registrierungs namens.</span><span class="sxs-lookup"><span data-stu-id="3ea51-103">Checks the availability of a container registry name.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ea51-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3ea51-104">SYNTAX</span></span>

```
Test-AzureRmContainerRegistryNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3ea51-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3ea51-105">DESCRIPTION</span></span>
<span data-ttu-id="3ea51-106">Das Test-AzureRmContainerRegistryNameAvailability-Cmdlet überprüft, ob ein Container Registrierungsname gültig und für die Verwendung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="3ea51-106">The Test-AzureRmContainerRegistryNameAvailability cmdlet checks whether a container registry name is valid and available to use.</span></span>

## <span data-ttu-id="3ea51-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3ea51-107">EXAMPLES</span></span>

### <span data-ttu-id="3ea51-108">Beispiel 1: überprüft die Verfügbarkeit eines Container Registrierungs namens</span><span class="sxs-lookup"><span data-stu-id="3ea51-108">Example 1: Checks the availability of a container registry name</span></span>
```powershell
PS C:\>Test-AzureRmContainerRegistryNameAvailability -Name 'SomeRegistryName'

NameAvailable Reason Message
------------- ------ -------
         True
```

<span data-ttu-id="3ea51-109">Dieser Befehl überprüft die Verfügbarkeit des Container Registrierungs namens \` SomeRegistryName \` .</span><span class="sxs-lookup"><span data-stu-id="3ea51-109">This command checks the availability of the container registry name \`SomeRegistryName\`.</span></span>

## <span data-ttu-id="3ea51-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3ea51-110">PARAMETERS</span></span>

### <span data-ttu-id="3ea51-111">-Name</span><span class="sxs-lookup"><span data-stu-id="3ea51-111">-Name</span></span>
<span data-ttu-id="3ea51-112">Container Registrierungs Name</span><span class="sxs-lookup"><span data-stu-id="3ea51-112">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ea51-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ea51-113">-DefaultProfile</span></span>
<span data-ttu-id="3ea51-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="3ea51-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3ea51-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ea51-115">CommonParameters</span></span>
<span data-ttu-id="3ea51-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ea51-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ea51-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ea51-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ea51-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3ea51-118">INPUTS</span></span>

### <span data-ttu-id="3ea51-119">Keine</span><span class="sxs-lookup"><span data-stu-id="3ea51-119">None</span></span>
<span data-ttu-id="3ea51-120">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="3ea51-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3ea51-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3ea51-121">OUTPUTS</span></span>

### <span data-ttu-id="3ea51-122">Microsoft. Azure. Management. ContainerRegistry. Models. RegistryNameStatus</span><span class="sxs-lookup"><span data-stu-id="3ea51-122">Microsoft.Azure.Management.ContainerRegistry.Models.RegistryNameStatus</span></span>

## <span data-ttu-id="3ea51-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="3ea51-123">NOTES</span></span>

## <span data-ttu-id="3ea51-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3ea51-124">RELATED LINKS</span></span>

[<span data-ttu-id="3ea51-125">Neu – AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="3ea51-125">New-AzureRmContainerRegistry</span></span>]()

