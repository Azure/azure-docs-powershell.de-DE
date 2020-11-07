---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 73B1EB7E-568E-44E8-993A-91678B7D8AEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountKey.md
ms.openlocfilehash: 11285a805444c270740d7158f66aa538fecfa1b6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661597"
---
# <span data-ttu-id="3984f-101">Get-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="3984f-101">Get-AzCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="3984f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3984f-102">SYNOPSIS</span></span>
<span data-ttu-id="3984f-103">Ruft die API-Schlüssel für ein Konto ab.</span><span class="sxs-lookup"><span data-stu-id="3984f-103">Gets the API keys for an account.</span></span>

## <span data-ttu-id="3984f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3984f-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3984f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3984f-105">DESCRIPTION</span></span>
<span data-ttu-id="3984f-106">Das Cmdlet " **Get-AzCognitiveServicesAccountKey** " Ruft die API-Schlüssel für ein bereitgestelltes Cognitive Services-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="3984f-106">The **Get-AzCognitiveServicesAccountKey** cmdlet gets the API keys for a provisioned Cognitive Services account.</span></span>
<span data-ttu-id="3984f-107">Ein Cognitive Services-Konto verfügt über zwei API-Schlüssel: key1 und key2.</span><span class="sxs-lookup"><span data-stu-id="3984f-107">A Cognitive Services account has two API keys: Key1 and Key2.</span></span>
<span data-ttu-id="3984f-108">Die Tasten ermöglichen die Interaktion mit dem Endpunkt des Cognitive Services-Kontos.</span><span class="sxs-lookup"><span data-stu-id="3984f-108">The keys enable interaction with the Cognitive Services account endpoint.</span></span>
<span data-ttu-id="3984f-109">Verwenden Sie New-AzCognitiveServicesAccountKey, um einen Schlüssel neu zu generieren.</span><span class="sxs-lookup"><span data-stu-id="3984f-109">Use New-AzCognitiveServicesAccountKey to regenerate a key.</span></span>

## <span data-ttu-id="3984f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3984f-110">EXAMPLES</span></span>

### <span data-ttu-id="3984f-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3984f-111">Example 1</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountKey -ResourceGroupName cognitive-services-resource-group -name myluis

Key1                             Key2
----                             ----
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

## <span data-ttu-id="3984f-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="3984f-112">PARAMETERS</span></span>

### <span data-ttu-id="3984f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3984f-113">-DefaultProfile</span></span>
<span data-ttu-id="3984f-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="3984f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3984f-115">-Name</span><span class="sxs-lookup"><span data-stu-id="3984f-115">-Name</span></span>
<span data-ttu-id="3984f-116">Gibt den Namen des Kontos an.</span><span class="sxs-lookup"><span data-stu-id="3984f-116">Specifies the name of the account.</span></span>
<span data-ttu-id="3984f-117">Dieses Cmdlet ruft die Schlüssel für dieses Konto ab.</span><span class="sxs-lookup"><span data-stu-id="3984f-117">This cmdlet gets the keys for this account.</span></span>

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

### <span data-ttu-id="3984f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3984f-118">-ResourceGroupName</span></span>
<span data-ttu-id="3984f-119">Gibt den Namen der Ressourcengruppe an, der das Konto zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="3984f-119">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="3984f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3984f-120">CommonParameters</span></span>
<span data-ttu-id="3984f-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3984f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3984f-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3984f-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3984f-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3984f-123">INPUTS</span></span>

### <span data-ttu-id="3984f-124">System. String</span><span class="sxs-lookup"><span data-stu-id="3984f-124">System.String</span></span>

## <span data-ttu-id="3984f-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3984f-125">OUTPUTS</span></span>

### <span data-ttu-id="3984f-126">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="3984f-126">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="3984f-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="3984f-127">NOTES</span></span>

## <span data-ttu-id="3984f-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3984f-128">RELATED LINKS</span></span>

[<span data-ttu-id="3984f-129">Neu – AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="3984f-129">New-AzCognitiveServicesAccountKey</span></span>](./New-AzCognitiveServicesAccountKey.md)


