---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: DC870E11-2129-4906-8357-D9BC1CF2E08E
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzLocation.md
ms.openlocfilehash: 22b9d3322baa146bcd916024b15eea96b824f2eb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944759"
---
# <span data-ttu-id="5f9f1-101">Get-AzLocation</span><span class="sxs-lookup"><span data-stu-id="5f9f1-101">Get-AzLocation</span></span>

## <span data-ttu-id="5f9f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f9f1-102">SYNOPSIS</span></span>
<span data-ttu-id="5f9f1-103">Ruft alle Speicherorte und die unterstützten Ressourcenanbieter für jeden Speicherort ab.</span><span class="sxs-lookup"><span data-stu-id="5f9f1-103">Gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="5f9f1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5f9f1-104">SYNTAX</span></span>

```
Get-AzLocation [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f9f1-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5f9f1-105">DESCRIPTION</span></span>
<span data-ttu-id="5f9f1-106">Das **Get-AzLocation-Cmdlet** ruft alle Speicherorte und die unterstützten Ressourcenanbieter für jeden Speicherort ab.</span><span class="sxs-lookup"><span data-stu-id="5f9f1-106">The **Get-AzLocation** cmdlet gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="5f9f1-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5f9f1-107">EXAMPLES</span></span>

### <span data-ttu-id="5f9f1-108">Beispiel 1: Alle Speicherorte und die unterstützten Ressourcenanbieter erhalten</span><span class="sxs-lookup"><span data-stu-id="5f9f1-108">Example 1: Get all locations and the supported resource providers</span></span>
```
PS C:\>Get-AzLocation
```

<span data-ttu-id="5f9f1-109">Dieser Befehl ruft alle Speicherorte und die unterstützten Ressourcenanbieter für jeden Speicherort ab.</span><span class="sxs-lookup"><span data-stu-id="5f9f1-109">This command gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="5f9f1-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5f9f1-110">PARAMETERS</span></span>

### <span data-ttu-id="5f9f1-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="5f9f1-111">-ApiVersion</span></span>
<span data-ttu-id="5f9f1-112">Gibt die vom Ressourcenanbieter unterstützte API-Version an.</span><span class="sxs-lookup"><span data-stu-id="5f9f1-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="5f9f1-113">Sie können eine andere Version als die Standardversion angeben.</span><span class="sxs-lookup"><span data-stu-id="5f9f1-113">You can specify a different version than the default version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f9f1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f9f1-114">-DefaultProfile</span></span>
<span data-ttu-id="5f9f1-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="5f9f1-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5f9f1-116">-Pre</span><span class="sxs-lookup"><span data-stu-id="5f9f1-116">-Pre</span></span>
<span data-ttu-id="5f9f1-117">Gibt an, dass dieses Cmdlet Vorabversions-API-Versionen berücksichtigt, wenn automatisch bestimmt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5f9f1-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f9f1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f9f1-118">CommonParameters</span></span>
<span data-ttu-id="5f9f1-119">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f9f1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f9f1-120">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5f9f1-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f9f1-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5f9f1-121">INPUTS</span></span>

### <span data-ttu-id="5f9f1-122">Keine</span><span class="sxs-lookup"><span data-stu-id="5f9f1-122">None</span></span>

## <span data-ttu-id="5f9f1-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5f9f1-123">OUTPUTS</span></span>

### <span data-ttu-id="5f9f1-124">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProviderLocation</span><span class="sxs-lookup"><span data-stu-id="5f9f1-124">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProviderLocation</span></span>

## <span data-ttu-id="5f9f1-125">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5f9f1-125">NOTES</span></span>

## <span data-ttu-id="5f9f1-126">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5f9f1-126">RELATED LINKS</span></span>
