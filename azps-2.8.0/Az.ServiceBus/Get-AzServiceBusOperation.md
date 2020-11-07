---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusOperation.md
ms.openlocfilehash: ee3ad345bdc5f8eaf18bd9a3d6eeedf5e46de0ab
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824803"
---
# <span data-ttu-id="ea2c3-101">Get-AzServiceBusOperation</span><span class="sxs-lookup"><span data-stu-id="ea2c3-101">Get-AzServiceBusOperation</span></span>

## <span data-ttu-id="ea2c3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ea2c3-102">SYNOPSIS</span></span>
<span data-ttu-id="ea2c3-103">Liste unterstützter ServiceBus-Vorgänge</span><span class="sxs-lookup"><span data-stu-id="ea2c3-103">List supported ServiceBus Operations</span></span>

## <span data-ttu-id="ea2c3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ea2c3-104">SYNTAX</span></span>

```
Get-AzServiceBusOperation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea2c3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ea2c3-105">DESCRIPTION</span></span>
<span data-ttu-id="ea2c3-106">Das Cmdlet " **Get-AzServiceBusOperation** " listet die von ServiceBus unterstützten Vorgänge auf.</span><span class="sxs-lookup"><span data-stu-id="ea2c3-106">The **Get-AzServiceBusOperation** cmdlet Lists the ServiceBus supported Operations.</span></span>

## <span data-ttu-id="ea2c3-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ea2c3-107">EXAMPLES</span></span>

### <span data-ttu-id="ea2c3-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ea2c3-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusOperation
```

<span data-ttu-id="ea2c3-109">Listet ServiceBus-unterstützte Vorgänge auf</span><span class="sxs-lookup"><span data-stu-id="ea2c3-109">Lists ServiceBus supported operations</span></span>

## <span data-ttu-id="ea2c3-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ea2c3-110">PARAMETERS</span></span>

### <span data-ttu-id="ea2c3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea2c3-111">-DefaultProfile</span></span>
<span data-ttu-id="ea2c3-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ea2c3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea2c3-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea2c3-113">CommonParameters</span></span>
<span data-ttu-id="ea2c3-114">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea2c3-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea2c3-115">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea2c3-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea2c3-116">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ea2c3-116">INPUTS</span></span>

### <span data-ttu-id="ea2c3-117">Keine</span><span class="sxs-lookup"><span data-stu-id="ea2c3-117">None</span></span>

## <span data-ttu-id="ea2c3-118">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ea2c3-118">OUTPUTS</span></span>

### <span data-ttu-id="ea2c3-119">Microsoft. Azure. Commands. ServiceBus. Models. PSOperationAttributes</span><span class="sxs-lookup"><span data-stu-id="ea2c3-119">Microsoft.Azure.Commands.ServiceBus.Models.PSOperationAttributes</span></span>

## <span data-ttu-id="ea2c3-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="ea2c3-120">NOTES</span></span>

## <span data-ttu-id="ea2c3-121">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ea2c3-121">RELATED LINKS</span></span>
