---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMUsage.md
ms.openlocfilehash: 22f77bfc5802527103dd0e391a11e16833696abd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499705"
---
# <span data-ttu-id="1e15c-101">Get-AzureRmVMUsage</span><span class="sxs-lookup"><span data-stu-id="1e15c-101">Get-AzureRmVMUsage</span></span>

## <span data-ttu-id="1e15c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1e15c-102">SYNOPSIS</span></span>
<span data-ttu-id="1e15c-103">Ruft die Verwendung des virtuellen Computers Core count für einen Speicherort ab.</span><span class="sxs-lookup"><span data-stu-id="1e15c-103">Gets the virtual machine core count usage for a location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e15c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e15c-104">SYNTAX</span></span>

```
Get-AzureRmVMUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e15c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1e15c-105">DESCRIPTION</span></span>
<span data-ttu-id="1e15c-106">Das Cmdlet " **Get-AzureRmVMUsage** " Ruft die Verwendung des Virtual Machine Core count für einen Speicherort ab.</span><span class="sxs-lookup"><span data-stu-id="1e15c-106">The **Get-AzureRmVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="1e15c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1e15c-107">EXAMPLES</span></span>

### <span data-ttu-id="1e15c-108">Beispiel 1: Abrufen der Core count-Verwendung für einen Speicherort</span><span class="sxs-lookup"><span data-stu-id="1e15c-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzureRmVMUsage -Location "Central US"
```

<span data-ttu-id="1e15c-109">Dieser Befehl ruft die Core count-Nutzung des virtuellen Computers für den Standort Central US ab.</span><span class="sxs-lookup"><span data-stu-id="1e15c-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="1e15c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1e15c-110">PARAMETERS</span></span>

### <span data-ttu-id="1e15c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e15c-111">-DefaultProfile</span></span>
<span data-ttu-id="1e15c-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1e15c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e15c-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="1e15c-113">-Location</span></span>
<span data-ttu-id="1e15c-114">Gibt den Speicherort an, für den dieses Cmdlet die Verwendung des Core count für virtuelle Maschinen erhält.</span><span class="sxs-lookup"><span data-stu-id="1e15c-114">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

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

### <span data-ttu-id="1e15c-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e15c-115">CommonParameters</span></span>
<span data-ttu-id="1e15c-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e15c-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e15c-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e15c-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e15c-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1e15c-118">INPUTS</span></span>

### <span data-ttu-id="1e15c-119">System. String</span><span class="sxs-lookup"><span data-stu-id="1e15c-119">System.String</span></span>

## <span data-ttu-id="1e15c-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1e15c-120">OUTPUTS</span></span>

### <span data-ttu-id="1e15c-121">Microsoft. Azure. Commands. Compute. Models. PSU</span><span class="sxs-lookup"><span data-stu-id="1e15c-121">Microsoft.Azure.Commands.Compute.Models.PSUsage</span></span>

## <span data-ttu-id="1e15c-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="1e15c-122">NOTES</span></span>

## <span data-ttu-id="1e15c-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1e15c-123">RELATED LINKS</span></span>

[<span data-ttu-id="1e15c-124">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="1e15c-124">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


