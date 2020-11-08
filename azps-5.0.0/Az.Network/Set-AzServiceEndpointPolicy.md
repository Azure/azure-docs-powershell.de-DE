---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicy.md
ms.openlocfilehash: 5b2d10f3ffa2d00942b8198c598c9ec821dead99
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177791"
---
# <span data-ttu-id="ab76d-101">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="ab76d-101">Set-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="ab76d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ab76d-102">SYNOPSIS</span></span>
<span data-ttu-id="ab76d-103">Aktualisiert eine Dienstendpunkt Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="ab76d-103">Updates a service endpoint policy.</span></span>

## <span data-ttu-id="ab76d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ab76d-104">SYNTAX</span></span>

```
Set-AzServiceEndpointPolicy -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab76d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ab76d-105">DESCRIPTION</span></span>
<span data-ttu-id="ab76d-106">Das Cmdlet " **festlegen-AzServiceEndpointPolicy** " erstellt eine Dienstendpunkt Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="ab76d-106">The **Set-AzServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="ab76d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ab76d-107">EXAMPLES</span></span>

### <span data-ttu-id="ab76d-108">Beispiel 1: Festlegen einer Dienstendpunkt Richtlinie</span><span class="sxs-lookup"><span data-stu-id="ab76d-108">Example 1: Sets a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicy $serviceEndpointPolicy -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="ab76d-109">Mit diesem Befehl wird eine Dienstendpunkt Richtlinie mit dem Namen "Fischereipolitik1" aktualisiert, die durch das Objekt definiert ist $serviceEndpointPolicy der "resourcegroup1"-ResourceGroup angehören.</span><span class="sxs-lookup"><span data-stu-id="ab76d-109">This command updates a service endpoint policy named Policy1 defined by the object $serviceEndpointPolicy belong to the resourcegroup "resourcegroup1".</span></span>

## <span data-ttu-id="ab76d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ab76d-110">PARAMETERS</span></span>

### <span data-ttu-id="ab76d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab76d-111">-DefaultProfile</span></span>
<span data-ttu-id="ab76d-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ab76d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab76d-113">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="ab76d-113">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="ab76d-114">Die ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="ab76d-114">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="ab76d-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ab76d-115">-Confirm</span></span>
<span data-ttu-id="ab76d-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ab76d-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab76d-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab76d-117">-WhatIf</span></span>
<span data-ttu-id="ab76d-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ab76d-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ab76d-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ab76d-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab76d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab76d-120">CommonParameters</span></span>
<span data-ttu-id="ab76d-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab76d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab76d-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab76d-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab76d-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ab76d-123">INPUTS</span></span>

### <span data-ttu-id="ab76d-124">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="ab76d-124">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="ab76d-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ab76d-125">OUTPUTS</span></span>

### <span data-ttu-id="ab76d-126">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="ab76d-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="ab76d-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="ab76d-127">NOTES</span></span>

## <span data-ttu-id="ab76d-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ab76d-128">RELATED LINKS</span></span>

[<span data-ttu-id="ab76d-129">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="ab76d-129">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="ab76d-130">Neu – AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="ab76d-130">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="ab76d-131">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="ab76d-131">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)
