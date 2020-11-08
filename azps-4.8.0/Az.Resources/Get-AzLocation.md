---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: DC870E11-2129-4906-8357-D9BC1CF2E08E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzLocation.md
ms.openlocfilehash: f14da4760f70c8e4ba95136b81a884f830f4f44a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94167391"
---
# <span data-ttu-id="24c09-101">Get-AzLocation</span><span class="sxs-lookup"><span data-stu-id="24c09-101">Get-AzLocation</span></span>

## <span data-ttu-id="24c09-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="24c09-102">SYNOPSIS</span></span>
<span data-ttu-id="24c09-103">Ruft alle Speicherorte und die unterstützten Ressourcenanbieter für jeden Standort ab.</span><span class="sxs-lookup"><span data-stu-id="24c09-103">Gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="24c09-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="24c09-104">SYNTAX</span></span>

```
Get-AzLocation [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24c09-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="24c09-105">DESCRIPTION</span></span>
<span data-ttu-id="24c09-106">Das Cmdlet " **Get-AzLocation** " ruft alle Speicherorte und die unterstützten Ressourcenanbieter für jeden Standort ab.</span><span class="sxs-lookup"><span data-stu-id="24c09-106">The **Get-AzLocation** cmdlet gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="24c09-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="24c09-107">EXAMPLES</span></span>

### <span data-ttu-id="24c09-108">Beispiel 1: Abrufen aller Speicherorte und der unterstützten Ressourcenanbieter</span><span class="sxs-lookup"><span data-stu-id="24c09-108">Example 1: Get all locations and the supported resource providers</span></span>
```
PS C:\>Get-AzLocation
```

<span data-ttu-id="24c09-109">Dieser Befehl ruft alle Speicherorte und die unterstützten Ressourcenanbieter für jeden Standort ab.</span><span class="sxs-lookup"><span data-stu-id="24c09-109">This command gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="24c09-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="24c09-110">PARAMETERS</span></span>

### <span data-ttu-id="24c09-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="24c09-111">-ApiVersion</span></span>
<span data-ttu-id="24c09-112">Gibt die API-Version an, die vom Ressourcenanbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="24c09-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="24c09-113">Sie können eine andere Version als die Standard Version angeben.</span><span class="sxs-lookup"><span data-stu-id="24c09-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="24c09-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24c09-114">-DefaultProfile</span></span>
<span data-ttu-id="24c09-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="24c09-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="24c09-116">-Pre</span><span class="sxs-lookup"><span data-stu-id="24c09-116">-Pre</span></span>
<span data-ttu-id="24c09-117">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="24c09-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="24c09-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24c09-118">CommonParameters</span></span>
<span data-ttu-id="24c09-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24c09-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24c09-120">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="24c09-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24c09-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="24c09-121">INPUTS</span></span>

### <span data-ttu-id="24c09-122">Keine</span><span class="sxs-lookup"><span data-stu-id="24c09-122">None</span></span>

## <span data-ttu-id="24c09-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="24c09-123">OUTPUTS</span></span>

### <span data-ttu-id="24c09-124">Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSResourceProviderLocation</span><span class="sxs-lookup"><span data-stu-id="24c09-124">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProviderLocation</span></span>

## <span data-ttu-id="24c09-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="24c09-125">NOTES</span></span>

## <span data-ttu-id="24c09-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="24c09-126">RELATED LINKS</span></span>
