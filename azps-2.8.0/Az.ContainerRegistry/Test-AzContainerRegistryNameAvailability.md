---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/test-azcontainerregistrynameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryNameAvailability.md
ms.openlocfilehash: 114fd947cb69f14e0e67b8a48cbe8b26a7c34101
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651816"
---
# <span data-ttu-id="aaa7e-101">Test-AzContainerRegistryNameAvailability</span><span class="sxs-lookup"><span data-stu-id="aaa7e-101">Test-AzContainerRegistryNameAvailability</span></span>

## <span data-ttu-id="aaa7e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="aaa7e-102">SYNOPSIS</span></span>
<span data-ttu-id="aaa7e-103">Überprüft die Verfügbarkeit eines Container Registrierungs namens.</span><span class="sxs-lookup"><span data-stu-id="aaa7e-103">Checks the availability of a container registry name.</span></span>

## <span data-ttu-id="aaa7e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="aaa7e-104">SYNTAX</span></span>

```
Test-AzContainerRegistryNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aaa7e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aaa7e-105">DESCRIPTION</span></span>
<span data-ttu-id="aaa7e-106">Das Test-AzContainerRegistryNameAvailability-Cmdlet überprüft, ob ein Container Registrierungsname gültig und für die Verwendung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="aaa7e-106">The Test-AzContainerRegistryNameAvailability cmdlet checks whether a container registry name is valid and available to use.</span></span>

## <span data-ttu-id="aaa7e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="aaa7e-107">EXAMPLES</span></span>

### <span data-ttu-id="aaa7e-108">Beispiel 1: überprüft die Verfügbarkeit eines Container Registrierungs namens</span><span class="sxs-lookup"><span data-stu-id="aaa7e-108">Example 1: Checks the availability of a container registry name</span></span>
```powershell
PS C:\>Test-AzContainerRegistryNameAvailability -Name 'SomeRegistryName'

NameAvailable Reason Message
------------- ------ -------
         True
```

<span data-ttu-id="aaa7e-109">Dieser Befehl überprüft die Verfügbarkeit des Container Registrierungs namens \` SomeRegistryName \` .</span><span class="sxs-lookup"><span data-stu-id="aaa7e-109">This command checks the availability of the container registry name \`SomeRegistryName\`.</span></span>

## <span data-ttu-id="aaa7e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="aaa7e-110">PARAMETERS</span></span>

### <span data-ttu-id="aaa7e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaa7e-111">-DefaultProfile</span></span>
<span data-ttu-id="aaa7e-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="aaa7e-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aaa7e-113">-Name</span><span class="sxs-lookup"><span data-stu-id="aaa7e-113">-Name</span></span>
<span data-ttu-id="aaa7e-114">Container Registrierungs Name</span><span class="sxs-lookup"><span data-stu-id="aaa7e-114">Container Registry Name.</span></span>

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

### <span data-ttu-id="aaa7e-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaa7e-115">CommonParameters</span></span>
<span data-ttu-id="aaa7e-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aaa7e-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaa7e-117">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aaa7e-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaa7e-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="aaa7e-118">INPUTS</span></span>

### <span data-ttu-id="aaa7e-119">System. String</span><span class="sxs-lookup"><span data-stu-id="aaa7e-119">System.String</span></span>

## <span data-ttu-id="aaa7e-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="aaa7e-120">OUTPUTS</span></span>

### <span data-ttu-id="aaa7e-121">Microsoft. Azure. Management. ContainerRegistry. Models. RegistryNameStatus</span><span class="sxs-lookup"><span data-stu-id="aaa7e-121">Microsoft.Azure.Management.ContainerRegistry.Models.RegistryNameStatus</span></span>

## <span data-ttu-id="aaa7e-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="aaa7e-122">NOTES</span></span>

## <span data-ttu-id="aaa7e-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="aaa7e-123">RELATED LINKS</span></span>

[<span data-ttu-id="aaa7e-124">Neu – AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="aaa7e-124">New-AzContainerRegistry</span></span>]()

