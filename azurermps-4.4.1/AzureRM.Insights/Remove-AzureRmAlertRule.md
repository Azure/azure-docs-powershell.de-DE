---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAlertRule.md
ms.openlocfilehash: de0c1f8fa66b195452d7f2c9447189b4e925136b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501842"
---
# <span data-ttu-id="2229b-101">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="2229b-101">Remove-AzureRmAlertRule</span></span>

## <span data-ttu-id="2229b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2229b-102">SYNOPSIS</span></span>
<span data-ttu-id="2229b-103">Entfernt eine Warnungsregel.</span><span class="sxs-lookup"><span data-stu-id="2229b-103">Removes an alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2229b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2229b-104">SYNTAX</span></span>

```
Remove-AzureRmAlertRule -ResourceGroup <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2229b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2229b-105">DESCRIPTION</span></span>
<span data-ttu-id="2229b-106">Das Cmdlet **Remove-AzureRmAlertRule** entfernt eine Warnungsregel.</span><span class="sxs-lookup"><span data-stu-id="2229b-106">The **Remove-AzureRmAlertRule** cmdlet removes an alert rule.</span></span>
<span data-ttu-id="2229b-107">Sie müssen den Namen der Warnungsregel und die Ressourcengruppe angeben, der Sie zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="2229b-107">You must specify the name of the alert rule and the resource group to which it is assigned.</span></span>

## <span data-ttu-id="2229b-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2229b-108">EXAMPLES</span></span>

### <span data-ttu-id="2229b-109">Beispiel 1: Entfernen einer Warnungsregel</span><span class="sxs-lookup"><span data-stu-id="2229b-109">Example 1: Remove an alert rule</span></span>
```
PS C:\>Remove-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="2229b-110">Dieser Befehl entfernt die Warnungsregel mit dem Namen myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 in der Ressourcengruppe Default-Web-centralus.</span><span class="sxs-lookup"><span data-stu-id="2229b-110">This command removes the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 in the resource group Default-Web-CentralUS.</span></span>

## <span data-ttu-id="2229b-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="2229b-111">PARAMETERS</span></span>

### <span data-ttu-id="2229b-112">-Name</span><span class="sxs-lookup"><span data-stu-id="2229b-112">-Name</span></span>
<span data-ttu-id="2229b-113">Gibt den Namen der zu entfernenden Warnungsregel an.</span><span class="sxs-lookup"><span data-stu-id="2229b-113">Specifies the name of the alert rule to remove.</span></span>

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

### <span data-ttu-id="2229b-114">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2229b-114">-ResourceGroup</span></span>
<span data-ttu-id="2229b-115">Gibt den Namen der Ressourcengruppe für die Warnungsregel an.</span><span class="sxs-lookup"><span data-stu-id="2229b-115">Specifies the name of the resource group for the alert rule.</span></span>

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

### <span data-ttu-id="2229b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2229b-116">-DefaultProfile</span></span>
<span data-ttu-id="2229b-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2229b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2229b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2229b-118">CommonParameters</span></span>
<span data-ttu-id="2229b-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2229b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2229b-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2229b-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2229b-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2229b-121">INPUTS</span></span>

## <span data-ttu-id="2229b-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2229b-122">OUTPUTS</span></span>

### <span data-ttu-id="2229b-123">System. Collections. Generic. List ' 1 [Microsoft. Azure. AzureOperationResponse]</span><span class="sxs-lookup"><span data-stu-id="2229b-123">System.Collections.Generic.List\`1[Microsoft.Azure.AzureOperationResponse]</span></span>

## <span data-ttu-id="2229b-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="2229b-124">NOTES</span></span>

## <span data-ttu-id="2229b-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2229b-125">RELATED LINKS</span></span>

[<span data-ttu-id="2229b-126">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="2229b-126">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="2229b-127">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="2229b-127">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="2229b-128">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="2229b-128">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="2229b-129">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="2229b-129">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="2229b-130">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="2229b-130">Get-AzureRmAlertRule</span></span>](./Get-AzureRmAlertRule.md)


