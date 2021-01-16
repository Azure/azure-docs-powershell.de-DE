---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistryusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryUsage.md
ms.openlocfilehash: e7d84439b2292d70604f3f7d9e827a0d8cc035e5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98293411"
---
# <span data-ttu-id="a9aef-101">Get-AzContainerRegistryUsage</span><span class="sxs-lookup"><span data-stu-id="a9aef-101">Get-AzContainerRegistryUsage</span></span>

## <span data-ttu-id="a9aef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9aef-102">SYNOPSIS</span></span>
<span data-ttu-id="a9aef-103">Holen Sie sich die Verwendung einer Azure-Container-Registrierung.</span><span class="sxs-lookup"><span data-stu-id="a9aef-103">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="a9aef-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a9aef-104">SYNTAX</span></span>

```
Get-AzContainerRegistryUsage -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9aef-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a9aef-105">DESCRIPTION</span></span>
<span data-ttu-id="a9aef-106">Holen Sie sich die Verwendung einer Azure-Container-Registrierung.</span><span class="sxs-lookup"><span data-stu-id="a9aef-106">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="a9aef-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a9aef-107">EXAMPLES</span></span>

### <span data-ttu-id="a9aef-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a9aef-108">Example 1</span></span>
```powershell
PS C:\> Get-AzContainerRegistryUsage -ResourceGroupName $resourceGroupName -RegistryName $RegistryName
```

<span data-ttu-id="a9aef-109">Holen Sie sich die Verwendung einer Azure-Container-Registrierung.</span><span class="sxs-lookup"><span data-stu-id="a9aef-109">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="a9aef-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a9aef-110">PARAMETERS</span></span>

### <span data-ttu-id="a9aef-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9aef-111">-DefaultProfile</span></span>
<span data-ttu-id="a9aef-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a9aef-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9aef-113">-Name</span><span class="sxs-lookup"><span data-stu-id="a9aef-113">-Name</span></span>
<span data-ttu-id="a9aef-114">Zielregistrierungsname</span><span class="sxs-lookup"><span data-stu-id="a9aef-114">Target registry name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RegistryName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9aef-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9aef-115">-ResourceGroupName</span></span>
<span data-ttu-id="a9aef-116">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="a9aef-116">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9aef-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9aef-117">CommonParameters</span></span>
<span data-ttu-id="a9aef-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9aef-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9aef-119">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a9aef-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9aef-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a9aef-120">INPUTS</span></span>

### <span data-ttu-id="a9aef-121">System.String</span><span class="sxs-lookup"><span data-stu-id="a9aef-121">System.String</span></span>

## <span data-ttu-id="a9aef-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a9aef-122">OUTPUTS</span></span>

### <span data-ttu-id="a9aef-123">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRegistryUsage</span><span class="sxs-lookup"><span data-stu-id="a9aef-123">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRegistryUsage</span></span>

## <span data-ttu-id="a9aef-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a9aef-124">NOTES</span></span>

## <span data-ttu-id="a9aef-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a9aef-125">RELATED LINKS</span></span>
