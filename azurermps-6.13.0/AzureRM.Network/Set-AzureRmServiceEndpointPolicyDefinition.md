---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 1348eff2e4a2ac755ac0f425ddb29816438199b7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663120"
---
# <span data-ttu-id="64fed-101">Set-AzureRmServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="64fed-101">Set-AzureRmServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="64fed-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="64fed-102">SYNOPSIS</span></span>
<span data-ttu-id="64fed-103">{{Füllen Sie die Zusammenfassung aus}}</span><span class="sxs-lookup"><span data-stu-id="64fed-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64fed-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="64fed-104">SYNTAX</span></span>

```
Set-AzureRmServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <System.Collections.Generic.List`1[System.String]>]
 [-Service <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64fed-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="64fed-105">DESCRIPTION</span></span>
<span data-ttu-id="64fed-106">Das Cmdlet " **Satz-AzureRmServiceEndpointPolicyDefinition** " erstellt eine Dienstendpunkt-Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="64fed-106">The **Set-AzureRmServiceEndpointPolicyDefinition** cmdlet create a service endpoint policy definition.</span></span>

## <span data-ttu-id="64fed-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="64fed-107">EXAMPLES</span></span>

### <span data-ttu-id="64fed-108">Beispiel 1: aktualisiert eine Dienstendpunkt-Richtliniendefinition in einer Dienstendpunkt Richtlinie</span><span class="sxs-lookup"><span data-stu-id="64fed-108">Example 1: Updates a service endpoint policy definition in a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzureRmServiceEndpointPolicyDefinition -Name "Policydef1" -ServiceEndpointPolicy $serviceEndpointPolicy
```

<span data-ttu-id="64fed-109">Mit diesem Befehl wird eine Dienstendpunkt-Richtliniendefinition mit dem Namen Policydef1 in der vom Objekt $ServiceEndpointPolicy definierten Dienstendpunkt Richtlinie aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="64fed-109">This command updates a service endpoint policy definition named Policydef1 in the service endpoint policy defined by the object $ServiceEndpointPolicy.</span></span>

## <span data-ttu-id="64fed-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="64fed-110">PARAMETERS</span></span>

### <span data-ttu-id="64fed-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64fed-111">-DefaultProfile</span></span>
<span data-ttu-id="64fed-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="64fed-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64fed-113">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="64fed-113">-Description</span></span>
<span data-ttu-id="64fed-114">Die Beschreibung der Definition</span><span class="sxs-lookup"><span data-stu-id="64fed-114">The description of the definition</span></span>

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

### <span data-ttu-id="64fed-115">-Name</span><span class="sxs-lookup"><span data-stu-id="64fed-115">-Name</span></span>
<span data-ttu-id="64fed-116">Der Name der Regel</span><span class="sxs-lookup"><span data-stu-id="64fed-116">The name of the rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64fed-117">-Service</span><span class="sxs-lookup"><span data-stu-id="64fed-117">-Service</span></span>
<span data-ttu-id="64fed-118">Name des Diensts</span><span class="sxs-lookup"><span data-stu-id="64fed-118">Name of the service</span></span>

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

### <span data-ttu-id="64fed-119">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="64fed-119">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="64fed-120">Die NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="64fed-120">The NetworkSecurityGroup</span></span>

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

### <span data-ttu-id="64fed-121">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="64fed-121">-ServiceResource</span></span>
<span data-ttu-id="64fed-122">Liste der Dienst Ressourcen</span><span class="sxs-lookup"><span data-stu-id="64fed-122">List of service resources</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64fed-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64fed-123">CommonParameters</span></span>
<span data-ttu-id="64fed-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64fed-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="64fed-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64fed-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64fed-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="64fed-126">INPUTS</span></span>

### <span data-ttu-id="64fed-127">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="64fed-127">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="64fed-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="64fed-128">OUTPUTS</span></span>

### <span data-ttu-id="64fed-129">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="64fed-129">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="64fed-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="64fed-130">NOTES</span></span>

## <span data-ttu-id="64fed-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="64fed-131">RELATED LINKS</span></span>
