---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: DC870E11-2129-4906-8357-D9BC1CF2E08E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmLocation.md
ms.openlocfilehash: a3169a78747a34a831ed6bd738e5647c3a4d9eb5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500430"
---
# <span data-ttu-id="ab47f-101">Get-AzureRmLocation</span><span class="sxs-lookup"><span data-stu-id="ab47f-101">Get-AzureRmLocation</span></span>

## <span data-ttu-id="ab47f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ab47f-102">SYNOPSIS</span></span>
<span data-ttu-id="ab47f-103">Ruft alle Speicherorte und die unterstützten Ressourcenanbieter für jeden Standort ab.</span><span class="sxs-lookup"><span data-stu-id="ab47f-103">Gets all locations and the supported resource providers for each location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab47f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ab47f-104">SYNTAX</span></span>

```
Get-AzureRmLocation [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ab47f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ab47f-105">DESCRIPTION</span></span>
<span data-ttu-id="ab47f-106">Das Cmdlet " **Get-AzureRmLocation** " ruft alle Speicherorte und die unterstützten Ressourcenanbieter für jeden Standort ab.</span><span class="sxs-lookup"><span data-stu-id="ab47f-106">The **Get-AzureRmLocation** cmdlet gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="ab47f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ab47f-107">EXAMPLES</span></span>

### <span data-ttu-id="ab47f-108">Beispiel 1: Abrufen aller Speicherorte und der unterstützten Ressourcenanbieter</span><span class="sxs-lookup"><span data-stu-id="ab47f-108">Example 1: Get all locations and the supported resource providers</span></span>
```
PS C:\>Get-AzureRmLocation
```

<span data-ttu-id="ab47f-109">Dieser Befehl ruft alle Speicherorte und die unterstützten Ressourcenanbieter für jeden Standort ab.</span><span class="sxs-lookup"><span data-stu-id="ab47f-109">This command gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="ab47f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ab47f-110">PARAMETERS</span></span>

### <span data-ttu-id="ab47f-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ab47f-111">-ApiVersion</span></span>
<span data-ttu-id="ab47f-112">Gibt die API-Version an, die vom Ressourcenanbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="ab47f-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="ab47f-113">Sie können eine andere Version als die Standard Version angeben.</span><span class="sxs-lookup"><span data-stu-id="ab47f-113">You can specify a different version than the default version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab47f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab47f-114">-DefaultProfile</span></span>
<span data-ttu-id="ab47f-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="ab47f-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ab47f-116">-Pre</span><span class="sxs-lookup"><span data-stu-id="ab47f-116">-Pre</span></span>
<span data-ttu-id="ab47f-117">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="ab47f-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab47f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab47f-118">CommonParameters</span></span>
<span data-ttu-id="ab47f-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab47f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab47f-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab47f-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab47f-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ab47f-121">INPUTS</span></span>

### <span data-ttu-id="ab47f-122">Keine</span><span class="sxs-lookup"><span data-stu-id="ab47f-122">None</span></span>
<span data-ttu-id="ab47f-123">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="ab47f-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ab47f-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ab47f-124">OUTPUTS</span></span>

### <span data-ttu-id="ab47f-125">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSResourceProviderLocation]</span><span class="sxs-lookup"><span data-stu-id="ab47f-125">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProviderLocation]</span></span>

## <span data-ttu-id="ab47f-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="ab47f-126">NOTES</span></span>

## <span data-ttu-id="ab47f-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ab47f-127">RELATED LINKS</span></span>
