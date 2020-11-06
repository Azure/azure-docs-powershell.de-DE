---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 12d809ad4c1df021891ab5acf384415d64aa08a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501998"
---
# <span data-ttu-id="48eca-101">New-AzureRmServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="48eca-101">New-AzureRmServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="48eca-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="48eca-102">SYNOPSIS</span></span>
<span data-ttu-id="48eca-103">{{Füllen Sie die Zusammenfassung aus}}</span><span class="sxs-lookup"><span data-stu-id="48eca-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48eca-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="48eca-104">SYNTAX</span></span>

```
New-AzureRmServiceEndpointPolicyDefinition -Name <String> [-Description <String>]
 [-ServiceResource <System.Collections.Generic.List`1[System.String]>] [-Service <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48eca-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="48eca-105">DESCRIPTION</span></span>
<span data-ttu-id="48eca-106">Mit dem Cmdlet **New-AzureRmServiceEndpointPolicyDefinition** erstellen Sie eine Definition für Dienstendpunkt Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="48eca-106">The **New-AzureRmServiceEndpointPolicyDefinition** cmdlet create a service endpoint policy definition.</span></span>

## <span data-ttu-id="48eca-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="48eca-107">EXAMPLES</span></span>

### <span data-ttu-id="48eca-108">Beispiel 1: Erstellen einer Dienstendpunkt Richtlinie</span><span class="sxs-lookup"><span data-stu-id="48eca-108">Example 1: Creates a service endpoint policy</span></span>
```
$policydef= New-AzureRmServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ResourceGroupName "ResourceGroup01" -Service "Microsoft.Storage" -ServiceResources "subscriptions/sub1" -Description "New Definition"
```

<span data-ttu-id="48eca-109">Mit diesem Befehl wird die Definition der Dienstendpunkt Richtlinie mit dem Namen ServiceEndpointPolicyDefinition1, dem Dienst Microsoft. Storage, den Dienst Ressourcen Abonnements/-Sub1 und der Beschreibung "neue Definition" erstellt, die zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und in der $policydef-Variablen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="48eca-109">This command creates the service endpoint policy definition with name ServiceEndpointPolicyDefinition1,  service Microsoft.Storage, service resources subscriptions/sub1 and description "New Definition" that belongs to the resource group named ResourceGroup01 and stores it in the $policydef variable.</span></span>

## <span data-ttu-id="48eca-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="48eca-110">PARAMETERS</span></span>

### <span data-ttu-id="48eca-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48eca-111">-DefaultProfile</span></span>
<span data-ttu-id="48eca-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="48eca-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48eca-113">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="48eca-113">-Description</span></span>
<span data-ttu-id="48eca-114">Die Beschreibung der Definition</span><span class="sxs-lookup"><span data-stu-id="48eca-114">The description of the definition</span></span>

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

### <span data-ttu-id="48eca-115">-Name</span><span class="sxs-lookup"><span data-stu-id="48eca-115">-Name</span></span>
<span data-ttu-id="48eca-116">Der Name der Dienstendpunkt Richtlinie</span><span class="sxs-lookup"><span data-stu-id="48eca-116">The name of the service endpoint policy</span></span>

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

### <span data-ttu-id="48eca-117">-Service</span><span class="sxs-lookup"><span data-stu-id="48eca-117">-Service</span></span>
<span data-ttu-id="48eca-118">Name des Diensts</span><span class="sxs-lookup"><span data-stu-id="48eca-118">Name of the service</span></span>

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

### <span data-ttu-id="48eca-119">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="48eca-119">-ServiceResource</span></span>
<span data-ttu-id="48eca-120">Liste der Dienst Ressourcen</span><span class="sxs-lookup"><span data-stu-id="48eca-120">List of service resources</span></span>

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

### <span data-ttu-id="48eca-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48eca-121">CommonParameters</span></span>
<span data-ttu-id="48eca-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48eca-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="48eca-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48eca-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48eca-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="48eca-124">INPUTS</span></span>

### <span data-ttu-id="48eca-125">Keine</span><span class="sxs-lookup"><span data-stu-id="48eca-125">None</span></span>


## <span data-ttu-id="48eca-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="48eca-126">OUTPUTS</span></span>

### <span data-ttu-id="48eca-127">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="48eca-127">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>


## <span data-ttu-id="48eca-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="48eca-128">NOTES</span></span>

## <span data-ttu-id="48eca-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="48eca-129">RELATED LINKS</span></span>
