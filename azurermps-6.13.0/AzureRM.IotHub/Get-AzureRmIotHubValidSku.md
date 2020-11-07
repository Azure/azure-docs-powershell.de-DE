---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubvalidsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubValidSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubValidSku.md
ms.openlocfilehash: d1c52cef6548f8762f972789a1fd9d47e8cc92aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664592"
---
# <span data-ttu-id="66657-101">Get-AzureRmIotHubValidSku</span><span class="sxs-lookup"><span data-stu-id="66657-101">Get-AzureRmIotHubValidSku</span></span>

## <span data-ttu-id="66657-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="66657-102">SYNOPSIS</span></span>
<span data-ttu-id="66657-103">Ruft alle gültigen SKUs ab, zu denen dieser IotHub wechseln kann.</span><span class="sxs-lookup"><span data-stu-id="66657-103">Gets all valid skus that this IotHub can transition to.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66657-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="66657-104">SYNTAX</span></span>

```
Get-AzureRmIotHubValidSku [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66657-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="66657-105">DESCRIPTION</span></span>
<span data-ttu-id="66657-106">Ruft alle gültigen SKUs ab, zu denen dieser IotHub wechseln kann.</span><span class="sxs-lookup"><span data-stu-id="66657-106">Gets all the valid skus that this IotHub can transition to.</span></span>
<span data-ttu-id="66657-107">Ein IotHub kann nicht zwischen der kostenlosen und der bezahlten SKUs wechseln und umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="66657-107">An IotHub cannot transition between free and the paid skus and vice versa.</span></span> <span data-ttu-id="66657-108">Sie müssen die iothub löschen und neu erstellen, wenn Sie dies erreichen möchten.</span><span class="sxs-lookup"><span data-stu-id="66657-108">You will have to delete and recreate the iothub if you want to achieve this.</span></span>

## <span data-ttu-id="66657-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="66657-109">EXAMPLES</span></span>

### <span data-ttu-id="66657-110">Beispiel 1 Abrufen der gültigen SKUs</span><span class="sxs-lookup"><span data-stu-id="66657-110">Example 1 Get the valid skus</span></span>
```
PS C:\> Get-AzureRmIotHubValidSku -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="66657-111">Ruft eine Liste aller SKUs für das IotHub mit dem Namen "myiothub" ab.</span><span class="sxs-lookup"><span data-stu-id="66657-111">Gets a list of all skus for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="66657-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="66657-112">PARAMETERS</span></span>

### <span data-ttu-id="66657-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66657-113">-DefaultProfile</span></span>
<span data-ttu-id="66657-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="66657-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="66657-115">-Name</span><span class="sxs-lookup"><span data-stu-id="66657-115">-Name</span></span>
<span data-ttu-id="66657-116">Der Name des viel-Hubs.</span><span class="sxs-lookup"><span data-stu-id="66657-116">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="66657-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66657-117">-ResourceGroupName</span></span>
<span data-ttu-id="66657-118">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="66657-118">Resource Group Name</span></span>

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

### <span data-ttu-id="66657-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66657-119">CommonParameters</span></span>
<span data-ttu-id="66657-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66657-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66657-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66657-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66657-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="66657-122">INPUTS</span></span>

### <span data-ttu-id="66657-123">System. String</span><span class="sxs-lookup"><span data-stu-id="66657-123">System.String</span></span>

## <span data-ttu-id="66657-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="66657-124">OUTPUTS</span></span>

### <span data-ttu-id="66657-125">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubSkuDescription</span><span class="sxs-lookup"><span data-stu-id="66657-125">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuDescription</span></span>

## <span data-ttu-id="66657-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="66657-126">NOTES</span></span>

## <span data-ttu-id="66657-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="66657-127">RELATED LINKS</span></span>
