---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubquotametric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
ms.openlocfilehash: 7da36f401647a4e020097eb2cfe6690aa1327755
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842219"
---
# <span data-ttu-id="7af02-101">Get-AzIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="7af02-101">Get-AzIotHubQuotaMetric</span></span>

## <span data-ttu-id="7af02-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7af02-102">SYNOPSIS</span></span>
<span data-ttu-id="7af02-103">Ruft die Kontingent Metrik für eine IotHub ab.</span><span class="sxs-lookup"><span data-stu-id="7af02-103">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="7af02-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7af02-104">SYNTAX</span></span>

```
Get-AzIotHubQuotaMetric [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7af02-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7af02-105">DESCRIPTION</span></span>
<span data-ttu-id="7af02-106">Ruft die Kontingent Metrik für eine IotHub ab.</span><span class="sxs-lookup"><span data-stu-id="7af02-106">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="7af02-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7af02-107">EXAMPLES</span></span>

### <span data-ttu-id="7af02-108">Beispiel 1 Abrufen der Kontingent Metriken</span><span class="sxs-lookup"><span data-stu-id="7af02-108">Example 1 Get the Quota Metrics</span></span>
```
PS C:\> Get-AzIotHubQuotaMetric -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="7af02-109">Ruft die Kontingent metrischen Informationen für das IotHub mit dem Namen "myiothub" ab.</span><span class="sxs-lookup"><span data-stu-id="7af02-109">Gets the Quota Metric information for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="7af02-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7af02-110">PARAMETERS</span></span>

### <span data-ttu-id="7af02-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7af02-111">-DefaultProfile</span></span>
<span data-ttu-id="7af02-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="7af02-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7af02-113">-Name</span><span class="sxs-lookup"><span data-stu-id="7af02-113">-Name</span></span>
<span data-ttu-id="7af02-114">Der Name des viel-Hubs.</span><span class="sxs-lookup"><span data-stu-id="7af02-114">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="7af02-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7af02-115">-ResourceGroupName</span></span>
<span data-ttu-id="7af02-116">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="7af02-116">Resource Group Name</span></span>

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

### <span data-ttu-id="7af02-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7af02-117">CommonParameters</span></span>
<span data-ttu-id="7af02-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7af02-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7af02-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7af02-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7af02-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7af02-120">INPUTS</span></span>

### <span data-ttu-id="7af02-121">System. String</span><span class="sxs-lookup"><span data-stu-id="7af02-121">System.String</span></span>

## <span data-ttu-id="7af02-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7af02-122">OUTPUTS</span></span>

### <span data-ttu-id="7af02-123">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="7af02-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubQuotaMetric</span></span>

## <span data-ttu-id="7af02-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="7af02-124">NOTES</span></span>

## <span data-ttu-id="7af02-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7af02-125">RELATED LINKS</span></span>
