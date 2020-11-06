---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubQuotaMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubQuotaMetric.md
ms.openlocfilehash: f0a3b446c6d40ff07efc35ca51cdf7f422491f33
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501826"
---
# <span data-ttu-id="e2ae3-101">Get-AzureRmIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="e2ae3-101">Get-AzureRmIotHubQuotaMetric</span></span>

## <span data-ttu-id="e2ae3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e2ae3-102">SYNOPSIS</span></span>
<span data-ttu-id="e2ae3-103">Ruft die Kontingent Metrik für eine IotHub ab.</span><span class="sxs-lookup"><span data-stu-id="e2ae3-103">Gets the Quota Metrics for an IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2ae3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2ae3-104">SYNTAX</span></span>

```
Get-AzureRmIotHubQuotaMetric [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2ae3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e2ae3-105">DESCRIPTION</span></span>
<span data-ttu-id="e2ae3-106">Ruft die Kontingent Metrik für eine IotHub ab.</span><span class="sxs-lookup"><span data-stu-id="e2ae3-106">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="e2ae3-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e2ae3-107">EXAMPLES</span></span>

### <span data-ttu-id="e2ae3-108">Beispiel 1 Abrufen der Kontingent Metriken</span><span class="sxs-lookup"><span data-stu-id="e2ae3-108">Example 1 Get the Quota Metrics</span></span>
```
PS C:\> Get-AzureRmIotHubQuotaMetric -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="e2ae3-109">Ruft die Kontingent metrischen Informationen für das IotHub mit dem Namen "myiothub" ab.</span><span class="sxs-lookup"><span data-stu-id="e2ae3-109">Gets the Quota Metric information for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="e2ae3-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2ae3-110">PARAMETERS</span></span>

### <span data-ttu-id="e2ae3-111">-Name</span><span class="sxs-lookup"><span data-stu-id="e2ae3-111">-Name</span></span>
<span data-ttu-id="e2ae3-112">Der Name des viel-Hubs.</span><span class="sxs-lookup"><span data-stu-id="e2ae3-112">Name of the IoT hub.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2ae3-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2ae3-113">-ResourceGroupName</span></span>
<span data-ttu-id="e2ae3-114">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="e2ae3-114">Resource Group Name</span></span>

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

### <span data-ttu-id="e2ae3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2ae3-115">-DefaultProfile</span></span>
<span data-ttu-id="e2ae3-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e2ae3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2ae3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2ae3-117">CommonParameters</span></span>
<span data-ttu-id="e2ae3-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2ae3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2ae3-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2ae3-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2ae3-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e2ae3-120">INPUTS</span></span>

### <span data-ttu-id="e2ae3-121">System. String</span><span class="sxs-lookup"><span data-stu-id="e2ae3-121">System.String</span></span>

## <span data-ttu-id="e2ae3-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e2ae3-122">OUTPUTS</span></span>

### <span data-ttu-id="e2ae3-123">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubQuotaMetric, Microsoft. Azure. Commands. IotHub, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e2ae3-123">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubQuotaMetric, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="e2ae3-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="e2ae3-124">NOTES</span></span>

## <span data-ttu-id="e2ae3-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e2ae3-125">RELATED LINKS</span></span>

