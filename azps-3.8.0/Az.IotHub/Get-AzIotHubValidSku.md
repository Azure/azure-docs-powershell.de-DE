---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubvalidsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubValidSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubValidSku.md
ms.openlocfilehash: e0f178c10fa74d8fa230472397d7bcc835f98bf4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004024"
---
# <span data-ttu-id="b2eda-101">Get-AzIotHubValidSku</span><span class="sxs-lookup"><span data-stu-id="b2eda-101">Get-AzIotHubValidSku</span></span>

## <span data-ttu-id="b2eda-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b2eda-102">SYNOPSIS</span></span>
<span data-ttu-id="b2eda-103">Ruft alle gültigen SKUs ab, zu denen dieser IotHub wechseln kann.</span><span class="sxs-lookup"><span data-stu-id="b2eda-103">Gets all valid skus that this IotHub can transition to.</span></span>

## <span data-ttu-id="b2eda-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b2eda-104">SYNTAX</span></span>

```
Get-AzIotHubValidSku [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b2eda-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b2eda-105">DESCRIPTION</span></span>
<span data-ttu-id="b2eda-106">Ruft alle gültigen SKUs ab, zu denen dieser IotHub wechseln kann.</span><span class="sxs-lookup"><span data-stu-id="b2eda-106">Gets all the valid skus that this IotHub can transition to.</span></span>
<span data-ttu-id="b2eda-107">Ein IotHub kann nicht zwischen der kostenlosen und der bezahlten SKUs wechseln und umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="b2eda-107">An IotHub cannot transition between free and the paid skus and vice versa.</span></span> <span data-ttu-id="b2eda-108">Sie müssen die iothub löschen und neu erstellen, wenn Sie dies erreichen möchten.</span><span class="sxs-lookup"><span data-stu-id="b2eda-108">You will have to delete and recreate the iothub if you want to achieve this.</span></span>

## <span data-ttu-id="b2eda-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b2eda-109">EXAMPLES</span></span>

### <span data-ttu-id="b2eda-110">Beispiel 1 Abrufen der gültigen SKUs</span><span class="sxs-lookup"><span data-stu-id="b2eda-110">Example 1 Get the valid skus</span></span>
```
PS C:\> Get-AzIotHubValidSku -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="b2eda-111">Ruft eine Liste aller SKUs für das IotHub mit dem Namen "myiothub" ab.</span><span class="sxs-lookup"><span data-stu-id="b2eda-111">Gets a list of all skus for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="b2eda-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2eda-112">PARAMETERS</span></span>

### <span data-ttu-id="b2eda-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2eda-113">-DefaultProfile</span></span>
<span data-ttu-id="b2eda-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="b2eda-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b2eda-115">-Name</span><span class="sxs-lookup"><span data-stu-id="b2eda-115">-Name</span></span>
<span data-ttu-id="b2eda-116">Der Name des viel-Hubs.</span><span class="sxs-lookup"><span data-stu-id="b2eda-116">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="b2eda-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2eda-117">-ResourceGroupName</span></span>
<span data-ttu-id="b2eda-118">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="b2eda-118">Resource Group Name</span></span>

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

### <span data-ttu-id="b2eda-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2eda-119">CommonParameters</span></span>
<span data-ttu-id="b2eda-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2eda-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2eda-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2eda-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2eda-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b2eda-122">INPUTS</span></span>

### <span data-ttu-id="b2eda-123">System. String</span><span class="sxs-lookup"><span data-stu-id="b2eda-123">System.String</span></span>

## <span data-ttu-id="b2eda-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b2eda-124">OUTPUTS</span></span>

### <span data-ttu-id="b2eda-125">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubSkuDescription</span><span class="sxs-lookup"><span data-stu-id="b2eda-125">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuDescription</span></span>

## <span data-ttu-id="b2eda-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="b2eda-126">NOTES</span></span>

## <span data-ttu-id="b2eda-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b2eda-127">RELATED LINKS</span></span>
