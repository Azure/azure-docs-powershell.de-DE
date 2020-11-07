---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMUsage.md
ms.openlocfilehash: 0996b327a0253e5f20c693fb8a3f3229597c80e8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661539"
---
# <span data-ttu-id="db77e-101">Get-AzVMUsage</span><span class="sxs-lookup"><span data-stu-id="db77e-101">Get-AzVMUsage</span></span>

## <span data-ttu-id="db77e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="db77e-102">SYNOPSIS</span></span>
<span data-ttu-id="db77e-103">Ruft die Verwendung des virtuellen Computers Core count für einen Speicherort ab.</span><span class="sxs-lookup"><span data-stu-id="db77e-103">Gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="db77e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="db77e-104">SYNTAX</span></span>

```
Get-AzVMUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db77e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="db77e-105">DESCRIPTION</span></span>
<span data-ttu-id="db77e-106">Das Cmdlet " **Get-AzVMUsage** " Ruft die Verwendung des Virtual Machine Core count für einen Speicherort ab.</span><span class="sxs-lookup"><span data-stu-id="db77e-106">The **Get-AzVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="db77e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="db77e-107">EXAMPLES</span></span>

### <span data-ttu-id="db77e-108">Beispiel 1: Abrufen der Core count-Verwendung für einen Speicherort</span><span class="sxs-lookup"><span data-stu-id="db77e-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzVMUsage -Location "Central US"
```

<span data-ttu-id="db77e-109">Dieser Befehl ruft die Core count-Nutzung des virtuellen Computers für den Standort Central US ab.</span><span class="sxs-lookup"><span data-stu-id="db77e-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="db77e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="db77e-110">PARAMETERS</span></span>

### <span data-ttu-id="db77e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db77e-111">-DefaultProfile</span></span>
<span data-ttu-id="db77e-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="db77e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db77e-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="db77e-113">-Location</span></span>
<span data-ttu-id="db77e-114">Gibt den Speicherort an, für den dieses Cmdlet die Verwendung des Core count für virtuelle Maschinen erhält.</span><span class="sxs-lookup"><span data-stu-id="db77e-114">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

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

### <span data-ttu-id="db77e-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db77e-115">CommonParameters</span></span>
<span data-ttu-id="db77e-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db77e-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db77e-117">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="db77e-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db77e-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="db77e-118">INPUTS</span></span>

### <span data-ttu-id="db77e-119">System. String</span><span class="sxs-lookup"><span data-stu-id="db77e-119">System.String</span></span>

## <span data-ttu-id="db77e-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="db77e-120">OUTPUTS</span></span>

### <span data-ttu-id="db77e-121">Microsoft. Azure. Commands. Compute. Models. PSU</span><span class="sxs-lookup"><span data-stu-id="db77e-121">Microsoft.Azure.Commands.Compute.Models.PSUsage</span></span>

## <span data-ttu-id="db77e-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="db77e-122">NOTES</span></span>

## <span data-ttu-id="db77e-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="db77e-123">RELATED LINKS</span></span>

[<span data-ttu-id="db77e-124">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="db77e-124">Get-AzVM</span></span>](./Get-AzVM.md)


