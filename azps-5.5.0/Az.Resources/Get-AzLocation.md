---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: DC870E11-2129-4906-8357-D9BC1CF2E08E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzLocation.md
ms.openlocfilehash: f14da4760f70c8e4ba95136b81a884f830f4f44a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100146060"
---
# <span data-ttu-id="22f84-101">Get-AzLocation</span><span class="sxs-lookup"><span data-stu-id="22f84-101">Get-AzLocation</span></span>

## <span data-ttu-id="22f84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22f84-102">SYNOPSIS</span></span>
<span data-ttu-id="22f84-103">Ruft alle Speicherorte und die unterstützten Ressourcenanbieter für jeden Standort ab.</span><span class="sxs-lookup"><span data-stu-id="22f84-103">Gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="22f84-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="22f84-104">SYNTAX</span></span>

```
Get-AzLocation [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22f84-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="22f84-105">DESCRIPTION</span></span>
<span data-ttu-id="22f84-106">Das **Cmdlet "Get-AzLocation"** ruft alle Speicherorte und die unterstützten Ressourcenanbieter für jeden Standort ab.</span><span class="sxs-lookup"><span data-stu-id="22f84-106">The **Get-AzLocation** cmdlet gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="22f84-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="22f84-107">EXAMPLES</span></span>

### <span data-ttu-id="22f84-108">Beispiel 1: Alle Speicherorte und die unterstützten Ressourcenanbieter erhalten</span><span class="sxs-lookup"><span data-stu-id="22f84-108">Example 1: Get all locations and the supported resource providers</span></span>
```
PS C:\>Get-AzLocation
```

<span data-ttu-id="22f84-109">Dieser Befehl ruft alle Speicherorte und die unterstützten Ressourcenanbieter für jeden Standort ab.</span><span class="sxs-lookup"><span data-stu-id="22f84-109">This command gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="22f84-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22f84-110">PARAMETERS</span></span>

### <span data-ttu-id="22f84-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="22f84-111">-ApiVersion</span></span>
<span data-ttu-id="22f84-112">Gibt die vom Ressourcenanbieter unterstützte API-Version an.</span><span class="sxs-lookup"><span data-stu-id="22f84-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="22f84-113">Sie können eine andere Version als die Standardversion angeben.</span><span class="sxs-lookup"><span data-stu-id="22f84-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="22f84-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22f84-114">-DefaultProfile</span></span>
<span data-ttu-id="22f84-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="22f84-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="22f84-116">-Pre</span><span class="sxs-lookup"><span data-stu-id="22f84-116">-Pre</span></span>
<span data-ttu-id="22f84-117">Gibt an, dass dieses Cmdlet Vorabversions-API-Versionen berücksichtigt, wenn automatisch bestimmt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="22f84-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="22f84-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22f84-118">CommonParameters</span></span>
<span data-ttu-id="22f84-119">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22f84-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22f84-120">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="22f84-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22f84-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="22f84-121">INPUTS</span></span>

### <span data-ttu-id="22f84-122">Keine</span><span class="sxs-lookup"><span data-stu-id="22f84-122">None</span></span>

## <span data-ttu-id="22f84-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="22f84-123">OUTPUTS</span></span>

### <span data-ttu-id="22f84-124">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProviderLocation</span><span class="sxs-lookup"><span data-stu-id="22f84-124">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProviderLocation</span></span>

## <span data-ttu-id="22f84-125">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="22f84-125">NOTES</span></span>

## <span data-ttu-id="22f84-126">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="22f84-126">RELATED LINKS</span></span>
