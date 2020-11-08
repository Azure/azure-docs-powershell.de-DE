---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azcomputeresourcesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
ms.openlocfilehash: 970cbb3e03a4934f648df2f6f8c06275a30740de
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175832"
---
# <span data-ttu-id="38e20-101">Get-AzComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="38e20-101">Get-AzComputeResourceSku</span></span>

## <span data-ttu-id="38e20-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="38e20-102">SYNOPSIS</span></span>
<span data-ttu-id="38e20-103">Auflisten aller Compute-Ressourcen-SKUs</span><span class="sxs-lookup"><span data-stu-id="38e20-103">List all compute resource Skus</span></span>

## <span data-ttu-id="38e20-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="38e20-104">SYNTAX</span></span>

```
Get-AzComputeResourceSku [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38e20-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="38e20-105">DESCRIPTION</span></span>
<span data-ttu-id="38e20-106">Auflisten aller Compute-Ressourcen-SKUs</span><span class="sxs-lookup"><span data-stu-id="38e20-106">List all compute resource Skus</span></span>

## <span data-ttu-id="38e20-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="38e20-107">EXAMPLES</span></span>

### <span data-ttu-id="38e20-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="38e20-108">Example 1</span></span>
```
PS C:\> Get-AzComputeResourceSku "westus";
```

<span data-ttu-id="38e20-109">Auflisten aller Compute-Ressourcen-SKUs in der Region West-US</span><span class="sxs-lookup"><span data-stu-id="38e20-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="38e20-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="38e20-110">PARAMETERS</span></span>

### <span data-ttu-id="38e20-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38e20-111">-DefaultProfile</span></span>
<span data-ttu-id="38e20-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="38e20-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38e20-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="38e20-113">-Location</span></span>
<span data-ttu-id="38e20-114">Gibt einen Speicherort der Liste der verfügbaren SKUs an.</span><span class="sxs-lookup"><span data-stu-id="38e20-114">Specifies a location of the available skus to list.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38e20-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38e20-115">CommonParameters</span></span>
<span data-ttu-id="38e20-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38e20-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38e20-117">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="38e20-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38e20-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="38e20-118">INPUTS</span></span>

### <span data-ttu-id="38e20-119">System. String</span><span class="sxs-lookup"><span data-stu-id="38e20-119">System.String</span></span>

## <span data-ttu-id="38e20-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="38e20-120">OUTPUTS</span></span>

### <span data-ttu-id="38e20-121">Microsoft. Azure. Commands. Compute. Automation. Models. PSResourceSku</span><span class="sxs-lookup"><span data-stu-id="38e20-121">Microsoft.Azure.Commands.Compute.Automation.Models.PSResourceSku</span></span>

## <span data-ttu-id="38e20-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="38e20-122">NOTES</span></span>

## <span data-ttu-id="38e20-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="38e20-123">RELATED LINKS</span></span>
