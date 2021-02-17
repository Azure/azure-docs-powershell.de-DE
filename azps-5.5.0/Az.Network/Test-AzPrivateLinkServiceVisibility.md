---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-azprivatelinkservicevisibility
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateLinkServiceVisibility.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateLinkServiceVisibility.md
ms.openlocfilehash: f443928a8a616e8b8c6c13e5ae941aff607638ef
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158772"
---
# <span data-ttu-id="c8c08-101">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="c8c08-101">Test-AzPrivateLinkServiceVisibility</span></span>

## <span data-ttu-id="c8c08-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8c08-102">SYNOPSIS</span></span>
<span data-ttu-id="c8c08-103">Mit **"Test-AzPrivateLinkServiceVisibility"** wird überprüft, ob ein privater Linkdienst für die aktuelle Verwendung sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="c8c08-103">The **Test-AzPrivateLinkServiceVisibility** checks whether a private link service is visible for current use.</span></span>

## <span data-ttu-id="c8c08-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c8c08-104">SYNTAX</span></span>

```
Test-AzPrivateLinkServiceVisibility -Location <String> [-ResourceGroupName <String>]
 -PrivateLinkServiceAlias <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8c08-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c8c08-105">DESCRIPTION</span></span>
<span data-ttu-id="c8c08-106">Überprüfen Sie, ob ein privater Linkdienst für die aktuelle Verwendung sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="c8c08-106">Check whether a private link service is visible for current use.</span></span>

## <span data-ttu-id="c8c08-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c8c08-107">EXAMPLES</span></span>

### <span data-ttu-id="c8c08-108">Beispiel 1: Überprüfen Sie, contoso.cloudapp.azure.com für die Verwendung zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="c8c08-108">Example 1: Check if contoso.cloudapp.azure.com is available for use.</span></span>
```
Test-AzPrivateLinkServiceVisibility -Location westus -PrivateLinkServiceAlias "TestPLS.00000000-0000-0000-0000-000000000000.azure.privatelinkservice"
```

## <span data-ttu-id="c8c08-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c8c08-109">PARAMETERS</span></span>

### <span data-ttu-id="c8c08-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8c08-110">-DefaultProfile</span></span>
<span data-ttu-id="c8c08-111">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c8c08-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8c08-112">-Location</span><span class="sxs-lookup"><span data-stu-id="c8c08-112">-Location</span></span>
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

### <span data-ttu-id="c8c08-113">-PrivateLinkServiceAlias</span><span class="sxs-lookup"><span data-stu-id="c8c08-113">-PrivateLinkServiceAlias</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8c08-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8c08-114">-ResourceGroupName</span></span>
<span data-ttu-id="c8c08-115">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="c8c08-115">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="c8c08-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8c08-116">CommonParameters</span></span>
<span data-ttu-id="c8c08-117">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8c08-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8c08-118">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c8c08-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8c08-119">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c8c08-119">INPUTS</span></span>

### <span data-ttu-id="c8c08-120">Keine</span><span class="sxs-lookup"><span data-stu-id="c8c08-120">None</span></span>

## <span data-ttu-id="c8c08-121">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c8c08-121">OUTPUTS</span></span>

### <span data-ttu-id="c8c08-122">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c8c08-122">System.Boolean</span></span>

## <span data-ttu-id="c8c08-123">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c8c08-123">NOTES</span></span>

## <span data-ttu-id="c8c08-124">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c8c08-124">RELATED LINKS</span></span>
