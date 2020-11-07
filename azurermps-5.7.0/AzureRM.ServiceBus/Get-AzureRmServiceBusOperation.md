---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusOperation.md
ms.openlocfilehash: de2e826223520c13306411c5d52f448468186804
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664199"
---
# <span data-ttu-id="ae23b-101">Get-AzureRmServiceBusOperation</span><span class="sxs-lookup"><span data-stu-id="ae23b-101">Get-AzureRmServiceBusOperation</span></span>

## <span data-ttu-id="ae23b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ae23b-102">SYNOPSIS</span></span>
<span data-ttu-id="ae23b-103">Liste unterstützter ServiceBus-Vorgänge</span><span class="sxs-lookup"><span data-stu-id="ae23b-103">List supported ServiceBus Operations</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae23b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ae23b-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusOperation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae23b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ae23b-105">DESCRIPTION</span></span>
<span data-ttu-id="ae23b-106">Das Cmdlet " **Get-AzureRmServiceBusOperation** " listet die von ServiceBus unterstützten Vorgänge auf.</span><span class="sxs-lookup"><span data-stu-id="ae23b-106">The **Get-AzureRmServiceBusOperation** cmdlet Lists the ServiceBus supported Operations.</span></span>

## <span data-ttu-id="ae23b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ae23b-107">EXAMPLES</span></span>

### <span data-ttu-id="ae23b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ae23b-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusOperation
```

<span data-ttu-id="ae23b-109">Listet ServiceBus-unterstützte Vorgänge auf</span><span class="sxs-lookup"><span data-stu-id="ae23b-109">Lists ServiceBus supported operations</span></span>

## <span data-ttu-id="ae23b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ae23b-110">PARAMETERS</span></span>

### <span data-ttu-id="ae23b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae23b-111">-DefaultProfile</span></span>
<span data-ttu-id="ae23b-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ae23b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae23b-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae23b-113">CommonParameters</span></span>
<span data-ttu-id="ae23b-114">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae23b-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae23b-115">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae23b-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae23b-116">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ae23b-116">INPUTS</span></span>

### <span data-ttu-id="ae23b-117">Keine</span><span class="sxs-lookup"><span data-stu-id="ae23b-117">None</span></span>

### <span data-ttu-id="ae23b-118">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. ServiceBus. Models. PSOperationAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.4.2.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="ae23b-118">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.PSOperationAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.4.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="ae23b-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ae23b-119">OUTPUTS</span></span>

### <span data-ttu-id="ae23b-120">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. ServiceBus. Models. OperationAttributes]</span><span class="sxs-lookup"><span data-stu-id="ae23b-120">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ServiceBus.Models.OperationAttributes]</span></span>

## <span data-ttu-id="ae23b-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="ae23b-121">NOTES</span></span>

## <span data-ttu-id="ae23b-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ae23b-122">RELATED LINKS</span></span>

