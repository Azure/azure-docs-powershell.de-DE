---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicy.md
ms.openlocfilehash: e8cf8b2abebd20b514d0bae2ad220d3e702f04f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946968"
---
# <span data-ttu-id="afbab-101">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="afbab-101">Set-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="afbab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="afbab-102">SYNOPSIS</span></span>
<span data-ttu-id="afbab-103">Aktualisiert eine Dienstendpunktrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="afbab-103">Updates a service endpoint policy.</span></span>

## <span data-ttu-id="afbab-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="afbab-104">SYNTAX</span></span>

```
Set-AzServiceEndpointPolicy -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afbab-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="afbab-105">DESCRIPTION</span></span>
<span data-ttu-id="afbab-106">Das **Cmdlet Set-AzServiceEndpointPolicy** erstellt eine Dienstendpunktrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="afbab-106">The **Set-AzServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="afbab-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="afbab-107">EXAMPLES</span></span>

### <span data-ttu-id="afbab-108">Beispiel 1: Legt eine Dienstendpunktrichtlinie fest</span><span class="sxs-lookup"><span data-stu-id="afbab-108">Example 1: Sets a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicy $serviceEndpointPolicy -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="afbab-109">Mit diesem Befehl wird eine Dienstendpunktrichtlinie namens "Richtlinie1" aktualisiert, die vom Objekt definiert $serviceEndpointPolicy der Ressourcengruppe "resourcegroup1" angehören.</span><span class="sxs-lookup"><span data-stu-id="afbab-109">This command updates a service endpoint policy named Policy1 defined by the object $serviceEndpointPolicy belong to the resourcegroup "resourcegroup1".</span></span>

## <span data-ttu-id="afbab-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="afbab-110">PARAMETERS</span></span>

### <span data-ttu-id="afbab-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afbab-111">-DefaultProfile</span></span>
<span data-ttu-id="afbab-112">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="afbab-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="afbab-113">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="afbab-113">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="afbab-114">The ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="afbab-114">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="afbab-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="afbab-115">-Confirm</span></span>
<span data-ttu-id="afbab-116">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="afbab-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afbab-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afbab-117">-WhatIf</span></span>
<span data-ttu-id="afbab-118">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="afbab-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="afbab-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="afbab-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afbab-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afbab-120">CommonParameters</span></span>
<span data-ttu-id="afbab-121">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afbab-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afbab-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afbab-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afbab-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="afbab-123">INPUTS</span></span>

### <span data-ttu-id="afbab-124">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="afbab-124">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="afbab-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="afbab-125">OUTPUTS</span></span>

### <span data-ttu-id="afbab-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="afbab-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="afbab-127">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="afbab-127">NOTES</span></span>

## <span data-ttu-id="afbab-128">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="afbab-128">RELATED LINKS</span></span>

[<span data-ttu-id="afbab-129">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="afbab-129">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="afbab-130">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="afbab-130">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="afbab-131">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="afbab-131">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)
