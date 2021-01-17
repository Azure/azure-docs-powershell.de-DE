---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 73B1EB7E-568E-44E8-993A-91678B7D8AEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountKey.md
ms.openlocfilehash: 8150abc726f990b699237dbaad3641a99bae2e2c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470976"
---
# <span data-ttu-id="3e7f9-101">Get-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="3e7f9-101">Get-AzCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="3e7f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e7f9-102">SYNOPSIS</span></span>
<span data-ttu-id="3e7f9-103">Ruft die API-Schlüssel für ein Konto ab.</span><span class="sxs-lookup"><span data-stu-id="3e7f9-103">Gets the API keys for an account.</span></span>

## <span data-ttu-id="3e7f9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3e7f9-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e7f9-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3e7f9-105">DESCRIPTION</span></span>
<span data-ttu-id="3e7f9-106">Das **Cmdlet "Get-AzCognitiveServicesAccountKey"** ruft die API-Schlüssel für ein bereitgestelltes Cognitive Services-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="3e7f9-106">The **Get-AzCognitiveServicesAccountKey** cmdlet gets the API keys for a provisioned Cognitive Services account.</span></span>
<span data-ttu-id="3e7f9-107">Ein Cognitive Services-Konto verfügt über zwei API-Schlüssel: Schlüssel1 und Schlüssel2.</span><span class="sxs-lookup"><span data-stu-id="3e7f9-107">A Cognitive Services account has two API keys: Key1 and Key2.</span></span>
<span data-ttu-id="3e7f9-108">Die Schlüssel ermöglichen die Interaktion mit dem Cognitive Services-Kontoendpunkt.</span><span class="sxs-lookup"><span data-stu-id="3e7f9-108">The keys enable interaction with the Cognitive Services account endpoint.</span></span>
<span data-ttu-id="3e7f9-109">Verwenden New-AzCognitiveServicesAccountKey zum erneuten Generierten eines Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="3e7f9-109">Use New-AzCognitiveServicesAccountKey to regenerate a key.</span></span>

## <span data-ttu-id="3e7f9-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3e7f9-110">EXAMPLES</span></span>

### <span data-ttu-id="3e7f9-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3e7f9-111">Example 1</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountKey -ResourceGroupName cognitive-services-resource-group -name myluis

Key1                             Key2
----                             ----
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

## <span data-ttu-id="3e7f9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3e7f9-112">PARAMETERS</span></span>

### <span data-ttu-id="3e7f9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e7f9-113">-DefaultProfile</span></span>
<span data-ttu-id="3e7f9-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="3e7f9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3e7f9-115">-Name</span><span class="sxs-lookup"><span data-stu-id="3e7f9-115">-Name</span></span>
<span data-ttu-id="3e7f9-116">Gibt den Namen des Kontos an.</span><span class="sxs-lookup"><span data-stu-id="3e7f9-116">Specifies the name of the account.</span></span>
<span data-ttu-id="3e7f9-117">Dieses Cmdlet ruft die Schlüssel für dieses Konto ab.</span><span class="sxs-lookup"><span data-stu-id="3e7f9-117">This cmdlet gets the keys for this account.</span></span>

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

### <span data-ttu-id="3e7f9-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e7f9-118">-ResourceGroupName</span></span>
<span data-ttu-id="3e7f9-119">Gibt den Namen der Ressourcengruppe an, der das Konto zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="3e7f9-119">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="3e7f9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e7f9-120">CommonParameters</span></span>
<span data-ttu-id="3e7f9-121">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e7f9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e7f9-122">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3e7f9-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e7f9-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3e7f9-123">INPUTS</span></span>

### <span data-ttu-id="3e7f9-124">System.String</span><span class="sxs-lookup"><span data-stu-id="3e7f9-124">System.String</span></span>

## <span data-ttu-id="3e7f9-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3e7f9-125">OUTPUTS</span></span>

### <span data-ttu-id="3e7f9-126">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="3e7f9-126">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="3e7f9-127">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3e7f9-127">NOTES</span></span>

## <span data-ttu-id="3e7f9-128">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3e7f9-128">RELATED LINKS</span></span>

[<span data-ttu-id="3e7f9-129">New-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="3e7f9-129">New-AzCognitiveServicesAccountKey</span></span>](./New-AzCognitiveServicesAccountKey.md)


