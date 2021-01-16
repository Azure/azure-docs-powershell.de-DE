---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzSecurityPartnerProvider.md
ms.openlocfilehash: 07a29a17a1a7c17a0bbf7b202b019e7d833a5050
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357495"
---
# <span data-ttu-id="7cf6a-101">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="7cf6a-101">Set-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="7cf6a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7cf6a-102">SYNOPSIS</span></span>
<span data-ttu-id="7cf6a-103">Speichert einen geänderten Azure SecurityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="7cf6a-103">Saves a modified Azure SecurityPartnerProvider.</span></span>

## <span data-ttu-id="7cf6a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7cf6a-104">SYNTAX</span></span>

```
Set-AzSecurityPartnerProvider -SecurityPartnerProvider <PSSecurityPartnerProvider> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7cf6a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7cf6a-105">DESCRIPTION</span></span>
<span data-ttu-id="7cf6a-106">Das **Cmdlet Set-AzSecurityPartnerProvider** aktualisiert ein Azure SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="7cf6a-106">The **Set-AzSecurityPartnerProvider** cmdlet updates an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="7cf6a-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7cf6a-107">EXAMPLES</span></span>

### <span data-ttu-id="7cf6a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7cf6a-108">Example 1</span></span>
```powershell
$securityPartnerProvider = Get-AzSecurityPartnerProvider -ResourceGroupName securityPartnerProviderRG -Name securityPartnerProvider
Set-AzSecurityPartnerProvider -SecurityPartnerProvider $securityPartnerProvider
```


## <span data-ttu-id="7cf6a-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7cf6a-109">PARAMETERS</span></span>

### <span data-ttu-id="7cf6a-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7cf6a-110">-AsJob</span></span>
<span data-ttu-id="7cf6a-111">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="7cf6a-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7cf6a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cf6a-112">-DefaultProfile</span></span>
<span data-ttu-id="7cf6a-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7cf6a-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cf6a-114">-SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="7cf6a-114">-SecurityPartnerProvider</span></span>
<span data-ttu-id="7cf6a-115">The SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="7cf6a-115">The SecurityPartnerProvider</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7cf6a-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7cf6a-116">-Confirm</span></span>
<span data-ttu-id="7cf6a-117">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7cf6a-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cf6a-118">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="7cf6a-118">-WhatIf</span></span>
<span data-ttu-id="7cf6a-119">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7cf6a-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cf6a-120">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7cf6a-120">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cf6a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cf6a-121">CommonParameters</span></span>
<span data-ttu-id="7cf6a-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cf6a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cf6a-123">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7cf6a-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cf6a-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7cf6a-124">INPUTS</span></span>

### <span data-ttu-id="7cf6a-125">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="7cf6a-125">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="7cf6a-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7cf6a-126">OUTPUTS</span></span>

### <span data-ttu-id="7cf6a-127">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="7cf6a-127">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="7cf6a-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7cf6a-128">NOTES</span></span>

## <span data-ttu-id="7cf6a-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7cf6a-129">RELATED LINKS</span></span>
