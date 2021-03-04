---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/get-azcontainerregistryusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryUsage.md
ms.openlocfilehash: 7a950bc3b375ea9d86ef71eda120ac1d92fbd8e9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938216"
---
# <span data-ttu-id="ddff6-101">Get-AzContainerRegistryUsage</span><span class="sxs-lookup"><span data-stu-id="ddff6-101">Get-AzContainerRegistryUsage</span></span>

## <span data-ttu-id="ddff6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ddff6-102">SYNOPSIS</span></span>
<span data-ttu-id="ddff6-103">Holen Sie sich die Verwendung einer Azure-Containerregistrierung.</span><span class="sxs-lookup"><span data-stu-id="ddff6-103">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="ddff6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ddff6-104">SYNTAX</span></span>

```
Get-AzContainerRegistryUsage -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ddff6-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ddff6-105">DESCRIPTION</span></span>
<span data-ttu-id="ddff6-106">Holen Sie sich die Verwendung einer Azure-Containerregistrierung.</span><span class="sxs-lookup"><span data-stu-id="ddff6-106">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="ddff6-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ddff6-107">EXAMPLES</span></span>

### <span data-ttu-id="ddff6-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ddff6-108">Example 1</span></span>
```powershell
PS C:\> Get-AzContainerRegistryUsage -ResourceGroupName $resourceGroupName -RegistryName $RegistryName
```

<span data-ttu-id="ddff6-109">Holen Sie sich die Verwendung einer Azure-Containerregistrierung.</span><span class="sxs-lookup"><span data-stu-id="ddff6-109">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="ddff6-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ddff6-110">PARAMETERS</span></span>

### <span data-ttu-id="ddff6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddff6-111">-DefaultProfile</span></span>
<span data-ttu-id="ddff6-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ddff6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddff6-113">-Name</span><span class="sxs-lookup"><span data-stu-id="ddff6-113">-Name</span></span>
<span data-ttu-id="ddff6-114">Zielregistrierungsname.</span><span class="sxs-lookup"><span data-stu-id="ddff6-114">Target registry name.</span></span>

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

### <span data-ttu-id="ddff6-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddff6-115">-ResourceGroupName</span></span>
<span data-ttu-id="ddff6-116">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ddff6-116">Resource group name.</span></span>

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

### <span data-ttu-id="ddff6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddff6-117">CommonParameters</span></span>
<span data-ttu-id="ddff6-118">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddff6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddff6-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ddff6-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddff6-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ddff6-120">INPUTS</span></span>

### <span data-ttu-id="ddff6-121">System.String</span><span class="sxs-lookup"><span data-stu-id="ddff6-121">System.String</span></span>

## <span data-ttu-id="ddff6-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ddff6-122">OUTPUTS</span></span>

### <span data-ttu-id="ddff6-123">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRegistryUsage</span><span class="sxs-lookup"><span data-stu-id="ddff6-123">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRegistryUsage</span></span>

## <span data-ttu-id="ddff6-124">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ddff6-124">NOTES</span></span>

## <span data-ttu-id="ddff6-125">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ddff6-125">RELATED LINKS</span></span>
