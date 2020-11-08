---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 11D5BFDF-5E5D-46B2-9F9B-A0524EFA1B42
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccount.md
ms.openlocfilehash: 3f442cc975c6fdbb95d53153c2c80615bb8676a4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995021"
---
# <span data-ttu-id="77dda-101">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="77dda-101">Get-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="77dda-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="77dda-102">SYNOPSIS</span></span>
<span data-ttu-id="77dda-103">Ruft ein Konto ab.</span><span class="sxs-lookup"><span data-stu-id="77dda-103">Gets an account.</span></span>

## <span data-ttu-id="77dda-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="77dda-104">SYNTAX</span></span>

### <span data-ttu-id="77dda-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="77dda-105">ResourceGroupParameterSet</span></span>
```
Get-AzCognitiveServicesAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="77dda-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="77dda-106">AccountNameParameterSet</span></span>
```
Get-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77dda-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="77dda-107">DESCRIPTION</span></span>
<span data-ttu-id="77dda-108">Das Cmdlet " **Get-AzCognitiveServicesAccount** " Ruft die bereitgestellten kognitiven Dienstkonten in der Ressourcengruppe ab, die vom *ResourceGroupName* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="77dda-108">The **Get-AzCognitiveServicesAccount** cmdlet gets the provisioned Cognitive Services accounts in the resource group specified by the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="77dda-109">Wenn Sie den *ResourceGroupName* -Parameter nicht angeben, ruft dieses Cmdlet alle kognitiven Dienstkonten für das aktuelle Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="77dda-109">If you do not specify the *ResourceGroupName* parameter, this cmdlet gets all Cognitive Services accounts for the current subscription.</span></span>

## <span data-ttu-id="77dda-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="77dda-110">EXAMPLES</span></span>

### <span data-ttu-id="77dda-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="77dda-111">Example 1</span></span>
```powershell
PS C:\> New-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -Type LUIS -SkuName S0 -Locati
on 'WestUS'

ResourceGroupName : cognitive-services-resource-group
AccountName       : myluis
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/cognitive-services-resource-group/providers/Microsoft.Cog
                    nitiveServices/accounts/myluis
Endpoint          : https://westus.api.cognitive.microsoft.com/luis/v2.0
Location          : WESTUS
Sku               : Microsoft.Azure.Management.CognitiveServices.Models.Sku
AccountType       : LUIS
ResourceType      : Microsoft.CognitiveServices/accounts
Etag              : "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
ProvisioningState : Succeeded
Tags              :
```

## <span data-ttu-id="77dda-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="77dda-112">PARAMETERS</span></span>

### <span data-ttu-id="77dda-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77dda-113">-DefaultProfile</span></span>
<span data-ttu-id="77dda-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="77dda-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="77dda-115">-Name</span><span class="sxs-lookup"><span data-stu-id="77dda-115">-Name</span></span>
<span data-ttu-id="77dda-116">Gibt den Namen des abzurufenden Cognitive Services-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="77dda-116">Specifies the name of the Cognitive Services account to get.</span></span>

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

### <span data-ttu-id="77dda-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77dda-117">-ResourceGroupName</span></span>
<span data-ttu-id="77dda-118">Gibt den Namen der Ressourcengruppe an, der das Cognitive Services-Konto zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="77dda-118">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

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

### <span data-ttu-id="77dda-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77dda-119">CommonParameters</span></span>
<span data-ttu-id="77dda-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77dda-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77dda-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="77dda-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77dda-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="77dda-122">INPUTS</span></span>

### <span data-ttu-id="77dda-123">System. String</span><span class="sxs-lookup"><span data-stu-id="77dda-123">System.String</span></span>

## <span data-ttu-id="77dda-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="77dda-124">OUTPUTS</span></span>

### <span data-ttu-id="77dda-125">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="77dda-125">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="77dda-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="77dda-126">NOTES</span></span>

## <span data-ttu-id="77dda-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="77dda-127">RELATED LINKS</span></span>

[<span data-ttu-id="77dda-128">Neu – AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="77dda-128">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="77dda-129">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="77dda-129">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)

[<span data-ttu-id="77dda-130">Satz-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="77dda-130">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)


