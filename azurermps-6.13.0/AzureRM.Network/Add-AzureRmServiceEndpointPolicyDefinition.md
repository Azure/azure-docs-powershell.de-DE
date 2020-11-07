---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmServiceEndpointPolicyDefinition.md
ms.openlocfilehash: ac58450295e0e2d988c12c308c0210b38ad71b4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664035"
---
# <span data-ttu-id="acc92-101">Add-AzureRmServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="acc92-101">Add-AzureRmServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="acc92-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="acc92-102">SYNOPSIS</span></span>
<span data-ttu-id="acc92-103">Fügt eine Dienstendpunkt-Richtliniendefinition zu einer angegebenen Richtlinie hinzu.</span><span class="sxs-lookup"><span data-stu-id="acc92-103">Adds a service endpoint policy definition to a specified policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="acc92-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="acc92-104">SYNTAX</span></span>

```
Add-AzureRmServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <System.Collections.Generic.List`1[System.String]>]
 [-Service <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="acc92-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="acc92-105">DESCRIPTION</span></span>
<span data-ttu-id="acc92-106">Das **Add-AzureRmServiceEndpointPolicyDefinition-** Cmdlet fügt der Richtlinie eine Dienstendpunkt-Richtliniendefinition hinzu.</span><span class="sxs-lookup"><span data-stu-id="acc92-106">The **Add-AzureRmServiceEndpointPolicyDefinition** cmdlet add a service endpoint policy definition to the policy.</span></span>

## <span data-ttu-id="acc92-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="acc92-107">EXAMPLES</span></span>

### <span data-ttu-id="acc92-108">Beispiel 1: aktualisiert eine Dienstendpunkt-Richtliniendefinition in einer Dienstendpunkt Richtlinie</span><span class="sxs-lookup"><span data-stu-id="acc92-108">Example 1: Updates a service endpoint policy definition in a service endpoint policy</span></span>
```
$policydef= New-AzureRmServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ResourceGroupName "ResourceGroup01" -Service "Microsoft.Storage" -ServiceResources "subscriptions/sub1" -Description "New Definition"
```

<span data-ttu-id="acc92-109">Dieser Befehl hat die Definition der Dienstendpunkt Richtlinie mit dem Namen ServiceEndpointPolicyDefinition1, dem Dienst Microsoft. Storage, den Dienst Ressourcen Abonnements/-Sub1 und der Beschreibung "neue Definition" aktualisiert, die zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert Sie in der $policydef Variablen.</span><span class="sxs-lookup"><span data-stu-id="acc92-109">This command updated the service endpoint policy definition with name ServiceEndpointPolicyDefinition1,  service Microsoft.Storage, service resources subscriptions/sub1 and description "New Definition" that belongs to the resource group named ResourceGroup01 and stores it in the $policydef variable.</span></span>

## <span data-ttu-id="acc92-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="acc92-110">PARAMETERS</span></span>

### <span data-ttu-id="acc92-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acc92-111">-DefaultProfile</span></span>
<span data-ttu-id="acc92-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="acc92-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="acc92-113">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="acc92-113">-Description</span></span>
<span data-ttu-id="acc92-114">Die Beschreibung der Definition</span><span class="sxs-lookup"><span data-stu-id="acc92-114">The description of the definition</span></span>

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

### <span data-ttu-id="acc92-115">-Name</span><span class="sxs-lookup"><span data-stu-id="acc92-115">-Name</span></span>
<span data-ttu-id="acc92-116">Der Name der Dienstendpunkt-Richtliniendefinition</span><span class="sxs-lookup"><span data-stu-id="acc92-116">The name of the service endpoint policy definition</span></span>

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

### <span data-ttu-id="acc92-117">-Service</span><span class="sxs-lookup"><span data-stu-id="acc92-117">-Service</span></span>
<span data-ttu-id="acc92-118">Name des Diensts</span><span class="sxs-lookup"><span data-stu-id="acc92-118">Name of the service</span></span>

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

### <span data-ttu-id="acc92-119">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="acc92-119">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="acc92-120">Die ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="acc92-120">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="acc92-121">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="acc92-121">-ServiceResource</span></span>
<span data-ttu-id="acc92-122">Liste der Dienst Ressourcen</span><span class="sxs-lookup"><span data-stu-id="acc92-122">List of service resources</span></span>

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

### <span data-ttu-id="acc92-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acc92-123">CommonParameters</span></span>
<span data-ttu-id="acc92-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acc92-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="acc92-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="acc92-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acc92-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="acc92-126">INPUTS</span></span>

### <span data-ttu-id="acc92-127">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="acc92-127">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="acc92-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="acc92-128">OUTPUTS</span></span>

### <span data-ttu-id="acc92-129">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="acc92-129">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="acc92-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="acc92-130">NOTES</span></span>

## <span data-ttu-id="acc92-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="acc92-131">RELATED LINKS</span></span>
