---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azautoapprovedprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAutoApprovedPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAutoApprovedPrivateLinkService.md
ms.openlocfilehash: b03aad1f76c5151746d50e69bc48ccf10e60842f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157049"
---
# <span data-ttu-id="b918c-101">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="b918c-101">Get-AzAutoApprovedPrivateLinkService</span></span>

## <span data-ttu-id="b918c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b918c-102">SYNOPSIS</span></span>
<span data-ttu-id="b918c-103">Ruft ein Array mit einer privaten Linkdienst-ID ab, die mit einem privaten Endpunkt verknüpft werden kann, der automatisch genehmigt wird.</span><span class="sxs-lookup"><span data-stu-id="b918c-103">Gets an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="b918c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b918c-104">SYNTAX</span></span>

```
Get-AzAutoApprovedPrivateLinkService -Location <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b918c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b918c-105">DESCRIPTION</span></span>
<span data-ttu-id="b918c-106">Der **Get-AzAutoApprovedPrivateLinkService** ruft ein Array mit einer privaten Linkdienst-ID ab, die mit einem privaten, automatisch genehmigten Endpunkt verknüpft werden kann.</span><span class="sxs-lookup"><span data-stu-id="b918c-106">The **Get-AzAutoApprovedPrivateLinkService** gets an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="b918c-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b918c-107">EXAMPLES</span></span>

### <span data-ttu-id="b918c-108">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b918c-108">Example</span></span>
```
Get-AzAutoApprovedPrivateLinkService -Location westus -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="b918c-109">Dieses Beispiel gibt ein Array mit einer privaten Linkdienst-ID zurück, die mit einem privaten, automatisch genehmigten Endpunkt verknüpft werden kann.</span><span class="sxs-lookup"><span data-stu-id="b918c-109">This example return an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="b918c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b918c-110">PARAMETERS</span></span>

### <span data-ttu-id="b918c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b918c-111">-DefaultProfile</span></span>
<span data-ttu-id="b918c-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b918c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b918c-113">-Location</span><span class="sxs-lookup"><span data-stu-id="b918c-113">-Location</span></span>
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

### <span data-ttu-id="b918c-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b918c-114">-ResourceGroupName</span></span>
<span data-ttu-id="b918c-115">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="b918c-115">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b918c-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b918c-116">CommonParameters</span></span>
<span data-ttu-id="b918c-117">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b918c-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b918c-118">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b918c-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b918c-119">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b918c-119">INPUTS</span></span>

### <span data-ttu-id="b918c-120">Keine</span><span class="sxs-lookup"><span data-stu-id="b918c-120">None</span></span>

## <span data-ttu-id="b918c-121">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b918c-121">OUTPUTS</span></span>

### <span data-ttu-id="b918c-122">Microsoft.Azure.Commands.Network.Models.PSAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="b918c-122">Microsoft.Azure.Commands.Network.Models.PSAutoApprovedPrivateLinkService</span></span>

## <span data-ttu-id="b918c-123">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b918c-123">NOTES</span></span>

## <span data-ttu-id="b918c-124">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b918c-124">RELATED LINKS</span></span>
