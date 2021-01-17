---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 11D5BFDF-5E5D-46B2-9F9B-A0524EFA1B42
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccount.md
ms.openlocfilehash: 3f442cc975c6fdbb95d53153c2c80615bb8676a4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470977"
---
# <span data-ttu-id="d248c-101">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="d248c-101">Get-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="d248c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d248c-102">SYNOPSIS</span></span>
<span data-ttu-id="d248c-103">Ruft ein Konto ab.</span><span class="sxs-lookup"><span data-stu-id="d248c-103">Gets an account.</span></span>

## <span data-ttu-id="d248c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d248c-104">SYNTAX</span></span>

### <span data-ttu-id="d248c-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="d248c-105">ResourceGroupParameterSet</span></span>
```
Get-AzCognitiveServicesAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d248c-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d248c-106">AccountNameParameterSet</span></span>
```
Get-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d248c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d248c-107">DESCRIPTION</span></span>
<span data-ttu-id="d248c-108">Das **Cmdlet "Get-AzCognitiveServicesAccount"** ruft die bereitgestellten Cognitive Services-Konten in der Ressourcengruppe ab, die durch den *Parameter "ResourceGroupName" angegeben* wird.</span><span class="sxs-lookup"><span data-stu-id="d248c-108">The **Get-AzCognitiveServicesAccount** cmdlet gets the provisioned Cognitive Services accounts in the resource group specified by the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="d248c-109">Wenn Sie den Parameter *"ResourceGroupName"* nicht angeben, ruft dieses Cmdlet alle Cognitive Services-Konten für das aktuelle Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="d248c-109">If you do not specify the *ResourceGroupName* parameter, this cmdlet gets all Cognitive Services accounts for the current subscription.</span></span>

## <span data-ttu-id="d248c-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d248c-110">EXAMPLES</span></span>

### <span data-ttu-id="d248c-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d248c-111">Example 1</span></span>
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

## <span data-ttu-id="d248c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d248c-112">PARAMETERS</span></span>

### <span data-ttu-id="d248c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d248c-113">-DefaultProfile</span></span>
<span data-ttu-id="d248c-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="d248c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d248c-115">-Name</span><span class="sxs-lookup"><span data-stu-id="d248c-115">-Name</span></span>
<span data-ttu-id="d248c-116">Gibt den Namen des zu erhaltenden Cognitive Services-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="d248c-116">Specifies the name of the Cognitive Services account to get.</span></span>

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

### <span data-ttu-id="d248c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d248c-117">-ResourceGroupName</span></span>
<span data-ttu-id="d248c-118">Gibt den Namen der Ressourcengruppe an, der das Cognitive Services-Konto zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d248c-118">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

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

### <span data-ttu-id="d248c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d248c-119">CommonParameters</span></span>
<span data-ttu-id="d248c-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d248c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d248c-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d248c-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d248c-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d248c-122">INPUTS</span></span>

### <span data-ttu-id="d248c-123">System.String</span><span class="sxs-lookup"><span data-stu-id="d248c-123">System.String</span></span>

## <span data-ttu-id="d248c-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d248c-124">OUTPUTS</span></span>

### <span data-ttu-id="d248c-125">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="d248c-125">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="d248c-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d248c-126">NOTES</span></span>

## <span data-ttu-id="d248c-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d248c-127">RELATED LINKS</span></span>

[<span data-ttu-id="d248c-128">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="d248c-128">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="d248c-129">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="d248c-129">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)

[<span data-ttu-id="d248c-130">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="d248c-130">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)


