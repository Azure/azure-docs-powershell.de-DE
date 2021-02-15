---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicy.md
ms.openlocfilehash: 5b2d10f3ffa2d00942b8198c598c9ec821dead99
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151380"
---
# <span data-ttu-id="43833-101">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="43833-101">Set-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="43833-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43833-102">SYNOPSIS</span></span>
<span data-ttu-id="43833-103">Aktualisiert eine Dienstendpunktrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="43833-103">Updates a service endpoint policy.</span></span>

## <span data-ttu-id="43833-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="43833-104">SYNTAX</span></span>

```
Set-AzServiceEndpointPolicy -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43833-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="43833-105">DESCRIPTION</span></span>
<span data-ttu-id="43833-106">Das **Cmdlet "Set-AzServiceEndpointPolicy"** erstellt eine Dienstendpunktrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="43833-106">The **Set-AzServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="43833-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="43833-107">EXAMPLES</span></span>

### <span data-ttu-id="43833-108">Beispiel 1: Legt eine Dienstendpunktrichtlinie fest</span><span class="sxs-lookup"><span data-stu-id="43833-108">Example 1: Sets a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicy $serviceEndpointPolicy -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="43833-109">Mit diesem Befehl wird eine Dienstendpunktrichtlinie namens "Richtlinie1" aktualisiert, die durch das Objekt definiert $serviceEndpointPolicy der Ressourcengruppe "resourcegroup1" angehören.</span><span class="sxs-lookup"><span data-stu-id="43833-109">This command updates a service endpoint policy named Policy1 defined by the object $serviceEndpointPolicy belong to the resourcegroup "resourcegroup1".</span></span>

## <span data-ttu-id="43833-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="43833-110">PARAMETERS</span></span>

### <span data-ttu-id="43833-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43833-111">-DefaultProfile</span></span>
<span data-ttu-id="43833-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="43833-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43833-113">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="43833-113">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="43833-114">The ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="43833-114">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="43833-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="43833-115">-Confirm</span></span>
<span data-ttu-id="43833-116">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="43833-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43833-117">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="43833-117">-WhatIf</span></span>
<span data-ttu-id="43833-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="43833-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="43833-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="43833-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43833-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43833-120">CommonParameters</span></span>
<span data-ttu-id="43833-121">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43833-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43833-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43833-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43833-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="43833-123">INPUTS</span></span>

### <span data-ttu-id="43833-124">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="43833-124">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="43833-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="43833-125">OUTPUTS</span></span>

### <span data-ttu-id="43833-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="43833-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="43833-127">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="43833-127">NOTES</span></span>

## <span data-ttu-id="43833-128">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="43833-128">RELATED LINKS</span></span>

[<span data-ttu-id="43833-129">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="43833-129">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="43833-130">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="43833-130">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="43833-131">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="43833-131">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)
