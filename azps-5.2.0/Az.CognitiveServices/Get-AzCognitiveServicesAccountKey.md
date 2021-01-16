---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 73B1EB7E-568E-44E8-993A-91678B7D8AEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountKey.md
ms.openlocfilehash: 8150abc726f990b699237dbaad3641a99bae2e2c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98293446"
---
# <span data-ttu-id="18ebc-101">Get-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="18ebc-101">Get-AzCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="18ebc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18ebc-102">SYNOPSIS</span></span>
<span data-ttu-id="18ebc-103">Ruft die API-Schlüssel für ein Konto ab.</span><span class="sxs-lookup"><span data-stu-id="18ebc-103">Gets the API keys for an account.</span></span>

## <span data-ttu-id="18ebc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="18ebc-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18ebc-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="18ebc-105">DESCRIPTION</span></span>
<span data-ttu-id="18ebc-106">Das **Cmdlet "Get-AzCognitiveServicesAccountKey"** ruft die API-Schlüssel für ein bereitgestelltes Cognitive Services-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="18ebc-106">The **Get-AzCognitiveServicesAccountKey** cmdlet gets the API keys for a provisioned Cognitive Services account.</span></span>
<span data-ttu-id="18ebc-107">Ein Cognitive Services-Konto verfügt über zwei API-Schlüssel: Schlüssel1 und Schlüssel2.</span><span class="sxs-lookup"><span data-stu-id="18ebc-107">A Cognitive Services account has two API keys: Key1 and Key2.</span></span>
<span data-ttu-id="18ebc-108">Die Schlüssel ermöglichen die Interaktion mit dem Endpunkt des Cognitive Services-Kontos.</span><span class="sxs-lookup"><span data-stu-id="18ebc-108">The keys enable interaction with the Cognitive Services account endpoint.</span></span>
<span data-ttu-id="18ebc-109">Verwenden New-AzCognitiveServicesAccountKey zum erneuten Generierten eines Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="18ebc-109">Use New-AzCognitiveServicesAccountKey to regenerate a key.</span></span>

## <span data-ttu-id="18ebc-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="18ebc-110">EXAMPLES</span></span>

### <span data-ttu-id="18ebc-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="18ebc-111">Example 1</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountKey -ResourceGroupName cognitive-services-resource-group -name myluis

Key1                             Key2
----                             ----
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

## <span data-ttu-id="18ebc-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="18ebc-112">PARAMETERS</span></span>

### <span data-ttu-id="18ebc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18ebc-113">-DefaultProfile</span></span>
<span data-ttu-id="18ebc-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="18ebc-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="18ebc-115">-Name</span><span class="sxs-lookup"><span data-stu-id="18ebc-115">-Name</span></span>
<span data-ttu-id="18ebc-116">Gibt den Namen des Kontos an.</span><span class="sxs-lookup"><span data-stu-id="18ebc-116">Specifies the name of the account.</span></span>
<span data-ttu-id="18ebc-117">Dieses Cmdlet ruft die Schlüssel für dieses Konto ab.</span><span class="sxs-lookup"><span data-stu-id="18ebc-117">This cmdlet gets the keys for this account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18ebc-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18ebc-118">-ResourceGroupName</span></span>
<span data-ttu-id="18ebc-119">Gibt den Namen der Ressourcengruppe an, der das Konto zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="18ebc-119">Specifies the name of the resource group the account is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18ebc-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18ebc-120">CommonParameters</span></span>
<span data-ttu-id="18ebc-121">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18ebc-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18ebc-122">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="18ebc-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18ebc-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="18ebc-123">INPUTS</span></span>

### <span data-ttu-id="18ebc-124">System.String</span><span class="sxs-lookup"><span data-stu-id="18ebc-124">System.String</span></span>

## <span data-ttu-id="18ebc-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="18ebc-125">OUTPUTS</span></span>

### <span data-ttu-id="18ebc-126">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="18ebc-126">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="18ebc-127">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="18ebc-127">NOTES</span></span>

## <span data-ttu-id="18ebc-128">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="18ebc-128">RELATED LINKS</span></span>

[<span data-ttu-id="18ebc-129">New-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="18ebc-129">New-AzCognitiveServicesAccountKey</span></span>](./New-AzCognitiveServicesAccountKey.md)


