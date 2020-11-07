---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubquotametric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
ms.openlocfilehash: 6d8ea34de1520326ead270ffa44837388729bc5a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93819768"
---
# <span data-ttu-id="26164-101">Get-AzIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="26164-101">Get-AzIotHubQuotaMetric</span></span>

## <span data-ttu-id="26164-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="26164-102">SYNOPSIS</span></span>
<span data-ttu-id="26164-103">Ruft die Kontingent Metrik für eine IotHub ab.</span><span class="sxs-lookup"><span data-stu-id="26164-103">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="26164-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="26164-104">SYNTAX</span></span>

```
Get-AzIotHubQuotaMetric [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26164-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="26164-105">DESCRIPTION</span></span>
<span data-ttu-id="26164-106">Ruft die Kontingent Metrik für eine IotHub ab.</span><span class="sxs-lookup"><span data-stu-id="26164-106">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="26164-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="26164-107">EXAMPLES</span></span>

### <span data-ttu-id="26164-108">Beispiel 1 Abrufen der Kontingent Metriken</span><span class="sxs-lookup"><span data-stu-id="26164-108">Example 1 Get the Quota Metrics</span></span>
```
PS C:\> Get-AzIotHubQuotaMetric -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="26164-109">Ruft die Kontingent metrischen Informationen für das IotHub mit dem Namen "myiothub" ab.</span><span class="sxs-lookup"><span data-stu-id="26164-109">Gets the Quota Metric information for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="26164-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="26164-110">PARAMETERS</span></span>

### <span data-ttu-id="26164-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26164-111">-DefaultProfile</span></span>
<span data-ttu-id="26164-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="26164-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="26164-113">-Name</span><span class="sxs-lookup"><span data-stu-id="26164-113">-Name</span></span>
<span data-ttu-id="26164-114">Der Name des viel-Hubs.</span><span class="sxs-lookup"><span data-stu-id="26164-114">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="26164-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26164-115">-ResourceGroupName</span></span>
<span data-ttu-id="26164-116">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="26164-116">Resource Group Name</span></span>

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

### <span data-ttu-id="26164-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26164-117">CommonParameters</span></span>
<span data-ttu-id="26164-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26164-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26164-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26164-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26164-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="26164-120">INPUTS</span></span>

### <span data-ttu-id="26164-121">System. String</span><span class="sxs-lookup"><span data-stu-id="26164-121">System.String</span></span>

## <span data-ttu-id="26164-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="26164-122">OUTPUTS</span></span>

### <span data-ttu-id="26164-123">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="26164-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubQuotaMetric</span></span>

## <span data-ttu-id="26164-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="26164-124">NOTES</span></span>

## <span data-ttu-id="26164-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="26164-125">RELATED LINKS</span></span>
