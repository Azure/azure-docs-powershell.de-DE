---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 73B1EB7E-568E-44E8-993A-91678B7D8AEE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountKey.md
ms.openlocfilehash: f9b9f48d671bd0cbae0b7f8a26eccb21f372c4ef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497830"
---
# <span data-ttu-id="65e3a-101">Get-AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="65e3a-101">Get-AzureRmCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="65e3a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="65e3a-102">SYNOPSIS</span></span>
<span data-ttu-id="65e3a-103">Ruft die API-Schlüssel für ein Konto ab.</span><span class="sxs-lookup"><span data-stu-id="65e3a-103">Gets the API keys for an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65e3a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="65e3a-104">SYNTAX</span></span>

```
Get-AzureRmCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65e3a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="65e3a-105">DESCRIPTION</span></span>
<span data-ttu-id="65e3a-106">Das Cmdlet " **Get-AzureRmCognitiveServicesAccountKey** " Ruft die API-Schlüssel für ein bereitgestelltes Cognitive Services-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="65e3a-106">The **Get-AzureRmCognitiveServicesAccountKey** cmdlet gets the API keys for a provisioned Cognitive Services account.</span></span>

<span data-ttu-id="65e3a-107">Ein Cognitive Services-Konto verfügt über zwei API-Schlüssel: key1 und key2.</span><span class="sxs-lookup"><span data-stu-id="65e3a-107">A Cognitive Services account has two API keys: Key1 and Key2.</span></span>
<span data-ttu-id="65e3a-108">Die Tasten ermöglichen die Interaktion mit dem Endpunkt des Cognitive Services-Kontos.</span><span class="sxs-lookup"><span data-stu-id="65e3a-108">The keys enable interaction with the Cognitive Services account endpoint.</span></span>

<span data-ttu-id="65e3a-109">Verwenden Sie New-AzureRmCognitiveServicesAccountKey, um einen Schlüssel neu zu generieren.</span><span class="sxs-lookup"><span data-stu-id="65e3a-109">Use New-AzureRmCognitiveServicesAccountKey to regenerate a key.</span></span>

## <span data-ttu-id="65e3a-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="65e3a-110">EXAMPLES</span></span>

## <span data-ttu-id="65e3a-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="65e3a-111">PARAMETERS</span></span>

### <span data-ttu-id="65e3a-112">-Name</span><span class="sxs-lookup"><span data-stu-id="65e3a-112">-Name</span></span>
<span data-ttu-id="65e3a-113">Gibt den Namen des Kontos an.</span><span class="sxs-lookup"><span data-stu-id="65e3a-113">Specifies the name of the account.</span></span>
<span data-ttu-id="65e3a-114">Dieses Cmdlet ruft die Schlüssel für dieses Konto ab.</span><span class="sxs-lookup"><span data-stu-id="65e3a-114">This cmdlet gets the keys for this account.</span></span>

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

### <span data-ttu-id="65e3a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65e3a-115">-ResourceGroupName</span></span>
<span data-ttu-id="65e3a-116">Gibt den Namen der Ressourcengruppe an, der das Konto zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="65e3a-116">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="65e3a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65e3a-117">-DefaultProfile</span></span>
<span data-ttu-id="65e3a-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="65e3a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65e3a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65e3a-119">CommonParameters</span></span>
<span data-ttu-id="65e3a-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65e3a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65e3a-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65e3a-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65e3a-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="65e3a-122">INPUTS</span></span>

## <span data-ttu-id="65e3a-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="65e3a-123">OUTPUTS</span></span>

### <span data-ttu-id="65e3a-124">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="65e3a-124">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="65e3a-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="65e3a-125">NOTES</span></span>

## <span data-ttu-id="65e3a-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="65e3a-126">RELATED LINKS</span></span>

[<span data-ttu-id="65e3a-127">Neu – AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="65e3a-127">New-AzureRmCognitiveServicesAccountKey</span></span>](./New-AzureRmCognitiveServicesAccountKey.md)


