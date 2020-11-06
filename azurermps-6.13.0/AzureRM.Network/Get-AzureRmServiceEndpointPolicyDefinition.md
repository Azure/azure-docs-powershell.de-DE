---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 547b38fd30f09a305c63054b2f27d33db5ae6a86
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501122"
---
# <span data-ttu-id="c2b46-101">Get-AzureRmServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c2b46-101">Get-AzureRmServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="c2b46-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c2b46-102">SYNOPSIS</span></span>
<span data-ttu-id="c2b46-103">{{Füllen Sie die Zusammenfassung aus}}</span><span class="sxs-lookup"><span data-stu-id="c2b46-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2b46-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2b46-104">SYNTAX</span></span>

```
Get-AzureRmServiceEndpointPolicyDefinition [-Name <String>] -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2b46-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c2b46-105">DESCRIPTION</span></span>
<span data-ttu-id="c2b46-106">Das Cmdlet " **Get-AzureRmServiceEndpointPolicyDefinition** " Ruft eine Dienstendpunkt-Richtliniendefinition ab.</span><span class="sxs-lookup"><span data-stu-id="c2b46-106">The **Get-AzureRmServiceEndpointPolicyDefinition** cmdlet gets a service endpoint policy definition.</span></span>

## <span data-ttu-id="c2b46-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c2b46-107">EXAMPLES</span></span>

### <span data-ttu-id="c2b46-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c2b46-108">Example 1</span></span>
```
$policydef= Get-AzureRmServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ServiceEndpointPolicy $Policy
```

<span data-ttu-id="c2b46-109">Dieser Befehl ruft die Dienstendpunkt-Richtliniendefinition mit dem Namen ServiceEndpointPolicyDefinition1 in ServiceEndpointPolicy ab $Policy speichert Sie in der $policydef-Variablen.</span><span class="sxs-lookup"><span data-stu-id="c2b46-109">This command gets the service endpoint policy definition named ServiceEndpointPolicyDefinition1 in ServiceEndpointPolicy $Policy stores it in the $policydef variable.</span></span>

## <span data-ttu-id="c2b46-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c2b46-110">PARAMETERS</span></span>

### <span data-ttu-id="c2b46-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2b46-111">-DefaultProfile</span></span>
<span data-ttu-id="c2b46-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c2b46-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2b46-113">-Name</span><span class="sxs-lookup"><span data-stu-id="c2b46-113">-Name</span></span>
<span data-ttu-id="c2b46-114">Der Name der Dienstendpunkt-Richtliniendefinition</span><span class="sxs-lookup"><span data-stu-id="c2b46-114">The name of the service endpoint policy definition</span></span>

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

### <span data-ttu-id="c2b46-115">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="c2b46-115">-ResourceId</span></span>
<span data-ttu-id="c2b46-116">{{Fill resourcel Description}}</span><span class="sxs-lookup"><span data-stu-id="c2b46-116">{{Fill ResourceId Description}}</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2b46-117">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="c2b46-117">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="c2b46-118">Die Dienstendpunkt Richtlinie</span><span class="sxs-lookup"><span data-stu-id="c2b46-118">The Service endpoint policy</span></span>

```yaml
Type: PSServiceEndpointPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2b46-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c2b46-119">-Confirm</span></span>
<span data-ttu-id="c2b46-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c2b46-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2b46-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2b46-121">-WhatIf</span></span>
<span data-ttu-id="c2b46-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c2b46-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c2b46-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c2b46-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2b46-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2b46-124">CommonParameters</span></span>
<span data-ttu-id="c2b46-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2b46-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2b46-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2b46-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2b46-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c2b46-127">INPUTS</span></span>

### <span data-ttu-id="c2b46-128">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="c2b46-128">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="c2b46-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c2b46-129">OUTPUTS</span></span>

### <span data-ttu-id="c2b46-130">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c2b46-130">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="c2b46-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="c2b46-131">NOTES</span></span>

## <span data-ttu-id="c2b46-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c2b46-132">RELATED LINKS</span></span>
