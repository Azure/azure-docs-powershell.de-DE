---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 6140E973-D7AB-4A28-A4FA-818E08129372
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAutoscaleSetting.md
ms.openlocfilehash: cd853184e06403f3c0d516ee1b0790c724adacb4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501838"
---
# <span data-ttu-id="24bee-101">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="24bee-101">Remove-AzureRmAutoscaleSetting</span></span>

## <span data-ttu-id="24bee-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="24bee-102">SYNOPSIS</span></span>
<span data-ttu-id="24bee-103">Entfernt eine AutoScale-Einstellung.</span><span class="sxs-lookup"><span data-stu-id="24bee-103">Removes an Autoscale setting.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24bee-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="24bee-104">SYNTAX</span></span>

```
Remove-AzureRmAutoscaleSetting -ResourceGroup <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24bee-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="24bee-105">DESCRIPTION</span></span>
<span data-ttu-id="24bee-106">Das Cmdlet **Remove-AzureRmAutoscaleSetting** entfernt eine AutoScale-Einstellung.</span><span class="sxs-lookup"><span data-stu-id="24bee-106">The **Remove-AzureRmAutoscaleSetting** cmdlet removes an Autoscale setting.</span></span>
<span data-ttu-id="24bee-107">Sie müssen den Namen der Einstellung und den Namen der Ressourcengruppe angeben, der Sie zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="24bee-107">You must specify the name of the setting and the name of the resource group to which it is assigned.</span></span>

## <span data-ttu-id="24bee-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="24bee-108">EXAMPLES</span></span>

## <span data-ttu-id="24bee-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="24bee-109">PARAMETERS</span></span>

### <span data-ttu-id="24bee-110">-Name</span><span class="sxs-lookup"><span data-stu-id="24bee-110">-Name</span></span>
<span data-ttu-id="24bee-111">Gibt den Namen der zu entfernenden AutoScale-Einstellung an.</span><span class="sxs-lookup"><span data-stu-id="24bee-111">Specifies the name of the Autoscale setting to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24bee-112">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="24bee-112">-ResourceGroup</span></span>
<span data-ttu-id="24bee-113">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="24bee-113">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24bee-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24bee-114">-DefaultProfile</span></span>
<span data-ttu-id="24bee-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="24bee-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24bee-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24bee-116">CommonParameters</span></span>
<span data-ttu-id="24bee-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24bee-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24bee-118">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24bee-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24bee-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="24bee-119">INPUTS</span></span>

## <span data-ttu-id="24bee-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="24bee-120">OUTPUTS</span></span>

### <span data-ttu-id="24bee-121">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="24bee-121">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="24bee-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="24bee-122">NOTES</span></span>

## <span data-ttu-id="24bee-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="24bee-123">RELATED LINKS</span></span>

[<span data-ttu-id="24bee-124">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="24bee-124">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="24bee-125">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="24bee-125">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)


