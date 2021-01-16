---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicy.md
ms.openlocfilehash: 5b2d10f3ffa2d00942b8198c598c9ec821dead99
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357481"
---
# <span data-ttu-id="819f0-101">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="819f0-101">Set-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="819f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="819f0-102">SYNOPSIS</span></span>
<span data-ttu-id="819f0-103">Aktualisiert eine Dienstendpunktrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="819f0-103">Updates a service endpoint policy.</span></span>

## <span data-ttu-id="819f0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="819f0-104">SYNTAX</span></span>

```
Set-AzServiceEndpointPolicy -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="819f0-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="819f0-105">DESCRIPTION</span></span>
<span data-ttu-id="819f0-106">Das **Cmdlet "Set-AzServiceEndpointPolicy"** erstellt eine Dienstendpunktrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="819f0-106">The **Set-AzServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="819f0-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="819f0-107">EXAMPLES</span></span>

### <span data-ttu-id="819f0-108">Beispiel 1: Legt eine Dienstendpunktrichtlinie fest</span><span class="sxs-lookup"><span data-stu-id="819f0-108">Example 1: Sets a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicy $serviceEndpointPolicy -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="819f0-109">Mit diesem Befehl wird eine Dienstendpunktrichtlinie namens "Richtlinie1" aktualisiert, die durch das Objekt definiert $serviceEndpointPolicy der Ressourcengruppe "resourcegroup1" angehören.</span><span class="sxs-lookup"><span data-stu-id="819f0-109">This command updates a service endpoint policy named Policy1 defined by the object $serviceEndpointPolicy belong to the resourcegroup "resourcegroup1".</span></span>

## <span data-ttu-id="819f0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="819f0-110">PARAMETERS</span></span>

### <span data-ttu-id="819f0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="819f0-111">-DefaultProfile</span></span>
<span data-ttu-id="819f0-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="819f0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="819f0-113">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="819f0-113">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="819f0-114">The ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="819f0-114">The ServiceEndpointPolicy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="819f0-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="819f0-115">-Confirm</span></span>
<span data-ttu-id="819f0-116">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="819f0-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="819f0-117">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="819f0-117">-WhatIf</span></span>
<span data-ttu-id="819f0-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="819f0-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="819f0-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="819f0-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="819f0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="819f0-120">CommonParameters</span></span>
<span data-ttu-id="819f0-121">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="819f0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="819f0-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="819f0-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="819f0-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="819f0-123">INPUTS</span></span>

### <span data-ttu-id="819f0-124">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="819f0-124">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="819f0-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="819f0-125">OUTPUTS</span></span>

### <span data-ttu-id="819f0-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="819f0-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="819f0-127">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="819f0-127">NOTES</span></span>

## <span data-ttu-id="819f0-128">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="819f0-128">RELATED LINKS</span></span>

[<span data-ttu-id="819f0-129">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="819f0-129">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="819f0-130">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="819f0-130">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="819f0-131">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="819f0-131">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)
