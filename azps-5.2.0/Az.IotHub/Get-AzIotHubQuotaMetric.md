---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubquotametric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
ms.openlocfilehash: 1f3fc05a71ec0d7c6f4926f47f6ab862af42b9e7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363053"
---
# <span data-ttu-id="69fd3-101">Get-AzIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="69fd3-101">Get-AzIotHubQuotaMetric</span></span>

## <span data-ttu-id="69fd3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69fd3-102">SYNOPSIS</span></span>
<span data-ttu-id="69fd3-103">Ruft die Kontingentmetriken für einen IotHub ab.</span><span class="sxs-lookup"><span data-stu-id="69fd3-103">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="69fd3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="69fd3-104">SYNTAX</span></span>

```
Get-AzIotHubQuotaMetric [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69fd3-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="69fd3-105">DESCRIPTION</span></span>
<span data-ttu-id="69fd3-106">Ruft die Kontingentmetriken für einen IotHub ab.</span><span class="sxs-lookup"><span data-stu-id="69fd3-106">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="69fd3-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="69fd3-107">EXAMPLES</span></span>

### <span data-ttu-id="69fd3-108">Beispiel 1: Kontingentmetriken erhalten</span><span class="sxs-lookup"><span data-stu-id="69fd3-108">Example 1 Get the Quota Metrics</span></span>
```
PS C:\> Get-AzIotHubQuotaMetric -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="69fd3-109">Ruft die Kontingentmetrikinformationen für IotHub mit dem Namen "myiothub" ab.</span><span class="sxs-lookup"><span data-stu-id="69fd3-109">Gets the Quota Metric information for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="69fd3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="69fd3-110">PARAMETERS</span></span>

### <span data-ttu-id="69fd3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69fd3-111">-DefaultProfile</span></span>
<span data-ttu-id="69fd3-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="69fd3-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="69fd3-113">-Name</span><span class="sxs-lookup"><span data-stu-id="69fd3-113">-Name</span></span>
<span data-ttu-id="69fd3-114">Name des IoT-Hubs.</span><span class="sxs-lookup"><span data-stu-id="69fd3-114">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="69fd3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69fd3-115">-ResourceGroupName</span></span>
<span data-ttu-id="69fd3-116">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="69fd3-116">Resource Group Name</span></span>

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

### <span data-ttu-id="69fd3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69fd3-117">CommonParameters</span></span>
<span data-ttu-id="69fd3-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69fd3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69fd3-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69fd3-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69fd3-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="69fd3-120">INPUTS</span></span>

### <span data-ttu-id="69fd3-121">System.String</span><span class="sxs-lookup"><span data-stu-id="69fd3-121">System.String</span></span>

## <span data-ttu-id="69fd3-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="69fd3-122">OUTPUTS</span></span>

### <span data-ttu-id="69fd3-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="69fd3-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubQuotaMetric</span></span>

## <span data-ttu-id="69fd3-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="69fd3-124">NOTES</span></span>

## <span data-ttu-id="69fd3-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="69fd3-125">RELATED LINKS</span></span>
