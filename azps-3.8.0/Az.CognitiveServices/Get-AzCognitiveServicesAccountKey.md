---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 73B1EB7E-568E-44E8-993A-91678B7D8AEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountKey.md
ms.openlocfilehash: 8150abc726f990b699237dbaad3641a99bae2e2c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995019"
---
# <span data-ttu-id="6172a-101">Get-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="6172a-101">Get-AzCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="6172a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6172a-102">SYNOPSIS</span></span>
<span data-ttu-id="6172a-103">Ruft die API-Schlüssel für ein Konto ab.</span><span class="sxs-lookup"><span data-stu-id="6172a-103">Gets the API keys for an account.</span></span>

## <span data-ttu-id="6172a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6172a-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6172a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6172a-105">DESCRIPTION</span></span>
<span data-ttu-id="6172a-106">Das Cmdlet " **Get-AzCognitiveServicesAccountKey** " Ruft die API-Schlüssel für ein bereitgestelltes Cognitive Services-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="6172a-106">The **Get-AzCognitiveServicesAccountKey** cmdlet gets the API keys for a provisioned Cognitive Services account.</span></span>
<span data-ttu-id="6172a-107">Ein Cognitive Services-Konto verfügt über zwei API-Schlüssel: key1 und key2.</span><span class="sxs-lookup"><span data-stu-id="6172a-107">A Cognitive Services account has two API keys: Key1 and Key2.</span></span>
<span data-ttu-id="6172a-108">Die Tasten ermöglichen die Interaktion mit dem Endpunkt des Cognitive Services-Kontos.</span><span class="sxs-lookup"><span data-stu-id="6172a-108">The keys enable interaction with the Cognitive Services account endpoint.</span></span>
<span data-ttu-id="6172a-109">Verwenden Sie New-AzCognitiveServicesAccountKey, um einen Schlüssel neu zu generieren.</span><span class="sxs-lookup"><span data-stu-id="6172a-109">Use New-AzCognitiveServicesAccountKey to regenerate a key.</span></span>

## <span data-ttu-id="6172a-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6172a-110">EXAMPLES</span></span>

### <span data-ttu-id="6172a-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6172a-111">Example 1</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountKey -ResourceGroupName cognitive-services-resource-group -name myluis

Key1                             Key2
----                             ----
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

## <span data-ttu-id="6172a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="6172a-112">PARAMETERS</span></span>

### <span data-ttu-id="6172a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6172a-113">-DefaultProfile</span></span>
<span data-ttu-id="6172a-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="6172a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6172a-115">-Name</span><span class="sxs-lookup"><span data-stu-id="6172a-115">-Name</span></span>
<span data-ttu-id="6172a-116">Gibt den Namen des Kontos an.</span><span class="sxs-lookup"><span data-stu-id="6172a-116">Specifies the name of the account.</span></span>
<span data-ttu-id="6172a-117">Dieses Cmdlet ruft die Schlüssel für dieses Konto ab.</span><span class="sxs-lookup"><span data-stu-id="6172a-117">This cmdlet gets the keys for this account.</span></span>

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

### <span data-ttu-id="6172a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6172a-118">-ResourceGroupName</span></span>
<span data-ttu-id="6172a-119">Gibt den Namen der Ressourcengruppe an, der das Konto zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="6172a-119">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="6172a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6172a-120">CommonParameters</span></span>
<span data-ttu-id="6172a-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6172a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6172a-122">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6172a-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6172a-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6172a-123">INPUTS</span></span>

### <span data-ttu-id="6172a-124">System. String</span><span class="sxs-lookup"><span data-stu-id="6172a-124">System.String</span></span>

## <span data-ttu-id="6172a-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6172a-125">OUTPUTS</span></span>

### <span data-ttu-id="6172a-126">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="6172a-126">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="6172a-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="6172a-127">NOTES</span></span>

## <span data-ttu-id="6172a-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6172a-128">RELATED LINKS</span></span>

[<span data-ttu-id="6172a-129">Neu – AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="6172a-129">New-AzCognitiveServicesAccountKey</span></span>](./New-AzCognitiveServicesAccountKey.md)


