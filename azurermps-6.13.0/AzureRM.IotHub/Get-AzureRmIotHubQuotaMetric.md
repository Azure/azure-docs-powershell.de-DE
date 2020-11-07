---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubquotametric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubQuotaMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubQuotaMetric.md
ms.openlocfilehash: 1de2d49d6e914635f8fc0d38ffa81755cc622481
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664598"
---
# <span data-ttu-id="0a05c-101">Get-AzureRmIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="0a05c-101">Get-AzureRmIotHubQuotaMetric</span></span>

## <span data-ttu-id="0a05c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0a05c-102">SYNOPSIS</span></span>
<span data-ttu-id="0a05c-103">Ruft die Kontingent Metrik für eine IotHub ab.</span><span class="sxs-lookup"><span data-stu-id="0a05c-103">Gets the Quota Metrics for an IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a05c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0a05c-104">SYNTAX</span></span>

```
Get-AzureRmIotHubQuotaMetric [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a05c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0a05c-105">DESCRIPTION</span></span>
<span data-ttu-id="0a05c-106">Ruft die Kontingent Metrik für eine IotHub ab.</span><span class="sxs-lookup"><span data-stu-id="0a05c-106">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="0a05c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0a05c-107">EXAMPLES</span></span>

### <span data-ttu-id="0a05c-108">Beispiel 1 Abrufen der Kontingent Metriken</span><span class="sxs-lookup"><span data-stu-id="0a05c-108">Example 1 Get the Quota Metrics</span></span>
```
PS C:\> Get-AzureRmIotHubQuotaMetric -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="0a05c-109">Ruft die Kontingent metrischen Informationen für das IotHub mit dem Namen "myiothub" ab.</span><span class="sxs-lookup"><span data-stu-id="0a05c-109">Gets the Quota Metric information for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="0a05c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0a05c-110">PARAMETERS</span></span>

### <span data-ttu-id="0a05c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a05c-111">-DefaultProfile</span></span>
<span data-ttu-id="0a05c-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="0a05c-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0a05c-113">-Name</span><span class="sxs-lookup"><span data-stu-id="0a05c-113">-Name</span></span>
<span data-ttu-id="0a05c-114">Der Name des viel-Hubs.</span><span class="sxs-lookup"><span data-stu-id="0a05c-114">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="0a05c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a05c-115">-ResourceGroupName</span></span>
<span data-ttu-id="0a05c-116">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="0a05c-116">Resource Group Name</span></span>

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

### <span data-ttu-id="0a05c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a05c-117">CommonParameters</span></span>
<span data-ttu-id="0a05c-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a05c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a05c-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a05c-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a05c-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0a05c-120">INPUTS</span></span>

### <span data-ttu-id="0a05c-121">System. String</span><span class="sxs-lookup"><span data-stu-id="0a05c-121">System.String</span></span>

## <span data-ttu-id="0a05c-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0a05c-122">OUTPUTS</span></span>

### <span data-ttu-id="0a05c-123">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="0a05c-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubQuotaMetric</span></span>

## <span data-ttu-id="0a05c-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="0a05c-124">NOTES</span></span>

## <span data-ttu-id="0a05c-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0a05c-125">RELATED LINKS</span></span>
