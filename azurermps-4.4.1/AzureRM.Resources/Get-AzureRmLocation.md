---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: DC870E11-2129-4906-8357-D9BC1CF2E08E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmLocation.md
ms.openlocfilehash: 62acee0398c9530a54e02c2347bf384498b07196
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503961"
---
# <span data-ttu-id="1da04-101">Get-AzureRmLocation</span><span class="sxs-lookup"><span data-stu-id="1da04-101">Get-AzureRmLocation</span></span>

## <span data-ttu-id="1da04-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1da04-102">SYNOPSIS</span></span>
<span data-ttu-id="1da04-103">Ruft alle Speicherorte und die unterstützten Ressourcenanbieter für jeden Standort ab.</span><span class="sxs-lookup"><span data-stu-id="1da04-103">Gets all locations and the supported resource providers for each location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1da04-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1da04-104">SYNTAX</span></span>

```
Get-AzureRmLocation [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1da04-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1da04-105">DESCRIPTION</span></span>
<span data-ttu-id="1da04-106">Das Cmdlet " **Get-AzureRmLocation** " ruft alle Speicherorte und die unterstützten Ressourcenanbieter für jeden Standort ab.</span><span class="sxs-lookup"><span data-stu-id="1da04-106">The **Get-AzureRmLocation** cmdlet gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="1da04-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1da04-107">EXAMPLES</span></span>

### <span data-ttu-id="1da04-108">Beispiel 1: Abrufen aller Speicherorte und der unterstützten Ressourcenanbieter</span><span class="sxs-lookup"><span data-stu-id="1da04-108">Example 1: Get all locations and the supported resource providers</span></span>
```
PS C:\>Get-AzureRmLocation
```

<span data-ttu-id="1da04-109">Dieser Befehl ruft alle Speicherorte und die unterstützten Ressourcenanbieter für jeden Standort ab.</span><span class="sxs-lookup"><span data-stu-id="1da04-109">This command gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="1da04-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1da04-110">PARAMETERS</span></span>

### <span data-ttu-id="1da04-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="1da04-111">-ApiVersion</span></span>
<span data-ttu-id="1da04-112">Gibt die API-Version an, die vom Ressourcenanbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="1da04-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="1da04-113">Sie können eine andere Version als die Standard Version angeben.</span><span class="sxs-lookup"><span data-stu-id="1da04-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="1da04-114">-Pre</span><span class="sxs-lookup"><span data-stu-id="1da04-114">-Pre</span></span>
<span data-ttu-id="1da04-115">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="1da04-115">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="1da04-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1da04-116">-DefaultProfile</span></span>
<span data-ttu-id="1da04-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1da04-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1da04-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1da04-118">CommonParameters</span></span>
<span data-ttu-id="1da04-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1da04-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1da04-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1da04-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1da04-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1da04-121">INPUTS</span></span>

## <span data-ttu-id="1da04-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1da04-122">OUTPUTS</span></span>

### <span data-ttu-id="1da04-123">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSResourceProviderLocation]</span><span class="sxs-lookup"><span data-stu-id="1da04-123">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProviderLocation]</span></span>

## <span data-ttu-id="1da04-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="1da04-124">NOTES</span></span>

## <span data-ttu-id="1da04-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1da04-125">RELATED LINKS</span></span>

