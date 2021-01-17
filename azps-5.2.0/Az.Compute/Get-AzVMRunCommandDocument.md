---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmruncommanddocument
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
ms.openlocfilehash: 5aeb8d7ba44f07519ff3cdfdc5e775687bd98260
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369479"
---
# <span data-ttu-id="f64d3-101">Get-AzVMRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="f64d3-101">Get-AzVMRunCommandDocument</span></span>

## <span data-ttu-id="f64d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f64d3-102">SYNOPSIS</span></span>
<span data-ttu-id="f64d3-103">Befehlsdokument "Ausführen" erhalten</span><span class="sxs-lookup"><span data-stu-id="f64d3-103">Get a run command document.</span></span>

## <span data-ttu-id="f64d3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f64d3-104">SYNTAX</span></span>

```
Get-AzVMRunCommandDocument [-Location] <String> [[-CommandId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f64d3-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f64d3-105">DESCRIPTION</span></span>
<span data-ttu-id="f64d3-106">Befehlsdokument "Ausführen" erhalten</span><span class="sxs-lookup"><span data-stu-id="f64d3-106">Get a run command document.</span></span>

## <span data-ttu-id="f64d3-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f64d3-107">EXAMPLES</span></span>

### <span data-ttu-id="f64d3-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f64d3-108">Example 1</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus' -CommandId 'RunPowerShellScript'
```

<span data-ttu-id="f64d3-109">Ruft ein spezielles Ausführungsbefehlsdokument für 'RunPowerShellScript' in 'westus' ab.</span><span class="sxs-lookup"><span data-stu-id="f64d3-109">Gets a specific run command document for 'RunPowerShellScript' in 'westus'.</span></span>

### <span data-ttu-id="f64d3-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="f64d3-110">Example 2</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus'
```

<span data-ttu-id="f64d3-111">Listet alle verfügbaren Ausführungsbefehle in "westus" auf.</span><span class="sxs-lookup"><span data-stu-id="f64d3-111">Lists all available run commands in 'westus'.</span></span>

## <span data-ttu-id="f64d3-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f64d3-112">PARAMETERS</span></span>

### <span data-ttu-id="f64d3-113">-CommandId</span><span class="sxs-lookup"><span data-stu-id="f64d3-113">-CommandId</span></span>
<span data-ttu-id="f64d3-114">Die Befehls-ID.</span><span class="sxs-lookup"><span data-stu-id="f64d3-114">The command ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f64d3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f64d3-115">-DefaultProfile</span></span>
<span data-ttu-id="f64d3-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f64d3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f64d3-117">-Location</span><span class="sxs-lookup"><span data-stu-id="f64d3-117">-Location</span></span>
<span data-ttu-id="f64d3-118">Der Speicherort, an dem Ausführungsbefehle abgefragt werden.</span><span class="sxs-lookup"><span data-stu-id="f64d3-118">The location upon which run commands are queried.</span></span>

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

### <span data-ttu-id="f64d3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f64d3-119">CommonParameters</span></span>
<span data-ttu-id="f64d3-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f64d3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f64d3-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f64d3-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f64d3-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f64d3-122">INPUTS</span></span>

### <span data-ttu-id="f64d3-123">System.String</span><span class="sxs-lookup"><span data-stu-id="f64d3-123">System.String</span></span>

## <span data-ttu-id="f64d3-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f64d3-124">OUTPUTS</span></span>

### <span data-ttu-id="f64d3-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="f64d3-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandDocument</span></span>

## <span data-ttu-id="f64d3-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f64d3-126">NOTES</span></span>

## <span data-ttu-id="f64d3-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f64d3-127">RELATED LINKS</span></span>
