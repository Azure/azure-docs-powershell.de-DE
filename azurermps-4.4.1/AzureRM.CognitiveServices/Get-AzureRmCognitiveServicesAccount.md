---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 11D5BFDF-5E5D-46B2-9F9B-A0524EFA1B42
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: c4419707c9c536a21e5fdc8aa39326b02e21937c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497834"
---
# <span data-ttu-id="27391-101">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="27391-101">Get-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="27391-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="27391-102">SYNOPSIS</span></span>
<span data-ttu-id="27391-103">Ruft ein Konto ab.</span><span class="sxs-lookup"><span data-stu-id="27391-103">Gets an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27391-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="27391-104">SYNTAX</span></span>

### <span data-ttu-id="27391-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="27391-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmCognitiveServicesAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="27391-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="27391-106">AccountNameParameterSet</span></span>
```
Get-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27391-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="27391-107">DESCRIPTION</span></span>
<span data-ttu-id="27391-108">Das Cmdlet " **Get-AzureRmCognitiveServicesAccount** " Ruft die bereitgestellten kognitiven Dienstkonten in der Ressourcengruppe ab, die vom *ResoureGroupName* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="27391-108">The **Get-AzureRmCognitiveServicesAccount** cmdlet gets the provisioned Cognitive Services accounts in the resource group specified by the *ResoureGroupName* parameter.</span></span>

<span data-ttu-id="27391-109">Wenn Sie den *ResoureGroupName* -Parameter nicht angeben, ruft dieses Cmdlet alle kognitiven Dienstkonten für das aktuelle Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="27391-109">If you do not specify the *ResoureGroupName* parameter, this cmdlet gets all Cognitive Services accounts for the current subscription.</span></span>

## <span data-ttu-id="27391-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="27391-110">EXAMPLES</span></span>

## <span data-ttu-id="27391-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="27391-111">PARAMETERS</span></span>

### <span data-ttu-id="27391-112">-Name</span><span class="sxs-lookup"><span data-stu-id="27391-112">-Name</span></span>
<span data-ttu-id="27391-113">Gibt den Namen des abzurufenden Cognitive Services-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="27391-113">Specifies the name of the Cognitive Services account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27391-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27391-114">-ResourceGroupName</span></span>
<span data-ttu-id="27391-115">Gibt den Namen der Ressourcengruppe an, der das Cognitive Services-Konto zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="27391-115">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27391-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27391-116">-DefaultProfile</span></span>
<span data-ttu-id="27391-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="27391-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27391-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27391-118">CommonParameters</span></span>
<span data-ttu-id="27391-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27391-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27391-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27391-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27391-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="27391-121">INPUTS</span></span>

## <span data-ttu-id="27391-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="27391-122">OUTPUTS</span></span>

### <span data-ttu-id="27391-123">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="27391-123">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="27391-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="27391-124">NOTES</span></span>

## <span data-ttu-id="27391-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="27391-125">RELATED LINKS</span></span>

[<span data-ttu-id="27391-126">Neu – AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="27391-126">New-AzureRmCognitiveServicesAccount</span></span>](./New-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="27391-127">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="27391-127">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="27391-128">Satz-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="27391-128">Set-AzureRmCognitiveServicesAccount</span></span>](./Set-AzureRmCognitiveServicesAccount.md)


